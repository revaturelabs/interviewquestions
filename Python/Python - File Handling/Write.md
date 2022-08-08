## Write

1.What are the Access modes for writing a file?

<details><summary><b>Show Answer</b></summary>

Whenever we want to write down text into a file, we've got to open the get in one of the specified access modes. we will open the file basically to browse, write or append and sometimes to do multiple operations on one file.

1.w - This mode is used to open a file for writing.

2.w+ - Open a file for both reading and writing

3.wb - This is used to opens a binary file for writing.

4.a - Used to opens a file for writing

5.a+ - Opens a file for both reading and appending.

</details>

---

2.What are the steps need to do writing data into a file?

<details><summary><b>Show Answer</b></summary>

1.Find the path of the file.

2.Open file in write mode.

3.Write a content into a file.

4.Close file after completing the write operation.

5.Append the content at the end of the file.

</details>

---

3.How will you open a file in write mode?

<details><summary><b>Show Answer</b></summary>

- First open the .txt file.
- Enter he data into the file(.txt)
- Close the file.

```python
f=open('file.txt','w')
f.write('Python is interpreted language')
f.close()
```

- The above code opens a file in write mode and then rewrites the file it contain "Python is interpreted language".

</details>

---

4.What are the similarity and  difference between a+ and w+?

<details><summary><b>Show Answer</b></summary>

- **Similarity**: In both the modes, we can do read and write operations.
- **Difference**: In w+ mode file will be truncated(previous data lost) while in a+ mode,file's existing data will not be deleted and new data will be added at the end of the file.
  
</details>

---

5.What is the difference between  **.** and **..** folders?

<details><summary><b>Show Answer</b></summary>

- In python the **.** folder is the current folder.
- In python the **..** is the paret folder.
  
</details>

---

6.What are the methods available to write to a file?

<details><summary><b>Show Answer</b></summary>

-In python we have two types methods available to write to a file.

1.Write(s): This method used to write a string s to the stream and it will return the number of characters written.

2.writelines(lines): This method write a list of lines into the stream and Each line must have an seperator at the end of it.

</details>

---

7.What are the modes used to appending the content to an existing file?

<details><summary><b>Show Answer</b></summary>

- 'a' or 'a+' modes are used to appends the content at the end of the existing file in the open() method.

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

8.Write a function in python to count the number of lowercase alphabets present in a text file "text.tx".

<details><summary><b>Show Answer</b></summary>

- Consider you have an "text.txt" file.

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

9.Write a python program to mutiple times at a time?

<details><summary><b>Show Answer</b></summary>

- In python we have writelines() method to save the contents of a list object in a file.

```python
a=["Hello World.\n","welcome to International Airport.\n"]
f=open("C:\text.txt","w")
f.writelines(a)
f.close()
```

</details>

---

10.Which method is used to set the position of a file pointer?

<details><summary><b>Show Answer</b></summary>

- seek() method is used to set the position of file pointer.
- A file pointer is denotes the position of file which file contents to be read or written.The file handler is called a file pointer.
- tell() method used to returns the current possition of a file pointer.
  
</details>

---

11.How will you write a single line in text file in python?

<details><summary><b>Show Answer</b></summary>

We can use write function to write the line to file.

```python
file=open('myfile','w')
file.write('Hello World!\n')
file.close()
```

</details>

---

12.How will you write binary data to a file ?

<details><summary><b>Show Answer</b></summary>

"Binary" files are any files wherever the format is not created of readable characters. Binary files will range from image files like JPEGs or GIFs, audio files like MP3s or binary document formats like Word or PDF. In python by default files are opened in text mode.To open files in binary mode, once specifying a mode, add 'b' to that.

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

</details>

---

13.What are the various methods to copy the source file content into destination file?

<details><summary><b>Show Answer</b></summary>

- shutil.copyfileobj():Used to copy the file object from source code to destination code.
- shutil.copyfile(): Used to copy the contents from one file to another file.
- shutil.copy():Copy the content from one source file to destination file along with the metadata.
- shutil.copy2():Copy namely data namely timestamps of the supply file to the destination.
  
</details>

---

14.What are the steps we need to do write text file in python?

<details><summary><b>Show Answer</b></summary>

There are four steps we need to do write text file in python,
- Open the text file("text.txt")
- Write a text file.
- To append a text file.
- Finally we need to close a text file.

</details>

---

15.Write a python program to open a file named "mark.txt" stored in folder "class.txt" in C drive.

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

16.Write a program to read first 20 characters from a file named "data.txt?

<details><summary><b>Show Answer</b></summary>

```python
f=open("data.txt","r")
data=f.read(20)
print(data)
```
</details>

---

17.Write a program to accecpt five names from the user and write into a file "file.txt".

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

18.Write a program in python to count the frequency of every vowels in a file "text.txt".

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

19.Write a python program to count which are starting from 'T' or 'M' in "sample.txt" file.

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

20.Write a python program to copy the entire content file "sample.txt" to "file.txt".

<details><summary><b>Show Answer</b></summary>
  
> We want to copy the entire file content to another text file. First read the content from one file to write another file.

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
