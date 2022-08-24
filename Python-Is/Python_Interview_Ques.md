
## Python Interview Questions

1.How can you say that python is a dynamically typed programming language.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Python is a dynamically-typed programming language.It means that the type of the variable can be changed dynamically by the program at the run time, without re-declaration of the variable.
- In Python,We first define a variable a to hold an integer literal and later in the below program, without re-declaring it, we make it hold a string literal or 
  
```python
a = 43 # Integer literal 
print(f"{a} => {type(a)}") 
 
a = "Welcome to My Home" # String literal 
print(f"{a} => {type(a)}") 
```
  
  </details>
  
--- 
  
2.Consider John have a list1 =[1,2,3,4,5].He want to get an output as list1=[5,4,3,2,1],How will you help him get that output?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

He want to get list1=[1,2,3,4,5] as [5,4,3,2,1], he can use `slicing` or `reverse` method to get that output.

```python
list1 =[1,2,3,4,5]
print("before reversing list",list1)
print("after reversing",list1[::-1])
```   
  
  </details>  
  
---
  
3.Jack want to enter these multiple line values  5 2 3 4 1 
into a single line and he is trying to order the list as [1,2,3,4,5] , which method is help him to get the values in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If he wants to enter mutiple line values into a single line we can use 'list' and separated by commas.
- If he want to order the list means use `sort()` method in python.
  
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
  
4.Consider you have a list which holds values of multiple datatypes how do you extract only the numbers from that list.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In list in Python can contain different types of data,  item in the list is separated by a comma and the entire list is enclosed in square brackets [].
- If we want to Extract only the numbers from list we can use `isinstance()` method through the loop `isinstance(int,float)` checking list contains numbers or not if in the list it contains int and float it will store into the another list and we will print the list.

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
  
5.If a function doesn’t have a return statement at the end of the function, is it valid in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If there is no return statement appears in a function definition, control automatically returns to the calling function after the last statement of the called function is executed.
- It will returns `None` if the function doesn't have a return statement.

</details>
  
---
  
6.Consider we have list is A= [1,4,6,7,9,66,4,94], you want to get output for A[3]. How will you help to get the output of the above list.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We have this list A= [1,4,6,7,9,66,4,94] and want to get the output for A[3]. For that we can use indexing.
- In python using indexing we can get particular value.
- To get the output of particular index use the below code,
 
```python
A= [1,4,6,7,9,66,4,94]
print("using index A[3] value is:" ,A[3])
```
  
**Output:**

using index A[3] value is: 7
  
  </details>
 
---
  
7.Can you tell me the reason why this Datatype `set` is called **the frozen set** in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
Frozen set is an immutable version of a Python set object in python.While elements of a set can be modified at any time.But the forzen set remain the same after the creation.

Syntax of `frozenset()` function is:
 
```python
frozenset([iterable])
```
  
</details>
  
---
  
8.Consider that I have a text that is "The Apple a Day Keeps the Doctor Away." We want to replace one string with another for the one/first two occurrences of "An Apple a Day Keeps the Doctor Away." Which method is used to do this?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to replace one string with an another string use `.replace()` method.
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
  
Before replacing the string is : The Apple a Day Keeps the Doctor Away.
After replacing the string is : An Apple a Day Keeps the Doctor Away.
  
</details>
  
---

9.Which delimiter is used to combine multiple lines of text into a single line in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>  
  
- we can use the triple quotes to print the multiple lines into a singe line in a python.
- Triple quotes ''" or '" are string delimiters that can span multiple lines in Python. Triple quotes are used when combine multiple lines, or enclosing a string that has a mix of single and double quotes.

</details>
  
---
   
10.Consider the string "Python Online Training" as an example. How do I get output that as ['Python', 'Online', 'Training']. Which process produces that result?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can use the `split()` method.
- In python you can specify the separator, default separator is any whitespace.
  
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
  
11.Shan want to iterate the for loop for a fixed number of times in Python,Which method is used to iterate the loop?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python `range()` function is used to create a series of sequential numbers and to iterate through a loop for a fixed number of times. This loop will be executed until the specified number in the `range()` function.
 
**Example:**
  
```python
C = ['Bat', 'Cat', 'Tat', 'Fat']
for i in range(len(C)):
     print("C values:", C[i])
```
 
</details>
  
---

12.Which variables are created globally in a class? Tell me the scope of the variables?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python global variables are created outside of a function.
- Global variables are can be used by everyone, both inside and outside of function.

