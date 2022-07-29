
# Python-Flow Control Statements 

1. Does python have a Switch-Case statement?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Python doesn't have a switch case statement, we can use the normal if else statements in it.
</details>

---
2. Does python have a while and do-while loop?
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** In Python, there is no do-while loop present. But we can use while loop in it.
</details>

---
3. Which keyword in python helps in including condition in code?

- a) for
- b) while
- c) if 
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) if. 

**Explanation:** for and while are the looping statements in python.
</details>

---
4. Write the syntax for if-else statement.
<details><summary> <b>Show Answer</b> </summary>

**Ans:** 
  ```
  if(condition):
        .
        .
        Statement 
  else:
        .
        .
        Statement
  ```
</details>

---
5. State True or False: We can write only 1 print statement inside if and else block respectively.

- a) True
- b) False 
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** correct option is b) False.
</details>

---
6. What will be the output of below code?
```
age = 16
if age >=18
   print("Eligible for voting")
else:
   print("Not eligible for voting")
```
- a) Not eligible for voting
- b) Eligible for voting 
- c) Eligible for voting 
   Not eligible for voting 
- d) SyntaxError 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) SyntaxError

**Explanation:** if statements should end with semicolon(:) in python.
</details>

---
7. Predict the output of following code.
```
num=43
if num%2==0:
   print("Number is Even")
else:
   print("Number is Odd")
```
- a) Number is Even
- b) Number is Odd
- c) "Number is Odd"
- d) "Number is Even" 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) Number is Odd 

**Explanation:** if condition becomes false as 43%2 is not equal to 0. Therefore else part executed.
</details>

---
8. Can we write if-else in a single line in python?

- a) Yes
- b) Not possible
- c) we can write it but have to import the module first.
- d) None of the above 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct option is a) Yes 

**Explanation:** Yes, it is possible to write if-else in single line. For example: print("hi") if 10<8 else print("hello")
</details>

 ---
9. Which one of the following is correct way of writing if statement in python?

- a) if (x>4)
- b) if (x=>4)
- c) if (x<4):
- d) if x>4 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) is correct

**Explanation:** all the other options except c) missed semicolon at last.
  </details>

 ---
10. What will be the output of following Python code?
```
a = 15
if a <= 15:
    print("Hi")
if a < 20:
    print("Hello")
else:
    print("Hello-World")
```
- a) Hi 
- b) Hello
- c) Hello-World
- d) Hi
     Hello
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 

**Explanation:** Both if statements result in true, so 'Hi' and 'Hello' will gets printed.
 </details>

---
11. Predict the output.
```
a = 1
b = 0
c = 0
if a+b*c:
    print("Hi-World")
else:
    print("Hello-World")
```
- a) Hi-World
- b) Hello-World 
- c) Hi-World
   Hello-World 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) Hi-World

**Explanation:** "Hi-world" is printed as if condition becomes true.
  </details>

---
12. Predict the output of the below code.
```
a = 1
b = 0
c = 0
if a*b+c:
    print("Hi-World")
else:
    print("Hello-World")
```
- a) Hi-World
- b) Hello-World 
- c) Hi-World
   Hello-World 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) Hello-World

**Explanation:** "Hello-World" is printed as if conditon becomes false.
  </details>
  
---
13. Which of the following is the correct output?
```
a = 1
b = 0
c = 0
if a ^ b:
    print("Hi-World")
else:
    print("Hello-World")
```
- a) Hi-World
- b) Hello-World 
- c) Hi-World
   Hello-World 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) Hi-World

**Explanation:** In if condition Bitwise xor ^ operator is used which returns 1 if either of the bits are 1 else return 0 if both the bits are 0 or 1. Therefore in the above code, 0 and 1 results in 1 which is true in python. Hence 1st print statement executes.
  </details>

---
14. Which of the following is the correct output?
```
a = 10
b = 4
c = 0
if a || b:
    print("Hi-World")
else:
    print("Hello-World")
```
- a) Hi-World
- b) Hello-World 
- c) Hi-World
   Hello-World 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) Error

**Explanation:** There is no || operator present in python. 
  </details>
  
---
15. Predict the output of the following code.
```
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
- a) Hi-World
- b) Hello-World 
- c) Hi-World
   Hello-World 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) Hi-world 

**Explanation:** "Hi-world" is executed because all the if conditions becomes true for the values of 'a' and 'b'. 
  </details>
  
---
16. What is the output of the following for loop?
```
for i in 'Akshay':
   if i == 'h':
      break
   print(i, end=", ")
