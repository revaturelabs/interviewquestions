
## Python Interview Questions


## Python Interview Questions

1.	How can you say that python is a dynamically typed programming language?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Python is a dynamically typed programming language. It means that the type of the variable can be changed dynamically by the program at the run time, without re-declaration of the variable.
- In Python, we first define a variable a to hold an integer literal and later in the below program, without re-declaring it, we make it hold a string literal or 
  
```python
a = 43 # Integer literal 
print(f"{a} => {type(a)}") 
 
a = "Welcome to My Home" # String literal 
print(f"{a} => {type(a)}") 
```
  
  </details>
  
--- 
  
2.	Consider John has a list1 =[1,2,3,4,5]. He wants to get an output as list1=[5,4,3,2,1]. How will you help him get that output?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

He wants to get list1=[1,2,3,4,5] as [5,4,3,2,1], he can use `slicing` or `reverse` method to get that output.

```python
list1 =[1,2,3,4,5]
print("before reversing list",list1)
print("after reversing",list1[::-1])
```   
  
  </details>  
  
---
  
3.	Jack wants to enter these multiple line values 5 2 3 4 1 into a single line and he is trying to order the list as [1,2,3,4,5]. Which method helps him to get the values in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If he wants to enter multiple line values into a single line, we can use 'list' separated by commas.
- If he wants to order the list means, we use the `sort()` method in python.
  
```python
values = [5,2,3,4,1 ]
print("list of values",values)
values.sort()
print("sorted values",values)
```

**Output:**
  
list of values [5, 2, 3, 4, 1]
sorted values [1, 2, 3, 4, 5]
  
  </details>
  
  ---
  
4.	Consider you have a list which holds values of multiple datatypes how do you extract only the numbers from that lis?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In a list, Python can contain different types of data, and an item in the list is separated by a comma and the entire list is enclosed in square brackets [].
- If we want to Extract only the numbers from the list, we can use `isinstance()` method through the loop `isinstance(int,float)`. Checking list contains numbers. If not, it contains int and float and it will store in another list, and we will print the list.

**Example**:
  
```python
list1 = ["a", 1, "b", 2, 3, 4, "c", "d"]
list2 = [val for val in list1 if isinstance(val, (int, float))]
print(list2)
```
  
**Output:**

[1, 2, 3, 4]
  
  </details>
  
---
  
5.	If a function doesn’t have a return statement at the end of the function, is it valid in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If there is no return statement that appears in a function definition, the control automatically returns to the calling function after the last statement of the called function is executed.
- It will return `None` if the function doesn't have a return statement.

</details>
  
---
  
6.	Consider we have a list A= [1,4,6,7,9,66,4,94], and you want to get output for A[3]. How will you get the output of the above list?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We have this list A= [1,4,6,7,9,66,4,94] and want to get the output for A[3]. For that, we can use indexing.
- In python, using indexing, we can get a particular value.
- To get the output of a particular index, use the below code,
 
```python
A= [1,4,6,7,9,66,4,94]
print("using index A[3] value is:" ,A[3])
```
  
**Output:**

using index A[3] value is: 7
  
  </details>
 
---
  
7.	Can you tell me the reason why this Datatype `set` is called **the frozen set** in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
A frozen set is an immutable version of a Python set object in python. While elements of a set can be modified at any time, the frozen set remains the same after the creation.

Syntax of `frozenset()` function is:
 
```python
frozenset([iterable])
```
  
</details>
  
---
  
8.	Assume that I have a text, "The Apple a Day Keeps the Doctor Away." We want to replace one string with another for the one/first two occurrences of "An Apple a Day Keeps the Doctor Away." Which technique is used to do this?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to replace one string with another string, use `.replace()` method.
- Syntax for String `replace()`

```python
string.replace(oldvalue, newvalue, count)
```
  
```python
text="The Apple a Day Keeps the Doctor Away."
print("Before replacing the string is :",text)
x=text.replace("The","An",1)
print("After replacing the string is :",x)
```
  
**Output:**
  
Before replacing the string: The Apple a Day Keeps the Doctor Away.
After replacing the string: An Apple a Day Keeps the Doctor Away.
  
</details>
  
---

9.	Fyodor combined multiple lines of text into a single line in python. Which delimiter is used to do that?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>  
  
- we can use triple quotes to print multiple lines into a single line in python.
- Triple quotes ''" or '" are string delimiters that can span multiple lines in Python. Triple quotes are used when combining multiple lines or enclosing a string that has a mix of single and double quotes.

</details>
  
---
   
10.	Consider the string "Python Online Training" as an example. How do I get output as ['Python', 'Online', 'Training'?. Which process produces this result?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can use the `split()` method.
- In python, you can specify the separator, default separator as any whitespace.
  
Syntax:
 
```python  
string.split(separator, maxsplit)
```

```python
txt = "Python Online Training"
x = txt.split()
print(x)
```
  
**Output:**
  
['Python', 'Online', 'Training']

  </details>
 
---  
  
11.	Shan wants to iterate the for loop for a fixed number of times in Python. Which method is used to iterate the loop?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, `range()` function is used to create a series of sequential numbers and to iterate through a loop for a fixed number of times. This loop will be executed until the specified number is in the `range()` function.
 
**Example:**
  
```python
C = ['Bat', 'Cat', 'Tat', 'Fat']
for i in range(len(C)):
     print("C values:", C[i])
```
 
</details>
  
---

12.	Which variables are created globally in a class? Tell me the scope of the variables.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, global variables are created outside of a function.
- Global variables be used by everyone, both inside and outside of function.
- The scope of the variable means the lifetime of the variable. The scope of the Global variable is inside and outside of the function.

```python
x = "global"
def func():
    print("x inside:", x)
func()
print("x outside:", x)
```
  
</details>
  
 ---
  
13.	Which one is used to provide a unique name for every object in python? What are the different types available in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, namespace is use to define as a system that is designed to provide a unique name for every object in python. Types of namespaces that are present in Python are:
   - Local namespace
   - Global namespace
   - Built-in namespace
  
  </details>
  
 ---
  
14.	Can you teach James, how to run the interactive Python interpreter?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- In python, open a command prompt and then type as python or python3, depending upon the Python installation, and then click Enter.
- After entering, we will get as >>>>,
Now you can write and run the Python code. The only drawback is when you close the session, your code will be gone.
  
  </details>
  
 ---
  
15.	James want to know list all the function in a module. Which method helps him to get all the functions in a module?	
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
In Python, if you want to get all the functions in a module, use `dir()` method.
  
**Example:**

```python
import some_module
print dir(some_module)
```

  </details>
  
---
  
16.	Junior developers want to repeat a particular part of the task a finite number of times in python. How is his senior going to help him to repeat the code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to repeat the part of the task for a finite number of times in python, use Enumerate loops.
- you can provide the number of iterations to be performed, as an integer value.
  
  </details>
  
 ---
  
17.	One of the coworkers was working on strings, he doesn't know how to remove whitespaces from a string in python. How would you help him to remove whitespaces?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- In python, to remove whitespaces from a string, we can use `strip()` function.

```python
s.strip()
```
  
- If you want to remove only right or left spaces, use `lstrip()` or `rstrip()` functions.

- We can use `replace()`  to remove all the whitespaces from the string. This function will remove whitespaces between words.
  
  </details>
  
  ---

18.	Ron asked Ken to show the reversed order of the contents of a file in python. How would he do that?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Get the file name from the user.
- Read each line from the file using for loop and store it in a list.
- Print the elements of a list in reverse order.
- Print the lines finally.

Here is the Python Program to read the contents of the file in reverse order. The program output is also shown below.

```python
filename=input("Enter file name: ")
for line in reversed(list(open(filename))):
    print(line.rstrip())
```
  
  </details>
  
---
  
19.	One of the developers is trying to run the following piece of code but after running the code, it throws a Syntax error,
  
```python
x = "CorporateWorld"
print ("Reverse is", [x : -1] ) 
```
  
How do you resolve the above Error?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can use slicing syntax [::-1]
  
```python
x = "CorporateWorld"
print ("Reverse is", x[ :: -1] )
```
  
</details>
  
---
  
20.	Is the `Xrange()` method occupy only the least memory? What would be the reason?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Yes, the `xrange()` method occupies only less memory comparing the `range()`.
- Because it only stores one number at a time in the memory.
  
  </details>
  
---
  
21.	Can you tell us something about generators in python and explain where can we use the generators?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In Python, a generator is a special type of function which does not return a single value, instead, it returns an iterator object with a sequence of values. In a generator function, a yield statement is used rather than a return statement.
- The difference is that while a return statement terminates a function entirely, the yield statement pauses the function saving all its states and later continues from there on successive calls.
  
</details>
  
  ---
  
22.	Consider your Team lead asks how you will handle errors. How will you describe the correct usage of error handling in Python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, `Try` and `except` statements are used to `catch` and handle exceptions. Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause.
  
```python
while True:
     try:
         x = int(input("Please enter a number: "))
         break
     except ValueError:
         print("Please Enter an integer number....")
```
  
</details>
  
---
  
23.	Junior was having some issues with their code. How would you help him to detect Python bugs and statistical issues?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can detect bugs in a python source code using a static analysis tool named `PyChecker`.
- Another tool called `PyLint` checks whether the Python modules meet their coding standards.
  
  </details>
  
  ---
  
24.	Which module in Python supports regular expressions?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python, `re` module supports regular expressions.

```python  
import re
```
  
- Regular Expressions (RegEx) is a special sequence of characters that uses a search pattern to find a string or set of strings.
  
  </details>
  
---
  
25.	How will you explain the function `re.match` to your junior developer?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- `re` in `re.match()` function in Python will search the regular expression pattern and return the first occurrence.
  
  </details>
  
  ---
  
26.Can we use the `+` operator to add elements to a set? If not, then how to add elements to a set?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- No, we can't use the `+` operator to add elements.
- We can use `set.add()` function to add elements.
  
```python
languages = {'Python', 'C++', 'Java', 'C'}
languages.add('.Net')
languages.add('ML')
print(languages)
```
  
  </details>
  
 ---

26.	John wants to check a string whether all characters are in uppercase. Joe helped him to check whether all the characters are in uppercase. Which method did she suggest to him?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, `String.isupper()` method is  used to check if all letters are in Uppercase.
- The `isupper()` method/function returns True if all the characters are in upper case, otherwise False. 

```python
a = "Hello World!"
b = "MY NAME IS KEN"
print(a.isupper())
print(b.isupper())
```
  
  </details>
  
  ---
 
27.	Can you list some differences between single `/` slash and double `//` slash in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- `/` returns float value. It is a Float Division        
- `//` floor division rounds the result down to the nearest whole number. It is Integer Division

```python
num1 = 5
num2 = 2
result = num1 / num2
print("The type of the result", type(result))
result = num1 // num2
print("The type of the result", type(result))
```
  
</details>

---
  
28.	Amie has the following code and is trying to get the output, but she keeps receiving NameError warnings. 
 
```python
list = [John, 70.2, 'abcd', 786, 2.23] 
print(list[7:3])
```
  
Joe was asked to assist their leader. How is she going to fix this issue?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- We are getting NameError because strings should be enclosed with single or double quotes.
- We will get output as an empty list [] because we don't have an index value is 7.
- Correct code is given below
  
```python
list = ['John', 70.2, 'abcd', 786, 2.23] 
print(list[7:3])
```
  
  </details>
  
  ---

29.	Henry wants to learn slicing, but he doesn’t know which data types of support slicing. How would you help him to learn the different data types supported for slicing?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
Python supports slices for any sequential data type like lists, strings, tuples, bytes, byte arrays, and ranges.
  
```python
a = ("a", "b", "c", "d", "e", "f", "g", "h")
x = slice(3, 5)
print(a[x])
```

  </details>
  
  ---
  
30.	John wants to print a single string 10 times using only one print statement. How can he do that?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If we want to print a single string 10 times using only one print statement, we can use the `*` operator.
 
```python
x="Hi"
print(X*10)
```
  
  </details>
  
  ---
  
31.	Consider Jack has this list [1,2,3,4,5,]. He wants to convert the list into the set as (1,2,3,4,5) and John wants to know if it maintains the same order?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If you’re converting a list to set the order, elements is changed.
 
```python
x=[1,2,20,6,210]
print(x,type(x))
# [1, 2, 20, 6, 210] # the order is the same as the initial order
x1=set(x)
print(x1,type(x1))
# set([1, 2, 20, 210, 6]) # in the set(x) output order is sorted
```
  
  </details>
  
 ---
 
32.	How do you find the type and identification number of an object in Python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Using `type()` for returning datatype.
- Using `id()` for returning the identification number.

  </details>
  
  ---
  
34.State some differences between Python 2.x and Python 3.x?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
The key difference between Python 2.x and Python 3.x is the behavior of the print function.
2.x print is treated as a statement whereas in 3.x, it is treated as a function print().
  
  </details>
  
  ---
  
35. James have set of names, roll number and date. He wants to store these values into a single name. Which data type can we use to store all the values into a single name?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- To store different data types into a single value, we can use the list.

 ```python
list1=["Jhon",123,06-09-1999,"jack",78,09-12-2000)
print(list1)
```
  
  </details>
  
  ---
  
36. How to check whether the two variables are pointing to the same object in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>
  
- To check the two variables are pointing to the same object in Python, we use `is` keyword.
- The test returns True if the two objects are the same object.

```python
x = ["a","b","c"]
y = ["a","b","c"]
print(x is y)
```
  
</details>
   
---
  
37. How can we install the particular package using command?
   
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, we can use `pip` command to install a particular package.
  
**Syntax:**
  `pip install package_name`
  
**Example:**

- Install pandas package for this installation and we can use pip install command.
  
```python
pip install pandas
```
  
  </details>
  
  ---
 
38. If Joe want to know the python checkers for Debugging, how will you help him to find them?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
There are many debugging tools, some of them are:
  
i)Pychecker – A tool for locating bugs in python ASCII text file (source code).