```python
x = "global"
def func():
    print("x inside:", x)
func()
print("x outside:", x)
```
  
</details>
  
  ---
  
13.Which one is used to provide a unique name for every object in python? What are the different types available in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python namespace use to defined as a system that is designed to provide a unique name for every object in python. Types of namespaces that are present in Python are:
   - Local namespace
   - Global namespace
   - Built-in namespace
  
  </details>
  
 ---
  
14.Can you teach to James, how will you run the interactive Python interpreter?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- In python open a command-prompt and then type in python , or python3 it's depending upon your Python installation, and then Enter .
- After enter that we will get this >>>>,
so now you can write and run Python code , with the only the drawback is that when you close the session, your code will be gone.
  
  </details>
  
 ---
  
15.James want to know list out all the function in a module. Which method is help him to get all the function in a module?	
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
If you want to get all the function in a module in python use `dir()` method.
  
**Example:**

```python
import some_module
print dir(some_module)
```

  </details>
  
---
  
16.Junior developer want to repeat the particular part of the task for a finite number of times in python,How his senior is going to help him to repeat the code ?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to repeat the particular part of the task for a finite number of times in python use Enumerate loops.
- you can provide the number of iterations to be performed: As an integer value.
  
  </details>
  
  ---
 
  
17.One of the junior developer was working on strings, he don't know how to remove whitespaces from a string in python.How is senior developer helped him to remove whitespaces?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- In python to remove whitespaces from a string we can use `strip()` function.

```python
s.strip()
```
  
- If you want to remove only right or left spaces, use `lstrip()` or `rstrip()` functions.

- We can use `replace()` also to remove all the whitespaces from the string. This function will remove whitespaces between words.
  
  </details>
  
  ---

18.Ron asked Ken to show the reversed order of the contents of a file in python,How he will do that?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Get the file name from the user.
- Read each line from the file using for loop and store it in a list.
- Print the elements of list in reverse order.
- Print the lines finally.

Here is the Python Program to read the contents of the file in reverse order. The program output is also shown below.

```python
filename=input("Enter file name: ")
for line in reversed(list(open(filename))):
    print(line.rstrip())
```
  
  </details>
  
---
  
19.Junior developer is trying to run the following piece of code but after running this code it’s throwing a Syntax error,
  
```python
x = "CorporateWorld"
print (“Reverse is”, [x : -1] )
```
  
As a senior developer how do you resolve that, Error.
  
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
  
20.Is the `Xrange()` method occupies only the least memory? What would be the reason?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- Yes,the `xrange()` method occupies only the less memeory comparing than the `range()`.
- Because it only stores one number at a time in the memory.
  
  </details>
  
---
  
21.Can you tell something about generators in python and explain where we can use the generators?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In Python a generator is a special type of function which does not return a single value, instead it returns an iterator object with a sequence of values.In a generator function, a yield statement is used rather than a return statement.
- The difference is that while a return statement terminates a function entirely, yield statement pauses the function saving all its states and later continues from there on successive calls.
  
</details>
  
  ---
  
22.Consider your senior is asking how will you handle errors ,How will you describe the correct usage of error handling in Python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python `Try` and `except` statements are used to `catch` and handle exceptions. Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause.
  
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
  
23.Junior was having some issues in their code, How will help him to detect Python bugs and statistical issues?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- We can detect bugs in a python source code using a static analysis tool named `PyChecker`.
- Another tool called `PyLint` that checks whether the Python modules meet their coding standards or not.
  
  </details>
  
  ---
  
24.Which module in Python supports regular expressions?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python `re` module  is supports regular expressions.

```python  
import re
```
  
- Regular Expressions (RegEx) is a special sequence of characters that uses a search pattern to find a string or set of strings.
  
  </details>
  
---
  
25.How will you explain the function `re.match` do to junior developer?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- `re.match()` function of re in Python will search the regular expression pattern and return the first occurrence.
  
  </details>
  
  ---
  
26.Can we use the `+` operator to add elements to a set? If not, then how to add elements into a set?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- No,We can't use the `+` operator to add elements.
- We can use `set.add()` function to add elements.
  
```python
languages = {'Python', 'C++', 'Java', 'C'}
languages.add('.Net')
languages.add('ML')
print(languages)
```
  
  </details>
  
 ---

