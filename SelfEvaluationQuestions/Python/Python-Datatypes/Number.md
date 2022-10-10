## Number

1.What do you mean by `datatype` in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
 > A data type is a classification or categorization of knowledge items. This represents a useful type of operation that is frequently performed on a particular piece of data. Since everything is an object in Python programming, the data type is a class and the variables are instances (objects) of those classes.

</details>

---

2.Can you name four of the main data types in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
  - Numeric
  - Sequence Type
  - Boolean
  - Set
  - Dictionary
  
- `Numbers`, `strings`, `lists`, `dictionaries`, `tuples`, `files`, and `sets` are generally considered as the main types of data. Types, None, and Booleans are sometimes classified this way. The integer, floating-point, complex, fraction and decimal are numerical data types, simple strings and Unicode strings in Python 2, text strings and byte strings in Python 3 are the types of string data types.
  
</blockquote>
    </details>

---

3.Why are the data types called Python's core data types?
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> They are known as the core data types because they are part of the Python language itself and are always available to create other objects, and you usually need to call functions in imported modules.
  
</details>

---

4.How will you find the type of the data?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> `type()` function is used to determine the type of data type.
  
**Example**:
 
```python
a= 5
print("type of data",type(a))
```
<details><summary> <b>Explanation</b> </summary>  
  
> In python, `type()` method is used to find the type of the data stored in a variable.
  
  </details>
  </details>
 
 ---
 
5.What does sequence mean and which three types of data fall into this category?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
 > - A sequence data type is a collection of objects ordered by a specific position. 
 > - In Python, `Strings`, `lists`, and `tuples` are the data types based on sequences. 
 > - The Sequences share common sequence operations, such as indexing, concatenation, and slicing, but also have type-specific method calls.
  
</details>

---

6.What does immutable and what are the three types of Python core data types that are considered immutable? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
 1. Immutable data types are object types that cannot be modified after they are created. 
    - Python numbers 
    - strings
    - tuples fall into this category. 
  
 2. You can't change an immutable object on the fly, but you can always create a new object by executing an expression.
  
</blockquote>
    </details>

---

7.How will you get input from user?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- In python, we can use `input()` function to take input from user. But,it will differ when it comes to another data type like String. In that case, we can use `int(input())` to take input as a integer from user.
  
1.integer input - `int(input())`
  
2.String input - `input()`
  
**Example**:
  
```python
x=int(input("Enter a integer value"))
```
  
</blockquote>
  </details>

---

8.What are the three numeric types in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- Number data types store numeric values. They are immutable data types, which means that changing the value of a number data type results in a newly allocated object. In python, we have three numeric data types,
  
 1.int
  
 2.float
  
 3.complex
  
 1.int:
  
   - This datatype can hold only the whole number,including negative numbers but not fractions. In Python, there is no limit to how long an integer value can be stored.
  
**Example** :
 
```python
 x=10  #int
```
 
 2.float:
  
 - Using this data type, we can store decimal values.
  
**Example** :

```python  
x=10.4  #float
```
  
 3.complex:
  
 - In this data type, we can store complex values.
  
**Example** :

```python  
x=2j  #complex
```
    
</details>

---

9.How will you verify the type of variable or any object ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
  <blockquote>
  
- In python, we can use the `type()` function
  
**Example**:
  
```python
x=10
print(type(x))
```
  
**Output**:
  
<class 'int'>
  
  </blockquote>
  </details>
  
  ---

10.Write a python program to perform arithmetic operations.
  
  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
```python
a=int(input())
b=int(input())
c=a+b
print("Addition",c)
d=a-b
print("Subtraction",d)
e=a//b
print("Division",e)
f=a*b
print("Multiplication",f)
g=a%b
print("Modulus",g)
h=a**b
print("Exponent",h)
```

**Output**:
  
enter the value of a:3
  
enter the value of b:4
  
Addition 7
  
Subtraction -1
  
Division 0
  
Multiplication 12
  
Modulus 3
  
Exponent 81

<details><summary> <b>Explanation</b> </summary>
  
- In this program, to perform an arithmetic operation, we declared two variables to store a value and then perform arithmetic operations like +,-,*,%,etc...
  
  </details>
  </details>
  
  ---
  
11.What is the output of the following code?
  
```python
a=50
type(a)
```
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> no output
  
<details><summary> <b>Explanation</b> </summary>
  
> Because we didn't print the type of the variable.
  
  </details>
  </details>

  ---
  
12.What is the output of the following code?

```python
print( (1.1 + 2.2) == 3.3 )
```
  
A.`True`
  
B.`False`

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>
  
> Option B.`False`
  