ii)pudb – PuDB could be a full-screen, console-based visual debugger for Python.

iii)pdb – The module PDB defines associate degree interactive ASCII text file(source code) debugger for Python programs.

iv)pylint – Analyzes Python ASCII text file (source code) trying to find bugs and signs of poor quality.
  
</details>
   
---
   
39. Ken wants to perform static analysis in Python. How will you help him to find the tools to perform static analysis?
   
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- For Static Analysis,
   -pylint - performs style checking against PEP-8 but also shows errors & potential issues.
   - PyFlakes - Error detection.
   - Bandit - Security Checks.
   - MyPy - Check for errors against optional static type annotations.

  </details>
  
  ---

40. James is working with identifiers in python. His coworker is asking if python is case sensitive when dealing with identifiers. What explanation did James give his coworker?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes
- Since Python is a case-sensitive programming language, it is case-sensitive when dealing with Identifiers. 
- Case is always significant.
 
  </details>
  
  ---
  
41.James is trying to check the python version in CMD. How will you help him to list out the steps needed?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python, we have more methods to check the version in cmd.
    - Using `sys.version` method
    - Using `python_version()` function
    - Using `python -V` command
- Here, this is one of the simplest ways to check the python current version.

  1.Open cmd/terminal
  2.Write python -V and press enter, it will return the current python interpreter version in the form of string.
  
```python
python -V
```

</details>
  
---
  
42. Jack wants to know how to process the file in python. How will you explain the file processing modes that Python supports?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg) 
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- A file is some information which is stored in the computer storage devices. Python provides basic functions and methods necessary to manipulate files by default. You can do most of the file manipulation using a file object. Python language supports two types of files. 
1.Text file 
2.Binary file

- Different modes for opening a file
     - `r` - open a file for reading.
     - `w` - open a file for reading. If the file exists, new file will be created.
     - `x` - open for exclusive creation, fail if the file already exists.
     - `a` - open for reading, appending to the end of the file that exists.
     - `b` - binary mode
     - `t` - text mode
     - `+r` - open a file for reading and writing.

</details>

---
 
43. Franz is asking to her junior to remove the duplicate values from a list. How is she going to get rid of duplicate elements from a list?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To remove duplicate elements/values from a list, we can use the built-in function `set()`.The specification of `set()` method is, it will return only the distinct elements.
  
```python
duplicate_values = [1,1,2,3,2,2,4,5,6,2,1]
distinct_values = set(duplicate_values)
print("Before removing duplicate values:",duplicate_values)
print("After removing duplicate values",list(distinct_values))
```
  
**Output:**
  
Before removing duplicate values: [1, 1, 2, 3, 2, 2, 4, 5, 6, 2, 1]
After removing duplicate values [1, 2, 3, 4, 5, 6]

</details>

---
  

44.Harry wants to know python's parameter passing mechanism. How will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python, parameter passing mechanism is a call by value.
- The call-by-value method arguments that are passed by assignment in Python. The actual parameters to a function call are introduced in the local symbol table of the called function when it is called, arguments are passed using call by value. If you change the value of the parameter within a function, the change is reflected in the calling function.
 
  
```python
def func(a, b):
    a = 'new-value'        
    b = b + 1              
    return a, b            
x, y = 'old-value', 88     # assign values to a and b
x, y = func(x, y)         # function calling
print (x, y )              
```

</details>

---
  
45. Jhon has a string as `hello world` and he wants to cut some part of the string. How will you help him to write a piece of code to cut part as `wo` in the string?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To cut or access some part of the string, we can use the slicing method in python.
  
```python
x='hello world'
y=x[6:8]
print(y)
```

**Output:**

wo
  
- He can use the above code to access 'wo' from 'hello world'.

</details>

---
  
46.Ernest is searching for **conditional expressions** in python. How will you help him to get to know about conditional expressions?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, **conditional expressions** are known as **Ternary operators**.Ternary operators are used to evaluate something based on whether the condition is true or not.
- Ternary operator allows testing a condition quickly instead of multiline if statement.

**Syntax:**

```python
[true] if [expression] else [false]
```
 
```python
x=25
y=10
result='x greater' if x>y else 'y greater'
print(result)
```
  
</details>

---
  
47. Can you explain the process of compilation and loading in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, first it compiles a source code (.py file) into a byte code. Compiling is a simple translation step, and byte code is a lower-level and platform-independent source code.
- After compilation, it is usually stored in `.pyc` files.
- The bytecode (.pyc file) is loaded into the Python runtime and interpreted by a Python Virtual Machine, a piece of code that reads each instruction in the bytecode and executes whatever operation is indicated. The byte code compilation is automatic, and the PVM is just part of the Python system that you have installed on your machine. The PVM is always present as part of the Python system and is the component that truly runs your scripts.
- Each time an interpreted program is run, the interpreter must convert source code into machine code and pull in the runtime libraries. This conversion process makes the program run slower than a comparable program written in a compiled language. 
- Python has something clever to improve the performance. It compiles to bytecode (.pyc files) the first time it executes a file. This substantially improves the execution of the code the next time the module is imported or executed.

</details>

---
  
48. Henry is asking about the `yield` keyword in python to his senior. How will he explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `yield` keyword can be used like the return statement in a function. When done so, the function instead of returning the output, returns a generator that can be iterated upon. 
- You can iterate through the generator to extract items. Iterating is done using a for loop or using the `next()` function.

```python
def Square(n):
  i = 1
  while i < n:
      yield i * i
      i += 1
print(list(Square(5)))
```
</details>

---
  
49. When you are doing a presentation, one of your coworkers is asking if all the memory is freed when python exits. How will you explain this to this coworker?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, Garbage collector releases unreferenced memory with `gc.collect()`. 
- Python will leak memory when you declare circular references in your object declarations and implement a custom __del__ destructor method in one of these classes. 
- Python modules are not always deallocated when Python exits. Python's garbage collector does this. So, Python doesn't detect and frees circular memory references before making use of the garbage collector.
- So, Python does not detect and free circular memory references before making use of the garbage collector.

</details>

---
  
50. How will you use the `split()` methods of the `re` module in python to one of your coworkers?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `re` module provides the regular expression matching operations. Both patterns and strings to be searched can be Unicode strings as well as 8-bit strings.
- `split()` uses a regex pattern to split the given string to a list.
  
```python
import re
str = "Python porgramming test"
print(re.split(" +", str))
```

**Output:**
  
['Python', 'porgramming', 'test']

</details>

---
  
51.Charles wants to print any one of the numbers between 1 to 1000. How will you teach him to print the number with a piece of code?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To generate a random number, first import the module called `random` and `randint()` function is used to get the random number.

