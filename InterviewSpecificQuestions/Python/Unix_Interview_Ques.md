
# Unix Interview Questions 

1.Which command can be used in `Unix` to get the current working directory?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> We can use the `pwd` command to see the current working directory.For that, we just have to write pwd in the UNIX shell.

</details markdown="1">

---
2.With the help of which command you can create a new directory in Unix?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> We can use the `mkdir` command to create a new directory.For example, `mkdir directory_name`.To create multiple directories, we can write like this `mkdir {directory1, directory2, directory3}`.

</details markdown="1">

---
3.How can you copy a file from "ABC" directory to "XYZ" directory in Unix?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To copy a file from one directory to another, we can use the `cp` command.For example, if we have to copy a test1.txt file of ABC directory to test2.txt file of XYZ directory, we can write as follows:  
`cp /ABC/test1.txt /XYZ/test2.txt`

</details markdown="1">

---
4.Give the syntax of the command which can be used to move the file from one directory to another.

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> For moving files from one directory to another we can use the `mv` command.For example, `mv example.txt /documents`, here we are moving the example.txt file of the current directory to the document’s directory.

</details markdown="1">

---
5.Your friend created a folder as "ABC" while working on an important project and dump the finance-related data in that folder.Now he wanted to rename the folder as "Finance_Data", what command he has to use to rename that folder in Unix?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> For renaming files and folders, we can use two commands in Unix, one is `mv` and the other one is `rename`.
  
> With `mv` command  
  `mv ABC Finance_Data` 
    
> With `rename` command  
  `rename 's/ABC/Finance_Data/'* `  
  
</details markdown="1">

---
6.Other than `touch` command, what command would you use to create an empty file in Unix?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Other than `touch` command, we can use `echo` and `cat` commands to create an empty file.    
      
> With `echo` command     
  `echo > file1.txt`    
    
> With `cat` command  
  `cat > file1.txt`  

</details markdown="1">

---
7.Suppose you have created 6 to 7 directories and files that are holding some sort of data and your boss wanted to see the permissions of all those files and folders, then, which command can be used to view the permissions on the file? 

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To see the permission on the files we can use the simple `ls` command with `-l` option.For example, `ls -l`.It will give the read-write execute permission information in the long format for all the files and directories.

</details markdown="1">

---
8.How to see which file is modified recently and at what time in UNIX?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To see what are all the files that are modified recently, we can use the `ls -l` command.
</details markdown="1">

---
9.Imagine you have two files "example1.txt" and " example2.txt" and you wanted to add the content of both files in another file named "combine.txt".Which command you will use to do that task and what will happen if the "combine.txt" file doesn't exist in your system?  

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To add the content of example1.txt and example2.txt files in the combine.txt file we can use the `cat` command.   
```
cat example1.txt example2.txt > combine.txt
```
Here if the combine.txt file doesn't exist in the system, it will create a combine.txt file and add the content of both files to it.
</details markdown="1">

---
10.How do you differentiate between the root and home directories in Linux?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> The root directory is the main directory of the system, and it contains the home directory in it.Everyone can access the root directory, but the home directory can be accessed by the owner of that directory only.There can be multiple home directories inside one root directory.
</details markdown="1">

---
11.Which command can we use to view the content of multiple files in the terminal?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> `cat` command can be used to view multiple files in the terminal at the same time.For example, `cat file1.txt file2.txt file3.txt`.

</details markdown="1">

---
12.A 'test.txt' file has some old content and 'test1.txt' file has some newly added content then how would you add the content of the test1 file at the end of the test file so that it has both old and new content together?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> we can use the `cat` command with two redirection operator `>>` to append the content of one file to another.In this case, we can write, `cat test1.txt >>test.txt`.

</details markdown="1">

---
13.Suppose using `mkdir` command you have created one directory as "program" which is empty and now you want to delete that directory from your system, then which command you will use for it?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using `rmdir` command we can delete an empty directory.Just we have to write the directory name after `rmdir` command.
```
rmdir program
```

</details markdown="1">

---
14.While working on a project you have created one directory as "program" and added some files and folders in it which contain some data related to the project.Now the project has been deployed in the working environment and there is no need for that directory in the system now.So, for deleting that directory what command you can write?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To delete a directory that contains some files and folders, we can use the `rm` command with `-r` option.
```
rm -r program
```

</details markdown="1">

---
15.How you can change the current directory in Linux?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using `cd` command, we can change the current directory in which we are working.For example, `cd program/user`.

</details markdown="1">

---
16.Which command can be used to search as a string in a file based on a pattern in Linux?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> `grep` command can be used in pattern searching in a string.For example, `grep -i "Hello" test1.txt`, here will search the 'hello' word in the test1.txt file and returns the whole sentence where it is present.`-i` option in `grep` is used to do the case insensitive search.

</details markdown="1">

---
17.Tell me the difference between `echo` and `printf` commands.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> The `printf` can be used to print the string, numbers, and other format specifiers whereas `echo` can only be used to print the string values.
Performance wise also `printf` is faster in execution than `echo` command.

</details markdown="1">

---

18.How to check the disk usage information on a filesystem?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using `df` command, we can check the information related to disk usage, that is, how much space is used by the filesystem and what is the available space.

</details markdown="1">

---

19.How to view all the partitions of a hard drive in Linux.

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using the` fdsik` command along with `-l` option, we can see all the partitions in the system.For example, ` sudo fdisk -l`.

</details markdown="1">

---
20.Explain about fdisk, sfdisk and cfdisk commands?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> All these 3 are used to create, view, update, and delete the partitions of a disk, but the fdisk and cfdisk provide fancy interfaces to do all these tasks, a sysadmin can easily do all these just by going into the menu interface without remembering all the commands.Whereas sfdisk doesn't provide the user interface, instead it is command driven and used in documentation.it can read input from file or stdin and writes into a partition table.