```
- a) A, k, s, h, a, y
- b) A, k, s, h 
- c) A, k, s,
- d) A, k, s 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) A, k, s, 

**Explanation:** The break statement jumps out of loop when the if condition becomes true i.e when the i value becomes equal to 'h'. So it prints from A till s with comma after each character and comes out of loop and will not print " h, a, y, " of "Akshay" string.
  </details>

---
17. What is the output of the following for loop?
```
for i in 'akshay':
   if i == 'a':
      continue
   print(i, end=", ")
```
- a) k, s, h, a, y
- b) a, k, s, h, a, y,
- c) , k, s, h, y
- d) k, s, h, y,
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) k, s, h, y,

**Explanation:** The continue statement skips the current iteration and moves to next iteration when the condition inside if becomes true. Here whenever the value of i becomes equal to a, it will not print the ith value for that iteration and iterates from next iteration. Hence 'a' is not printed anytime in output screen and we get the output as "k, s, h, y,".
  </details>

---
18. What is the output of the following for loop?
```
for i in 'akshay':
   if i == 'a':
      pass
   print(i, end=", ")
```
- a) k, s, h, a, y
- b) a, k, s, h, a, y,
- c) , k, s, h, y
- d) k, s, h, y,
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) a, k, s, h, a, y,

**Explanation:** The pass statement in python does not do anything and therefore all the characters of string is printed with comma(,) at last of each character.
  </details>

--- 
19. Predict the output of the below code.
```
for num in range(8, 12):
   for i in range(2, num):
       if num%i == 1:
          print(num)
          break
```
- a) 8
     9
     10
     11
- b) 8 
     9 
     10
- c) 9 
     11
- d) None
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a)

**Explanation:** Here in the above code, for each iteration, if the num%i == 1 condition gets true then only it prints the num value and breaks the inner loop and jumps to the outer loop otherwise the i value of inner loop keeps on changing untill i<n or if condition becomes true, whichever comes first. It prints 8 when the value of num and i are 8 and 7 respectively. It prints 9 when the value of num and i are 9 and 2 respectively. It prints 10 when the value of num and i are 10 and 3 respectively. It prints 11 when the value of num and i are 11 and 2 respectively. Hence the correct option is a).   
</details>

---
20. Predict the output of the below code.
```
for num in range(8, 12):
   for i in range(2, num):
       if num%i == 0:
          print(num)
          break
```
- a) 8
     9
     10
     11
- b) 8 
     9 
     10
- c) 9 
     11
- d) None
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is b)

**Explanation:** Here in the above code, for each iteration, if the num%i == 0 condition gets true then only it prints the num value and breaks the inner loop and jumps to the outer loop otherwise the i value of inner loop keeps on changing untill i<n or if condition becomes true, whichever comes first. It prints 8 when the value of num and i are 8 and 2 respectively. It prints 9 when the value of num and i are 9 and 3 respectively. It prints 10 when the value of num and i are 10 and 2 respectively. For num =11, there is no i value that satisfy the if condition therfore it is not printed. Hence the correct option is b).
</details>

---
21. Select which is/are true for "for Loop".

- a) Python’s for loop used to iterates over the items of list, tuple, dictionary, set, or string.
- b) else clause of for loop is executed when the loop terminates abruptly.
- c) else clause of for loop is executed when the loop terminates naturally.
- d) We use for loop when we want to perform a task indefinitely until a particular condition is met.
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option are a) and c). 
  </details>

--- 
22. What is the output of the following code?
```
for i in range(4,-2,-1):
    print(i, end=", ")
```
- a) 4, 3, 2, 1, 0 
- b) 4, 3, 2, 1, 0, 1, 2,
- c) 4, 3, 2, 1, 0, -1,
- d) 4, 1, -1, -3,
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 

**Explanation:** The range() function prints the i value from 4 and decrement by 1 at each iteration till i>-2.
 </details>
  
---
23. What is the output of the below code?
```
numbers = [4, 5]
items = ["Apple", "Orange"]

for x in numbers:
   for y in items:
      print(x+1, y)
