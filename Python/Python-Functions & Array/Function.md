## Function

1.What is function?

<details>
  <summary>
    <b>Show Answer</b>
  </summary>
  
A function is a block of organized, reusable code that is used to perform a single, related action. Functions provide better modularity for your application and a high degree of code reusing.In python we have three types of functions.
  <ul>
    <li> Built-in print()</li>
    <li>User-defined functions(UDF)</li>
    <li>Anonymous-Lambda()</li>
  </ul>
</details>

2.What is the difference between call by value and call by reference?

<details>
  <summary>
    <b>Show Answer</b>
  </summary>
  
Call by value:<ol>
  <li>A copy of the variable is passed.</li>
  <li>Change in a copy of variable doesn't modifyy the orginal value of variable.</li>
  <li>Syntax: function_name(variable_name1,variable_name2)</li>
  <li>Default calling-primitive type are passed using the call_by_value.</li>
  </ol>
Call by reference:<ol>
  <li>A variable itself is passed.</li>
  <li>Change in a copy of variable modify the original value of variable.</li>
  <li>Syntax: function_name(&variable_name1,&variable2...)</li>
  <li>Default calling-Objects are implicitly passed using call_by_reference.</li>
  </ol>
</details>

3.How many scope of variables are in python?

<details><summary><b>Show Answer</b></summary>
  
There are two basic scope of variable are in python.
<ol><li>Global variables</li>
    <li>Local variables</li>
  </ol>
<ul>
Global variable:
  
  * Global variable are those which are not defined inside any function and have a global scope.
  
Local variable:
  
  * Local variables are those which are defined inside a function and its scope is limited to that function only.
</details>

4.How does a function return values?
  
<details><summary><b>Show Answer</b></summary>
  
A function uses the 'return' keyword to return a value. 
  
**Example**:
  
```Python
def add(a,b):
    return a+b
print(add(2,3))

```  
<details><summary> <b>Output</b> </summary>
  
      5
</details>
</details>

5.What will be the output of the following code?
  
```Python
def my_func()
   x = 10
   print("Value :",x)
x = 20
my_func()
print("Value :",x)
```
<details><summary> <b>Show Answer</b> </summary>
  
**Output**:
  
def my_func()
                 ^
SyntaxError: invalid syntax
  
<details><summary> <b>Explanation</b> </summary>  
  
Here, we are getting syntax error because the syntax is def function_name():
  
</details>
</details>
  
6.Can you tell me some Built-in functions in python?
  
<details><summary> <b>Show Answer</b> </summary>
  
Functions that are built into Python.we have so many built-in functions in python.Here i have mentioned some built-in funtions,
- python abs()-returns absolute value of a number
- python all()-returns true when all elements in iterable is true
- python ascii()-eturns String Containing Printable Representation
- python delattr()-deletes attribute from the object
- python eval()-runs code within program
  
</details>

7.Can we use local variable in the local global scope?
  
<details><summary> <b>Show Answer</b> </summary>
  
No,We cannot use local variables in the global scope.
  
**For example**:
  
  ```Python
def spam():
  calls = 31337
  spam()
print(calls)
  ```
 
if run this program, the output will be:
Traceback (most recent call last):
  File "C:/test1.py", line 4, in <module>
    print(Calls)
  
<details><summary> <b>Explanation</b> </summary> 
  
NameError: name 'calls' is not defined
The error happens because the calls variable exists only in the local scope created when spam()is called.once the program execution returns from spam, that local scope is destroyed, and there is no longer a variable named calls.
  </details>
  </details>
  
8.What is the data type of None?
  
<details><summary> <b>Show Answer</b> </summary>
  
   **None** has a special status in Python. The None is used to define a null variable or an object, and it is a data type of the class NoneType.

**Example**:

```python
x=None
print(type(x))
```
<b>Output:</b> 
  
<class 'NoneType'>
</details>
  
9.When does the code in a function execute: when the function is defined or when the function is called?
  
<details><summary> <b>Show Answer</b> </summary>
  
The code in a function executes when the function is called, not when the function is defined.
  
**Example**:
```python
def greet(name1):  
    print ('Hello ', name1)
greet('Sam')
```
**Output**:
  
Hello  Sam
  </details>

10.How many global scopes are there in a Python program? 
  
<details><summary> <b>Show Answer</b> </summary>
There's only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are forgotten.
  
**Example**:
  
```Python
q = "I love coffee" # global variable
def f():
    p = "Welcome to corporate." # local variable
    print(p)
    f()
print (q)
```
**Output**:
  
   I love coffee
  </details>
  
11.Which return type reuturns a value?
  
<details><summary> <b>Show Answer</b> </summary>
  
You declare a method's return type in its method declaration. Within the body of the method, you use the return statement to return the value. Any method declared void doesn't return a value.
  
</details>
  
12.When a function does not have a return statement What does the function return when called in Python?

<details><summary> <b>Show Answer</b> </summary>
  
 So, if you don't explicitly use a return value in a return statement, or if you totally omit the return statement, then Python will implicitly return a default value for you. That default return value will always be None .
 
  </details>

13.How can you force a variable in a function to refer to the global variable?
  
<details><summary> <b>Show Answer</b> </summary>
  
If you want to refer to a global variable in a function you can use the global keyword to declare wh ich variables are global.In Python, global keyword allows you to modify the variable outside of the current scope. It is used to create a global variable and make changes to the variable in a local context.

 ```Python
x = 5
def change():
	global x
	x = x + 5
	print("Value of x inside a func:", x)
change()
print("Value of x outside a func :", x)
```
**Output**:
  
  Value of x inside a funct : 10
  Value of x outside a funct : 10
  </details>
  
14.Can you tell me some Built-in functions in python? 
  
<details><summary> <b>Show Answer</b> </summary>
  
The functions which are come along with python itself are called a buli-in functions or **predefined function**.Some of the functions,
- range()
- id()
- type()
- input()
- eval() etc...
  
**Example**:

  ```python
for i in range(1, 10):
    print(i, end=' ')
  ```
  
**Output**:

1 2 3 4 5 6 7 8 9 
  
  </details>
  
15.What will be the output of the following code?
  

<details><summary> <b>Show Answer</b> </summary>
  
```python
def outer_function(a, b):
    def inner_function(c, d):
        return c + d
    return inner_function(a, b)
    return a
Output = outer_function(45, 10)
print(Output)
  ```

  **Output**:
  
  55