</details markdown="1">

---
21.which command is used to give information about block devices like hard drives, flash drives, CD-ROMs?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To view the details of all available block devices, we can use the `lsblk` command.For example, `lsblk -a`, lists all the block devices including empty devices.

</details markdown="1">

---

22.How do you manage and monitor software RAID devices in Linux?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using `mdadm` command, we can create software RAID and help manage RAID on devices.

</details markdown="1">

---

23.Give the general format of the UNIX command?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> When writing a UNIX command in shell, we can follow one pattern:  
```
command_name (-n_arguments) (filename)
```
  
</details markdown="1">

---

24.Is the kernel and Operating System the same?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> No both are not the same, OS is a system software, whereas kernel is a part of OS.OS acts as an interface between the user and hardware, whereas the kernel is a core of OS and is used to interact between applications and hardware.
  
</details markdown="1">

---

25.Name some of the file editors used in Unix/Linux?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> There are many file editors that can be used to write down the commands like:  
> - Vi/VIM editor
> - Nano editor
> - Gedit editor
> - VS Code

</details markdown="1">

---

26.How to change the permission set of a file in UNIX?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> To change the permission to read, write and execute a file, we can use the `chmod` command.For example, `chmod g+w test_file` will change the file permission to write for the group owner.

</details markdown="1">

---

27.Assume you have to change ownership of a file in Linux, how will you do that?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> To change ownership of a file, we can use `chown` command.For example, `chown Henry work_file`.Here the new owner’s name is Henry, and the file name is work_file.

</details markdown="1">

---

28.Is there any difference between `vi` and `vim` editors in Linux?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 
  
> - `vi` is a standard text editor in Linux, whereas `vim` is an enhanced version of vi text editor.
> - With `vi` we can undo the last command only, whereas `vim` can be used to undo multi-level undo.
> - While working with `vi` we cannot highlight any syntax or code, but with `vim` we can do it.
> - `vi` doesn't have GUI, but `vim` have.
  
</details markdown="1">

---

29.Tell me the use of the `chmod` command in UNIX?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> The `chmod` command is used to change the permission set of a file, it can give read, write, and execute permission to a user, group of users, to all etc.In Numeric 0 means no permission, 1 means execute, 2 means write, and 4 means read.For example, if we are giving all three permissions to a file then we have to write, `chmod 777 file_name`, where '777' represents 'rwx'.

</details markdown="1">

---

30.How will you give only read and write permission to all the users of a file named as "test1"?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> we can use the `chmod` command to do so, just we have to write `chmod ugo+rw test1`.

</details markdown="1">

---

31.Imagine Henry wants to be the owner of the two files, "test1" and "test2" in Linux then what he has to do?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To change ownership of a file, he can use `chown` command:    
```
chmod Henry test1 test2
```

</details markdown="1">

---

32.Suppose you have a file which has read and write permission and now you want to remove the write permission from it, then what you will do to remove the write permission from a file?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> For removing the write permission from a file, we can write  
```
chmod u-w file_name
```

</details markdown="1">

---

33.How will you give read and write permission to a user and group and only the read permission to others on a file named as an "example"?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> we can write     
```
chmod 664 example
```
Here, the first 6 represent read and write permission to a user, the next 6 represent read and write permission to a group, and the last 4 represent only the read permission to others.

</details markdown="1">

---

34.How will you differentiate between `df`, `blkid` and `lsblk` commands?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> The `df` command give the details of the mounted file system, on the other hand `blkid` gives the details of block devices that are not mounted and `lsblk` command is used to get the details of both the mounted and unmounted file system.

</details markdown="1">

---

35.As a developer, if you wanted to check how many block devices are available in your system that is not mounted, which command you will use for that in UNIX?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To check what are all the available block devices in the system, we can use the `blkid` command.

</details markdown="1">

---

36.In Linux, how will you display the number of times a substring is present in a line?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> Using `grep` command with `-c` option, it will give the count of the number of matches of a string or pattern in a line.For example, `grep -c "hello" example.txt`.Here we are finding how many times "hello" is present in a line in the example.txt file.

</details markdown="1">

---

37.If you have to show in which line number a given string or pattern is present in a file then which command you will use for that?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> We can use the `grep` command with `-n` argument to get the line number where the word is present along with the whole line.For that we have to write ` grep -n "Pattern" File_name`.

</details markdown="1">

---

38.To view the content of a small file we can use the `cat` command, but what will happen if we use the same `cat` command to view the content of a large file?  Also, tell me which command can be used to see the content of a large file in a more convenient way.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> When we use the `cat` command to see the content of a large file that will not be fixed in a single terminal screen, then it will move the cursor to the end of the file and to view the content from the start of the file we have to scroll it up.Therefore, it is not a convenient way to see the content of a large file.But, for that, there is a command called `more` through which we can see the content of a file in a convenient way.It will not move directly to the end of the file, instead, it stops at the end of the terminal with a prompt message at the bottom of the terminal showing how much content is present in the terminal at that moment in terms of percentage.We can press enter key to move down line by line and for scrolling down we can use the space key.

</details markdown="1">

---

39.Both `more` and `less` command in Linux, is used to view the content of a large file then what is the difference between both of them?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> The `more` command, when used to see the content of a big file, allows the user to scroll down only with limited or no scroll up.Whereas the `less` command is used for both forward and backward navigation in a file.

</details markdown="1">

---

40.How will you terminate a process that is running in the background with the process id of 3007?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b>Show Answer</b> </summary> 

> To terminate or end a process, we can use the `kill` command in Linux.
```
kill -15 3007

```
Here, -15 represents a termination signal.

</details markdown="1">

---

