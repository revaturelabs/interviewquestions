## Read

1. How would you create a file in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - In python, we use `open()` built-in function to create a file.
	
```python
open("myfile.txt","W+")
```
> - If `myfile.txt` exists, the file would be opened. If not, it will create a file and open the created file.
	
**Note**: Files will be created within the current directory (the directory wherever your Python code runs).

</details>

---

2.What is the procedure to open the file in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> We can use the same code that we used  to create a file and use `open()` built-in function to create a file.
	
```python	
open("myfile.txt","r") as fObj6.
```
	
</details>

---

3.Write a python program to read an entire text file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Consider you have some `.txt file`, the following code is used to read that text file.

```python
def file_read(fname):
    txt = open(fname)
    print(txt.read())
file_read('test.txt')
```

</details>

---

4.How many types of modes are available to open a file? Also, explain what are the uses of those modes?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

 - There are four different methods(modes) to open a file,
  
 i)`r` - Read - Default value. Opens a file for reading, and shows error if the file does not exist.

 ii)`a` - Append - Opens a file for appending, and creates the file if it does not exist.

 iii)`w` - Write - Opens a file for writing, and creates the file if it does not exist.

 iv)`x` - Create - Creates the specified file, and returns an error if the file exists.

</blockquote>

</details>

---

5.Write a python program to read a file line-by-line into list?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
with open("myFile.txt") as fObj:
    liData = fObj.readlines()
    print(liData)
```

> - Each line within the file is saved as one part in the list. The size of the list remains same as the range of the lines lies within the file.
> - Once the file content is read within the list, we simply need to loop over every element within the list and perform the desired operation.

</details>

---

6.What are the file methods used to read the data from a file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

 There are three methods in python to read data from file:

 1.`read(chars)`: In python, `read()` method is used to read the specified number of characters from the current position.

 2.`readline()`: This method reads the characters starting from the current reading position to a newline character.

 3.`readlines()`: This method reads all lines until the end of file and returns a list object.

	</blockquote>

</details>

---

7.Name two types of data files in python.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

In python, we have two types of data files:

 i)Text File-A document that consists of human readable characters, which might be opened by any text editor. 

 ii)Binary File- contains non-human readable characters and symbols, that requires specific programs to access its contents.

	</blockquote>

</details>

---

8.Write a python program to read all the lines from a file?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> To read all the lines from the file, we have so many methods. Following is one of the method.

```python
L = ["Welcome\n", "to\n", "my\n","world\n"]
file1 = open('text.txt', 'w')
file1.writelines(L)
file1.close()
file1 = open('text.txt', 'r')
Lines = file1.readlines()
count = 0
for line in Lines:
	count += 1
	print("Line{}: {}".format(count, line.strip()))

```

**Output**:

Line1: Welcome

Line2: to

Line3: my

Line4: world

</details>

---

9.What is the return type of open ()?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> `Open()` method returns a bool value indicating whether the file is opened or some error has occurred. 

</details>

---

10.What is the use of 'r' as prefix in the below statement?  

```python   
f = open(r, "d:\Python\test.txt")
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f = open(r, "d:\Python\test.txt")
```

> In the above program,'r' makes the string as raw string, which means, there is no special character in the string.

</details>

---

11.What is the difference between the `read()` and `readlines()` methods in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - The `read()` method returns the file's entire contents as a single string value.
> - The `readlines()` method returns a list of strings, where each string is a line from the file contents.

</details>

---

12.Is there any way to read file without opening? Which function is used to open a file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - No,we can't read file without opening.
> - If you want to read a file, open the file first then, use `open()` function to open a file.
  
</details>

---

13.Which of the following are correct when a file is opened using `with` statement?

A.The with statement simplifies exception handling.

B.The file is automatically closed after leaving the block, and all the resources that are tied up with the file are released.

C.File reading and writing are faster using the with statement.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option A and B are the correct statements.

<details><summary><b>Explanation</b></summary>
	<blockquote>

 - The with statement simplifies exception handling by encapsulating common preparation and cleanup tasks.
 - This additionally ensures that a file is automatically closed when leaving the block.
 - As the file is closed automatically, it ensures that each one of the resources that are bound with the file are released.

</blockquote>
</details>
</details>

---

14.What are the 3 "mode" arguments that may be passed to the `open()` function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	<blockquote>

 - `r`,`w` and `a` are the three mode arguments that can be passed to the `open()` function.

 i) `r`-it's used for read mode.

 ii) `w`-it's used for write mode.

 iii) `a`-this is used for an append mode.
		
		
</blockquote>
</details>

---

15.What type mode is used to Read a Binary file in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> In python, we can use `rb` mode in the `open()` function to read a binary file.

</details>

---

16.Write a python program to read the binary file?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f = open('C:\img.png', 'rb') # opening a binary file
content = f.read() # reading all lines
print(content)
f.close()
```

> Using `rb` mode, we can read the binary file in python.

</details>

---

17.Which of the below is incorrect with respect to file access mode?

A.`r`

B.`ab+`

C.`rw+`

D.`wb+`

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	<blockquote>

- Option C .`rw+`

<details><summary><b>Explanation</b></summary>

- r: This mode opens an existing file as read-only mode. The file pointer exists at the beginning.

- ab+:This mode is used to open a file to append and read, both in binary format.

- wb+: This is used to open the file to write and read, both in binary format.
	
	</blockquote>

</details>
</details>

---

18.How to get the list of files from the directory ?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> `os.listdir()` - This method is used to get all the files from the particular directory.

</details>

---

19.How to check whether the given file exists or not?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Use the `os.path.isfile('file_path')` function to see whether a file exists. Pass the file name or file path to the current to perform as associate degree argument. This returns True if a file is present in the given path. Otherwise, it returns False.

</details>

---

20.Write a python program to display only unique words from the file `sales.txt`.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f = open("sales.txt", "r")
d = f.read()
d = d.split()
str = " "
m = []
for i in d:
  if i not in str:
       str=str+i
       print(i, end=" ")
f.close()
```

</details>

----