27.John wants to check in a string that all characters are in uppercase or not Joe helped him to check the all the characters are in uppercase or not, which method she said to him?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python `String.isupper()` method used to check if all letters are in Uppercase.
- The `isupper()` method/function returns True if all the characters are in upper case, otherwise False. 

```python
a = "Hello World!"
b = "MY NAME IS KEN"
print(a.isupper())
print(b.isupper())
```
  
  </details>
  
  ---
 
28.Can you list some differences between single `/` and double `//` in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- `/` returns float value,It is Float Division        
- `//` floor division rounds the result down to the nearest whole number.It is Integer Division

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
  
29.Amie has the following code and is trying to get the output, but she keeps receiving NameError warnings. 
 
```python
list = [John, 70.2, 'abcd', 786, 2.23] 
print(list[7:3])
```
  
Joe was asked to assist their leader. How is she going to fix this issue?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- We are getting NameError because strings should be enclosed with an single or double quotes.
- We will get output as empty list [] because we don't have index value is 7.
- Correct code is given below
  
```python
list = ['John', 70.2, 'abcd', 786, 2.23] 
print(list[7:3])
```
  
  </details>
  
  ---

30.Henry wants to learn slicing but he don't know Which data types of support slicing,How you help him to learn the different data types supported for slicing?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
Python supports slice for any sequential data type like lists, strings, tuples, bytes, bytearrays, and ranges.
  
```python
a = ("a", "b", "c", "d", "e", "f", "g", "h")
x = slice(3, 5)
print(a[x])
```

  </details>
  
  ---
  
31.John wants to print a single string 10 times using only one print statement. How can he do that?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If we wants to print a single string 10 times using only one print statement,we can use `*` operator.
 
```python
x="Hi"
print(X*10)
```
  
  </details>
  
  ---
  
32.Consider Jack have this list [1,2,3,4,5,]. He wants to convert list into set as (1,2,3,4,5) and john wants to know does it maintains same order or not?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- If your converting a list to set the order of elements is changed.
 
```python
x=[1,2,20,6,210]
print(x,type(x))
# [1, 2, 20, 6, 210] # the order is same as initial order
x1=set(x)
print(x1,type(x1))
# set([1, 2, 20, 210, 6]) # in the set(x) output order is sorted
```
  
  </details>
  
 ---
 
33.How do you find the type and identification number of an object in Python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Using `type()` for returning datatype.
- Using `id()` for returning identification number.

  </details>
  
  ---
  
34.State some differences between Python 2.x and Python 3.x?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
The key difference between Python 2.x and Python 3.x is the behaviour of the print function.
in 2.x print is treatted as a statement whereas in 3.x it is treated as a function print().
  
  </details>
  
  ---
  
35.James have set of names, roll number and date. He wants to store these values into a single name. which data type can we use to store all the values into a single name?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- To Store differenct data types into a single value we can use the list.

 ```python
list1=["Jhon",123,06-09-1999,"jack",78,09-12-2000)
print(list1)
```
  
  </details>
  
  ---
  
36.How to check whether the two variables are pointing to the same object in Python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>
  
- To check the two variables are pointing to the same object in Python use `is` keyword.
- The test returns True if the two objects are the same object.

```python
x = ["a","b","c"]
y = ["a","b","c"]
print(x is y)
```
  
  </details>
   
   ---
  
37.How can you initialize a 5*5 NumPy array with only zeroes?
   
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- For that we need to import numpy first
  
```python
import numpy
z=numpy.zeros((5,5),int)
print(z)
```
  
  </details>
  
  ---
 
38.How to create a data frame from a dictionary?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
 <details><summary><b>Show Answer </b></summary>
<blockquote>
  
```python
  import pandas as pd
diction={'Name' : ['Rohit','Brad']
    'Age' : [23, 21],
    'College choices' : ['MIT','Stanford','Caltech']}
df = pd.DataFrame(diction)
```
  
- Using the above code we can create data frame in python.
  
  </details>
   
   ---
39.Ken wants to perform static analysis in Python. How will you help him to find the tools to perform static analysis?
   
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary><b>Show Answer </b></summary>
<blockquote>
 
- For Static Analysis
   -pylint - performs style checking against PEP-8 but also shows errors & potential issues.
   - PyFlakes - Error detection.
   - Bandit - Security Checks.
   - MyPy - Check for errors against optional static type annotations.

  </details>
  
  ---

