
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

