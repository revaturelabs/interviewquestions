## Read

1.How will you create a file in python?

<details><summary><b>Show Answer</b></summary>

- In python we are using open() built-in function to make a file.
open("myfile.txt","W+")
- This is the only open method that may create the file if it's not present.
- To add content in fresh created file,You should open the file in write mode.
- There are 2 arguments are passed to the open() builtin function- the name of the file and mode the file (w+).
Here,

- w– produce the file in write mode

- +– create a file if it’s not present within the current directory.

**Note**: File will be created within the current directory (the directory wherever your Python code is running).

</details>

---

2.What is the procedure to open the file in python?

<details><summary><b>Show Answer</b></summary>

We can use the same code as what we have used for creating a file.
	
```python	
open("myfile.txt","r") as fObj6.
```
	
</details>

---

3.Write a python program to read an entire text file?

<details><summary><b>Show Answer</b></summary>

Consider you have a some **.txt file**, this code is used to read that text file.

```python
def file_read(fname):
    txt = open(fname)
    print(txt.read())
file_read('test.txt')
```

</details>

---

4.How many types of modes available in opening a file? Can you explain me what are use of those modes?

<details><summary><b>Show Answer</b></summary>

- There are four different methods(modes) for opening a file.
  
i)"r" - Read - Default value. Opens a file for reading, error if the file does not exist.

ii)"a" - Append - Opens a file for appending, creates the file if it does not exist.

iii)"w" - Write - Opens a file for writing, creates the file if it does not exist.

iv)"x" - Create - Creates the specified file, returns an error if the file exists.

</details>

---

5.Write a python program to read lin-by-line file into list?

<details><summary><b>Show Answer</b></summary>

```python
with open("myFile.txt") as fObj:
    liData = fObj.readlines()
    print(liData)
```

- Each line within the file are saved as one part in the list. that the size of the list are the same because the range of lines within the file.
- Reading a go in the list is very vital once you wish to manipulate the text in every line of the file. once reading file content within the list, you simply need to loop over every element within the list and perform your desired operation.

</details>

---

6.What are the file methods used to read the data from file?

<details><summary><b>Show Answer</b></summary>

- There are three methods in python to read data from file.

1.read(chars): In python read() method used to reads the specified number of characters from the current position.

2.readline(): This method reads the characters starting from the current reading position up to a newline character.

3.readlines(): This method reads all lines until the end of file and returns a list object.

</details>

---

7.Name two types of data files available in python .

<details><summary><b>Show Answer</b></summary>

- In python we have two types of data files available in python .

The two types of files are,

i)Text File-A document consists of human readable characters, which might be opened by any text editor. 

ii)Binary File-In binary files contains non-human readable characters and symbols, that require specific programs to access its contents.

</details>

---

8.Write a python program to read all the lines from file?

<details><summary><b>Show Answer</b></summary>

To read all the lines from the file we have so many methods.This is one of the method.

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

9.How will you read a file without opening? Which funtion used to open a file?

<details><summary><b>Show Answer</b></summary>

- No,we can't able to read file without opening.
- open() function used to open a file.

</details>

---

10.What is the use of 'r' as prefix in the given statement?  

```python   
f = open(r, "d:\Python\test.txt")
```

<details><summary><b>Show Answer</b></summary>

```python
f = open(r, "d:\Python\test.txt")
```

In the above program 'r' makes the string as raw string, it means there is no special character in string.

</details>

---

11.What is the difference between the read() and readlines() methods in python?

<details><summary><b>Show Answer</b></summary>

- The read() method returns the file's entire contents as a single string value.
- The readlines() method returns a list of strings, where each string is a line from the file contents.

</details>

---

12.Can we read file without opening? Which funtion used to open a file?

<details><summary><b>Show Answer</b></summary>

- No,we can't able to read file without opening.
- If you want to read a file, open the file first then, use open() function to open a file.
  
</details>

13.Select all the correct statements when a file is opened using the with statement.

**A**.The with statement simplifies exception handling

**B**.The file is automatically closed after leaving the block, and all the resources that are tied up with the file are released.

**C**.File reading and writing are faster using the with statement.

<details><summary><b>Show Answer</b></summary>

option A and B are the correct statements.

<details><summary><b>Explanation</b></summary>

- The with statement is simplifies exception handling by encapsulating common preparation and cleanup tasks.
- This additionally ensures that a file is automatically closed when leaving the block.
- As the file is closed automatically it ensures that each one the resources that are bound with the file are released.

</details>
</details>

---

14.What are the 3 "mode" arguments that may be passed to the open() function?

<details><summary><b>Show Answer</b></summary>

- 'r','w' and 'a' these are the three mode arguments that can be passed to the open() function.
- 
i) 'r'-it's used for read mode.

ii) 'w'-it's used for write mode.

iii) 'a'-this is used for an append mode.

</details>

---

15.What type mode used to Reading a Binary file in python?

<details><summary><b>Show Answer</b></summary>

In python we can use **rb** mode in the *open()* function to read a binary files.

</details>

---

16.Write a python program to read the binary file?

<details><summary><b>Show Answer</b></summary>

```python
f = open('C:\img.png', 'rb') # opening a binary file
content = f.read() # reading all lines
print(content)
f.close()
```

- Using 'rb' mode we can read the binary file in python.

</details>

---

17.which one is incorrect  file access mode?

**A**.r

**B**.ab+

**C**.rw+

**D**.wb+

<details><summary><b>Show Answer</b></summary>

Option c

<details><summary><b>Explanation</b></summary>

> r: This mode opens an existing file to read-only mode. The file pointer exists at the beginning.

> ab+:This mode used to opens a file to append and read both in binary format.

> wb+: This is used opens the file to write and read both in binary format.

</details>
</details>

---

18.How will you get the list of files from the directory ?

<details><summary><b>Show Answer</b></summary>

**os.listdir()** - This method is used to get all the files from the particular directory.

</details>

---

19.How will you check the given File is exists or not?

<details><summary><b>Show Answer</b></summary>

Use the **os.path.isfile('file_path')** function to see whether a file exists. Pass the file name or file path to the current perform as associate degree argument. This performs returns True if a file is gift on the given path. Otherwise, it returns False.

</details>

---

20.Write a python program to display only unique words from the file "sales.txt".

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
