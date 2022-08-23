
# Unix Interview Questions 

1. Which command can be used in `Unix` to get the current working directory?

<details><summary> <b>Show Answer</b> </summary> 

> We can use the `pwd` command to see the current working directory. For that we just have to write pwd in the unix shell.

</details>

---
2. With the help of which command you can create a new directory in Unix?

<details><summary> <b>Show Answer</b> </summary> 

> We can use the `mkdir` command to create a new directory. For example, `mkdir directory_name`. To create multiple directories we can write like this `mkdir {directory1, directory2, directory3}`.

</details>

---
3. How can you copy a file from "ABC" directory to "XYZ" directory in Unix?

<details><summary> <b>Show Answer</b> </summary> 

> To copy a file from one directory to another, we can use the `cp` command. For example, if we have to copy a test1.txt file of ABC directory to test2.txt file of XYZ directory, we can write as follows:  
`cp /ABC/test1.txt /XYZ/test2.txt`

</details>

---
4. Give the syntax of the command which can be used to move the file from one directory to another.

<details><summary> <b>Show Answer</b> </summary> 

> For moving files from one directory to another we can use the `mv` command. For example, `mv example.txt /documents` , here we are moving example.txt file of current directory to documents directory.

</details>

---
5. Your friend created a folder as "ABC" while working on an important project and dump the finance related data in that folder. Now he wanted to rename the folder as "Finance_Data", what command he has to use to rename that folder in Unix?

<details><summary> <b>Show Answer</b> </summary> 

> For renaming file and folder we can use two commands in Unix, one is `mv` and other one is `rename`.  
  
> With `mv` command  
  `mv ABC Finance_Data` 
    
> With `rename` command  
  `rename 's/ABC/Finance_Data/'* `  
  
</details>

---
6. Other than `touch` command, what command would you use to create an empty file in Unix?

<details><summary> <b>Show Answer</b> </summary> 

> Other than `touch` command, we can use `echo` and `cat` command to create an empty file.      
      
> With `echo` command     
  `echo > file1.txt`    
    
> With `cat` command  
  `cat > file1.txt`  

</details>

---
7. Suppose you have created 6 to 7 directories and files that are holding some sorts of data and your boss wanted to see the permissions of all those file and folders then which command can be used to view the permissions on the file. 

<details><summary> <b>Show Answer</b> </summary> 

> To see the permission on the files we can use the simple `ls` command with `-l` option. For example, `ls -l`. It will give the read write execute permission information in the long format for all the files and directories.

</details>

---
8. How to see which file is modified recently and at what time in unix?

<details><summary> <b>Show Answer</b> </summary> 

> To see what are all the files that are modified recently, we can use the `ls -l` command. 
</details>

---
9. Imagine you have two files "example1.txt" and " example2.txt" and you wanted to add the content of both the files in another file named as "combine.txt". Which command you will use to do that task and what will happen if the "combine.txt" file doesn't exist in your system.  

<details><summary> <b>Show Answer</b> </summary> 

> To add the content of example1.txt and example2.txt file in the combine.txt file we can use the `cat` command.     
```
cat example1.txt example2.txt > combine.txt
```
Here if the combine.txt file doesn't exists in the system, it will create a combine.txt file and add the content of both the files to it. 
</details>

---
10. How do you differentiate between root and home directory in Linux?

<details><summary> <b>Show Answer</b> </summary> 

> The root directory is the main directory of the system and it contains the home directory in it. Everyone can access the root directory but home directory can be access by the owner of that directory only. There can be multiple home directories inside one root directory. 
</details>

---
11. 

