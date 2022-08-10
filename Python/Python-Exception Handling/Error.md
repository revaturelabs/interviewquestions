## Error

1.Ron is trying to `open` a file that doesn't exist in his computer system with the following line of code:

```python
file_open = open('file1.txt', 'r')
```

What Error he will get after executing this line in python interpreter?

A.`FileFoundError`
 
B.`NoFileFoundError`

C.`FileNotFoundError`

D.`FileNotExistError`

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option C.`FileNotFoundError`

<details><summary><b>Explanation</b></summary>

> When a user tries to open a file for reading purpose that does not exists than the program will throw the `FileNotFoundError`, `No such file` or directory: 'myfile.txt'. If you are sure that file is present in the system than, make sure that you are providing the correct path of the file in the program. 

</details>
</details>

---

2.What will happen if a user writes the following code to get the list element?

```python
list1 = [1, 2, 3, 4]
print(list1[4])
```

A.It will print 4.

B.It will result in error because list elements are not iterable.

C.It will print 3.

D.It will result in error because list index is out of range. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option D.It will result in `error` because list index is out of range.

<details><summary><b>Explanation</b></summary>

> The above code will result in IndexError becuase list indexing starts from 0, not 1, and goes till length of the list minus 1 that is len(list)-1. So we have to access the last element from the above list than we have to write print(list1[3]). 

</details>
</details>

---

3.What are the common reasons of getting errors in python program?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>
 
 There can be muliple reasons of getting errors in your python code, some of the common reasons are:
- Not proper indentation   
- Using the variables before defining 
- Misspelling variable names or keywords. for example, you have declared a variable as `num1= 4`, When you want to print that number if you use`print(num)` it would give error. 
- Missing colon or comma at the end of the functions
 </blockquote>
</details>

---

4.What are the types of `Error` in python? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>
 
Generally there are two types of errors, when is **Syntax error** and another is **Logical error**. 

- **Syntax error**: 
  - These types of error will occur at compile time. When we write something wrong in the program with respect to structure or syntax of the language these errors were thrown in the program. 
  
**Example**: 

```python
print("hello")
print("hi")
```

- **Logical error**: 
  - These types of error will occur at run time. When there is no mistake in writing code according to the structure and syntax of the language and still we are getting errors than that is because of the logic that we have provided in the code. 
  
**Example**: 

```python
print(10/0)
``` 
 </blockquote>

</details>

---

5.What will happen when we run the below code? 

```python
print("hello")
 print("hi")
```

A.hello will be printed

B.hi will be printed

C.hello and hi both will be printed

D.we get the indentation error

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
 
<blockquote>

- Option D.we get the indentation error

<details><summary><b>Explanation</b></summary>

- After running the above code, the program will throw the `IndentationError` because 2nd print statement is not correctly indented. To resolve this error, remove the spaces before 2nd print statement. 

 </blockquote>
</details>
</details>

---

6.While running the below code, robsin is getting some error. As he is new to the python language he is not able to rectify what to do to get the correct output. Help him by resolving all the errors.

```python
num1 = 12
num2 = 14
prnt(num1 + num)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
 <blockquote>

- In the above code there were two errors, one is spelling of print keyword and another one is using num inside print which is undefined. So after changing `prnt` to `print` and `num` to `num2`, we will get the correct output.

```python
num1 = 12
num2 = 14
print(num1 + num2)  # output: 26 
```

 </blockquote>
</details>

---

7.Find the error(s) in the following code and rewrite it again.

```python
a, b = 10      #line 1
if (a == b)    #line 2
c= a + b       #line 3
print(C)       #line 4
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> In the above code, in line 1, one value is missing for b variable. In line 2, colon is missing after if condition. In line 3, the expression should be inside if block not outside. In line 4, we are printing capital C value which is not used throughout the program so it will result in name error.
After removing all the errors from the code, the code will look like this:

```python
a, b = 10, 10
if (a == b):
    c= a + b
print(c)
```

</details>

---

8.What is the difference between `exceptions` and `error`?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

**Exceptions**:
   - Errors detected during execution are called `exceptions`.
   - It is not possible to recover.

