## Function

1.What is a function?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary>
    <b>Show Answer</b>
  </summary>
  
> A function is a block of organized, reusable code that is used to perform a single, related action. Functions provide better modularity for your application and a high degree of code reusing.In python, we have three types of functions:

> 1. Built-in `print()`
> 2. User-defined functions(UDF)
> 3. Anonymous-`Lambda()`
  
</details>

---

2.What is the difference between call by value and call by reference?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
 <blockquote>
  
- **Call by value:**
   - A copy of the variable is passed.
   - Change in the copy of variable doesn't modify the original value of variable.
   - **Syntax: function_name(variable_name1,variable_name2)**
   - Default calling-primitive type are passed using the call_by_value.
	
- **Call by reference:**
   - A variable itself is passed.
   - Change in the copy of variable modify the original value of variable.
   - Syntax: function_name(&variable_name1,&variable2...)
   - Default calling-Objects are implicitly passed using call_by_reference.
 
 </blockquote>
</details>

---

3.How many scope of variables are in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  
> There are two basic scope of variable in python,
	
1.Global variable
	
2.Local variable
	
**Global variable:**
	
>  Global variables are those which are not defined inside any function and have a global scope.
  
**Local variable:**
  
> Local variables are those which are defined inside a function and its scope is limited to that function only.
</details>

---	
	
4.How does a function return values?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer</b></summary>
  
> A function uses the `return` keyword to return a value. 
  
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

---	
	
5.What is the output of the following code?
  
```Python
def my_func()
   x = 10
   print("Value :",x)
x = 20
my_func()
print("Value :",x)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
**Output**:
  
def my_func()
                 ^
SyntaxError: invalid syntax
  
<details><summary> <b>Explanation</b> </summary>  
  
> Here, we get `Syntax error` because the syntax is `def function_name():`

```Python
def my_func():
   x = 10
   print("Value :",x)
x = 20
my_func()
print("Value :",x)
```	
  
</details>
</details>
	
---
  
6.Specify few Built-in functions in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
	 <blockquote>
	
 - python `abs()`-returns absolute value of a number
 - python `all()`-returns true when all elements in iterable is true
 - python `ascii()`-eturns String Containing Printable Representation
 - python `delattr()`-deletes attribute from the object
 - python `eval()`-runs code within program
  
 </blockquote>
</details>

--

7.Can we use local variables in the local global scope?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> `No`,we cannot use local variables in the global scope.
  
**For example**:
  
  ```Python
def spam():
  calls = 31337
  spam()
print(calls)
  ```
 
> If this program is executed, the output will be:
Traceback (most recent call last):
  File "C:/test1.py", line 4, in <module>
    `print(Calls)`
  
<details><summary> <b>Explanation</b> </summary> 
  
> `NameError`: name 'calls' is not defined
> The error happens because the calls variable exists only in the local scope created, when spam() function is called. Once the program execution returns from spam, the local scope is destroyed, and there is no longer a variable as calls.
  </details>
  </details>
	
---
  
8.What is the data type of None?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> `None` has a special status in Python. The `None` is used to define a null variable or an object, and it is a data type of the `class NoneType`.

**Example**:

```python
x=None
print(type(x))
```
	
<b>Output:</b> 
  
`<class 'NoneType'>`
	
</details>
 
---
	
9.When does the code in a function gets executed: when the function is defined or when the function is called?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> The code in a function executes when the function is called, and not when the function is defined.
  
**Example**:
	
```python
def greet(name1):  
    print ('Hello ', name1)
greet('Sam')
```
	
**Output**:
  
`Hello  Sam`
	
<details><summary> <b>Explanation</b> </summary>
	
> The code will be executed when the function is called,because at that time only that block of code will be get execute.
	
</details>	
  </details>

---
	
10.How many global scopes are there in a Python program? 
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
	
> There's only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are forgotten.
  
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
 
---	
	
11.Which return type returns a value?
	
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> You declare a method's return type in its method declaration. Within the body of the method, you use the `return` statement to return the value. Any method declared as `void` doesn't return a value.
  
</details>
	
---	
  
12. In python, when a function does not have a return statement, what does the function return when it is called?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> If you don't explicitly use a return value in a `return` statement, or if you totally omit the return statement, then Python will implicitly return a default value. That default return value will always be None.
 
  </details>

---	
	
13.How can you force a variable in a function to refer to the global variable?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> If a global variable has to be refered in a function, the `global` keyword can be used to declare the respective variables as global.In Python, `global` keyword allows us to modify the variable outside of the current scope. It is used to create a global variable and make changes to the variable in a local context.

 ```Python