40.James is working with identifiers in python. His coworker is asking, is python case sensitive or not when dealing with identifiers. What explanation did James give his coworker?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes
- As you might be knowing that Python is a case-sensitive programming language. So, Python is case sensitive when dealing with Identifiers. 
- Case is always significant.
 
  </details>
  
  ---
  
41.James trying to check the python version in CMD? how will you help him to list out what are the steps needed?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>
  
- In python we have more there are more methods to check the python version in cmd.
    - Using `sys.version` method
    - Using `python_version()` function
    - Using `python -V` command
- Here this is one of the simplest way to check the python current version

  1.Open cmd/terminal
  2.Write python -V and press enter,it will return the current python interpreter version in the form of string.
  
```python
python -V
```

</details>
  
---
  
42.Jacks wants to know how to process the file in python. How will you explain the file processing modes that Python supports.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg) 
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- A file is some information which is stored in the computer storage devices. Python provides basic functions and methods necessary to manipulate files by default. You can do most of the file manipulation using a file object. Python language supports two types of files. 
1.Text dile 
2.Binary file

- Different modes to opening a file
     - `r` - open a file for reading.
     - `w` - open a file for reading.If the file exists new file will be created.
     - `x` - open for exclusive creation,fail if the file is already exists.
     - `a` - open for rading,appending to the end of the file it exists.
     - `b` - binary mode
     - `t` - text mode
     - `+r` - open a file for reading and writing.

</details>

---
 
43.Franz is asking to her junior to remove the duplicate values froma list.How she will be going to get rid of duplicate elements from a list?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To remove duplicate elements/values from a list ,we can use the buitl-in function `set()`.The specify of `set()` method is it will return only the distinct elements.
  
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
  

44.Harry wants to know What is python's parameter psssing mechanism? How will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In Python parameter passing mechanism is a call by value.
- The call by value method is arguments are passed by assignment in Python. The actual parameters to a function call are introduced in the local symbol table of the called function when it is called,arguments are passed using call by value.If you change the value of the parameter within a function, the change is reflected in the calling function .
 
  
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
  
45.Jhon has a string as `hello world` he wants to cut some part of the string. How will you help him to write a piece of code to cut part as `wo` in the string?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- To cut or access some part of the string, We can use slicing method in python.
  
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
  
46.Ernest is searching for **conditional expressions** in python how will you help him to get to know about conditional expressions?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python **conditional expressions** are known as **Ternary operators**.Ternary operators are used to evaluate something based on the condition is true or not.
- Ternary operator allows to test a condtion quickly instead of multiline if satatement.

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
  
47.Can you explain what will be the process of compilation and loading in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python first compiles a source code (.py file) into a byte code. Compiling is a simple translation step, and byte code is a lower-level and platform-independent source code.
- After compilation is usually stored in `.pyc` files.
- The bytecode (.pyc file) is loaded into the Python runtime and interpreted by a Python Virtual Machine, a piece of code that reads each instruction in the bytecode and executes whatever operation is indicated. The byte code compilation is automatic, and the PVM is just part of the Python system that you have installed on your machine.The PVM is always present as part of the Python system and is the component that truly runs your scripts.
- Each time an interpreted program is run, the interpreter must convert source code into machine code and also pull in the runtime libraries. This conversion process makes the program run slower than a comparable program written in a compiled language. 
- Python has something clever to improve the performance. It compiles to bytecode (.pyc files) the first time it executes a file. This substantially improves the execution of the code the next time the module is imported or executed.

</details>

---
  
48.Henry is asking about What does the `yield` keyword do in python to his senior and how he will explain it to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python `yield` keyword can be use like the return statement in a function. When done so, the function instead of returning the output, it returns a generator that can be iterated upon. 
- You can iterate through the generator to extract items. Iterating is done using a for loop or using the `next()` function.

```python
def Squre(n):
  i = 1
  while i < n:
      yield i * i
      i += 1
print(list(Squre(5)))
```
</details>

---
  
49.when you are doing a presentation, one of your coworkers is asking Is all the memory freed when python exists how will you explain this to this coworker?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python Garbage collector to release unreferenced memory with `gc.collect()`. 
- Python will definitely leak memory is when you declare circular references in your object declarations and implement a custom __del__ destructor method in one these classes. 
- Python modules are not always deallocated when Python exits.Python's garbage collector does this. So, Python doesn't detect and free circular memory references before making use of the garbage collector.
- So, Python does not detect and free circular memory references before making use of the garbage collector.