```
- a) 5 Apple
     5 Orange
     6 Apple
     6 Orange
- b) 5 Apple
     6 Orange
- c) 5 Apple
     5 Apple
     6 Orange 
     6 Orange
- d) 5 Apple
     6 Orange
     5 Apple
     6 Orange 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) is correct.

**Explanation:** In both the iteration, for each value of x+1 every value of y is printed. 
  </details>

---
24. Which of the following is not used as loop in Python?

- a) for loop
- b) while loop
- c) do-while loop
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) do-while loop
  </details>

---
25. Select the statement which is True regarding loops in Python?

- a) Loops should be ended with keyword "end".
- b) "break" can be used to bring control out of the current loop.
- c) No loop can be used to iterate through the elements of strings.
- d) "continue" is used to continue with the remaining statements inside the loop.
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b).
 </details>

---
26. Predict the output of the following while loop code.
```
i = 2
while True:
    if i%5 == 0:
        break
    print(i)
 
    i + = 1
```
- a) 2
     3
     4
- b) 2
     3 
- c) 2
     3 
     4
     5 
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct option is d)

**Explanation:** There should be no space between + and = in last line of code.
  </details>
  
---
27. Predict the output of the following while loop code.
```
i = 2
while True:
    if i%5 == 0:
        break
    print(i)
 
    i += 1
```
- a) 2
     3
     4
- b) 2
     3 
- c) 2
     3 
     4
     5 
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct option is a)

**Explanation:** it will print 2 3 4 only not 5 because when the i value becomes 5 it satisfies the if condition and therefore the iteration comes out of loop. 
  </details>

---
28) What will be the output of below code?
```
n=8
c=2

while(n):

    if(n>5):
        c=c+n-1
        n=n-1

    else:
        break

print(n)
print(c)
```
- a) 5
     18 
- b) 5
     20
- c) 6
     18
- d) 4 
     20 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 

**Explanation:** It executes the statements present inside if untill the if condition becomes false and it breaks the loop and jumps out of it, having the final value of n as 5 and c as 20.
  </details>

---
29) Predict the output of the below code
```
str1="akshay"
c=0
for i in str1:
   if(i!="a"):
       c=c+1
   else:
       pass
print(c)
```
- a) 2
- b) 3
- c) 4
- d) 5
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is c) 4

**Explanation:** Here the value of c is incremented by 1 whenever the if condition satisfy. 
  </details>

---
30. Predict the output of the below code
```
str1="akshay"
c=0
for i in str1:
   if(i!="a"):
       if(i!="s"):
            c=c+1
   else:
       c=c+1
print(c) 
```
- a) 2
- b) 3
- c) 4
- d) 5
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is d) 5

**Explanation:** Here the value of c is incremented by 1 when both outer and inner if condition becomes true or when outer if condition becomes false. The c value is not incremented when outer if becomes true but inner if becomes false. Hence the output is 5 in this case. 
</details>

---
31. Predict the output of the below code
```
str1="akshay"
c=0
for i in str1:
   if(i!="a"):
       if(i!="s"):
            c=c+1
   else:
       c=c-1
print(c) 
```
- a) 3
- b) 1
- c) 2
- d) 4
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is b) 1 

**Explanation:** Here the value of c is incremented by 1 when both outer and inner if condition becomes true and decremented by 1 when outer if condition becomes false. The c value doesn't change when the outer if condition satisfy but not inner. Hence the output is 1 in this case.
  </details>

---
32. State True or False: "We can use else condition only 1 time in the program".
- a) True
- b) False 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option b) False is correct.
  </details>

---
33. Odd one out: Which of the below code will give different output from others?

- a) for i in [0,1,2,3,4,5]:
      print(i)
- b) for i in [0,1,2,3,4]:
      print(i)
- c) for i in range(0,5):
      print(i)
- d) for i in range(0,5,1):
    print(i)
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is a)

**Explanation:** every option except a) gives output as 0 1 2 3 4, but a) option code gives output as 0 1 2 3 4 5.
  </details>

---
34. How many times will the loop run?
```
i=2
while i:
    i=i-1 
```
- a) 1
- b) 2
- c) 0
- d) infinite 
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option b) is correct 

**Explanation:** For the value of i = 2 and i = 1, the loop runs. Hence 2 times.
  </details>

---
35. How many times will the loop run?
```
i=2
while True:
    i=i-1 
```
- a) 1
- b) 2
- c) 0
- d) infinite 
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option d) is correct 

**Explanation:** As in the above code the while loop condition is True always, so it will run infinite times.
  </details>

---
36. What will be the output of the following code?
```
for i in range(0,2,-1):
    print("Hi")
