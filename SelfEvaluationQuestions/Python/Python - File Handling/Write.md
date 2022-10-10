## Write

1.What are the Access modes to write a file?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

- Whenever a text has to be written to a file, we've to open to get in to one of the specified access modes. We will open the file to browse, write or append and sometimes to do multiple operations on a file.

 1.`w` - This mode is used to open a file for writing.

 2.`w+` - Open a file for both reading and writing

 3.`wb` - This is used to open a binary file for writing.

 4.`a` - Used to open a file for writing

 5.`a+` - Opens a file for both reading and appending.
    
 </blockquote>

</details>

---

2.What are the steps needed to write data into a file?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

 1.Find the path of the file.

 2.Open file in write mode.

 3.Write the content into a file.

 4.Close file after completing the write operation.

 5.Append the content at the end of the file.
    

</details>

---

3.How will you open a file in write mode?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - First open the `.txt` file.
> - Enter the data into the file(.txt)
> - Close the file.

```python
f=open('file.txt','w')
f.write('Python is interpreted language')
f.close()
```

> - The above code opens a file in write mode, rewrites the file and then it contains "Python is interpreted language".

</details>

---

4.What are the similarities and differences between `a+` and `w+`?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - **Similarity**: In both the modes, we can do read and write operations.
> - **Difference**: In `w+` mode, file will be truncated(previous data is lost) while in a+ mode,file's existing data will not be deleted and new data will be added at the end of the file.
  
</details>

---

5.What is the difference between  `.` and `..` folders?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details><summary><b>Show Answer</b></summary>

> - In python, the `.` folder is the current folder.
> - In python, the `..` is the parent folder.
  
</details>

---

6.What are the methods to write something to a file?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

 In python, we have two types of methods to write to a file:

 1.`Write(s)`: This method is used to write a string 's' to the stream and it will return the number of characters written.

 2.`writelines(lines)`: This method writes a list of lines into the stream and each line must have a seperator at the end of it.
    
    </blockquote>

</details>

---

7.What are the modes used to append the content to an existing file?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> `a` or `a+` modes are used to append the content at the end of the existing file using the `open()` method.

```python
f=open('C:\file.txt','a')
f.write("Welcome!")
f.close()
```

```python
# reading a file
f=open('C:\file.txt','r')
f.read()
f.close()
```

</details>

---

8.Write a function program in python to count the number of lowercase alphabets in a text file `text.tx`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Consider an `text.txt` file.

```python
def countlower():
    f=open("text.txt","r")
    d=f.read()
    c=0
    for i in d:
        if i.islower():
            c=c+1
    print("Total number of lowercase in text file",c)
countlower()
```

</details>

---

9.Write a python program to write mutiple lines at a time?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

- In python, we have `writelines()` method to save the contents of a list object in a file.

```python
a=["Hello World.\n","welcome to International Airport.\n"]
f=open("C:\text.txt","w")
f.writelines(a)
f.close()
```
</blockquote>
</details>

---

10.Which method is used to set the position of a file pointer?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

 - `seek()` method is used to set the position of file pointer.
 - A file pointer denotes the position of the file contents to be read or written.The file handler is called as a file pointer.
 - `tell()` method is used to return the current position of a file pointer.
    
    </blockquote>
  
</details>

---

11.How will you write a single line in a text file in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

- We can use `write()` function to write a single line to a file.

```python
file=open('myfile','w')
file.write('Hello World!\n')
file.close()
```

 
</details>

---

12.How to write binary data to a file ?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details><summary><b>Show Answer</b></summary>
  <blockquote>

- "Binary" files are any files for which the format is not created for readable characters. Binary files will range from image files like JPEGs or GIFs, audio files like MP3s or binary document formats like Word or PDF. In python, default files are opened in text mode. To open files in binary mode, after specifying a mode, add `b` to that.

**Example**:

```python
file=open('file.txt','w+b')
byte_arr=[125,34,240,0,100]
binary_format=bytearray(byte_arr)
a=file.write(binary_format)
print(a)
file.close()
```

**Output**:

5

 </blockquote>   
</details>

---

13.What are the various methods to copy the source file content into destination file?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

 - `shutil.copyfileobj()`:Used to copy the file object from source code to destination code.
 - `shutil.copyfile()`: Used to copy the contents from one file to another file.
 - `shutil.copy()`:Copy the content from source file to destination file along with the metadata.
 - `shutil.copy2()`:Copy data,timestamps of the supply file to the destination.
    
</blockquote>
  
</details>

---

14.What are the steps to write text file in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

There are four steps to write text file in python,
 - Open the `text file("text.txt")`
 - Write a text file.
 - Append a text file.
 - Finally, we need to close a text file.

    </blockquote>
</details>

---

15.Write a python program to open a file named as `mark.txt` and store in a folder `class.txt` in C drive.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
file=open("C:\\class\\mark.txt")
```

**OR**

```python
file=open("C:\class\mark.txt")
```

</details>

---

16.Write a python program to read first 20 characters from a file named `data.txt`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f=open("data.txt","r")
data=f.read(20)
print(data)
```
</details>

---

17.Write a python program to get five names from the user as input and write into a file `file.txt`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f = open("file.txt","w")
for i in range(5):
   n = input("Enter name")
   f.write(n)
f.close()
```
</details>

---

18.Write a python program to count the frequency of every vowels in a file `text.txt`.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
f = open("text.txt", "r")
d = f.read()
va=ve=vo=vu=vi=0
for i in d:
     if i=='a' or i=='A':
         va=va+1
     if i=='e' or i=='E':
         ve=ve+1
     if i=='i' or i=='I':
         vi=vi+1
     if i=='o' or i=='O':
         vo=vo+1
     if i=='u' or i=='U':
         vu=vu+1
print("Freq of vowel \"a\" is", va)
print("Freq of vowel \"e\" is", ve)
print("Freq of vowel \"i\" is", vi)
print("Freq of vowel \"o\" is", vo)
print("Freq of vowel \"u\" is", vu)
```

</details>

---

19.Write a python program to count the words that starts as 'T' or 'M' in `sample.txt` file.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
file=open("sample.txt", "r")
d=file.readlines()
c=0
for i in d:
     if i[0] == 'M' or i[0] == 'T':
        c=c+1
print("Total lines are :", c)

```

</details>

---

20.Write a python program to copy the entire content file `sample.txt` to `file.txt`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  
> First, read the content from one file and write to another file.
We want to copy the entire file content to another text file. 
  
```python
f = open("file.txt", "r")
f1 = open("sample.txt", "w")
d = f.read()
f1.write(d)
f.close()
f1.close()
```

</details>

---
