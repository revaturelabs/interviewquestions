## Delete

1.How will you delete a file in python?

<details><summary><b>Show Answer</b></summary>

- So Many times you need to delete the file instead of closing it.
- If you try to delete the file which is not present, it will throw an Input Output error.

```python
import os
#delete file
os.remove("File.txt")
```

The remove objects and path are described in the os module.So,you have to import the "os" module.

</details>

---

2.What will be the use of checking the file is exist or not?

<details><summary><b>Show Answer</b></summary>

- To avoid obtaining an error, you would possibly need to check if the file exists before you try to delete it.

</details>

---

3.Write a program to check if file is exist or not?

<details><summary><b>Show Answer</b></summary>

```python
import os
if os.path.exists("my_file.txtt"):
    os.remove("my_file.txtt")
else:
    print("the file doesn't exist")
```

</details>

---

4.How will you close a file in python?

<details><summary><b>Show Answer</b></summary>

```python
open("myFile.txt", "r") as fObj
#perform file operations
fObj.close()
```

- It is always good practice to close the file after using it.

Orelse,
- We can use "with" statement while opening the file. You don’t got to explicitly close the file object. As soon as the pointer goes out of the with statement block, the file object are closed.
  
```python
with open("myFile.txt", "r") as fObj:
#perform file operations
#file is closed automatically
```

</details>

---

5.How will you delete a folder?

<details><summary><b>Show Answer</b></summary>

- Inpython to delete an folder,we can use os.rmdir() method.
  
```python
import os
os.rmdir("folder_name")
```

</details>

---

6.Can we delete a folder?

<details><summary><b>Show Answer</b></summary>

Yes,we can delete/remove a folder.But,you can remove only empty folders.

</details>

---

7.How will you listing the files in a directory?

<details><summary><b>Show Answer</b></summary>

- To lisiting all the files or directories from a particular path we can use os.listdir() method.

```python
import os
for x in os.listdir('_'):
    print(x)
```

</details>

---

8.Write a program to read the file "rename.txt" and display the entire content after removing leading and trailing spaces.

<details><summary><b>Show Answer</b></summary>

```python
f = open("star.txt", "r")
d = f.readlines()
for i in d:
    print(i.strip())
f.close()
```

</details>

---

9.What will be the output of the folowing code?

```python
f = None
for i in range (5):
    with open("data.txt", "w") as f:
        if i > 2:
            break
print(f.closed)
```

A.True

B.False

C.None

D.Error

<details><summary><b>Show Answer</b></summary>

Option A.True

<details><summary><b>Explanation</b></summary>

> The WITH statement once used with open file guarantees that the file object is closed once the with block exits.

</details>
</details>

---

10.The readlines() method returns

A.str

B.return a list of lines

C.return a list of single characters

D.a list of integers

<details><summary><b>Show Answer</b></summary>

Option B.return a list of lines

<details><summary><b>Explanation</b></summary>

> Every lines are stored in a list and it will returned.

</details>
</details>

---

11.Write a python program to count number of lines from "data.txt" which are not starting from 'M'.

<details><summary><b>Show Answer</b></summary>

```python
file=open("data.txt")
d=f.readlines()
count=0
for i in d:
     if i[0] != 'M':
         count=count+1
print("Total lines are :", count)
```

</details>

---

12.What will be the output of the following code?

```python
f=open('C:\file.txt')
a=f.read()
```

<details><summary><b>Show Answer</b></summary>

It will read the content from the file.txt until end of file.

<details><summary><b>Explanation</b></summary>

> The read() method reads all the contents from the file.

</details>
</details>

---

13.To open a file c:\scores.txt for appending information, we have a tendency to use

A.outfile = open("c:\\scores.txt", "a")

B.outfile = open("c:\\scores.txt", "rw")

C.outfile = open(file = "c:\scores.txt", "w")

D.outfile = open(file = "c:\\scores.txt", "w")

<details><summary><b>Show Answer</b></summary>

Option A.outfile = open("c:\\scores.txt", "a")

<details><summary><b>Explanation</b></summary>

> it is used to indicate the data to be append.

</details>
</details>

---

14.Write a python program to read the content from "file.txt" and display all numbers.

<details><summary><b>Show Answer</b></summary>

```python
file = open("file.txt", "r")
d = file.read()
for i in d:
  if i.isdigit():
    print(i)
file.close()
```

</details>

---

15.Write a program to replace all the 'a' by '@' in a file "select.txt".

<details><summary><b>Show Answer</b></summary>

```python
f = open("select.txt", "r")
d = f.read()
d = d.replace('a', '@')
f.close()
f=open("select.txt", "w")
f.write(d)
f.close()
```

</details>

---

16.What are the modes are valid to opening file to read and write?

<details><summary><b>Show Answer</b></summary>

1.r+

2.w+

3.wb+

<details><summary><b>Explanation</b></summary>

> To open the files in read-write operations, + is used to append to file mode.

</details>
</details>

---

17.How will you get current position within the files?

A. fp.seek()

B. fp.tell()

C. fp.loc

D. fp.pos

<details><summary><b>Show Answer</b></summary>

Option B. fp.tell()

<details><summary><b>Explanation</b></summary>

> fp.tell() method used to get the current position within the file.

</details>
</details>

---

18.What will be the output of the following code?

```python
str=input("enter the input")
print("Received input",str)
```

<details><summary><b>Show Answer</b></summary>

enter the input:[x*5 for x in range(2,10,2)]
received input is:[x*5 for x in range(2,10,2)]

<details><summary><b>Explanation</b></summary>

> it will printing whatever we are giving input

</details>
</details>

---

19.What is the difference between  r+and w+ modes in python?

<details><summary><b>Show Answer</b></summary>

**r+**:

- It will not create a file if it does not exist.
- If the file is already exists opening it with r+ it does not destroys is contents.
  
**w+**:

- If it does not exist,it will create a file.
- If the file is already exists opening it with r+ it will destroys is contents.

</details>

---

20.How will you delete multiple files in python?

<details><summary><b>Show Answer</b></summary>

- To delete multiple files, simply loop over your list of files and use the higher than os. rmdir() operate. 
- To delete a folder containing all files you want to remove got to import shutil package. Then you can take away the folder as follows.
  
</details>

---