```
- a) Hi 
- b) Hi
     Hi
- c) No output
- d) Error
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option c) is correct

**Explanation:** The i value never falls in the range of values given, Therefore no output is printed.
  </details>
  
---
37. Which of the following is not valid for loop in Python?

- a) for i in range(len(a)):
- b) for(i=0;i<len(a);i++)
- c) for i in a:
- d) for i in range(len(a),2,-1):
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option b) is correct 
  </details>

---
38. When does the statement in else part written after loop executes?

- a) When loop condition becomes true
- b) when loop condition becomes false 
- c) Else statement is always executed
- d) We cannot write else part without if part. 
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option b) is correct
  </details>

---
39. Predict the output
```
x = "Hello-World"
i = "0"

while i in x:
    print(i, end=" ")
```
- a) Hello-World
- b) H e l l o - W o r l d
- c) No output
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) No output

**Explanation:** In while loop, the value of i never matches with the value of x. Therefore no output is printed in console.
  </details>

---
40. Predict the output of below code
```
x = "apple"

for i in range(len(x)):
    if i%2==0:
        print(i, end=" ")
```
- a) 1 2 3 4
- b) a p p l e
- c) 0 1 2 3 4
- d) 0 2 4
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d)

**Explanation:** The for loop runs till the value of string length, that is till 4 starting from 0. And for each value of i which is divisible by 2 and gives remainder as 0 will gets printed in output screen. Therefore option d) is correct.
  </details>

---
41.  Predict the output of below code
```
x = "apple"

for i in range(len(x)):
    if i%2==0:
        print(x[i], end=" ")
```
- a) a p e
- b) a p p l e
- c) 0 2 4
- d) p l
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is a) 

**Explanation:** Here in the above code, for the index value of i =0, 2 and 4, the character present in that position in string gets printed. Hence the option a) is correct. 
  </details>

--- 
42. Predict the output of below code
```
num = 123
for i in num:
    print(i, end=" ")
```
- a) 1 2 3
- b) 123
- c) Error
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) Error is correct 

**Explanation:**  It will give "TypeError: 'int' object is not iterable". 
  </details>
 
---
43. Predict the output of below code
```
num = '123'
for i in num:
    print(i, end=" ")
```
- a) 1 2 3
- b) 123
- c) Error
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) is correct 

**Explanation:** In the above code, num is a string. So, "123" string will be printed character by character having space in between because of end keyword. 
  </details>

---
44. We can check the condition in which of the following loop?

- a) for loop
- b) do while loop
- c) while loop
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) while loop

**Explanation:** In for loop we cannot check the condition, whereas do while loop is not present in python.
</details>

---
45. What is the output of below code?
```
l =[]
for i in l:
    print(i)
```
- a) []
- b) list
- c) list()
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d)

**Explanation:** Because in the above code 'l' is an empty list, therefore it will print anything.
  </details>

---
46. To break the infinite loop, which keyword we can use in python?

- a) exit
- b) break
- c) continue
- d) pass
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) break
  </details>

---
47. What to put at the last of a loop in python?

- a) semicolon ;
- b) Nothing to put
- c) colon :
- d) comma ,
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option c) colon : is correct
  </details>
 
---
48. Which of the following is/are an infinite loop condition?

- a) while 1:
- b) while True:
- c) while 0:
- d) while -1:
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** options a), b) and d) are correct. 

**Explanation:** While 0: in python means false.
  </details>
 
---
49. State True and False: " In python while(0): and while False: both are same." 

- a) True
- b) False
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option a) True is correct.
  </details>

---
50. State True and False: " range() function in python creates iterable elements."

- a) True
- b) False
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option a) is correct. 
  </details>

---
51. Which is not a decision making statement in python?

- a) if-elif
- b) if-else
- c) for
- d) if
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is c) for.
  </details>

---
52. Predict the output of following python code.
```
list1 = [3 , 2 , 5 , 6 , 0 , 7, 9]
sum1 = 0
sum2 = 0
for elem in list1:
    if (elem % 2 == 0):
        sum1 = sum1 + elem
        continue
    if (elem % 3 == 0):
        sum2 = sum1 + elem
print(sum1 , end=" ")
print(sum2)
```
- a) 8 12
- b) 8 17
- c) 12 8
- d) 8  8
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option b) is correct

**Explanation:** When the elements that are present in a list is divisible by 2 ,the statement present inside first if is exceuted. When the elements that are present in a list is divisible by 3 ,the statement present inside 2nd if is exceuted.  
  </details>

---
53. Predict the output of following python code.
```
list1 = [3 , 2 , 5 , 6 , 0 , 7, 9]
sum1 = 0
sum2 = 0
for elem in list1:
    if (elem % 2 == 0):
        sum1 = sum1 + elem
        continue
    if (elem % 3 == 0):
        sum2 = sum1 + sum2
