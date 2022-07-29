# Python Basics Questions And Answers

1. Python was developed in which year?
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
- a) 1990
- b) 1987
- c) 1989 
- d) 1991 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 1989.
</details>

---

2. How many keywords are there in Python 3.7?

- a) 31
- b) 32
- c) 37
- d) 33
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 33 
</details>

---

3. What do you mean by keywords?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Keywords are the reserved words that have special meaning in python. We cannot use keywords as identifier, function and variable name. All the keywords are in lower case except "True" and "False". Python 3.7 have total of 33 keywords.  
For Example: and, or, if, elif,True, etc. 
</details>

---
4. What is an identifiers?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Identifier is the name given to variable, function, class, etc in python. It consists of character, digit and underscore("_", [special character]). 
There are some rules for Identifier in python, let's talk about them one by one: 
- Identifier should start with a character or an underscore. 
- A character can be a lowercase(a-z) or uppercase(A-Z). 
- A digit(0-9) can be placed at any position except at the starting. 
- No special characters(@,!,#,$,%,&) are allowed other than underscore. 
For Example:  first_name, _rollNo, id_1, etc. 
</details>

---
5. Which of the following statement is false regarding Identifiers? 

- a) Variable name can have lower and upper case letters.
- b) Identifier should start with a character or a number. 
- c) A digit(0-9) can be placed at any position except at the starting. 
- d) No special characters(@,!,#,$,%,&) are allowed other than underscore. 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b)

**Explanation:** Identifier can start with character or underscore, but not with a number.
</details>

---
6. Which is not a feature of Python?

- a) Easy to learn
- b) Platform independent 
- c) Dynamically Typed
- d) mid-level language
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) mid-level language.

**Explanation:** Python is a High- level language.
</details>

---

7. Which of the below mentioned is the correct extension of python file?

- a) .py
- b) .python
- c) .cpp
- d) none of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) .py 
</details>

---

8. What are the advantages of python over other programming languages?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Python offers some key features that makes it different from other programming languages such as:
- Easy to code: any non- programmer can also learn python basics in few hours but that is not true with Java or C++. 
- No need to remember where to add curly braces({}) or semi-colon (;) throughout the program.
- It is dynamically typed means, we don't need to specify the type of variable as the variable type is decided at the run time. 
- It has a large set of libraries that provides built-in functions and modules so that every time we don't have to write the code for every single thing. 
</details>

---
9. How do you differentiate between Interpreter and Compiler?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** These are the following differences between Interpreter and Compiler:
- Compiler translates our program in a single run, whereas Interpreter translates our program line by line.
- In terms of CPU utilization, Compiler utilizes more CPU than Interpreter. 
- In compilation all the errors in the program are shown in the end together, whereas in Interpreter errors of the code are shown line by line. 
- As the code size increases Complier takes more time to Scan a code compared to Interpreters.
- Example: C, C++, java, etc are based on Compiler whereas Python, Ruby, MATLAB, etc are interpreted language.
</details>

---

10. Is Python an Interpreted language or Compiled?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Python is an Interpreted language because it checks our code line by line not all together. For example suppose there are 2 errors in your code one in line 3 and other one in line 4. When you run the code it will only throw error for line 3 in console( output screen) but not  for line 4. The reason behind it is that it checks the code one line at a time. 
</details>

---
11. Is "true" an Identifier or Keyword?

- a) Keyword
- b) Identifier
- c) both a and b
- d) None of the above.
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) Identifier. 

**Explanation:** True is a keyword, whereas true with first letter in lower case is an Identifier. 
</details>

---
12. Point out whether the identifiers mentioned in a list are valid or not: [Last_Name, student@id, 4_id, var, for]. 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Last_Name and var are the only valid identifiers from the above list. 
- student@id is not a valid identifier because it has a special character "@" in it.
- 4_id is not a valid identifier because the identifier should not start with a digit. 
- for is invaild because it a reserved word in python. 
</details>

---
13. Predict the output of below code.
```
print("9/2")
```
- a) 4.5
- b) 4.0
- c) 4 
- d) 9/2 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 9/2. 

**Explanation:** 9/2 is a string here.
</details>

