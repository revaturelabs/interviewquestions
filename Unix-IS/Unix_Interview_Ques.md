
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
11. Which command can we use to view content of multiple files in the terminal?

<details><summary> <b>Show Answer</b> </summary> 

> `cat` command can be used to view multiple files in the terminal at the same time. For example, `cat file1.txt file2.txt file3.txt`. 

</details>

---
12. A 'test.txt' file has some old content and 'test1.txt' file has some newly added content then how would you add the content of test1 file in the end of test file so that it has both old and new content together?

<details><summary> <b>Show Answer</b> </summary> 

> we can use the `cat` command with two redirection operator `>>` to append the content of one file to another. In this case, we can write, `cat test1.txt >>test.txt`.

</details>

---
13. Suppose using `mkdir` command you have created one directory as "program" and that is an empty directory and now you want to delete the directory from your system, then which command can be used to delete that directory?

<details><summary> <b>Show Answer</b> </summary> 

> Using `rmdir` command we can delete an empty directory. Just we have to write the directory name after `rmdir` command.  
```
rmdir program
```

</details>

---
14. While working on a project you have created one directory as "program" and added some files and folders in it which contains some data related to the project. Now the project has been deployed in the working environment and there is no need of that directory in the system now. So, for deleting that directory what command you can write?

<details><summary> <b>Show Answer</b> </summary> 

> To delete a directory that contains some files and folders, we can use the `rm` command with `-r` option.  
```
rm -r program
```

</details>

---
15. How you can change the current directory in linux?

<details><summary> <b>Show Answer</b> </summary> 

> Using `cd` command we can change the current directory in which we are working. For example, `cd program/user`.

</details>

---
16. Which command can be used to search as tring in a file based on pattern in linux.

<details><summary> <b>Show Answer</b> </summary> 

> `grep` command can be used in pattern searching in a string. For example, `grep -i "Hello" test1.txt`, here it will search the 'hello' word in the test1.txt file and returns the whole sentance where it is present. `-i` option in `grep` is used to do the case insensitive search.

</details>

---
17. Tell me the difference between `echo` and `printf` command.

<details><summary> <b>Show Answer</b> </summary> 

> The `printf` can be used to print the string, numbers and other format specifiers also whereas `echo` can only be used to print the string values.
Performance wise also `printf` is faster in execution than `echo` command.

</details>

---

18. 

<details><summary> <b>Show Answer</b> </summary> 

>

</details>

---

19. 

<details><summary> <b>Show Answer</b> </summary> 

>

</details>

---
20. 

<details><summary> <b>Show Answer</b> </summary> 

>

</details>

---
21. 

<details><summary> <b>Show Answer</b> </summary> 

