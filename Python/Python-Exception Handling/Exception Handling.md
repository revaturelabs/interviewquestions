## Exception Handling

1.What is Exception?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

- An exception is an occurrence that happens throughout the execution of programs that disrupt the normal flow of execution (e.g., KeyError Raised once a key's not found during a dictionary.) an exception could be a Python object that represents an error..
- In Python, an exception is an object derives from the BaseException class that contains data concerning an error event that occurred inside a technique. Exception object contains:
    - Error type (exception name)
    - The state of the program once the error occurred
    - An error message describes the error event.
	
</blockquote> 
</details>

---

2.What are the different types of exceptions?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

1.FileNotFoundException

2.ImportError

3.RuntimeError

4.NameError

5.TypeError
	
</blockquote>

</details>

---

3.What is the use of `Exception` Handling?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

1.**Standardized error handling**: using built-in exceptions or making a custom exception with a a lot of precise name and description, you can adequately define the error event, that helps you correct the error event.

2.**Cleaner code**: Exceptions separate the error-handling code from regular code, that helps us to keep up large code easily.

3.**Robust application**: With the assistance of exceptions, we will develop a solid application, which might handle error event with efficiency.

4.**Exceptions propagation**: By default, the exception propagates the decision stack if you don’t catch it. as an example, if any error event occurred in a very nested perform, you do not got to explicitly catch-and-forward it; automatically, it gets forwarded to the career perform wherever you'll handle it.

5.**Different error types**: Either you'll use built-in exception or produce your custom exception and group them by their generalized parent category, or Differentiate errors by their actual class.

</blockquote>	
</details>

---

4.What is the difference between Built-in exception and User-defined exception?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

**Built-in exception**:

- The exceptions which are raised automatically by python whenever a particular event occurs.

**Example**:

```python
print(10/0) ===>ZeroDivisionError
```

**User-defined exceptions**:

- User-defined exceptions is making your own exception class and throwing that exception using the 'throw' keyword. as an example, MyException within the below code extends the Exception category.
	
</blockquote>  
  </details>

---

5.What are the different types of Built-in Exceptions?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

1.EOFError - Raised once the `input()` perform hits the end-of-file condition.

2.FloatingPointError- Raised once a machine operation fails.

3.GeneratorExit - Raise once a generator’s `close()` methodology is named.

4.ImportError	- Raised once the foreign module isn't found.

5.IndexError- Raised once the index of a sequence is out of vary.

6.KeyError - Raised once a secret is not found in a very dictionary.

7.KeyboardInterrupt - Raised once the user hits the interrupt key.

8.MemoryError- It  will raised an exceptions when an operation runs out of memory.
	
</blockquote>
</details>

---

6.What will be the output of the following code?

```python
def excep():
    try:
        return 1
    finally:
        return 2
s = excep()
print(s)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>
	
> 2

<details><summary><b>Explanation</b></summary>

> The finally block is executed even there's a return statement within the try block.

</details>
</details>

---

7.How `exceptions` are handled in Python?  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>
<blockquote>

- To handle exceptions or to call code when an exception occur, at the time we can use try/except statements in Python.

**Syntax**:

```python
try:
    #some lines of code
except:
    #code
```
	
</blockquote>
</details>

---

8.What will be the output of the following code?

```python
def Except():
    try
        print(10)
    finally:
        print(12)
Except()
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>

try
       ^

SyntaxError: invalid syntax

<details><summary><b>Explanation</b></summary>

> In the above program we missed **:** in the 2 line.

</details>
</details>

---

9.What happens once '1' == `one` is executed?

 A.we get a real
 
 B.we get a False
 
 C.associate TypeError happens
 
 D.a ValueError happens
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer </b></summary>

> Option B.we get a `False`

<details><summary><b>Explanation</b></summary>

> It simply evaluates to `False` and does not raise any exception.

</details>
</details>

---

10.Can we handle multiple exception with one block of except statements ?

 A.Yes, like except TypeError, SyntaxError [,…]
 
 B.Yes, like except [TypeError, SyntaxError]
 
 C.No
 
 D.None of the mentioned
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer </b></summary>

> Option A.`Yes, like except TypeError, SyntaxError [,…]`

<details><summary><b>Explanation</b></summary>

> Each type of exception can be specified directly. There is no need to put it in a list.

</details>
</details>

---

11.Predict the output of the following code?

```python
try:
    if '10' != 1:
        raise "Error"
    else:
        print("Error has not occurred")
except "Error":
    print ("Error has occurred")
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Invalid code

<details><summary><b>Explanation</b></summary>

> A new exception class must inherit from a BaseException. There is no such inheritance here.

</details>
</details>

---

12.Debug the code and give the correct solution for this code?

```python
a=5
b=0
try:
    result=a/b
except ZeroDivisionError:
print(result)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
a=5
b=0
try:
    result=a/b
except ZeroDivisionError:
    result="Divide by zero error"
print(result)
```

**Output**:

`Divide by zero error`

</details>

---

13.How will try() block work?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- First, the try clause is executed i.e. the code between attempt to except clause.
- If there's no exception, then solely the try clause can run, except the clause is finished.
- If any exception happens, the try clause are skipped and except clause can run.
- If any exception happens, however the except clause inside the code doesn’t handle it, it's passed on to the outer try statements. 
- A try statement will have more than one except clause.
  
**Example**:

```python
def divide(x, y):
	try:
		result = x // y
		print("answer is :", result)
	except ZeroDivisionError:
		print("dividing by zero ")
divide(3, 2)
```
	
</blockquote>
</details>

---

14.What is else clause ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

In python, you'll also use the else clause on the try-except block that should be present in any case the except clauses. The code enters the else block as long as the try clause doesn't raise an exception.

**Syntax**:

```python
try:
    # Code
except:
    # it will excecute if error in the try block
else: 
    # if no exception it will excecute this block
```

</blockquote>	
</details>

---

15.What is the use of finally keyword in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- Python provides a keyword `finally`, that is often executed when the `try` to except blocks. the `final` block continuously executes when normal termination of strive block or when `try` block terminates due to some exception.

**Syntax**:

```python
try:
    # Code
except:
    # optional block
    #if required we can add this block when handling of exception 
else:
    # if no exception at that time it will excecute
finally:
    # always executed block
```

</blockquote>
</details>

---

16.Which of the following is not from the built-in error?

 A.EOFError
 
 B.KeyError
 
 C. LoopError
 
 D.None

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option C. LoopError

</details>

---

17.Which keyword is used to raise an `error` in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- Python additionally provides the `raise` keyword to be utilized in the context of exception handling. It causes associate exception to be generated expressly. inbuilt errors are raised implicitly. However, a inbuilt or custom exception is forced throughout execution.

**Example**:

`````python
try:
    x=int(input('Enter a number upto 100: '))
    if x > 100:
        raise ValueError(x)
except ValueError:
    print(x, "is out of allowed range")
else:
    print(x, "is within the allowed range")
`````

</blockquote>
</details>

---

18.Predict the output of the following code?

```python
def getValue(m):
    if m<1 or m>12:
        raise ValueError("Invalid input")
    print(m)
getValue(7)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- 7

<details><summary><b>Explanation</b></summary>

- In the code shown above, since the value passed as an argument to the perform is between one and twelve (both included), thus the output is that the value itself, that is 7. If the worth had been higher than twelve and less than one, a ValueError would are thrown.

</blockquote>
</details>
</details>

---

19.What will be the output of the following code?

```````python
try:
    amount = 1999
    if amount < 2999:
        # raise the ValueError
        raise ValueError("please add money in your account")
    else:
        print("You are eligible to purchase DSA Self Paced course")
        # if false then raise the value error
except ValueError as e:
    print(e)
```````

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
 
> please add money in your account

</details>

---

20.When will the finally block be executed?

 A.once there's no exception
 
 B.once there's an exception
 
 C.given that some condition that has been specified  is satisfied
 
 D.always
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	<blockquote>

- Option D.always

<details><summary><b>
Explanation</b></summary>

- The finally block is always executed.

	</blockquote>
</details>
</details>

---

21.What will happen if the file is not found in the following program?

```python
a=False
while not a:
    try:
        f_n = input("Enter file name")
        i_f = open(f_n, 'r')
    except:
        print("Input file not found")
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

`File not found`

<details><summary><b>Explanation</b></summary>

- if the computer file in not found, then the statement: “Input file not found” is written on the screen. The user is then prompted to reenter the file name. Error isn't thrown.

	</blockquote>	
</details>
</details>

---

22.What is the output of the following code?

r[5]

 A.IndexError
 
 B.NameError
 
 C.TypeError
 
 D.ValueError

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- Option B.NameError

<details><summary><b>Explanation</b></summary>

- The above code result is showing the output is NameError.Because this file name r nis not defined.

</blockquote>
</details>
</details>

---

23.Predict the output of the folowing code?

```python
valid = False
while not valid:
    try:
        num=int(input("enter a number"))
        while num%2==0:
            print("Welcome")
        valid = True
    except ValueError:
        print("invalid")
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- Welcome(printed infinite number of times)

<details><summary><b>Explanation</b></summary>

- The output of the above code is welcome(printed infinite number of times).Because an even number is given as `input`. If an odd number is given as `input`, then there is no output.

	</blockquote>
</details>
</details>

---

24.What will be the output of the following code?

```python
print("Good evening")
print("Good night)
```

 A.Syntax,Syntax
 
 B.Semantic,Syntax
 
 C.Semantic,Syntax
 
 D.Syntax,Semantic
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary><b>Show Answer</b></summary>
<blockquote>

- Option B.Semantic,Syntax

<details><summary><b>Explanation</b></summary>

- The first code shows an error detected throughout execution. This may occur often. In second line code represents a syntax error. once there's deviation from the principles of a language, a software error is thrown.

	</blockquote>	
</details>
</details>

---

25.Why should we use else block with try?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- In python use else statements with try block to check whether the try block is executed without any exception or else if you want to run a specific code only if an exceptions is not raised.
  
**Syntax**:

```python
try:
    #code
except Exception:
    #block of code
else:
    #it will executed when exception is not occured
```

- `try` : The try block used to throw an exception.
- `except` : The except used to handle error raised in try block.
- `else` : This block is executed if there is no exception.

</blockquote>	
</details>

---

26.What will be the output of the following code?

```python
a = [1, 3, 5]
try:
    a.get()
except:
    pass
print(a)
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- [1,3,5]

<details><summary><b>Hint</b></summary>

- All you have got to try and do is kind pass away the proper line with the proper indentation.
- Watch out for once you use except and pass statements like this as they're pretty generalist statements and may cause bother in more advanced programs.

</blockquote>	
</details>
</details>

---

27.what will be the output for the following code?

```python
a="Hello World"
try:
    a + 10
except Exception:
    msg="can't add int to string"
print(msg)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

> Can't add int to string

</details>

---

28.Write a python code for exception handling?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

```python
try:
    num1 = 10
    num2 = 0;
    print(num1/num2);
except:
    print("error occur, due to divided by zero")

```

**Output**:

`error` occur, due to `divided by zero`

	</blockquote>
</details>

---

29.What is the purpose of with/as statement in Python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- with statement in Python is used in exception handling to make the code cleaner and much more readable. It simplifies the management of common resources like file streams.

	</blockquote>
</details>

---

30.What is exception chaining?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>
<blockquote>

- The exception chaining is accessible only in Python three. The raise statements permit North American country as ex gratia from statement, that permits chaining exceptions. thus we will implement exception chaining in python3 by exploitation raise…from clause to chain exception.

- When exception `raise`, `exception` chaining happens mechanically. The `exception` are often raised within except or `finally` block section. we have a tendency to additionally disabled `exception` chaining by exploitation from None idiom.

**Sample code**:

```python
    a = int(input("Enter value of a:"))
    b = int(input("Enter value of b:"))
    c = a/b
    print("The answer of a divide by b:", c)
except ZeroDivisionError as e:
    raise ValueError("Division failed") from e
```

</blockquote>	
</details>

---
