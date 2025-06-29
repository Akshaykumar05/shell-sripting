# shell-sripting
In this repo, we are learning and doing hands-on of shell (bash) scripting language.
```
mkdir myscript
```
```
cd myscript
```
* Now edit the file
```
vim 01_basic.sh
```
```
#!/bin/bash
echo "Hello Buddy"
```
* Run the script using following commands:
1. Direct using bash
```
bash 01_basic.sh
```
<img width="536" alt="image" src="https://github.com/user-attachments/assets/e6abbfcc-b557-42a7-92ce-c95d3f33964e" />

2. Run the script at current location
```
./01_basic.sh
```
Sometime it can show a permission issue, where we need to give the executable (x) permission to the file.
```
chmod +x -1_basic.sh
```
Again run the script, it should be working now.

<img width="603" alt="image" src="https://github.com/user-attachments/assets/990e1105-fda5-47c8-bf4e-7e7c3d809198" />

3. Run the script using path
```
/home/akshay/myscript/01_basic.sh
```
   
![image](https://github.com/user-attachments/assets/4c2ceab2-b68d-49cd-991a-a0c0d25a8935)

### Comments:
1. Single line comment
* Using #
```
vim 02_comment.sh
```

<img width="383" alt="image" src="https://github.com/user-attachments/assets/e8d2718f-91fe-4b95-91f7-1fb6f0c208cc" />

2. Multiline comment
* Using <<comment
* Edit the script file 
<img width="650" alt="image" src="https://github.com/user-attachments/assets/21d6ea05-d312-40cd-be5e-10a77be0aafe" />

* And run the file
```
bash 02_comment.sh
```
<img width="523" alt="image" src="https://github.com/user-attachments/assets/9b0e2fc2-e469-408e-b8da-840615f853a9" />

### What are Variables
We will add some variables, and will run the script

<img width="458" alt="image" src="https://github.com/user-attachments/assets/d5255690-798a-4b72-98b8-c662bb9d6e77" />

<img width="551" alt="image" src="https://github.com/user-attachments/assets/c2d05add-bed0-4c71-9e16-263d58c8792f" />

Now lets add some more same variable in the file e.i name

<img width="584" alt="image" src="https://github.com/user-attachments/assets/0c4d8046-5f55-4546-a5d5-b83a0f19f494" />

<img width="544" alt="image" src="https://github.com/user-attachments/assets/9426f9cd-6277-40bb-87a0-10e2928cc900" />

* Use variable to store the output of a command

```
vim 03_varcode.sh
```
Add the hostname value

<img width="610" alt="image" src="https://github.com/user-attachments/assets/35c97db4-e051-48a3-82db-d9645f18118e" />

<img width="485" alt="image" src="https://github.com/user-attachments/assets/a22ad1b4-206a-45d7-a6f7-49bd147d70bf" />

#### Constant variable
* Once you defined a variable and dosn't wanna change it untill end of the script.
* Command use ```readonly var_name="Hi"```
* Create a new script and add the constant variable
  ```
  vim 04_constant_var.sh
  ```
  <img width="565" alt="image" src="https://github.com/user-attachments/assets/2194e1a4-a46b-417b-baf5-6d4726b6d178" />

  <img width="610" alt="image" src="https://github.com/user-attachments/assets/339dc45f-4f9c-4153-8e2a-9776c67b4a76" />

### Array
1. How to get an array?
  ```myArray=(1 2 Hello "Hey man")```

2. How to get value from an array?
  ```
  echo "${myArray[0]}"
  echo "${myArray[1]}"
  ```
 3. Now create and edit a script file
   ```
   vim 05_arrays.sh
   ```
   <img width="494" alt="image" src="https://github.com/user-attachments/assets/d4764807-3694-4fa9-9392-ead7bfd3a596" />

 * We have given the value to an array: numbers, string, multi string. Now run the script and get the value in the 3rd index as below.
   ```
   bash 05_arrays.sh
   ```

   <img width="521" alt="image" src="https://github.com/user-attachments/assets/d386cc37-1634-43b6-b8a9-8e39110427f1" />

 * To get all the values in the array, edit the script one more line
   ```
   echo "All the values in array are ${myArray[*]}"
   ```
   <img width="607" alt="image" src="https://github.com/user-attachments/assets/00a9bbef-7d85-4914-9147-775861439538" />

 * Now run the script to retrive all the values.

   <img width="577" alt="image" src="https://github.com/user-attachments/assets/090cbcf0-3a12-4a3c-8335-3bdf6cd47757" />

 4. How to get length of array?
 - Add this line in the script
   ```echo "${#myArray[*]}"```

   <img width="576" alt="image" src="https://github.com/user-attachments/assets/f4661f2d-e562-49a0-994f-5d79bc476a3e" />

   <img width="649" alt="image" src="https://github.com/user-attachments/assets/996c2f8c-7bd2-46b8-812e-d48ea846186b" />

  5. How to get specific values?
    ```echo "${myArray[*]:1}"```
    ```echo "${myArray[*]:1:2}"```

   <img width="601" alt="image" src="https://github.com/user-attachments/assets/640bc618-b7d5-4c60-9f14-f0282409e070" />

   <img width="671" alt="image" src="https://github.com/user-attachments/assets/c6058d3b-ab28-416f-9740-ec15c491ba1f" />
   
  6. How to update an array?

    ```maArray+=( New 20 30)```

    
    <img width="526" alt="image" src="https://github.com/user-attachments/assets/04042969-2f2c-49f5-9008-ea238f89866c" />

    <img width="483" alt="image" src="https://github.com/user-attachments/assets/55e2eb14-cecc-4e6c-9b69-3e164201e379" />

  7. Array: Key-values
     
     ```declare -A myArray```
     
     ```myArray=( [name]=Akshay [city]=Delhi```
     
     ```echo "${myArray[Name]}"```

     * Now create a new script and edit
       
     ```
     vim 06_key-values.sh
     ```
     <img width="520" alt="image" src="https://github.com/user-attachments/assets/6d8e6791-8b94-4d03-b0af-fc349fcf4582" />

     <img width="532" alt="image" src="https://github.com/user-attachments/assets/175039e4-4ee8-4992-a28b-8aea3fa4f501" />

   9. String Operations
      
      ```myVar="Hello World"```
      
      ```length=${#myVar}```
      
      ```upper=${X^^}```
      
      ```lower=${Y,,}```
      
      ```replace=${myVar/world/Buddy}```
      
      ```slice=${myVar:6:11}```

      * Create a scrpt and edit
      ```
      vim 07_string_ops.sh
      ```
      <img width="684" alt="image" src="https://github.com/user-attachments/assets/4956fb49-d20a-48bc-a558-5f68984c24d1" />


      <img width="720" alt="image" src="https://github.com/user-attachments/assets/5c8c370d-9336-4c80-acad-0e0d8e162d43" />


### User Interaction
```
vim 08_user_int.sh
```
* Create th script

<img width="347" alt="image" src="https://github.com/user-attachments/assets/dd2f534a-b32d-45da-8f2c-29a496545fc5" />
 
<img width="447" alt="image" src="https://github.com/user-attachments/assets/b698113e-d8a5-4e12-a442-d436d75a932b" />


```
#!/bin/bash

read -p "What is your name?"  name
echo "Your name is $name"
```
```
bash 08_user_int.sh
```

### Arithmetic Operation
```
vim 09_arith_ops.sh
```
```
#!/bin/bash

#Maths Calculation

X=10
Y=5

let mul=$X*$Y
echo "$mul"

let sum=$X+$Y
echo "$sum"

echo "subscription is $(($X-$Y))"
```

<img width="489" alt="image" src="https://github.com/user-attachments/assets/c77982a1-663f-4b1a-91cb-c290b4f56dd4" />