</details>

---
  
50.Can you explain how will you use the `split()` methods of the `re` module in python to one of your coworkers?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python `re` module provides the regular expression matching operations.Both patterns and strings to be searched can Unicode strings as well as 8-bit strings.
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

- To generate random number first import the module called `random` and `randint()` function is used to get the random number.

```python
import random
print(random.randint(1,1000))
```

**Output:**
  
669
  
</details>

---
  
52.Can you explain what are accessor and mutator methods in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The method defined within a class can either be an Accessor or a mutator method in python. The  accessor method is a function that returns a copy of an internal variable or computed value. Some Examples of Accessor method is,
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

- The `isinstance()` method checks whether the object is and instance of a class or not.
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
  
54.Fyodor is trying to get a copy of one object in python. How will you help him to get a copy of an object?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python we can use the deepcopy to copy an object.The `=` use to assign another reference to the same object in memory .
- The deepcopy used to creates a new object in memory with the values of A and B will reference it. 

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
 
55.Can you explain static variables in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python static variables are allocated statically,The scope the variable is entire run of the program.
- Variables are declared inside the class definition but not inside a method are class or static variables.
  
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
     - Doesn't need self parameter
     - Deosen't need self or cls as parameter
     - Need decorator @staticmethod
     - Can only access variables passed as argument.
- `@classmethod`
     - Doesn't need self parameter
     - Need cls as parameter
     - Need decorator @classmethod
     - Can be accessed directly through the class.Don't need instance class.

</details>

---
  
57.John wants to get a list of class attributes in python. How will you help him to get it?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python the **inspect module** provides several useful functions to help get information about live objects such as modules, classes, methods, functions, tracebacks, frame objects, and code objects. 
- The **getmembers(object)** method return all the members of an object in a list of (name, value) pairs sorted by name.

</details>

---
  
58.Does python support interfaces like other languages in java or c?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- No, python doesn't support interfaces.
- Python does not support multiple inheritance.But,you can easily emulate the equivalence of interfaces.

</details>

---
  
59.Can you explain how would you achieve web scraping in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Webscraping is a computer software technique of extracting information from the websites.This technique is mostly focuses of unstructured data on the web into structured data.
- Python has some options for HTML scraping,These are,
     - Mechanize
     - Scrapemark
     - Scrapy
     - BeautifulSoup
  
</details>

---
  
60.Franz wants to protect his python source code for that he is asking for some help from the jack, How will be going to help to do it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Python, is a byte-code-compiled interpreted language, it is very difficult to protect. Even if you use an exe-packager like py2exe, the layout of the executable is well-known, and the Python byte-codes are well understood. 
- To protect the only way is to license it because if you compile your code, let us say machine code if your work is not protected by a license, it can still be commercialized against your will.

</details>

---
  
61.How will you install pip on windows can you list out some steps to do it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- `pip` is a package managements system.It is used to install and manage  software packages in python.If you have python 3.4 pip is included with Python and it should be already be working on your system.
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
  
63.Ken wants to know about exception handling in python how will you teach him to do it in object-oriented programming?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- An exception is a type of notification that interrupts the usual program execution. Exceptions help you to detect and react to unexpected events. The program’s state is saved when an exception arises, and control is passed to an exception handler. The exceptions are thrown or raised by programming code that must send a signal to the executing program about an error or an unusual situation.

**For example**, when you want to open a file that doesn’t exist, the code responsible for opening the file will detect this and throw an exception with a proper error message. Exceptions are of two types in OOPs, such as checked exceptions and unchecked exceptions. 

 - **Checked exception** - The classes which inherit compile-time exceptions are known as checked exceptions.
 - **Unchecked exception** - The classes which inherit Runtime exceptions are known as unchecked exceptions.

</details>

---
  
64.How many except statements can a try-except block have in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python we can have more than zero except statements.
- There has to be at least only one except statement.
  
**Syntax:**
  
```python
try:
   You do your operations here;
except Exception1:
   if the exception1 then excecute this block
except Exception2:
   if the exception2 then excecute this block
else:
   If there is no exception then execute this block.
```

</details>

---
  
65.James asking to his junior want to run this piece of code
  
  ```python
  print([1, 2, 3] + 4, 5, 6)
  ```
  