```python
import random
print(random.randint(1,1000))
```

**Output:**
  
669
  
</details>

---
  
52. What are accessor and mutator methods in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The method defined within a class can either be an Accessor or a mutator method in python. The  accessor method is a function that returns a copy of an internal variable or computed value. Some examples of Accessor method is,
    - `index()`
    - `count()`
- A mutator method is a function that modifies the value of an internal data variable. 
    - `append()`

</details>

---
  
53.How will you determine the type of instance and inheritance in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The `isinstance()` method checks whether the object is an instance of a class or not.
- The `issubclass()` method asks whether one class is a subclass of another class or not.
  
```python
class MyClass1(object):
  pass
class MySubClass1(MyClass1):
  pass
print(isinstance(MySubClass1, object))
print(issubclass(MySubClass1, MyClass1))
print(isinstance(MySubClass1, MyClass1))
  
```

</details>

---
  
54. Fyodor is trying to get a copy of one object in python. How will you help him to get a copy of an object?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can use the deepcopy to copy an object. The `=` use to assign another reference to the same object in memory.
- The deepcopy used to create a new object in memory with the values of A and B will reference it. 

```python
from copy inport deepcopy
x= deepcopy(y)
```
  
```python
y = x
print( id(A), id(B))
```
  
- Above progran Output is same ids.  
  
```python
y = deepcopy(x)
print( id(y), id(x)
```
  
- Above program Output is different ids.
  
</details>

---
 
55. Can you explain static variables in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, static variables are allocated statically. The scope of the variable is the entire run of the program.
- Variables declared inside the class definition but not inside a method are class or static variables.
  
```python
class My_class:
    static_var = 2
print (My_class.static_var) #2
My_class.static_var = 5
print ( My_class.static_var ) #5
```

</details>

---
  
56.Difference between @static method and @classmethod in python.
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- `@static method`
     - Doesn't need self-parameter
     - Don’t need self or cls as a parameter
     - Need decorator @staticmethod
     - Can only access variables have passed as argument.
- `@classmethod`
     - Doesn't need self parameter
     - Need cls as a parameter
     - Need decorator @classmethod
     - Can be accessed directly through the class. Don't need an instance class.

</details>

---
  
57. John wants to get a list of class attributes in python. How will you help him to get it?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the **inspect module** provides several useful functions to help get information about live objects such as modules, classes, methods, functions, tracebacks, frame objects, and code objects. 
- The **getmembers(object)** method return all the members of an object in a list of (name, value) pairs sorted by name.

</details>

---
  
58. Does python support interfaces like other languages in java or c?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- No, python doesn't support interfaces.
- Python does not support multiple inheritances. But ,you can easily emulate the equivalence of interfaces.

</details>

---
  
59. Can you explain how to achieve web scraping in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Webscraping is a computer software technique for extracting information from websites. This technique mostly focuses on unstructured data on the web into structured data.
- Python has some options for HTML scraping. They are,
     - Mechanize
     - Scrapemark
     - Scrapy
     - BeautifulSoup
  
</details>

---
  
60. Franz wants to protect his python source code for which he asks help from Jack. How is he going to help it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python is a byte-code-compiled interpreted language, it is very difficult to protect. Even if you use an exe-packager like py2exe, the layout of the executable is well-known, and the Python byte codes are well-understood. 
- To protect the only way is to license it because if you compile your code, let us say machine code, if your work is not protected by a license, it can still be commercialized against your will.

</details>

---
  
61. How will you install pip on windows and can you list out some steps to do it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- `pip` is a package management system. It is used to install and manage software packages in python. If you have python 3.4 pip included with Python, it should already be working on your system.
- To install pip, first download `get-pip.py`.
    - Open your command prompt window and run
        `python get-pip.py`
    - To verify the installation in your command prompt 
         `pip --version`
    - Upgrade pip on windows
         `python -m pip install --upgrade pip`

</details>

---
  
62.What do *args and **kwargs mean?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The parameter with ** and * allow for functions to be defined to accept and for users to pass any number of arguments, positional (*) and keyword (**). The single * form is used to pass a non-keyworded when we aren't sure how many arguments are going to be passed to a function, or if we want to pass a stored list or tuple of arguments to a function. The double **  form is used to pass keywords when we don't know how many keyword arguments will be passed to a function, which will be in a dict named kwargs.
 
***args example**
  
```python
def print_colours(*args):
    print(args)
print_colours('red','blue','gray','yellow')
```

** **kwargs example **
  
```python
def print_num(**kwargs):
  for key in kwargs:
      print (key, kwargs[key])
print_numb(one=1, two="two",three=3,four="four")
```

</details>

---
  
63. Ken wants to know about exception handling in python how will you teach him to do it in object-oriented programming?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- An exception is a type of notification that interrupts the usual program execution. Exceptions help you to detect and react to unexpected events. The program’s state is saved when an exception arises, and control is passed to an exception handler. The exceptions are thrown or raised by programming code that must send a signal to the executing program about an error or an unusual situation.

**For example**, when you want to open a file that doesn’t exist, the code responsible for opening the file will detect this and throw an exception with a proper error message. Exceptions are of two types in OOPs, such as checked exceptions and unchecked exceptions. 

 - **Checked exception** - The classes which inherit compile-time exceptions are known as checked exceptions.
 - **Unchecked exception** - The classes which inherit Runtime exceptions are known as unchecked exceptions.

</details>

---
  
64. How many except statements can a try-except block have in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can have more than zero except statements.
- There has to be at least only one except statement.
  
**Syntax:**
  
```python
try:
   You do your operations here;
except Exception1:
   if the exception1 then execute this block
except Exception2:
   if the exception2 then execute this block
else:
   If there is no exception, then execute this block.
```

</details>

---
  
65. James asks his junior to run the following piece of code.
  
  ```python
  print([1, 2, 3] + 4, 5, 6)
  ```
  
He is asking to print the output for the code, but he got some error. How will you help him to correct the error and get the output?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If he runs the above code, he will get a TypeError as it can only concatenate list (not "int") to list
  
**Correct code:**
  
 ```python 
 print([1, 2, 3] + [4, 5, 6])
 ```

**Output:**
  
[1, 2, 3, 4, 5, 6]
  
- We can add only the two list, not an integer value.
  
</details>

---
  
66. Charles wants to move the python shell to the home directory using `~` in python. How will you guide him to move to the home directory through a piece of code?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer </b></summary>
<blockquote>

- On Unix and Windows, return the argument with an initial component of ~ or ~user replaced by that user's home directory.
  
```python
import os
home = str(os.path.expanduser('~'))
print(home)
```

</details>

---
  
67. Ryan asks you to test on variables against multiple values. How will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We can use the `in` operator to test variables against multiple values.
  
```python
x=5
if x in (1,2,3,4,5):
  print("found")
else:
  print("Not found")
```
  
- The above program validates x=1 or x=2 or x=3 or x=4 or x=5.

</details>

---
  
68. How to call an external command in Python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The subprocess module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. The subprocess.call() method runs the command described by args. Wait for the command to complete, then return the returncode attribute.
  
```python
from subprocess import call
call(["dir"])
```

</details>

---
  
69. Kein is asking about the meaning of a single and double underscore before an object name to his senior coworker. How will he explain it to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- _fun: weak "internal use" indicator. E.g., from X import * does not import objects whose name starts with a single underscore.
- __fun: the interpreter replaces this name with _classname__fun to ensure that the name will not overlap with a similar name in another class.

</details>

---
  
70. Can you write a piece of code to read a single character from the user?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

```python
while True:
  Input = input('>>')
  if len(Input) == 1:
      break
  print ("enter only one character")
```

</details>

---
  
71. Fyodor asked a doubt to his coworker to explain the difference between `raw_input()` and `input()` in python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python 2, `raw_input()` takes only what exactly user the enter by themself and passes it back as a string.
- In python 3, `raw_input()` was taken as `input()`. So it will return exactly what the user entered and the old input() was removed.

</details>

---
  
72. Can you explain why Python is not fully object-oriented?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

Python is an object-oriented programming language but not completely. Because, Python doesn't support strong encapsulation, which is one of many features associated with the term 'object-oriented'.

</details>

---
  
73. Henry was checking if there is any way to kill a thread in python. How will you help him to find it and explain it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can kill a thread. To kill a thread, we have many methods which are,
    - Create an **Exit_Request** flag.
    - Using the `multiprocessing` module.
    - Using the `trace` module.
    - Use the `ctypes` to raise Exceptions in a thread.
- We can use any one of the methods and we can kill the thread.
  
</details>

---

74. Can you explain if it is necessary to put a space between operators and operands in python?
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, it is necessary to put a space between operators and ooperandsin python.
- If we use space in between both operator and operands, it will help readability.
  
```python
x + y
(sum ** 2) + 3 * val - 1
x * (3 + 8)
b + math.sqrt(3 * max_val)
```

</details>

---
  
75. Can you explain why assignment operators cannot be used in an expression?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The error is a simple typo: x = 0, which assigns 0 to the variable x, and was written while the comparison x == 0 is certainly what was intended.
- The reason that it is not allowing assignment in Python expressions could be a common, hard-to-find bug in those different languages, caused by this construct:

```python
if (x = 0) {
...error handling...
}
else {
...code that only works for nonzero x...
}
```

</details>

---
  
76. Charles asked what are the rules for local and global variables in Python. How will you explain this to him?  
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the variables referenced within a function are global.
- When a variable is assigned a new value anyplace within the body of a function then it's assumed as local.
- In a function, if a variable is ever assigned a new value, then the variable is implicitly local and explicitly it should be declared as global.

</details>

---
 
77. How will you create an empty class in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to write an empty class in python, we can use the pass statement. Pass is a special statement in python, but it does nothing.
- Pass works as a dummy statement.
- Regardless, objects of an empty class can also be created.

</details>

---
  
78. Can you train your coworker on how will you pass optional or keyword parameters from one function to another function in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

To pass the keywords from one function to another function, we can use the keyword arguments.

```python
def func (**kwargs):
 print('func kwargs:', kwargs)
def funcy (a, b, c, **kwargs):
  print('other args:', a, b, c)
  print('keyword args:', kwargs)
def funcy(a, b, c, **kwargs):
    print('other args:', a, b, c)
    print('keyword args:', kwargs)
    func(**kwargs)
```

</details>

---
  