---
14. What is the output of below code?
```
i = 4
while i < 7:
       print(i)
       i++
       print(i+2)
       break
``` 

- a) 4 
     6 
- b) 4 
     7 
- c) Error
- d) 5 
     7 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) Error. 

**Explanation:** '++' and '--' symbols are not present in python. To incremenet or decrement a value, we can use assignment operators like += and -= respectively.
</details>
 
---
15. Define Namespace, explain the types of namespaces in python. 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:**  A namespace is a way to provide unique name for each and every object in python. An object can be a variable or a method. There are three types of namespace present in python:
i) **Local Namespace:** the variable names defined in a class, function, loop or in any block of code are comes under local namespace. These variables cannot be accessed by outer Namespace in python. Local namespace can access the global namespace objects and built-in namespace..

ii) **Global Namespace:** the object name that are defined in a main program or in a module comes under global namespace. These are outside any function or block of code. It can access the builtin namespace objects. 

iii) **Built-in Namespace:** it contains the names of built-in methods and variables. It can be a datatype, exceptions and methods like print() & input(). 

Example: 

def student(name):
    new_name ="rohit"   #local namespace
    return new_name

name ="rohan"     #global namespace
print(student(name))  #built-in namespace 

output: rohit 
</details>

---
16. What is the use of Operators in Python & what are its types? 
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** Operators are the symbol that are used to perform opertions on an operands. An operand is a variable or a value on which operator is applied. 
Types of Operators: 
- Arithmetic operators :  [+, -, *, /, %, **, //]
- Assignment operators :  [=, +=, -=, *=, /=, %=, //=, **=] 
- Comparison operators :  [==, !=, >, <, >=, <=]
- Logical operators :  [and, or, not]
- Identity operators :  [is, is not] 
- Membership operators: [in, not in]
- Bitwise operators: [&, |, ^, ~, <<, >>]
  </details>

  ---
17. What is the difference b/w "is" and "==" in python?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** The first difference b/w both is that, 'is' operator is an Identity operator, whereas '==' is an comparison operator. 'is' operator is used to check whether both operands belongs to same location or not in the memory. On the other hands '==' is used to check whether both the operands have same value or not. 
  </details>

 ---
18. Which of the following is not a comparison operator?

- a) ==
- b) >
- c) >> 
- d) <= 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) >>

**Explanation:** >> is a bitwise operator.
  </details>

---
19. Which of the following is an assignment operator?

- a) =
- b) ==
- c) is 
- d) != 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) = 

**Explanation:** option b) and d) are comparison operators and option c) is an identity operator. 
  </details>

---
20. Which is/are not a membership operators?

- a) in 
- b) not in
- c) is 
- d) is not 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct options are c) and d).

**Explanation:** is and is not are identity operators.
  </details>
  
---
21. What is the difference b/w 'and' and 'or' operator?
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** Both "and" and "or" are the logical operators which requires two operands and both return True and False after evaluation. The "and" operator returns True when both the operands are True otherwise False, whereas "or" operator returns True if either operand is True and return False when both operands are False. 
  </details>

---
22. Predict the output for the below code:
```
a = 9
b = 5
  
print(a and b) 
print(a & b) 
```

- a) 5
     5 
- b) 5 
     1 
- c) 9 
     9
- d) 9 
     0       
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b). 

**Explanation:** In 1st print statement logical "and" operator is used, which checks if both operand values are non- zero it will return the value of operand mentioned in last i.e 'b=5'. In 2nd print statement bitwise operator '&' is used, which converts the operands values in binary[ in terms of 0 and 1] and compares and returns 1 if both the bits are 1 otherwise 0. So, a=9 in binary is 1001 and b=5 in binary is 0101. therefore after comparing both operand values bit by bit we get final result as 0001 in binary which is equal to 1 in decimal format. Hence the output (b).
  </details>

---
23. Which of the below code shows the correct representation of taking integer values as user input in Python3?

- a) n = int(input())
- b) n = input() 
- c) n = raw_input()
- d) n = int(raw_input())
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a)

**Explanation:** option b) is used to take user input as string values in python. option c) and d) are the functions of Python2.
  </details>

---
24. Which of the following is the correct way for single line comment in python?

