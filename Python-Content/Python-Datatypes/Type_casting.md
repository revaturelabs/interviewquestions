## Type Casting

1. What is Type casting?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python type casting is a method to change the variables/values declared in a certain data type into a different data type to match the operation required to be performed by the code snippet.
The type casting process's execution can be performed by using two different types of type casting,
1)Implicit type casting
2)Explicit type casting
  
  </details>
  
  ---

2. What is the difference between Implicit type casting and explicit type casting ?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Implicit casting doesn't require a casting operator. Implicit Type Conversion is automatically performed by the Python interpreter. Python avoids the loss of data in Implicit Type Conversion. Explicit type casting is performed by the programmer. Explicit Type Conversion is also called Type Casting, the data types of objects are converted using predefined functions by the user.

</details>

---

3. What are all the advantages of typecasting?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
 > - Python provides the loss of data implicit type conversion.
 > - In python automatically converts one data type to another data type. This process doesn't need any user involvement, python promotes the conversion of lower data types.
 > - For example, integer to higher data type says float to avoid data loss. This type of conversion or type of casting is called UpCasting.
  
  </details>
  
  ---

4. Can we convert the complex into int datatype?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
  > No, we can't
  > We can convert any type to int type, but we cannot perform complex to int type.
  
  </details>
  
  ---
  
5. What is the use of the `int()` function?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
>  The `int()` function converts a string, hexadecimal, binary,octal and float to int. If the argument is a floating point, the conversion truncates the number. If the argument is outside the integer range, It converts the number into a long type.

  </details>
  
  ---
  
6. After executing the following line of code, what would be the data type of data?

> d = 7,

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> The data type of d is tuple. Because python tuple does not need brackets/parentheses, if there is more than one element, tuples need a comma to distinguish from a numeric data element.

</details>

---

7. How will you convert float value 12.6 to integer value?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
>  Float value can be converted to an integer value by calling the `int()` function.
  
**Example**:
  
```python  
a=7.5
print(type(a))
a1=int(a)
print(type(a1))
```
**Output**:
  
<class 'float'>
<class 'int'>
  
<details><summary> <b>Explanation</b> </summary> 
  
> In python `int()` function is used to convert a float value into integer.
  
</details>
</details>
  
  ---

8. How do you remove a reference to a variable?
  
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
 - You can delete a reference to an object using the `del` keyword.
  
**Example**:
  
```python
a=8
print(a)
del(a)
print(a)
```
  
**Output**:
  
8
  
Traceback (most recent call last):
  
File "<string>", line 21, in <module>
  
NameError: name 'a' is not defined
    
    </blockquote>
  </details>
  
  ---
  
9. How will you convert integer value (18) to float value?
    
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Integer value can be converted to a Float value by calling the `float()` function.
  
**Example**:

  ```python
a=107
print(type(a))
a1=float(a)
print(type(a1))
 ```
  
**Output**: 
 
<class 'int'>
<class 'float'>
  
  </details>
  
  ---

10. What will be the output of the following code?

```python  
type(range(5))
```

  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> The above program will return the data type as `range()`. 
  
<details><summary> <b>Explanation</b> </summary>
  
> In Python 3, the `range()`  function returns range object, not list.
  
  </details>
  </details>

11. Predict the output of the following code?

```python  
x = 80
def func1():
    x = 25
    print(x)
func1()
print(x)
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
**Output**:
  
25
  
80
  
<details><summary> <b>Explanation</b> </summary>
  
> A variable declared outside of all functions has a GLOBAL SCOPE. Thus, it is accessible throughout the file. And variable declared inside a function is a local variable whose scope is limited to its function.
  
  </blockquote>
    </details>
  </details>
  
  ---

12. What will be the output of the following code?
  
  ```python
def func1():
    y = 50
    return y
func1()
print(y)
```
  
 A.50
  
 B.NameError
  
 C.None
  
 D.0
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> `NameError`
  
<details><summary> <b>Explanation</b> </summary>
  
> You will get an error as `NameError: name 'y' is not defined`. To access the function’s return value we must accept it using an assignment operator like this.
  
```python
def myfunc():
    y = 50
    return y
x = myfunc()
print(y)
```
  
  </details>
  </details>
  
  ---
  
13. What is the output of the following code?
  
```python
print(bool(0), bool(3.14159), bool(-3), bool(1.0+1j))
```
  
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg) 
  
<details><summary> <b>Show Answer</b> </summary>
  
> False True True True
  
<details><summary> <b>Explanation</b> </summary>
  
> - If we pass zero values to bool() constructor, it will treat it as zero.
> - Any non-zero value is boolean True.
  
  </details>
  </details>
  
  ---

14. What is the `del` keyword in python and explain with an example.
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> `del` keyword is used to delete objects in python.
> You can delete a reference to an object using the del keyword.
  
**Example**:
  
```python  
a=8
print(a)
del(a)
print(a)
```
  
**Output**:
8
Traceback (most recent call last):
  File "<string>", line 21, in <module>
NameError: name 'a' is not defined
  
</details>

---
  
15. Predict the output of the following code?
  
```python  
x=56.9
print(type(x))
x1=int(x)
print(type(x1))
x2=7+1j
print(type(x2))
x3=int(x2)
```
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
<class 'float'>
<class 'int'>
<class 'complex'>
TypeError: can't convert complex to int
  
<details><summary> <b>Explanation</b> </summary>
  
  - It will be printing the type of x variable.
  - It will convert float to integer.
  - In line 6 it's converting complex to an integer. But, it will throw a type error because we can't able to convert the complex into integers.
  
  </blockquote>
  </details>
  </details>
  
  ---