79. How will you find methods or attributes of an object in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, attributes of a class can even be accessed using the following built-in methods and functions:
   - `getattr()` – This function is used to access the attribute of an object.
   - `hasattr()` – This function is used to check if an attribute exists or not.
   - `setattr()` – This function is used to set an attribute.

</details>

---
  
80. How will you make a higher-order function in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- A higher-order function accepts one or additional functions as input and returns a new function. Sometimes it's needed to use function as data. To form a higher-order function, we need to import the functools module.

</details>

---
  
81. Franz asked about the new and override modifiers in python. How will explain this to him.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- **New Modifiers** - In python, state the compiler to run a new function and not use the one from the base class.
- **Override Modifier** - Instructs to run the base class version of a class and it will not create a new one. This reduces redundant repetitions of writing codes.

</details>

---
  
82. Can you explain something about the `new` method in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the `new` method creates the instance of a class. It will allocate memory for the object. The instance variable of an object needs memory to hold it. This new will be called at the time of object creation.
- This `new` method will be used to control the creation of a new instance. 

</details>

---
  
83. William is asking about the strong typing in python. How will you clarify it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, when the object is passed in the strong typing, it checks whether the method is present in the object. Using the python `hasattr()` function, using we can check whether the method is present in the past object.

</details>

---
  
84. James wants to write a piece of code to pick a random item from a list or tuple. How will you help him to do it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can use the `random` keyword to get a random item from a list.
 
```python
import random
x=['a','b','c','d']
print(random.choice(x))
```

</details>

---
  
85. How do we make forms in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, cgi module make forms. It has some attributes: form.name:name of field
  - **form.filename**: Client-side filename for FTP transactions.
  - **form.value**: Value of field as a string.  
  - **form.file**: File object from which to read data.
  - **form.type**: Content type.
  - **form.type_options**: Options of 'content-type' line of HTTP request, returned as a dictionary.
  - **form.disposition**: The field 'content-disposition'.
  - **form.disposition_options**: Options for 'content-disposition'.
  - **form.headers**: All HTTP headers are returned as a dictionary.

</details>

---
  
86. Ernest asks why the identifier names with a leading underscore are disparaged. How will you explain this to him?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python doesn't have a concept of private variables, use the leading underscores to declare a variable as private.

</details>

---
  
87. Is it possible to call the parent class without its instance creation in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, it is possible if other child classes instantiate the base class or if the base class is a static method.

</details>

---
  
88. Ken asks if the methods and constructors are the same things in python.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- **No**, In python there are some differences between both methods and constructors.
- **Method**: It is a function that is a member of a class. Methods consist of statements that may or may not return an output. 
- **Constructor**:  It is a special type of method that has the same name as the class name. These methods are used to initialize an object's state.

</details>

---
  
89. What do you mean by file-related modules in Python? Can you list some of the file-related modules in Python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python arrives with some file-related modules that have functions to manipulate text files and binary files in a file system. These modules can be used to create text or binary files, update their content, copy, delete, and more.
- Some file-related modules are `os, os. path, and shutil.os`. The `os.path` module has functions to access the file system, while the shutil.os module can be used to copy or delete files.

</details>

---
  
90. Kein asks about `exec()` and `eval()` in python. How will you explain this to him?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the `exec()` function executes the specified Python code. The `exec()` function accepts large blocks of code.
- In python, the `eval()` function only accepts a single expression.

</details>

---
  
91. Can you explain to me what is the Metaclasses in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

- A metaclass in Python is a class of a class that defines how a class behaves. A class in itself is an instance of a metaclass. A class in Python defines how the instance of the class can behave. To grasp metaclasses well, one has to have prior experience working with Python classes.

</details>

---
  
92. The senior developer asks his junior developer to explain the `swapcase()` function in python. How would he explain this to him?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `swapcase()` is a string’s function
- It converts all the uppercase characters into lowercase and vice versa.

</details>

---
  
93. Can you explain to your junior why would you use NumPy arrays instead of lists in Python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

-NumPy arrays are providing users with three main advantages as below:
   - It consumes a lot less memory, thereby making the code more efficient.
   - It executes faster and does not add heavy processing to the runtime.
   - NumPy has a highly readable syntax, making it easy and convenient for programmers.

</details>

---
  
94.Can we import multiple modules in python. Give an example?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, we can import multiple modules in python.
- If we want to use more than one module, then we can import multiple modules. This is the simplest form to import a statement.
**Syntax:**
  `import module1[,module2[,.. moduleN]`
  
```python
# Importing two modules
import math, random
print(math.fact(5))
print(random.randint(10, 20))
```
  
</details>

---
  
95. How can we use `re.split()` function in a module?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, re.split() is used to define how many splits you want to perform.
For example, if maxsplit=3, then it will do 3 splits.

**Syntax:**
`re.split(pattern,string,maxsplit=0,flags=0)`
  
  - In a regular expression, patterns and strings are the mandatory ones.
  - maxsplit and flag functions are not mandatory.
  
1.pattern: In a regular expression pattern, a function is used for splitting the string.

2.string: The string we want to perform the split.

3.maxsplit: The number of splits you want to perform. It's based on the split size.

4.flags: There are no flags applied, by default.


  
 
  
  
</details>

---

96. What is functional programming? Does Python follow a functional programming style? If yes, list a few methods to implement functionally oriented programming in Python.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, Functional programming is a coding style where the main source of logic in a program comes from functions.
- Incorporating functional programming in our codes means writing pure functions.
- Pure functions are functions that cause little or no changes outside the scope of the function. These changes are referred to as side effects. To reduce side effects, pure functions are used, which makes the code easy-to-follow, test, or debug.

</details>

---
  
97. Can you explain if it is necessary for every `if` block to be accompanied with an else block. Comment on this statements with the help of an example.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- No, it’s not required to write the else part for the if statement.

-In fact, most of the developers prefer and recommend avoiding the else block.

Instead of writing

```python
if (number >= 19) {
    allow_user = true;
} else {
    allow_user = false;
}
```
  
Most of the developers prefer:

```python
allow_user = false;
if (number >= 18) {
    allow_user = true;
}
```

</details>

---
  
98. Can you tell me the approaches you would use for module importation in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If you need to import some particular module, use the import keyword, such as: `import array` or `from array import *.`There are some other ways, they are,
  - Import the whole module using its original name: pycon import random
  - Import specific things from the module: pycon from random import choice, randint
  - Import the whole module and rename it, usually using a shorter variable name: pycon import pandas as pd
  - Import specific things from the module and rename them as you're importing them: pycon from os. path import joins as join_path
  
</details>

---
  
99. Show the polymorphism concept by using `+` operator inside a class.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python, `+` operator is not only used to add values together but, it can also be used to concatenate two or more string values. Let's understand this better through a code.
  
```python
class Operator:
    
    def add(self, x, y):
        return x + y
    
    def concatenate(self, a, b):
        return a + b

obj = Operator()
print(obj.add(10, 20))
print(obj.add("Jack","ken"))
```
  
</details>

---
  
100. Is there any way to read files without opening them? Which function is used to open a file?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- No, we can't read files without opening.
- If you want to read a file, open the file first then, use open() function to open a file.

</details>

---
  
  
101. Can you list out python logging functions?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- **logging.info()**  for the detailed output of events that occur during the normal operation of a program.
- **warnings.warn()** issues a warning for a runtime event if the issue is avoidable.
- **logging.warning()** issues a warning for a runtime event if we need to note the event even when the client can do nothing about it.
- **logging.error()**, **logging.exception()** report the suppression of an error without raising an exception

</details>

---
  
102. William raised a question to his colleague whether a function can call another function. What should be his colleague’s answer to William's question?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, it is possible for a function to call another function in python.

```python
def add(x):
    return x+1
def Function(One, x):
    return addOne(x)**2
```
  
- Whenever we call Function(One,x), we will get the output.

</details>

---
  
103. Jane asked his colleague about when python decorator is used and how will explain this to him.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

-  In python, a decorator is a design pattern that allows a user to add new functionality to an existing object without modifying its structure. These decorators are usually called before the definition of a function you want to decorate.
  
```python
def my_decorator_function(func):
    def wrapper_func():
        func()
    return wrapper_function
``` 

</details>

---
  
104. In python, list, and array both are similar. How one should choose which data type to go for?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- list
  - When you want to store multiple datatypes into a single name, we can use list.
  - We can't handle arithmetic operators directly.
  - It is a small sequence
- array
  - Using an array, we can store single data types under a single name.
  - We can handle arithmetic operators directly.
  - It is a longer sequence.

</details>

---
  
105. Can you draw a comparison between recursive and iterative techniques forproblem-solving.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

**Recursive:**
  - It is a technique of defining anything in terms of itself.
  - There must be an exclusive if statement inside the recursive function specifying stopping condition.
  - Not all problems have the recursive solution.
  
**Iteration:**
  - It is a process of executing statements repeatedly until some specific condition is specified.
  - Iteration involves four clear-cut steps, initialization,condition,execution and updating.
  - Any recursive problem can be solved iteratively.

</details>

---
  
106. Can you tell me how long an identifier can be in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, an identifier can be of infinite length. The PEP-8 standard sets a rule that you should limit all lines to a maximum of 79 characters.

</details>

---
  
107. Ernest asked his senior to explain the docstrings for python modules. How would he explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python, docstring is a string used to document a Python module, class, function or method, so that programmers can understand what it does without having to read the details of the implementation. Also, it is a common practice to generate online documentation automatically from docstrings.

</details>

---
  
108. If Brian wants to create a new test suite with Python unit test, how would he create the test?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- You can create a new test suite with Python unittest by subclassing unittest, TestSuite and add your test cases.

</details>

---
  
109. How does one use multiple assertions to verify that all conditions have been met in Python unittest?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, by using the `assertTrue()` and `assertFalse()` methods, it is possible to check multiple conditions in a single test. 
  For example, to check that a list is not empty and that its first element is greater than 5, one could use the following code:

```python
assertTrue(len(mylist) > 0)
assertTrue(mylist[0] > 5)
```

</details>

---
  
110. What do you understand about the Assert keyword in python unittest?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `Assert` is a keyword used in the Python unittest module to make assertions about the code being tested. Assertions are checks that the code does, and it is supposed to be doing, and they will throw an error if the check fails. This is useful for finding bugs in code, and for making sure that the code behaves as expected.