print(sum1 , end=" ")
print(sum2)
```
- a) 8 12
- b) 8 17
- c) 12 8
- d) 8  8
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** option d) is correct

**Explanation:** When the elements that are present in a list is divisible by 2 ,the statement present inside first if is exceuted. When the elements that are present in a list is divisible by 3 ,the statement present inside 2nd if is exceuted.  
  </details>
  
---
54. Predict the output of following python code.
```
list1 = [3 , 2 , 5 , 6 , 0 , 7, 9]
sum1 = 0
sum2 = 0
for elem in list1:
    if (elem % 2 == 0):
        sum1 = sum2 + elem
        continue
    if (elem % 3 == 0):
        sum2 = sum1 + elem
print(sum1 , end=" ")
print(sum2)
```
- a) 8 12
- b) 12 4
- c) 3 12
- d) 8  8
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) is correct 

**Explanation:** When the elements that are present in a list is divisible by 2 ,the statement present inside first if is exceuted. When the elements that are present in a list is divisible by 3 ,the statement present inside 2nd if is exceuted.  
<details>
  
---
55. Predict the output of the following python code.
```
list1 = [3 , 2 , 5 , 6 , 0 , 7, 9]
sum1 = 0
sum2 = 0
for elem in list1:
    if (elem % 2 == 0):
        sum1 = sum1 + sum2
        continue
    if (elem % 3 == 0):
        sum2 = sum1 + elem
print(sum1 , end=" ")
print(sum2)
```
- a) 9 18
- b) 8 17
- d) 8 18
- c) 9 17
<details><summary> <b>Show Answer</b> </summary>

**Ans:** correct option is a) 9 18

**Explanation:** When the elements that are present in a list is divisible by 2 ,the statement present inside first if is exceuted. When the elements that are present in a list is divisible by 3 ,the statement present inside 2nd if is exceuted.  
  </details>

---
56. What will be the output of below code?
```
if 4+5 < 10:
    print("True")
else:
    print("False")
print ("True")
```
- a) True
   True
- b) True
   False
- c) False
   False
- d) False
   True
<details><summary> <b>Show Answer</b> </summary>

**Ans:** option a) is correct

**Explanation:** The first if condition becomes true, as 9<10, in the above code, so 'True' is printed. Also last 'True' is always printed as it is not a part of if-else statements.
</details>
  
---
57. What will be the output of below code?
```
if 4+5 < 10:
    print("True")
else:
    print("False")
# print ("True")
```
- a) True
   True
- b) True
   False
- c) False
   True
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option d) is correct

**Explanation:** The first if condition becomes true, as 9<10, in the above code, so 'True' is printed. Last print statement is not executed because it is started with # which makes it as comment in the code.
</details>
  
---
58. What will be the output of the following code?
```
if 4+5 < 10 and 5+5>10:
    print("True")
if 8//2*2!=4:
    print("False")
if 10//2**2==25:
    print("True")
print ("True")
```
- a) True
   True
   True
- b) False 
   True
- c) True
- d) True
   False
   True 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b).

**Explanation:** The first and thrid print statements are not executed as if condition becames false. The second print statement is executed as 8!=4 condition becomes true. Also last 'True' is always printed as it is not a part of if-else statements. Hence option b) is correct.
</details>
 
---
59. What will be the output of the following code?
```
if 4+5 < 10 and 5+5>10:
    print("True")
if 8//2*2!=4:
    print("False")
if 10//2**2==2:
    print("True")
print ("True")
```
- a) False
   True
   False
- b) False 
   True 
- c) True
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** correct option is d)

**Explanation:** The first print statement is not executed as if condition becames false. The 2nd and 3rd print statements are executed as if condition for both becomes true. Also last 'True' is always printed as it is not a part of if-else statements. Therefore, it will print "False", "True", "True" each in new line. Hence option d) is correct.
  </details>
 
---
60. What will be the output of the below code for a=5 and b=5?
```
a= int(input())
b= int(input())
if a*b > 10 and a+b<10:
    print("True")
else: 
    print("False")
```
- a) True
- b) False
- c) No Output
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) False.

**Explanation:** The first if condition becomes false as 10<10 is false. Therfore the else part is executed and printed 'False' in console. 
  </details>
 
 ---
61. 


