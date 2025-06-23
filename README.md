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

  