</details>

---
  
111. Ernest wants to find some tools for unit tests. Which tools do you suggest using for automating unit tests?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We can use the Python `unittest` module for automating unit tests. This module is part of the standard library, so it is always available, and it is relatively easy to use.

</details>

---
  
112. One of your colleagues is asking you to create your own package in Python. How would you do it?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- It overrides any initialization from an inherited class and is called when the class is instantiated.
- We know that a package may contain sub-packages and modules. A module is nothing but Python code.
To create a package of our own, we create a directory and create a file __init__.py in it. We leave it empty. Then, in that package, we create a module(s) with whatever code we want. For a detailed explanation with pictures, refer to Python Packages.

</details>

---
  
113. What is Monkey patching in python? Can you Give an example?  
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We can dynamically modify a class or module at run-time in python.
  
```python
class A:
    def func(self):
        print("Hi")
    def monkey(self):
        print "Hi, monkey"
    m.A.func = monkey
    a = m.A()
    a.func()
```

</details>

---
  
114. Keith asked his employee the purpose of PYTHONSTARTUP, PYTHONCASEOK, PYTHONHOME & PYTHONPATH environment variables. How would he be answering him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- PYTHONSTARTUP − It contains the path of an initialization file containing Python source code. It is executed every time you start the interpreter. It is named as .pythonrc.py in Unix and it contains commands that load utilities or modify PYTHONPATH.

- PYTHONCASEOK − It is used in Windows to instruct Python and to find the first case-insensitive match in an import statement. Set this variable to any value to activate it.

- PYTHONHOME − It is an alternative module search path. It is usually embedded in the PYTHONSTARTUP or PYTHONPATH directories to make switching module libraries easy.

- PYTHONPATH − It has a role like PATH. This variable tells the Python interpreter where to locate the module files imported into a program. It should include the Python source library directory and the directories containing Python source code. PYTHONPATH is sometimes preset by the Python installer.

</details>

---
  
115. Suppose class C inherits from classes A and B as class C(A,B). Classes A and B both have their own versions of method `func()`. If we call `func()` from an object of class C, which version gets invoked?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python, we already know about Multiple Inheritance, Method Resolution Order (MRO). C does not contain its own version of `func()`. Since the interpreter searches in a left-to-right fashion, it finds the method in A, and does not look for it in B.

</details>

---
 
116. The manager asks if Stacie can tell how to convert a string to a number?
  