<details><summary> <b>Explanation</b> </summary>
  
> (1.1 + 2.2) it is not equal to 3.3, it is 3.3000000000000003.Use the `round()` function to compare exact values.
  
**Example**:

```python
print(round(1.1 + 2.2, 10) == round(3.3, 10))
```
  
  </details>
  </details>

 ---
  
13.What is the use of `int()` function?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> The `int()` function converts a string,hexadecimal,binary,octal and float to int.If the argument is a floating point, the conversion truncates the number. If the argument is outside the integer range, it converts the number into long type.
  
  </details>
  
  ---

14.Please select the correct expression to reassign a global variable "x" to 20 inside a function `fun1()`.

  ```python
x = 50
def fun1():
    # your code to assign global x = 20
fun1()
print(x)
```
  
 A.global x=20
  
 B.global var x
    x=20
  
 C.global x
    x=20
  
 D.global.x=20
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option C.global x
             x=20  
  
<details><summary> <b>Explanation</b> </summary>
  
> global x  x=20  is the correct answer,because other declarations are not the correct syntax for global variable declarations.
  
<details><summary> <b>Correct Code</b> </summary>

```python
x = 50
def fun1():
   global x
   x=20  
fun1()
print(x)
```
  
  </details>
  </details>
  </details>
  
  ---
  
15.Can we convert complex numbers to any other number type?
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
  
> `No`  
  
<details><summary> <b>Explanation</b> </summary>
  
> We can't convert complex numbers to any other number type as python will give you TypeError.This function converts other numeric values into floating values.

**Example**:
  
```python
i=10+1j
c=int(i)
print(c)
print(type(c))
```
  
</details>
  
**Output**:
  
it will throw an error the error is,
TypeError: can't convert complex to int

  </details>
  
  ---

16.What is the output of the following program?
  
```python
print(type(0xFF))
```

 A.number
  
 B.hexint
  
 C.hex
  
 D.int

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- Option D.int
  
<details><summary> <b>Explanation</b> </summary>
  
- We can represent an integer in binary,octal and hexadecimal formats.
  
 - 0b or 0B for Binary and base is 2
 - 0o or 0O for Octal and base is 8
 - 0x or 0X for Hexadecimal and base is 16
  
  </details>
  </details>

  ---
  
17.Predict the output of the following code.
  
```python
a=0b101
print(b)
print("The data type of the variable",type(b))
``` 
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg) 
  
<details><summary> <b>Show Answer</b> </summary> 
   
**Output**: 
  
8
  
The data type of the variable <class 'int'>
   
<details><summary> <b>Explanation</b> </summary>
   
> Integers can be binary, octal, and hexadecimal values.
   
   </details>
   </details>
   
 --- 
  
18.In Python 3, what is the output of `type(range(5))`? (What data type it will return).
   
 A.int
  
 B.list
  
 C.range
  
 D.None

 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> Option C.`range`
  
<details><summary> <b>Explanation</b> </summary>
  
> In python 3, the `range()` function returns range object,not list.

  </details>
   </details>

 --- 
  
19.How will you convert float value 12.6 to integer value?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary> <b>Show Answer</b> </summary>
  
> Float value can be converted to an integer value by calling  `int()` funtion.
  
**Example**:
  
```python
a=7.5
print(type(a))
a1=int(a)
print(type(a1))
```
  
</details>
  
 --- 
  
20.How will you convert real numbers to complex numbers. Give an example?
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Numeric values can be converted into complex numbers with `complex()` function. 
  
**Example**:
  
```python 
a=8
print(a)
print(complex(a))
```
  
**Output**:
  
8
(8+0j)
  
<details><summary> <b>Explanation</b> </summary>

> To convert real numbers into complex numbers we can use `complex()` method.
  
</details>
 </details>
  
  ---

21.What is the output of the following code?

```python
a = 7
b = -8
x = complex(a,b)
print(x)
print(x.real)
print(x.imag)
```
   
  A.7-8
    7.8
   -8j
  
  B.(7-8j)
    7.0
   -8.0
  
  C.7-8j
    7.0
   -8.j
  
  D.None

  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

 > Option c
     (7-8j)
     7.0
     -8.0
  
   </details>

  ---
  
22.What are the 4 built-in numeric data types in python?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
   
<details><summary> <b>Show Answer</b> </summary>
  
  <blockquote>
  
   - int: These are whole numbers of unlimited range. 
   - long: These are long integers in Python 2. 
   - float: These are floating point numbers represented as 64-bits double precision numbers. 
   - complex: unsigned numbers with real and imaginary components.
  
   </blockquote>
    </details>
   
---