x = 5
def change():
	global x
	x = x + 5
	print("Value of x inside a function:", x)
change()
print("Value of x outside a function :", x)
```
	
**Output**:
  
  Value of x inside a function : 10
	
  Value of x outside a function : 10
	
  </details>

---	
	
14.Is `bytes()` a Built-in function or predefined function in python and explain any one of the Built-in function? 
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
- `Yes, bytes()` is a Built-in function.
- The functions which along with python itself are called a `Bulit-in function` or `predefined function`.
	
- `range()`
  
**Example**:

  ```python
for i in range(1, 10):
    print(i, end=' ')
  ```
  
**Output**:

1 2 3 4 5 6 7 8 9 
  
   </blockquote>
	 </details>
 
---	
	
15.What is the output of the following code?
  
```python
def outer_function(a, b):
    def inner_function(c, d):
        return c + d
    return inner_function(a, b)
    return a
Output = outer_function(45, 10)
print(Output)
  ```
	
 A.55
	
 B.(45,10)
	
 C.45
	
 D.Syntax Error
	
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
	
<details><summary> <b>Show Answer</b> </summary>
	
> Option B.55
	
<details><summary> <b>Explanation</b> </summary>

> Adding multiple return statements doesn’t perform any task. Once function execution is encountered with the return statement, it stops the execution by returning whatever is specified by the return statement.
	</details>
	</details>

---	
	
16.Debug and correct the following code and find the output for the same?
	
``` python

# Type your answer here.
print(func(999))
```
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
<details><summary> <b>Hint</b> </summary>
	
> Create a function named `func`.
	
> `reutrn` a value which always returns the number: 100
	
</details>
	
<details><summary> <b>Show Answer</b> </summary>
	
```python
	
def func(x):
    return 100
print(func())
```
	
</details>

---	
	
17.What is the output of the following code?
	
```python
def salary(**kwargs):
    for i in kwargs:
        print(i)
salary(emp="Anto", salary=10000)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
	
<details><summary> <b>Show Answer</b> </summary>
	
emp
	
salary

<details><summary> <b>Explanation</b> </summary>

> To accept Variable Length of Keyword Arguments, i.e., To create functions that take 'n' number of Keyword arguments, we use `**kwargs` (prefix a parameter name with a double asterisk ** ).

> keyword arguments: display(emp="Anto", salary=10000)
	
> This `**kwargs` collects all passed arguments into a new dictionary, where the argument names are the keys, and their values are the key’s values. So, to get the values, we need to iterate the kwargs dictionary.
	
**Example**:
	
('emp', 'Anto')
	
('salary', 10000)
	
</details>
</details>

---	
	
18.Complete the following code and get the correct output for the same.
(Write a function named func which will ask user for their name and print Hello!, Name)

```python
# Type your answer here.
func()
```
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)	
	
<details><summary> <b>Hint</b> </summary>

> You can use `input()` function to ask for user input. And you can assign it to a variable.
	
</details>
	
<details><summary> <b>Show Answer</b> </summary>

```python
def func():
    name = input("Please enter your name.")
    print("Hello!", name)
func()
```
	
**Sample Output**:
	
Hello! Jack

</details>
	
---
	
19.Choose the correct function declaration of `fun1()` so that we can execute the following function call successfully.

```python
fun1(25, 75, 55)
fun1(10, 20)
```
	
 A.`def func1(**kwargs)`
	
 B.No,it is not possible 
	
 C.`def fun1(args*)`
	
 D.`def fun1(*data)`
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
<details><summary> <b>Show Answer</b> </summary>	

> Option D:`def fun1(*data)`

<details><summary> <b>Explanation</b> </summary>

> To accept multiple values or if the number of arguments is unknown, we can add the `*` before the parameter name to accept arbitrary arguments. i.e., To accept Variable Length of Positional Arguments. To create functions that take 'n' number of Positional arguments, we use `*args`(prefix a parameter name with an asterisk *).
	
*Example*:
	
```python
def fun1(*data):
    for i in data:
      print(i)
      print("Done!")
fun1(25, 75, 55)
fun1(10, 20)
```
	
</details>	
</details>
	
---	
	
20. How does the range function work?
	
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
	
<details><summary> <b>Show Answer</b> </summary>
	
> The `range()` function returns the sequence of numbers between the start to stop with a step increment. The syntax of the range function is range(start, stop[, step]).
> The `stop` argument is mandatory. The arguments `start` and `step` are optional. The default value of start and step are 0 and 1, respectively.

**Example**:
	
```python
print(list(range(1, 10, 2)))
```
	
**Output:**
	
[1, 3, 5, 7, 9]
	
</details>
	
---
	