.[Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

If you want to convert String to a number using the built-in int() function, it takes in any python data type and converts it into a integer.
  
```python
n="548"
n1=int(n)
print(type(n1),n1)
```
  
</details>

---
  
117. Joe was asking about the difference between the assertTrue() and assertFalse() methods in python. How will you explain this to her?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the `assertTrue()` method checks whether the given condition is True. While the `assertFalse()` method checks the given condition is False, these methods are used to check the return value of a given function.

</details>

---
  
118. If you're ever stuck in an infinite loop, how could you break out of it?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can press Ctrl+C to interrupt the execution. Let's create an infinite loop for an example.
  
```python
def c_func(n):
    while(n==7):
        print(n)
c_func(7)
```
  
**Output:**
7
7
7
7
7
.
.
.

- Whenever we press ctrl+c, we will get the below 
  
Traceback (most recent call last):
File "<pyshell#332>", line 1, in counterfunc(7)
File "<pyshell#331>", line 2, in counterfunc
while(n==7):print(n)
KeyboardInterrupt

</details>

---
 
119. Jack wants to share his global variable with his friend across modules, but he doesn't know how to do it. Can you help him to do this?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To share global variables across modules, we need to create a special module, and then import the config module into all modules of our application. This lets the module be global to all modules.

</details>

---  
  
120. Brian is asking his student about the directory that is currently used and he/she won't know where they are. How will you help them to find the current directory?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To find the current directory, we use the function/method `getcwd()`. We need to import it from the module os.

```python
import os
os.getcwd()
```
 
'C:\Users\lifei\AppData\Local\Programs\Python\Python36-32'

`type(os.getcwd)`
  
<class 'builtin_function_or_method'>

- We can also change the current working directory with `chdir()`.

```python
os.chdir('C:\\Users\\lifei\\Desktop')
os.getcwd()
```
  
'C:\Users\lifei\Desktop'

</details>

---
  
121. Can you list out some pdb commands in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Some pdp comments are given below,
  
- `<b>` — Add breakpoint
- `<c>` — Resume execution
- `<s>` — Debug step by step
- `<n>` — Move to next line
- `<l>` — List source code
- `<p>` — Print an expression`
  
</details>

---
  
122. Can you explain JSON? Describe in brief how you'd convert JSON data into Python data.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer </b></summary>
<blockquote>

- JSON stands for JavaScript Object Notation. It is a highly popular data format, and it stores data in NoSQL databases.
    - 1.A collection of <name,value> pairs
    - 2. An ordered list values.
- Python supports JSON parsers. In fact, JSON-based data is internally represented as a dictionary in Python. It will convert JSON data into Python data, and for that we use the `load()` function from the JSON module.
  
</details>

---
  
123. In python optionally, what statements can you put under a try-except block and can you explain this with an example?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To put under a try-except block, we have two of these blocks,

     - `else`- To run a piece of code when the try-block doesn't create an exception.

     - `finally`- To execute some piece of code regardless of whether there is an exception.

```python
try:
    print("Hello")
except:
    print("Sorry")
else:
    print("Oh then")
finally:
    print("Bye")
```
 
**Output:  **
  
Hello
Oh then
Bye 

</details>

---

124. Paul wants to know how to use GUI that comes with Python to test your code. How will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

That is just an editor and a graphical version of the interactive shell. You can write your code or load code and run it or type it into the shell. There is no automated testing.

</details>

---    
  
125. Why is it that none of my threads is not running? How can I make it work and explain with an example?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- As soon as the main thread exits, all threads are killed. Your main thread is running too quickly, giving the threads no time to do any work. A simple fix is to add a sleep to the end of the program that's long enough for all the threads to finish,
  
```python
import threading, time
def thread_task(name, n):
    for i in range(n):
        print (name, i)
for i in range(10)
```

</details>

---

  
126. The brain wants to write a program that will accept an email id, using regular expressions and the re-module. He is asking his coworker how he will help him to write code.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- First, we need to import `re` module first and write regular expressions conditions to search the email.
  
```python
import re
e=re.search(r'[0-9a-zA-Z.]+@[a-zA-Z]+\.(com|co\.in)$','brian@gmail.com')
e.group()
```

**Output:**
brian@gmail.com 
 
</details>

---
  
127. Wiliam is asking the way to skip a particular test method or class using the decorator @unittest.skip in python. How will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, you can use the @unittest.skip decorator to skip a particular test method or class. This is useful when you want to temporarily disable a test or if you know that a particular test will not work on your system.

</details>

---
  
128. Under what circumstances would one use a while statement rather than for?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the while statement is used for simple repetitive looping.
- The `for` statement is used when one wishes to iterate through a list of items, such as database records, characters in a string, etc.

</details>

---
  
129. What will be printed by the below last statement?
  
```python
flist = []
for i in range(3):
    flist.append(lambda: i)

[f() for f in flist]   # what will this print?
```
  
In any closure in Python, variables are bound by name. Thus, the above line of code will print the following:
[2, 2, 2]
Presumably not what the author of the above code intended?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>

-  For that, we can use either create a separate function or pass the args by name.
  
```python
flist = []
for i in range(3):  
    flist.append(lambda i = i : i)

[f() for f in flist]
[0, 1, 2]
  ```
  
</details>

---

130. Can you discuss how to count the lines in a file? How would you do it if the file is too big to hold in memory?
   
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We can use `readlines()` or a loop solution if the file size is small.
- Use Generator and Raw interface to get line count if you are working with large files.
- We can use a loop and `enumerate()` for large files because we don’t need to load the entire file in memory.
  
```python
f = open(file_name, 'rt')
line = f.readline()
while line:
    line = f.readline()
f.close()
```

</details>

---
  
131. Wiliam asks his junior to predict the output of the following code.
  
```python
a = 10
b = 4
c = 0
if a | b:
    if a ^ b:
        if a or b:
            print("Hi-World")
else:
    print("Hello-World")
```
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The output of the above code is Hi-world.
- "Hi-world" is executed because all the `if` conditions become true for the values of 'a' and 'b'.

</details>

---
  
132. Does python support switch or case statement? If not, what is the reason for the same?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Python doesn’t have a switch/case statement because of some unsatisfactory proposals.
- Most of the programming languages have switch/case because they don't have proper mapping constructs. You cannot map a value to a function, that's why they have it.
- But in Python, you can easily have a mapping table(dict) where a certain value maps to a certain function. Python functions are first-class values, you can use the functions as the values of the dictionary get(key[, default]) method. Performance-wise, the Python dictionary lookup will almost certainly be more efficient than any solution you can rig yourself.

</details>

---
  
133. What is the statement that can be used in Python if a statement is required syntactically but the program requires no action?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `pass` keyword is used to fulfil the syntactical requirements.
  
```python
try x[10]:
    print(x)
except:
    pass
```
  
- Use the `pass` keyword here like,
  
```python
if a > 0:
    print("Hello")
else:
    pass
```

</details>

---
  
134. James wants to perform some pattern matching in python. How will you help him to perform pattern matching and how would you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python, Regular Expressions/REs/ regexes enable you to specify expressions that can match specific "parts" of a given string. 
- For instance, we can use a regular expression to match a single character or a digit, a telephone number, an email address, etc. 
- The Python `re` module provides regular expression patterns. 
- This module is providing methods for searching text strings or replacing text strings along with methods for splitting text strings based on the pattern defined.

</details>

---

135. Can you name a few methods that are used to implement Functionally Oriented Programming in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python supports methods, such as `filter()`, `map()`, and `reduce()`, that are very useful when you need to iterate over the items in a list, create a dictionary, or extract a subset of a list.

`filter()` – enables you to extract a subset of values based on conditional logic.
`map()` – it is a built-in function that applies the function to each item in an iterable.
`reduce()` – repeatedly performs a pair-wise reduction on a sequence until a single value is computed.

</details>

---
  
136. How do I call a method defined in a base class from a derived class that overrides it?
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, if you're using new-style classes, use the built-in `super()` function:

```python
class Derived(Base):
    def math (self):
        super(Derived, self).math() 
```
 
If you're using classic classes: For a class definition such as class Derived (Base): you can call method `math()` defined in Base as Base. `math(self,arguments)`. Here, Base.math is an unbound method, so you need to provide the self-argument.

</details>

---
  
137.Todd wants to know some membership operators in python. How will you explain him?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, with the operators `in` and `not in`, we can confirm if a value is a member of another.
  
```python
'me' in 'x'
```
 
True
  
```python
'us' not in 'y'
```

</details>

---

138. Why is the `:` `if` statement invalid syntax (Python, Python 3.x, if statement)?
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In Python, "SyntaxError: invalid syntax" will occur when we use a single equals operator instead of the double equals operator in an if statement. To resolve the error, we can use the double equals == if comparing values and the line of the if statement ends with a colon.
 
```python 
if a=b:
    print("equal")
else:
    print("not equal")
```

</details>

---
  
139. Stacie got some error while executing a piece of code in python and the error is "valueerror: invalid literal for int() with base 10". How will you help her to resolve this error?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- This error occurs because we try to convert "7.4: to an integer. The value "7.4" is formatted as a string. Python cannot convert a floating-point number in a string to an integer.
- To overcome this issue, we need to convert the value a user inserts to a floating-point number. Then, we can convert it to an integer.
We can do this by using the `float()` and `int()` statements. The `int()` function returns an integer. The `float()` function returns a floating-point representation of a float.
- Finally, the code first converts the value of the variable to a float. Next, it will convert the value to an integer.

</details>

---
  
140. Which one is the built-in function used in Python to iterate over a sequence of numbers?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To iterate over a sequence of numbers, we can use `range()`,`for` loop built-in functions.
  
Syntax: `range(start,end,step count)`
  
```python
a = range(1,10,2)
print (a)
```

To iterate, 
  
```python
for i in range(1,10):
    print (i)
```
  
</details>

---
  
141. What is used to represent Strings in Python? Are single or double quotes used for String representation in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python, double quotes are used for String representation and single quotes are used for String representation. These work in Python. The most used way by PEP 8 is in double quotes.

</details>

---
  
142.Why is this 'raw_input' detected as an error in Python-v3.0?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

It depends upon the python version. If you are using python 2.5, we can use `input()` instead of `raw_input()` to take input from user.

```python
name = raw_input("enter your name please")
print(name)
```
  
Now Input is used to take from user input in python.

```python
name = input("enter your name please:")
print(name)
```

</details>

---
  
143. If Carmella wants to upgrade all Python packages at one time, how will you help him to upgrade all the packages?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

If you want to upgrade all Python packages at one time with pip, we have so many ways and this is one way to do it.
  
To upgrade all local packages, you can install `pip-review`:

` pip install pip-review`
  
After that, you can either upgrade the packages interactively:

` pip-review --local --interactive`
  
Or automatically:

` pip-review --local --auto`

</details>

---
  
144. Considering I have a custom class,
  
```python
class A:
    def __init__(self, a, b):
        self.a = a
        self.b = b
```  
  
The class is not iterable or indexable or anything like that. If possible, I would like to keep it that way. Can you tell me if there is a way to return a custom value for min and max in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, it is possible. When min takes one argument, it assumes it to be an iterable, iterates over it and takes the minimum value. So,
  C  
```python
class A:
    def __init__(self, a, b):
        self.a = a
        self.b = b
    def __iter__(self):
        yield self.a
        yield self.b
```  
  
- If you don't want to use `__iter__`. You want to create your own min function, that calls some _min_ method if there is one in the argument, it is passed to and calls the mini else.

```  
mini = min
def min(*args):
    if len(args) == 1 and hasattr(args[0], '_min_'):
        return args[0]._min_()
    else:
        return mini(*args)  
```  

</details>

---
  
145. If Henry wants to know the parameter-passing mechanism in python, how will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To pass its parameters to a function in Python, we can use pass-by-reference. If you want to change a parameter within a function, the change reflects in the calling function. This is its default behaviour.
- However, when we pass literal arguments like strings, numbers, or tuples, they it is pass by value. Because they are immutable.

</details>

---
  
146. In python, I want to add created date, and created user details (some basic details) at the start of each log file. How will you help him to add some basic details in the string of each log file?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can use this to add some basic details in the string of each log file.
- Then change your handler class to this custom one.

```python
from datetime import date
import os

class HeaderFileHandler(logging.FileHandler):
    def _open(self):
        open_func = self._builtin_open
        new_log = not os.path.exists(self.baseFilename)
        f = open_func(self.baseFilename, self.mode,
                         encoding=self.encoding, errors=self.errors)
        if new_log:
            f.write(f"Log created on {date.today()}\n")
        return f
 ```

</details>

---
  
147. How can you declare multiple assignments in one statement?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we have two more ways to assign multiple values in a single statement.
  
```python
a,b,c=3,4,5     #This assigns 3, 4, and 5 to a, b, and c.
a = b = c =3         #This assigns 3 to a, b, and c
```
</details>

---
  
148. Consider I have a req.txt file, then tried to install the packages according to my text from my local directory. How can I install packages using pip according to the req.txt file from a local directory in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can use the below command
  
```python
pip install -r /path/to/req.txt
```
  
**Explanation:**
  
 -r, --req < filename >

</details>

---
  
149. Can you explain the closure in Python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python, a closure is said to occur when a nested function references a value in its enclosing scope. The whole point here is that it remembers the value.
  
```python
def A(x):
    def B():
        print(x)
    return B

A(7)()
```
  
7  

</details>

---
  
150. Can you tell me how to handle configuration settings and databases when running automated unit tests?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, when we are running automated unit tests, you will need to consider how your configuration settings and databases are set up. You will need to make sure that your tests are able to run without affecting the live data in your databases. One way to do this is to create a separate testing database that your tests can run against. This way, your tests can be run without affecting the data in your production database.

</details>

---

151. Paul is working on some content work. By mistake, he added some unnecessary files to the folder. He wants to remove or delete files from the folder. How will you help him to remove or delete files or folders in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we have three or more commands to remove or delete files or folders from the directory.
  
 - `os.remove() - removes a file
 - `os.rmdir()` - it will remove an empty directory
 - `shutill.rmtree()` - deletes a directory and all its contents.

</details>

---
  
152. Corner is trying to convert an integer to a Unicode character in python, but he can’t do that. How will you help him with that conversion?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, `chr()` returns the string `str` representing a character whose Unicode code point is the specified integer `int`.
  
```python
print(chr(65))
# A
print(type(chr(65)))
# <class 'str'>
```

</details>

---
  
153. Brian asks, what happens in Python when a global variable and a local variable share the same name? How will you explain this to him?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python, when a local variable is given the same name as a global variable, the global variable is shadowed in the scope of the local variable and cannot be accessed. 

</details>
  
---
  
154. Can you tell me if it is possible to call the parent class without its instance creation in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, it is possible in python.
- If the base class is instantiated by other child classes or if the base class is a static method.

</details>

---
  
155. Consider if you have already installed a module with pip but it doesn’t import in your IDLE, what could it possibly be?  
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Well, for one, it could be that I installed two versions of Python on my system- possibly, both 32-bit and 64-bit.
- The Path variable in my system’s environment variables is probably set to both, but one of them prior to the other- say, the 32-bit.
- This made the command prompt use the 32-bit version of pip to install the module I chose.
- When I run the IDLE, I run the 64-bit version.

</details>

---  

156. Jack asks his friend how will you set the environment variables in python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python `os.environ`, consider a python dictionary, so all the common dictionary operations can be performed. In addition to the get and set operations mentioned in the other answers, we can also simply check if a key exists. The keys and values should be stored as strings.

Python 3

For python 3, dictionaries use the in keyword instead of has_key

```python
import os
'HOME' in os.environ  # Check an existing env. variable
```
  
True
...

</details>

---
  
157. Can you explain the differences between a package and a module in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the module is a single file. A module can `import` other modules as objects. A package is a folder/directory where different sub-packages and modules reside.

- A python module is created by saving a file with the extension of .py. This file will have classes and functions that are reusable in the code as well as across modules.

- A python package can be created using the below steps,

   - Create a directory and give a valid name that represents its operation.
   - Place modules of one kind in this directory.
   - Create a `__init__.py` file in this directory. This python knows the directory we created is a package. The content of this package can be imported across different modules in other packages to reuse the functionality.

</details>

---
  
158. Ken is asking his senior if I can dynamically load a module in Python. What will be the answer that he gives him? 
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

Dynamic loading is where we do not load a module until we need it. This is slow but lets us utilize the memory more efficiently. In Python, you can use the importlib module.
 
```python
import importlib
module = importlib.import_module('my_package.my_module')
```

</details>

---
  
159. How would you make a Python script executable on Unix?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to make a python script executable on Unix, it will meet two conditions.
   - The script file’s mode must be executable
   - The first line must begin with a hash(#). An example of this will be: #!/usr/local/bin/python

</details>

---
  
160. What is wrong with my Python code? The PWD should be more than 6 and less than 12 letters. It is working fine, but the real problem starts if we enter exactly 4 letters. We aren't getting the required output.
  
```python
pwd=raw_input("Register Your Passowrd Now:- ") 
pwd = pwd.strip() 
num1=len(pwd) 
print("Number of Characters Entered=", num1) 
num2=num3=num4=0 
if(num1>=6 and num1<=12): 
 num1 = 0  
 for z in pwd: 
 if z.isupper(): 
 num1=1 
 if z.islower(): 
 num2=1 
 if z.isdigit(): 
 num3=1 
 if z in ['#','$','@'] : 
 num4=1 
 if num1 + num2 + num3 + num4 == 4: 
 print("Your PWD is:", pwd) 
 print("PWD Registered Successfully. Thank You!") 
 else: 
 print("Not the Proper Password. Please Register Again:") 
 ```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Minimum no of characters in the password is 6 and the maximum no of characters is 12.
- It should have at least one uppercase, lowercase, and special character.
Find the below code. This will meet the above requirements. It is working fine for 4 characters.
  
```python
import re  
password = input('Enter your password: ') 
    digit_regex = re.compile(r'[0-9]') 
    lower_regex = re.compile(r'[a-z]') 
    upper_regex = re.compile(r'[A-Z]') 
    special_regex = re.compile(r'[#, $, @]') 
 
    if len(password) >= 6 and len(password) <= 12 and digit_regex.search(password) and lower_regex.search(password) and upper_regex.search(password) and special_regex.search(password): 
        print('Password Registered Successfully. Thank You.') 
 
    else: 
        print('Not the proper password. Please register again.')                                                
```  
                                                
</details>

---
  
161. The Junior developer is trying to get an output of the following piece of code but after running this code, what will be the output of the code?
  
```python
x = "code practice"
i = "e"
while i in x:
    print(i, end=" ")
```
  
As a senior developer, how will you help him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If we run the above code, we will get an infinite number of e.
- If you want to exit from the infinite loop, Press ctrl+c you will exit from the loop and you will get the `KeyboardInterrupt` error.

</details>

---
  
162. Charles needs to calculate exponential power calculation using the operator, but he doesn't know which operator can be used and he is asking for help from his friend. How will you help him to find the operators?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If we want to perform power calculations in python, we can use the `**`.
- This operator is known as the exponent operator.

```python
a=4
b=3
print(a**b)
```

</details>

---
  
163.Consider I am in this `/home/user/work/project`. What is the correct way to fix this ImportError error? Now if I type this `python ./programs/my_python_program.py` I will get an import error as `ImportError`. How will you help me to fix this `Importerror`?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

Python does not add the current directory to `sys.path`, but rather the directory that the script is in. Add the /home/user/work/project to either `sys.path` or `$PYTHONPATH.`

</details>

---
  
164. Can you tell me about Zoneinfo in python and what it does?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, Zoneinfo is a python module. Zoneinfo provides a time zone. By default, it uses thesystem’s time zone data but if not available, it will use data in PyPI.

from zoneinfo import ZoneInfo
from datetime import datetime, timedelta
  
```python
dt = datetime(2020, 1, 31, 12, tzinfo=ZoneInfo("India/Los_Angeles"))
print(dt) 
```

</details>

---
  
166. Joe is asking what mapping means and what kind of data type is based on mapping in python. What will be your answer to this question?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, mapping refers to an object that maps keys to be associated with the values. 
- The Python `dictionary` is the only type of mapping in the base typeset. 
- In python, Mappings do not maintain any left-to-right position order, it will support access to stored data by key, as well as type-specific method calls.

</details>

---
  
167. Jhon is having python program named "first.py" and Brian is having the same file but a different name as "first.pyc". Their manager asks about the differences between the files in python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The difference between the `.py` files is python files that have the source code but `.pyc` has the bytecode of your program.

</details>

---
  
168. Can you tell me how will you get environment variables in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- `getenv()` method is used to get the value of the environment variable key if it exists. Else the default value will be returned. 
  
```python
import os
print(os.environ['HOME'])
```
  
- We can see a list of all environment variables:

`print(os.environ)`

</details>

---
  
169.State logical operators available in python language with an example.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We have some different types of logical operators. They are,

     - `==`	Equal to
     - `!=`	Not equal to
     - `<`	Less than
     - `>`	Greater than
     - `<=`	Less than or equal to
     - `>=`	Greater than or equal to
These operators are used to compare the two values.

</details>

---
  
170. Can you categorize the different types of errors that arise during programming? Interpret the following python code.

```python
import os
cwd=os.getcwd()
print cwd
```
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If I run the above program, I get the syntax error in line 3.
- Because in line 3, missing parentheses in call to 'print'.

```python
import os
cwd=os.getcwd()
print(cwd)
```

</details>

---
  
171. Can you tell me if all the developers use a Python debugger?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

Multiple junior-level programmers manage to care debugging, so having a debugging process is important for all developers. Whether you are a savvy developer or just starting, understanding how to discover and fix bugs is important.

</details>

---
  
172. Can you list out the skills you need for efficient debugging in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- For efficient debugging, we can have the following skills,
   - Problem-solving skills
   - python skills
   - Unit testing skills
   - Time management

</details>

---
  
173. Can you tell me the difference between a logical error and compile error?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

**Logical Error:**
   - Logical errors are not detected by the computer.
   - Logical errors cause your results to be wrong.
**Compile Error/Syntax Error:**
   - Syntax errors are "grammatical errors" and this will be detected when you compile the program.
   - Syntax errors prevent your program from executing.

</details>

---
  
174. Paul is asking his junior if he can tell what the background debug mode is. What will be the answer that he gives to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, background debug mode is an interface that enables developers to debug the embedded systems. This mode facilitates debugging in microcontrollers.

</details>

---
  
175. Can you explain the main steps involved in debugging Python code in Visual Studio Code?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- First, begin with the Debug > Start Debugging command to launch the startup file
- Right-click a particular code line and choose Breakpoint > Insert Breakpoint
- Then run code blocks or stop at certain points 
- Finally, Inspect and modify the values of the variables

</details>

---
  
176. Consider Jane has this following piece of code.
  
```python
class samp:
    def add(a,b):
        return a+b
ob=samp()
print(ob.add())
```
  
The above code results in an error, what can be done to resolve this error?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In the above code, values are not passed the parameter values. It will throw an TypeError: add() missing 1 required positional argument: 'b'.
  
```python
class samp:
    def __init__(self,a,b):
        self.a=a
        self.b=b

    def add(self,a,b):
        return a+b

ob=samp(5,3)
print(ob.add(5,3))
```

</details>

---
  
177. The Junior developer is having a doubt and he is asking if a class has one class variable, then how many copies will be created for that variable to the senior? How will you help him to get an answer?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>

Only one copy of static variables is created when a class is loaded. Each object instantiated has its own copy of instance variables. Only one copy of static variables is created when a class is loaded. Each object instantiated has its own copy of instance variables.

</details>

---
   
178.Consider you have the following piece of code,
   
```python
print(0.2+0.4==0.6)
```
After running this code what will be the output and explain how you got that?
   
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>

- After running the above code, we will get the output as `False`.
- The round-off errors from 0.2 and 0.4 add and therefore there is a difference between (0.2 + 0.4) and 0.6. This is because you can't compare floating point values, and it cannot be considered exact.

</details>

---
  
179.Can you tell me what type of inheritance is illustrated in the following Python code? 
  
```python
class A():
    pass 
class B(A): 
    pass 
class C(B): 
    pass
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In multi-level inheritance, a subclass derives from another class which itself is derived from another class. In multi-level inheritance, a subclass derives from another class which itself is derived from another class.

</details>

---
  
180. Jane has this piece code and he wants to find the output of the following code. How will you help him to find the output of the code?
  
```python
a = 3 
b = 1 
print(a, b) 
a, b = b, a 
print(a, b)
```
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

The given python snippet is, a = 3, b = 1, print(a, b) a, b = b, a print(a, b). Here "a" and "b" values are assigned. a=3 b=1. The print function prints 3 and 1. a, b = b, a. It is evaluated by pushing both the values to the stack and the top two values will be rotated (so that the values will be swapped) and the values are assigned back to "a" and "b". So, it swapped values become, a=1 b=3. The print function prints 1 and 3. Hence, the correct answer is 3 1 1 3.

</details>

---
  
181. Considering you are the lead of junior sources. Ask your juniors what the output of the following command in python will be.

```python
print (r"\nhello")
```

What will they answer to this question?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In python language, when 'r' or 'R' is used before the string, it converts the string into a raw string and the escape sequence like \n is not converted. Therefore, the answer is \nhello.

</details>

---
  
182. Your manager is giving the following piece of code.
  
```python
str1="Hello Friends"
c=0
for x in str1:
   if(x!="l"):
       c=c
   else:
       pass
print(c) 
```
  
He is asking what the output of the code is and if is it correct. If it's not, suggest the correct code and output.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>

- If I run the above code, the output is 0.
- The output of the code should be some numbers because inside the loop it's checking whether the values are equal to l. If not, it should count the number of characters that is not equal to l.
- So, increase the count to 1. The correct code is mentioned below
  
```python
str1="Hello Friends"
c=0
for x in str1:
   if(x!="l"):
       c=c+1
   else:
       pass
print(c) 
```
  
- Finally, the output will be 11 because characters are not equal to l.

</details>

---
  
183.Can you clarify/tell me what is Python path?
   
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>

The **PYTHONPATH** environment variable is used by Python to define a list of directories that modules can import from Windows. For most installations, you should not set these variables since they are not needed for Python to run. Python understands where to see its standard library.
  
</details>

--- 
  
184. Considering you as the manager of your team, you need to show enum implementation in python to some other team associates. How will you train this to your team members and can you explain me?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, an enumeration is a set of symbolic names bound to an individual, with unchanging values. Within an enumeration, the values can be compared by identity, and the enumeration itself can be iterated over. In Python 3.4, you can create Enum the base class.
  
```python
from enum import Enum
```
  
- Enum creation in python
  
```python
from enum import Enum
class directions(Enum):
    East, West,North,South = range(4)
print(directions.North.value)
```

</details>

---

185. Consider you are accessing the value both inside and outside of the function, which is fine, but what happens if you try to modify the `global` scope variable value inside a function?   
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The below example is accessing the value both inside and outside of the functions
  
```python
x="my first global variable"
def myfunc():
    print("accessing inside a function :",x)
myfunc()
print("Accessing outside a function :",x)
```
 
- If I am trying to modify the global scope variable value inside a function, the below code is an example of this.
  
```python
x=5
def myfunc():
    x=x*2 #Modifying global variable value inside a function
    print("accessing inside a function :",x)
myfunc()
print("Accessing outside a function :",x)
```
  
- After running this code, this throws an error as `UnboundLocalError`: local variable 'x' referenced before assignment. Because, while modifying the values, Python treats x as a local variable, but x is also not defined inside the function `(myfunc())`.

</details>

---
   
 
186. Does Charles want to know what will happen if a local variable exists with the exact name as the global variable you want to access, how will you help him to know about it?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

If the local variable exists with the exact name as the global variable that you want to access, then the global variable is shadowed as variable that is, preference is given to the local variable.

</details>

---

187. Considering you are attending the python developer interview, the interviewer is asking what do you mean by identifier and what is the permitted length of the identifier. What will be the explanation you would provide for this query?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- A Python identifier is a term used to determine a variable, function, class, module, or object. Identifiers can be a mix of letters in lowercase (a to z) or uppercase (A to Z) or digits (0 to 9) or an underscore _. 
- In python, the length of the identifier can be of any size. The most extended identifier will be from PEP – 8 and PEP – 20.

</details>

---
  
  
188. Joe and William are presenting a python project to their team in between the project presentation. They got some errors for the following piece of code.
  
```python
x=9
y=5
if x>y:
print(x)
else:
print(y)
```

One of the coworkers is asking what this error is and how will you resolve the error and whether it is mandatory in python or not.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- After running the above code, we get the `IndentationError`: expected an indented block, because indentation is missing at line 4 and line 6.
- Yes, in python, indentation is mandatory. If not done properly, the code is not executed properly and might throw errors. Indentation is usually done using four space characters.
- Correct code is mentioned here,
  
```python
x=9
y=5
if x>y:
    print(x)
else:
    print(y)
```

</details>

---
  
189. Do runtime errors exist in Python? Explain with an example.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes, runtime errors exist in Python. 
- Example, 
    - if you are duck typing and things look like a duck, then it is assumed a duck even if that is just a flag or stamp. The code, in this case, would be a run-time error. 
- For example, Print "Hello world" would result in the runtime error of the missing parenthesis that is needed by print ( ).

</details>

---
  
190. Justin Ward wants to create variables using global scope in Python. Can you list out all the steps to create variables With Examples?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- You can create a variable with global scope by initializing outside all the functions in a python program. And you can access the variable from anywhere. 
- Steps 
   - Define the global variable
   - Declaring a function
   - Accessing the global variable 
   - Finally, call the function
  
**Example:**
  
```python
x = "Powerful"
def func():
    print("Python is " + x)
func()
```

</details>

---
  
191. Can we use a break and continue together in Python? How?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can use both break and continue together. The break will stop the current loop from execution, while the jump will take it to another loop.
- The break will stop the current loop from execution, while the jump will take it to another loop.
  
```python
n=["a","b","c","d"]
for n in n:
    if len(n)!=4:
        continue
    print("continue statement")
    if n=="c":
        break
print("Break statement")
```

</details>

---
  
192. Consider you want to extract all the behaviours from one class to another class. Which concept will be useful for this and explain with an example? 
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- For that, we can use the inheritance concepts.
- A class can inherit attributes and behaviour methods from another class, called the superclass. A class that inherits from a superclass is called a subclass, also called heir class or child class. Inheritance allows us to define a class that takes all the functionality from the parent class and allows us to add more.
  
```python
class Animals(object):
  def makeSound(self):
      raise NotImplementedError()
class Dog(Animals):
  def makeSound(self):
      print ("woff!")
class Cat(Animals):
  def makeSound(self):
      print ("meow")
```

</details>

---
  
193. John is creating a class named Don, which has __init__() method that has one parameter as "name". He forgets how to create a "getName()" method that returns the name when the method is called and a "setName()" method which sets the value for the 'name' parameter. Given below is an incomplete piece of code. Help john to make his code work. Provide your logic in the given spaces.
  
```python
class Don:
    def __init__(self, name=None):
        self.name = name
        
    # write your logic here

obj = Don()
obj.setName("pup")
print(obj.getName())
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

```python
class Don:
    def __init__(self, name=None):
        self.name = name
        
    def getName(self):
        return self.name
    
    def setName(self, name):
        self.name =name

obj = Don()
obj.setName("pup")
print(obj.getName())
```

</details>

---
  
194. Jack is trying the polymorphism concept in his code for the first time, he remembered something about method overriding and is able to create one method, in Parent class Animal, named "leg()" and has given the implementation of leg() method. He also created one more class named Human which inherited the Base class Animal. But he forgets what to write in the Human class to complete the concept of method overriding and how to create an object of that class. Help Jack in solving his problem, and you have to create a leg() method in the Human class which prints "Humans have legs" and create an object for the Human class to call leg() method. Given below has some code written and write your logic in the spaces provided.
  
```python
class Animal:
    
    def leg(self):
        print("Not all Animals have legs")
        
class Human(Animal):
___________________
  
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer </b></summary>
<blockquote>

```python
class Animal:
    
    def leg(self):
        print("Not all Animals have legs")
        
class Human(Animal):
    
    def leg(self):
        print("Humans have legs")
        
obj1 = Human()
obj1.leg()
```

</details>

---
  
195. Create a class that shows the concept of method overloading in python.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Default implementation of method overloading is not possible in python, but we can implement and show overloading by passing default arguments to methods. Let's see how to do it.
  
```python
class Overloading:
    
    def add(self, x, y, z = 0):
        return x + y + z

obj = Overloading()
print(obj.add(10, 20))        # output: 30
print(obj.add(10, 20, 30))    # output: 60
```
  
Here, we have passed a different number of arguments at the time of calling, and we are getting different outputs as well for that.

</details>

---
  
196. Suppose there are three classes, Animal, Dog, and Cat. Class Dog inherits properties from the Animal class and class Cat also inherits properties from the Animal class, then which type of inheritance can be depicted from the above scenario?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

In the above scenario, class Animal is a parent class of both Dog and Cat classes. Also, Dog and Cat both classes inherit from the same base class which is the Animal class. So, Dog and Cat are derived classes of the same base class, which is the definition of Hierarchical inheritance.

</details>

---
  
197. Does python support method overloading and method override?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python doesn't support method overloading but it supports method overriding. That is, we can define the same function in the child and parent class with the same signature and the child's function overrides the parent class function. But when we define multiple functions with the same name with different signatures and try to call both with a different number of arguments passing, it executes the latter one but gives an error for trying to call the other functions as in namespace there will always be a single entry against each function name. let's see this with an example.
  
**Example**:
  
```python
def add(a,b):
    return a+b 

def add(a,b,c):
    return a+b+c

print(add(2,4))
print(add(2,4,6))
```
  
 - After writing and calling the above two methods together, we are getting "TypeError: add() missing 1 required positional argument: 'c'". But if we commented the first calling function i.e add() with two arguments and call only the last function, it will execute and gives the output as 12.
  
```python
def add(a,b):
    return a+b 

def add(a,b,c):
    return a+b+c
# print(add(2,4))
print(add(2,4,6))   # output: 12 
```

</details>

---
  
198. Suppose there are three classes, Father, Mother and Child. The Child class inherits properties from two classes, Father and Mother class, then which type of inheritance can be depicted from the above scenario?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

By the definition, Multiple inheritances state that one derived class can inherit properties from more than 1 base class. In the above scenario also, we can see that the Child class is a derived class which inherits all the properties from the 2 base classes, that is Father and Mother classes.

</details>

---
  
199. William asks "Polymorphism provides a default implementation of function overloading in python" to his junior. Is it true or false and give an explanation.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

- False
- Suppose, if we define two functions with the same name and different argument lists in python, and when we try to call the first function, it will give an error in the program. But, when we try to call the second function, it doesn't give the error and overrides the prior function and generates the output.

</details>

---

200. Franz has a piece of code
  
```python
class Vehicle:
    def wheel(self):
        print("It can have 2 or more wheels")
        
class Car(Vehicle):
    def wheel(self):
        print("It has 4 wheels")

obj = Car()
obj
````
  
He is trying to run that, but he got some error can you help him to resolve the error and give the output of the code?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Correct code is mentioned below,
  
```python
class Vehicle:
    def wheel(self):
        print("It can have 2 or more wheels")
        
class Car(Vehicle):
    def wheel(self):
        print("It has 4 wheels")

obj = Car()
obj.wheel()
```

- Output for the above code is, `It can have 2 or more wheels`.
- Car class overrides the wheel() method of Vehicle class and therefore when calling the wheel() method of Car using the object of Car class, it prints the statement present inside it.
  
</details>

---
  
201. John is asking his friend if the len() function can be used in polymorphism in python. What would be the answer that he gives?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, len() is used to find the length of different datatypes like string, list, tuple, etc. The below code will show how we can use len() function with different types of data.
  
```python
print(len("William"))           #Output: 6
print(len([1, 2, 3, 4]))       #Output: 4
print(len((1.5, 2.8, 3.3)))    #Output: 3 
```
  
- Different types of values are present in different print statements. First, it is a string, then it is a list, and at last, it is a tuple. The len() function returns the length of these values.

</details>

---
  
202. Ken asks his friend to run the following code. Tell me the output of the code and explain how he got that.
  
```python
x = 40
class Test:
    x =20 
    def show(self):
        print(x)
    
obj = Test()
print(x)
obj.show()
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If I run the above code, I get output as 40
                                          40
-Before method calling, the first print statement prints the value of the global variable i.e 40. And when the show() method is called, the print statement present inside will also print the value of x as 40, not 20, because x= 20 is a class variable which must be accessed by using the class name before the variable name. Therefore, it will also take the global variable value i.e 40 in this case.

</details>

---
  
203. How do you differentiate between Interpreter and Compiler?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The compiler translates our program in a single run, whereas the Interpreter translates our program line by line.
- In terms of CPU utilization, the Compiler utilizes more CPU than the Interpreter.
- During compilation, all the errors in the program are displayed in the end together, whereas in the Interpreter, errors of the code are displayed line by line.
- As the code size increases, the compiler takes more time to scan a code compared to Interpreters.
- Example: C, C++, java, etc are based on Compilers whereas Python, Ruby, MATLAB, etc. are interpreted languages.

</details>

---
  
204. Franz is asking his senior developer/lead if he/she can help him to find out whether these identifiers are valid or not. How would he help him? 
[Last_Name, student@id, 4_id, var, for].  
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Last_Name and var are the only valid identifiers from the above list.
- student@id is not a valid identifier because it has a special character "@" in it.
- 4_id is not a valid identifier because the identifier should not start with a digit.
- for is invalid because it is a reserved word in python.

</details>

---
  
205. Consider your manager giving the following piece of code.
  
```python
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    # write your logic here
```
  
He asks you to write your own logic inside the for loop to print the values 4, 2, 7, 8, and 9 on the output screen. How will you do this?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The correct code is,
  
```python
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    if i%2==0 or i>3:
     print(i)
```
  
- i%2==0 is the condition for printing even numbers and i> 3 will take the value of i which is greater than 3 and there is a logical or operator between both the if conditions. Therefore, when either of the conditions becomes true only then the print statement inside if will executes. Hence, we get the result as 4, 2, 7, 8, and 9.

</details>

---
  
 
  
  
  
  
  