- a) //
- b) @
- c) #
- d) <!...> 
 <details><summary> <b>Show Answer</b> </summary>
**Ans:** correct option is c)
  </details>

---
25. Which of the following is the correct way for multi-line comments in python?

- a) // hi 
      this is abc //
- b) @ hi 
     this is abc @
- c) # hi
     this is abc #
- d) ''' hi 
        this is abc '''
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 
  </details>

---
26. State True or False: "Comments are always required in the code. Without comments the code will not run". 

- a) True
- b) False
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) False.

**Explanation:** Comments are used to make the code easy to understand. It is not mandatory to use comments while writing program.
  </details>

---
27. What is a Ternary operator in Python? Give Example.
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Ternary operator are like if-else statements but with a difference, it allows checking a condition in single line only replacing the multiline if-else block in python. 

For example: 
num1 = 5
num2 = 8 

maximum =  num1 if num1>num2 else num2
print(maximum)  # it returns 8 as output.
  </details>
  
---
28. Predict the output of below code:
```
value =  10//2**3*3+4/2
print(value) 
```
- a) 377 
- b) 5
- c) 5.0 
- d) 2 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 5.0. 

**Explanation:** According to precedence of operators, Exponent(**) has highest precedence in this expression. After that Multiplication(*), Division(/), Floor division(//) all three have same precedence so, it is evaluated from left to right order in an expression. And at last Addition(+). So 2**3 will evaluate first and gives,'8'. Then 10//8 gives 1 because of floor division. Then 1*3 gives '3' and 4/2 gives '2.0'. Hence the final result will come out as 3+2.0 = 5.0
  </details>

---
29. Odd one out: Which of the following statement is incorrect?

- a) '+' is an arithmetic operator.
- b) '+=' is an arithmetic operator.
- c) '>=' is a comparison operator.
- d) 'and' is a logical operator. 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b).

**Explanation:** += is an assignment operator
  </details>

 ---
30. Which of the following is not a logical operator?

- a) and
- b) or
- c) not in
- d) not 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c).

**Explanation:** not in is a membership operator in python.
  </details>
  
---
31. Select the correct expression to reassign a global variable “y” to 30 inside a function reassign() 
```
y = 50
def reassign():
    # your code to assign global y = 30
reassign()
print(y) # it should print 30
```

- a) global y = 30
- b) global var y 
     y = 30
- c) global.y = 30
- d) global y 
     y = 30 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option d) is correct.

**Explanation:** First we have to declare the variable y with global keyword inside the reassign() function, then we can assign the value to y variable. Hence option (d).
  </details>

---
32. What is the data type of print(type(5))

- a) float
- b) integer
- c) int 
- d) number 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c).

**Explanation:** 5 is an integer value in python
  </details>

---
33. What is the output of the following code?
```
x = 50
def fun1():
    x = 25
    print(x)
    
fun1()
print(x) 
```
- a) 25 
     25 
- b) 25 
     50 
- c) NameError
- d) None
 <details><summary> <b>Show Answer</b> </summary>
 
**Ans:** correct option is b) 

**Explanation:** fun1() is called first, so the statements that are there in fun1() will executes first and therefore prints the value of x = 25 in first line in console and then prints 50 in new line after comming out of fun1() function. 
  </details>

---
34. What will be the output of following code?
```
x = 75
def myfunc():
    x = x + 1
    print(x)

myfunc()
print(x)
```
- a) Error 
- b) 76 
- c) 76
     75
- d) 76
     76 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) 

**Explanation:** UnboundLocalError: local variable 'x' referenced before assignment.
  </details>

---
35. Which is not a datatype in Python?

- a) int
- b) float 
- c) char 
- d) bool 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) char 

**Explanation:** In python we can create char by creating a string of length 1. 
  </details>
  
---
36. Which is not a datatype in python?

- a) bool
- b) double
- c) float 
- d) str 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) double.

**Explanation:** In python, every number with decimal values will comes under float class.
  </details>

---
37. Which is a datatype in python?

- a) number
- b) char
- c) complex
- d) double 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) complex

**Explanation:** we can create complex numbers by using complex datatype.
  </details>

---
38. Which of the following is not a correct way of making string in python?

