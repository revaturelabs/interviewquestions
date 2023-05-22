## Technical

1. What is Shell?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Shell is a command interpreter, which interprets the command given by the user to the kernel. 
- It is an interface between a user and an operating system.

</blockquote>

</details>

---

2. What is Shell Scripting?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Shell scripting is a series or sequence of UNIX commands written in a plain text file. We used to give a list of UNIX commands like a to-do list in a file to execute it.

</blockquote>

</details>

---

3. Define Shell Variable.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Shell variable forms the core part of a shell script or program. The variable allows the shell to manipulate the stored information within a shell program. It is generally stored as a string variable. 

</blockquote>

</details>

---

4. What is the absolute and relative path?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Absolute path is the full path of the directory. It always starts with “/”
  - Example:
    **`cd  /var/tmp/abrt/`**
- Relative path is necessary from the current location to reach a particular directory that doesn’t start with “/”.
  - Example:
    **`cd .. ,   cd –`**

</blockquote>

</details>

---

5.  How to create, read and delete files?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The `touch` command is used for creating files.
  - Example:
    `#touch filename` 
- The `cat` command is used for reading files.
  - Example:
    `#cat filename`
- The `rm` command is used to delete a file.
  - Example:
    `#rm –f  filename` 

</blockquote>

</details>

---

6.  How to create and delete a directory?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The mkdir command is used for creating a directory. 
  - Example:
  `# mkdir filename`
- The rmdir command is used to remove the directory. 
  - Example:
  `#rmdir filename` 

</blockquote>

</details>

---

7.  What is the use of `head` and `tail` commands?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `Head` command is used to display started 10 lines.
- `Tail` command is used to display started 10 lines.

</blockquote>

</details>

---

8. What is the significance of `$#`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It represents the total number of arguments passed by string.

</blockquote>

</details>

---

9. What is the difference between `$*` and `$@`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`$*` consider the entire set of positional parameters as a single string, but `$@` treat each quoted argument as a separate argument.

</blockquote>

</details>

---

10. How to make variables unchangeable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Variables can be made unchangeable using read-only. For instance, if we want variable ‘a’ value to remain as 10 and not change, then we can achieve this using read-only.
- Example:
  - $ a=10
  - $ readonly a

</blocckquote>

</details>

---

11. What is the alternative command available to echo and what does it do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `tput` is an alternative command to `echo`.
- Using this, we can control the way in which the output is displayed on the screen.

</blockquote>

</details>

---

12. What are the default permissions of a file when it is created?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

666 i.e. rw-rw-rw- is the default permission of a file, when it is created.

</blockquote>

</details>

---

13. What does `ls` command do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

1. It lists files in the current directory.
2. It lists files in a long format.

- Example

    1. $ ls
    2. $ ls –lrt or $ ls -ltr

</blockquote>

</details>

---

14. What is the use of `cd` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

1. It changes the directory to your home directory.
2. It changes the directory to test.
3. It moves back to one directory or to the parent directory of your current directory.

</blockquote>

</details>

---

15. How to copy, move and compress the files?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- To copy the file

  - `$ cp file1 test`         - It copies file1 to test directory.
  - `$ cp file1 file1.bak`    - It takes a backup of file1. 

- To move the file 
 
  - `$ mv file1 file2`	      - It moves or renames file1 to file2.

- To compress the file

  - `$ compress file1` - It reduces the size of file1 and creates a compressed file called file1.z and deletes file1.
</blockquote>

</details>

---

16. What is the use of `date`, `diff` and `find` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**date**    -   `$ date`                        - It displays the current date and time.
e.g. Output:
Wednesday, October 2022 03:58:06 PM MDT

**diff**    -   `$ diff file1 file2`	        - It displays line by line difference between file1 and file2.

**find**    -	`$ find . –name ‘*.t’ -print`	- It searches in the current directory and in all its subdirectories for files ending with .t, and writes their names in the output.


</blockquote>

</details>

---

17. What is the difference between the `finger` and `who` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**finger**	`$ finger`	        - It displays information about the user.
**who** 	`$ who`         	- It lists the users who are logged in on the machine.

</blockquote>

</details>

---

18. What is the use of `grep` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`$ grep Hello file1`        -   It searches for the lines containing Hello in file1.
`$ grep –c Hello file1`     -   It gives the count or number of lines that contain Hello in file1.

</blockquote>

</details>

---

19. Does `passwd` and `pwd` both are same?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- No both are different.

**passwd**	`$ passwd`	    -   It is used to change the password.
**pwd** 	`$ pwd`         -   It displays the present working directory.

</blockquote>

</details>

---

20. What is the use of `ps`, `talk` and `wc` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**ps**	    `$ ps`          -   It displays the list of processes which are currently running on the machine.
**talk**	`$ talk user1`	-   It is used to talk to the user1 who is currently logged into the same machine.
**wc**	    `$ wc file1`    -   It counts the number of lines, words, and characters in file1.

</blockquote>

</details>

---

21. What `sort` command does?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`$ sort file1`	        - This will sort the contents of file1 and display sorted output on the screen.

</blockquote>

</details>

---

22. What does the. (dot) indicate at the beginning of a file name and how should it be listed?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A file name that begins with a. (dot) is called a hidden file. Whenever we try to list the files, it will list all the files except hidden files.

- To list the hidden file, we need to use –the option of ls. i.e. `$ ls –a`

</blockquote>

</details>

---

23.  What is the difference between diff and cmp commands?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`diff` – Basically, it tells about the changes which need to be made to make files identical.

`cmp` – Basically it compares two files byte by byte and displays the very first mismatch.

</blockquote>

</details>

---

24. What is Shebang in a shell script?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Shebang is a `# sign` followed by an exclamation i.e. !.
- Generally, this can be seen at the beginning or top of the script/program. This is used to avoid repetitive work. Shebang mainly determines the location of the engine which is to be used to execute the script.

**Example: #!/bin/bash**        - The above line also tells which shell to use.
   - Here ‘#’ symbol is called hash and ‘!’ is called a bang.

</blockquote>

</details>

---