**Error**:
   - Errors are the problems which stop the program execution.
   - It is possible to recover the `error`.

 </blockquote>
</details>

---

9.Write a sample program for an syntax errors?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
a = 105
if (a>200)
    print("eligible for travel")
```

**Output**:

> Syntax error

<details><summary><b>Explanation</b></summary>

> It will show an syntax error because, missed ":" in line2 .

</details>
</details>

---

10.What are the different types of logical errors?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - `Index error`: When the wrong index of a list is retrived.
> - `KeyError`: It will occur when the key is not defined.
> - `TypeError`: When a function is declared or defined incorrect type.
> - `NameError`: It will occur when the variable is not defined.
> - `MemoryError`: It will happen when program runs out of memory.

</details>

---

11.What are the two parts in an error message? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> The `error` message has two parts: the type of error before the colon, and specification about the error after the colon.
> **Example**: 

```python
print(10 * (1/0))
```

**Output**:

Traceback (most recent call last):   

File "<stdin>", line 1, in ? 

`ZeroDivisionError` : integer division or modulo by zero 

</details>

---

12.What is `IndexError` and Explain with an Example?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> **IndexError** is occur when the index is out of range.

**Example**:

```python
list=[34,67,5,8,2]
print(list[7])
```

**Output**:

Traceback (most recent call last): 
 
File "<pyshell#16>", line 1, in <module> 
 
print list[7] 
 
`IndexError`: list index out of range

</details>

---

13.Find the `syntax error` in the given code.

```python
while True print("Software engineer")
```
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> In the above given program, colon is missing after the condition.
> The Correct code for above program is,

```python
while True:  
    print("Software engineer")
```

</details>

---

14.Categorise the different types errors arises during programming. Interpret the following python code.

```python
import os 
cwd = os.getcwd() 
print cwd 
```
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer</b></summary>
 
<blockquote>

**Basic types of errors**

**Syntax Error**: 
  
 - Raised by the parser when a syntax error is encountered.

**Semantic Error**:
 
  - Raised by the parser when there is logical error in the program. 

  - Here in the above given program, Syntax error occurs in the third line (print cwd).

**SyntaxError**: Missing parentheses in call to `print`. 

 </blockquote>
 </details>

---

15.What will be the output of the following code?

```python
int('76.98')
```

A.TypeError

B.NameError

C.ValueError

D.ImportError
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> `Option C.ValueError`

<details><summary><b>Explanation</b></summary>

> The above program result is valueError because there is an ivalid litreal for `int()`.

</details>
</details>

---

16.What will be the output of the following code?

```python
print("Good Morning")
print(Good Day")
```

A.Semantic,Syntax

B.Syntax,Semantic

C.Semantic,Syntax

D.Syntax,Syntax
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option A.`Semantic,Syntax`

<details><summary><b>Explanation</b></summary>

> The code shows an `error` detected during `execution`.The second line shows an `syntax error`. When there is an deviation form rules of a language, syntax error is occured.

</details>
</details>

---

17.What will be the output of the following code?

```python
D1={'1':"aa", '2':"bb", '3':"cc"}
print(D1['4'])
```

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer</b></summary>

> Traceback (most recent call last):
> File "<pyshell#15>", line 1, in <module>

<details><summary><b>Explantion</b></summary>

> It will throw an key `Error`,Because key is not found.

```python           
D1['4']
KeyError: '4'
```

</details>
</details>

---

18.What is import error?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary><b>Show Answer</b></summary>

> This function is occur when the specified funcytion is not found.

```python
from math import cube
```

> from math import cube
ImportError: cannot import name 'cube'

</details>

---

19.What is `NameError` give an example?
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> The `NameError` is thrown when an object could not be found.

```python
print(age)
```

**Output**:

Traceback (most recent call last):
File "<pyshell#6>", line 1, in <module>

</details>

---

20.What will be the output of the following code?

```python
x=100/0
print(x)
```

 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary><b>Show Answer</b></summary>
 <blockquote>

 - This expression `x=100/0` throws `ZeroDivisionError: division by zero` error.
 - The `ZeroDivisionError` is thrown whenever we are trying to divide a number by zero.

 </blockquote>  
</details>

---