- a) str1 = "hi"
- b) str1 = 'hi'
- c) str1 = '''hi'''
- d) str1 = '"hi"
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) str1 = '"hi" 

**Explanation:** option d) will lead to an SyntaxError.
  </details>

---
39. predict the output of following code. 
```
def func1():
    x = 25
    return x
func1()
print(x)
```
- a) NameError
- b) 25
- c) 0
- d) none of the above 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) NameError. 

**Explanation:** option a) is correct because, in python, it will give a NameError that name "x" is not defined.
  </details>

---
40. Which of the following is not a built-in function in python?

- a) sum()
- b) avg()
- d) all() 
- d) len() 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) avg() 

**Explanation:** there is no function with name avg() in python.
  </details>

---
41. Which of the following is not a built-in function in python?

- a) input()
- b) print()
- c) type()
- d) count()
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) count()

**Explanation:** there is no function with name count() in python.
  </details>

---
42. Which of the following is a built-in function in python?

- a) add()
- b) avg()
- c) count()
- d) max() 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) max() 

**Explanation:** options a), b) and c) are not a built-in function.
  </details>

---
43. What is the output of following code?
```
a = [1, 2]
b = a
b += [3, 4]
print(a)
print(b)
```
- a) [1, 2, 3, 4]
     [1, 2, 3, 4]
- b) [1, 2]
     [1, 2, 3, 4] 
- c) [1, 2, 3, 4]
     [1, 2]
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a)  

**Explanation:** In the above code, both a and b shares the same memory in python, any change made to a will reflects in b and vise-versa.
  </details>

---
44. Predict the output of below code.
```
x = 4
y = 5
if x ** 2 > 16 and y+1 < 10:
    print(x, y)
```
- a) None 
- b) 4 5 
- c) 0 6 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) is correct

**Explanation:** In if statement, first condition is false as 16 greater then 16 is false and 2nd condition is true as 6 less then 10 is true. and operator is used between first and second condition therefore the resultant of true and false is false. Hence the print statement inside if block will not executes.
</details>

---
45. What is the output of below print statement?
```
print(-22//4)
```
- a) -5
- b) 5
- c) -6
- d) 6 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) -6. 
 
**Explanation:** // is a floor division operator, it returns the integer value after division.
</details>

---
46. What are the Bitwise operators present in python?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:**  Bitwise operators first converts the integer to binary and then performs bit-by-bit operations on it. The final result is returned in decimal format. 
In python, there are 6 Bitwise operators:
- & - Bitwise AND
- | - Bitwise OR 
- ~ - Bitwise NOT 
- ^ - Bitwise XOR 
- >> - Bitwise right shift 
- << - Bitwise left shift 
</details>

---
47. What is the use of left shift and right shift operators?
<details><summary> <b>Show Answer</b> </summary>

**Ans:** *Bitwise left shift* operator shifts the bits of the integer number to the left and put 0 on voids right as a result. 
For example: 
x = 4 = 0100 (binary) 
x << 1 = 1000 = 8   # Here it shifts the bit by 1 on the left side.
*Bitwise right shift* operator shifts the bits of integer number to the right and put 0 on voids left as a result. 
For example: 
x = 4 = 0100 (binary)
x >> 1 = 0010 = 2  # Here it shifts the bit by 1 on the right side.
</details>

---
48. What is the output of below code?
```
a = 5
b = 10
print(a | b)
print(b >> 2)
```
- a) 15         
     1              
- b) 15                        
     2                    
- c) 14                   
     1 
- d) 14 
     2 
     
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 

**Explanation:** In both the print statements Bitwise operators are used. In first print statement, bitwise or operator is used which converts values of a and b in binary and returns 1 if either of the bit is 1 else 0. Binary value of 5 is 0101 and binary value of 10 is 1010 so the resultant will be 1111 in binary which is equivalent to 15 in decimal. Therefore 1st print statement prints 15 as output. In 2nd print statement Bitwise right shift operator is used which shifts the bits of a number to the right and fills 0 on voids left. So 1010 is shifted twice to the right as mentioned in print statement and we got the result as 0010 in binary which is equivalent to 2 in decimal. Hence the output 15 and 2.    
</details> 

