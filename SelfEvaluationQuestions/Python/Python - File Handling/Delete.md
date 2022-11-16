## Delete

1.How will you delete a file in python?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

 - Many a times you need to delete the file instead of closing it.
 - If you try to delete the file which is not present, it will `throw` an Input Output error.

```python
import os
#delete file
os.remove("File.txt")
```

> The remove objects and path are described in the os module and hence it is to be imported.
        
</blockquote>

</details>

---

2.What is the use of checking whether a file exists or not?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> To avoid obtaining an error, we would possibly need to check if the file exists before trying to delete it.

</details>

---

3.Write a program to check if a file exist or not?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    
> If we want to check whether the given file exists, we could use `.exists("file_name")`

```python
import os
if os.path.exists("my_file.txtt"):
    os.remove("my_file.txtt")
else:
    print("the file doesn't exist")
```

</details>

---

4.How do we close a file in python?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

```python
open("myFile.txt", "r") as fObj
#perform file operations
fObj.close()
```

 - It is always a good practice to close the file after using it.

Or else,
 - We can use "with" statement while opening the file. We don’t have to explicitly close the file object. As soon as the pointer goes out of the 'with' statement block, the file object is closed.
  
```python
with open("myFile.txt", "r") as fObj:
#perform file operations
#file is closed automatically
```

</blockquote>        
</details>

---

5.How do we delete a folder?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> - In python, to delete a folder, we can use `os.rmdir()` method.
> - This `os.rmdir()` methos is used to delete only the empty folders.  
  
```python
import os
os.rmdir("folder_name")
```

</details>

---

6.Can we delete a folder?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> Yes,we can delete/remove a folder.But,you can remove only empty folders.
> We can't delete the folder which contains content inside the folder.

</details>

---

7.How do we list the files in a directory?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> To list all the files or directories from a particular path, we can use `os.listdir()` method.

```python
import os
for x in os.listdir('_'):
    print(x)
```

</details>

---

8.Write a program to read the file `rename.txt` and display the entire content after removing the leading and trailing spaces.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

```python
f = open("star.txt", "r")
d = f.readlines()
for i in d:
    print(i.strip())
f.close()
```
    
<details markdown="1"><summary> <b>Explanation</b> </summary>
    
> In the above program, we need to first read the file. After removing spaces, diplay the entire content in the file `rename.txt`.
    
</details>
    </details>

---

9.What is the output of the following code?

```python
f = None
for i in range (5):
    with open("data.txt", "w") as f:
        if i > 2:
            break
print(f.closed)
```

A.`True`

B.`False`

C.`None`

D.Error

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> Option A.`True`

<details markdown="1"><summary><b>Explanation</b></summary>

> The `WITH` statement which is used to open file, guarantees that the file object is closed once the `with` block exits.

</details>
</details>

---

10.What would the `readlines()` method return?

A.str

B.return a list of lines

C.return a list of single characters

D.a list of integers

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> Option B.return a list of lines

<details markdown="1"><summary><b>Explanation</b></summary>

> Every line is stored in a list and it will be returned.

</details>
</details>

---

11.Write a python program to count the number of lines from `data.txt` which does not start from `M`.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

```python
file=open("data.txt")
d=f.readlines()
count=0
for i in d:
     if i[0] != 'M':
         count=count+1
print("Total lines are :", count)
```

<details markdown="1"><summary> <b>Explanation</b> </summary>
    
- To count number of lines from `data.txt`, we can use `readlines()` method and then count the number of lines which doesn't start from M.
    
    </details>
</details>

---

12.What is the output of the following code?

```python
f=open('C:\file.txt')
a=f.read()
```

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> It will read the content from the `file.txt` until the end of the file.

<details markdown="1"><summary><b>Explanation</b></summary>

> The `read()` method reads all the contents from the file.

</details>
</details>

---

13.To open a file `c:\scores.txt` for appending the information, we have the tendency to use,

A.outfile = open("c:\\scores.txt", "a")

B.outfile = open("c:\\scores.txt", "rw")

C.outfile = open(file = "c:\scores.txt", "w")

D.outfile = open(file = "c:\\scores.txt", "w")

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> Option A. `outfile = open("c:\\scores.txt", "a")`

<details markdown="1"><summary><b>Explanation</b></summary>

> It is used to indicate the data to be appended.

</details>
</details>

---

14.Write a python program to read the content from `file.txt` and display all numbers.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

```python
file = open("file.txt", "r")
d = file.read()
for i in d:
  if i.isdigit():
    print(i)
file.close()
```
<details markdown="1"><summary> <b>Explanation</b> </summary>
    
- To read the content from file `file.txt`, use `read()` method and to display all the numbers from the file, use `isdigit()` method.
    
</details>       
</details>

---

15.Write a program to replace all the 'a' by '@' in a file "select.txt".

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

```python
f = open("select.txt", "r")
d = f.read()
d = d.replace('a', '@')
f.close()
f=open("select.txt", "w")
f.write(d)
f.close()
```
    
<details markdown="1"><summary> <b>Explanation</b> </summary>
    
- To replace one character with another character, we use `.replace()` method.
    
</details>       
</details>

---

16.What modes are valid to open a file to read and write?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">

 1.r+

 2.w+

 3.wb+
   
  </blockquote>

<details markdown="1"><summary><b>Explanation</b></summary>

> To open the files in read-write operations, `+` is used to append to file mode.

</details>
</details>

---

17.How would you get the current position within the files?

A.fp.seek()

B.fp.tell()

C.fp.loc

D.fp.pos

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> Option B.`fp.tell()`

<details markdown="1"><summary><b>Explanation</b></summary>

> `fp.tell()` method is used to get the current position within the file.

</details>
</details>

---

18.What is the output of the following code?

```python
str=input("enter the input")
print("Received input",str)
```

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> enter the input:[x*5 for x in range(2,10,2)]
> received input is:[x*5 for x in range(2,10,2)]

<details markdown="1"><summary><b>Explanation</b></summary>

> It will print whatever is given as input

</details>
</details>

---

19.What is the difference between `r+` and `w+` modes in python?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
    <blockquote markdown="1">

 **r+**:

 - It will not create a file if it does not exist.
 - If the file already exists, opening it with r+ does not destroy the contents.
  
 **w+**:

 - If the file does not exist,it will be created.
 - If the file already exists, opening it with r+ will destroy the contents.
        
        </blockquote>
</details>

---

20.How will you delete multiple files in python?

![Simple](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

> - To delete multiple files, we can use loop over the list of files and use the higher than `os. rmdir()` operate. 
> - To delete a folder that contains all files, you want to remove `import shutil` package. 
  
</details>

---