He is asking to print the output for the code but he got some error in this how will you help him to correct the error and get the output?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If he run the above code he will get an TypeError as can only concatenate list (not "int") to list
  
**Correct code:**
  
 ```python 
 print([1, 2, 3] + [4, 5, 6])
 ```

**Output:**
  
[1, 2, 3, 4, 5, 6]
  
- We can add only the two list not an integer values.
  
</details>

---
  
66.Charles wants to move the python shell to the home directory using `~` in python how will you guide him to move the home directory through the piece of code?
  
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
  
67.Ryan asking to you test on variables against multiple values how will you explain this to him?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- We can use the `in` operator to test on variables against multiple values .
  
```python
x=5
if x in (1,2,3,4,5):
  print("found")
else:
  print("Not found")
```
  
- The above program validate x=1 or x=2 or x=3 or x=4 or x=5.

</details>

---
  
68.How to call an external command in Python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The subprocess module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. The subprocess.call() method run the command described by args. Wait for command to complete, then return the returncode attribute.
  
```python
from subprocess import call
call(["dir"])
```

</details>

---
  
69.Kein is asking about the meaning of a single and double underscore before an object name to his senior coworker and how he will explain it to him. 
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- _fun: weak "internal use" indicator. E.g. from X import * does not import objects whose name starts with a single underscore.
- __fun: the interpreter replaces this name with _classname__fun as a way to ensure that the name will not overlap with a similar name in another class.

</details>

---
  
70.Can you write a piece of code to read a single character from the user?
  
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
  
71.Fyodor asked doubt to his coworker to explain the difference between `raw_input()` and `input()` in python.
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python 2, `raw_input()` takes only the what exactly user enter by themself and passes it back as a string.
- In python 3, `raw_input()` was taken as `input()`.So it will return exact what the user enter and old input() was removed.

</details>

---
  
72.Can you explain Why is Python not fully object-oriented?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

In Python is an object-oriented programming language but not pure. Because, Python doesn't support strong encapsulation , which is only one of many features associated with the term 'object-oriented'.

</details>

---
  
73.Henry was checking Is there any way to kill a thread in python how will you help him to find it and explain it?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, we can able to kill a thread. To kill a thread we have many methods in these are,
    - Create an **Exit_Request** flag.
    - Using the `multiprocessing` module.
    - Using the `trace module.
    - Use the `ctypes` to raise Exceptions in a thread.
- We can use any one of the methods and we can kill the thread.
  
</details>

---

74.Can you explain is it necessary to put a space between operators and operand in python?
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- Yes,it is it necessary to put a space between operators and operand in python.
- If we are use sapce in between both operator and operands it will help readability.
  
```python
x + y
(sum ** 2) + 3 * val - 1
x * (3 + 8)
b + math.sqrt(3 * max_val)
```

</details>

---
  
75.Can you explain to me why I can't use assignment operators in an expression?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- The error is a simple typo: x = 0, which assigns 0 to the variable x, was written while the comparison x == 0 is certainly what was intended.
- The reason for it is not allowing assignment in Python expressions could be a common, hard-to-find bug in those different languages, caused by this construct:

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
  
76.Charles asked what are the rules for local and global variables in Python, how will you explain this to him?  
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python, the variables referenced within a function are global.
- When a variable is assigned  new value anyplace within the body of a function then it's assumed as local.
- In a function, if a variable ever assigned  new value then the variable is implicitly local and explicitly it should be declared as global.

</details>

---
 
77.Tell me how will you create an empty class in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- If you want to write an empty class in python we can use the pass statement. Pass is a special statement in python but it does nothing.
- Pass works as a dummy statement.
- Regardless, objects of an empty class can also be created.

</details>

---
  
78.Can you train your coworker on how will you pass optional or keyword parameters from one function to another function in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

To pass the keywords from one function to another function we can use the keyword arguments.

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
  
79.Can you tell me how will you find methods or attributes of an object in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- In python attributes of a class can even be accessed using the following built-in methods and functions:
   - `getattr()` – This function is used to access the attribute of an object.
   - `hasattr()` – This function is used to check if an attribute exists or not.
   - `setattr()` – This function is used to set an attribute.

</details>

---
  
80.How will you make a higher order function in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer </b></summary>
<blockquote>

- A higher-order function accepts one or more functions as input and returns a new function. Sometimes it is required to use function as data. - To make high order function , we need to import functools module.

</details>

---
  
81.
  
  
  
  
  
  
  
  