---
49. Predict the output of the following code.
```
str1 = 'and'
str2 = 'or'
print(str1 and str2) 
```
- a) and 
- b) True
- c) or 
- d) False 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) or

**Explanation:** Because both the values are true and the "and" operator is used in print(), therefore it prints the value of last variable in output screen that is 'or'.
  </details>

---
50. Predict the output of the following code.
```
str1 = 'and'
str2 = 'or'
print(str1 or str2) 
```
- a) and 
- b) True
- c) or 
- d) False 
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** correct option is a) and 

**Explanation:** Because both the values are true and the "or" operator is used in print(), therefore it prints the value of first variable in output screen that is 'and'.
  </details>

---
51. State True or False: "the result of a division operator(/), is always float value".

- a) True
- b) False 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) True is correct. 

**Explanation:** In python, division (/) operator returns the float value whereas, floor division (//) operator returns the int value.
  </details>

---
52. Predict the output.
```
x = 20//4**2-10*2/ 3
print(x)
```
- a) -6.0
- b)  6.67
- c) -5.67
- d) -6.67 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct output is option c) -5.67 

**Explanation:** The operations will be performed based on the precedence of operators. Exponent (**) operator has the highest precedence in this expression, so it evaluates first resulting in 16. After that Multiplication(*), Division(/), Floor division(//) all three have same precedence so, it is evaluated from left to right order in an expression. And at last subtraction(-). So, 20//16 gives 1 and 10*2/3 gives 6.67. At last 1 - 6.67 results in -5.67, hence the answer.
</details>

---
53. What is the output of below mentioned code?
```
x = 6
y = 4
print(y ^ x)
```
- a) 1
- b) 2
- c) 3
- d) 0 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 2.

**Explanation:** Bitwise xor operator is used in the print statement that returns 0 if both the bit is 0 or 1 and returns 1 if either of the bit is 1. 6 in binary is 110 and 4 in binary is 100, therefore after doing xor operation the resultant will be 010, which is 2 in decimal. Hence the option b) is correct.
</details>

---
54. Choose the correct option, for the below code, that will not lead to any error.
```
a, b = 1   # line 1
if (a = b):  # line 2
    c= a+b   # line 3 
    print(c) # line 4
```
- a) change line 1 to a = b =1 and rest all is ok. 
- b) change line 1 to a = b =1 and line 2 to if(a==b): and rest all is ok.
- c) change line 2 to if(a==b): and rest all is ok.
- d) No error in the above code.
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b).
</details>

---
55. What is the output of below print statement?
```
print(3%6) 
```
- a) 2
- b) Value Error
- c) 3 
- d) 0.5 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 3

**Explanation:** Modules (%) operator gives the remainder of two numbers after division. 
  </details>

---
56. Which of the following operators has the highest precedence?

- a) *
- b) &
- c) not
- d) +
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) is correct.

**Explanation:** From the given options, multiplication (*) has the highest precedence and not has the lowest precedence. 
  </details>

---
57. State True or False: "Bitwise shift operators (<<, >>) has lower precedence than Bitwise And(&) operator".

- a) True
- b) False
 <details><summary> <b>Show Answer</b> </summary>
   
**Ans:** option b) False.
  </details>

---
58. What is the output of the following code?
```
b = 8
a = b += 3
print(a)
```
- a) 11
- b) 8
- c) SynatxError
- d) None of the above 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) is correct. 

**Explanation:** In line 2 of the above code, it is invalid to assign the value of b to a at the time of increment.
  </details>
  
---
59. Which of the following statement is not a correct representation of comments in python?

- a) # this is a sample.
- b) """ this is a sample."""
- c) s = ''' this is a sample.'''
- d) ''' this is a sample.'''
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c)

**Explanation:** option c) is a string, rest all are comments in python.
  </details>

---
60. Which of the following code will not lead to SyntaxError in python?

- a) for i in range(4)
         print(i) 
- b) for i in range(4):
         print(i) 
- c) for i range(4):
         print(i) 
- d) fro i in range(4):
         print(i)
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b)

**Explanation:** Semicolon is missing in option a). In option c) in operator is missing. In option d) 'fro' will result in syntax error.
  </details>

---
  
