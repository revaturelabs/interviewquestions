
# Python-Flow Control Statements 

1. Does python have a Switch-Case statement?
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Python doesn't have a switch case statement, we can use the normal if else statements in it.
</details>

---
2. Does python have a while and do-while loop?
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** In Python, there is no do-while loop present. But we can use while loop in it.
</details>

---
3. Which keyword in python helps in including condition in code?
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
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
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
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
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
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
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
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
![EASY](https://github.com/revaturelabs/JavaFSQuestions/blob/main/Java/JavaIntro/JavaFeatures/Easy%20(2).jpg)
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
          print(num, end=" ")
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
          print(num, end=" ")
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
</details>
  
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
61. What is the output of this while loop code?
```
i = -5
j = 1

while i<0:
    i += j
    j +=1
print(j)
``` 
- a) 8
- b) 6
- c) 4
- d) 3
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 4.

**Explanation:** The while loop will run until i becomes equal to or greater then 0. Whenever the while loop condition becomes true it will first add the values of i and j and stores it in i variable. then it will increment the value of j by 1. When the while condition becomes false it will print the final value of j in the console. 
  </details>
  
---
62. What should be the condition for a while loop to run?

- a) While something equals something
- b) While something is greater than something
- c) While something is True
- d) All of these
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option d) is correct.
  </details>
  
---
63. What will be the output of the following code?
```
a = ['ABC', 'XYZ']  
for i in a:  
    i.lower() 
print(i)  
```
- a) XYZ
- b) ABC
- c) abc
- d) xyz
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) XYZ

**Explanation:** The print statement is outside the for loop therefore only the last value of i is printed. 
  </details>

--- 
64. What will be the output of the following code?
```
a = ['ABC', 'XYZ']  
for i in a:  
    s= i.lower() 
print(s)  
```
- a) XYZ
- b) ABC
- c) abc
- d) xyz
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) xyz

**Explanation:** Here, 's' is storing the lowercase values of list 'a'. The print statement is outside the for loop therefore only the last value of 's' is printed. 
  </details>
  
---
65. What will be the output of the following code?
```
a = ['ABC', 'XYZ']  
for i in a:  
    s= i.lower() 
print(a)  
```
- a) ['abc','xyz']
- b) ['ABC', 'XYZ']
- c) ['abc']
- d) ['XYZ']
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct option is b)

**Explanation:** Print statement have 'a' which is a list, so the whole list is printed in the console without modification. 
  </details>

---
66. Predict the output of the following code.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    if(i < 6) and (i%2!=0):
        print(i+1, end =" ")
    else:
        print(i-1, end =" ")
```
- a) 5 3 8 2 7 8 2
- b) 3 1 6 4 7 8 2
- c) 4 2 6 2 8 8 2
- d) 3 1 7 3 9 9 1
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Correct option is b) 

**Explanation:** The if conditon becomes true for the values 3 and 1 and false for the rest of the values present in list1. Therefore when if becomes true it increments the value of i by 1 and decrements the value of i by 1 when if becomes false.
 </details>

---
67. Predict the output of the following code.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    if(i < 6) and (i%2=0):
        print(i+1, end =" ")
    else:
        print(i-1, end =" ")
```
- a) 5 3 8 2 7 8 2
- b) 3 1 6 4 7 8 2
- c) 4 2 6 2 8 8 2
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** Option d) is correct. 

**Explanation:** The above code will result in syntax error because of the if condition i%2=0, as here = is an assignment operator not comparison which is not allowed in if condition.
  </details>

---
68. Predict the output of the following code.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    if(i < 6) and (i%2==0):
        print(i+1, end =" ")
    else:
        print(i-1, end =" ")
```
- a) 5 3 8 2 7 8 2
- b) 5 1 6 4 7 8 0
- c) 5 3 6 2 7 8 0
- d) 4 2 6 2 8 8 2 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) is correct

**Explanation:** The if conditon becomes true for the values 4 and 2 and false for the rest of the values present in list1. Therefore when if becomes true it increments the value of i by 1 and decrements the value of i by 1 when if becomes false.
  </details>
 
---
69. Write your own logic inside the for loop to print the values 4, 2 and 8 in the output screen.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    # write your logic here
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:**
``` 
if(i%2==0):
     print(i)
```    

**Explanation:** i%2==0 is the condition for printing even numbers. Therefore it will print 4, 2 and 8 in console.
  </details>

---
70. Write your own logic inside the for loop to print the values 7, 3, 9 and 1 in the output screen.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    # write your logic here
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** 
```
if(i%2!=0):
     print(i)
```     

**Explanation:** i%2!=0 is the condition for printing odd numbers. Therefore it will print 7, 3, 9 and 1 in console.
  </details>

---
71. Write your own logic inside the for loop to print the values 7 and 9 in the output screen.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    # write your logic here
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** 
```
if i%2!=0 and i>3:
     print(i)
```    

**Explanation:** i%2!=0 is the condition for printing odd numbers and i> 3 will take the value of i which is greater then 3 and there is a logical 'and' operator between both the if conditions. Therefore when both the conditions becomes true only then the print statement inside if will executes. Hence, we get the final result as 7 and 9. 
  </details>

--- 
72. Write your own logic inside the for loop to print the values 4, 2, 7, 8 and 9 in the output screen.
```
list1 = [4, 2, 7, 3, 8, 9, 1]  
for i in list1:  
    # write your logic here
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** 
```
if i%2==0 or i>3:
     print(i)
```

**Explanation:** i%2==0 is the condition for printing even numbers and i> 3 will take the value of i which is greater then 3 and there is a logical 'or' operator between both the if conditions. Therefore when either of the conditions becomes true only then the print statement inside if will executes. Hence, we get the final result as 4, 2, 7, 8, and 9. 
  </details>

---
73. The order of execution of the statements in a python program is known as ______.

- a) central flow
- b) selection
- c) flow of control
- d) iteration
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) flow of control.
  </details>

---
74. Which loop in python is used to run for infinite times when required?

- a) for 
- b) while
- c) do-while
- d) both a) and b)
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correc option is b) while loop.
  </details>

--- 
75. What is a nested if in python?

- a) if condition inside for loop.
- b) if condition inside another if condition
- c) if condition with elif and else block
- d) None of the above
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option b) is correct.
  </details>

---
76. Predict the output of the below code.
```
var = 5
if 5!=var:
 print("Hello")
else :
 print("Hi")
```
- a) Error
- b) Hello
- c) Hi
- d) Nothing will be printed
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option c) is correct.

**Explanation:** The if condition becomes false as 5!= var is false. Hence Hi is printed.
  </details>

---
77. Predict the output of the below code.
```
for = 5
if 5!=for:
 print("Hello")
else :
 print("Hi")
```
- a) Error
- b) Hello
- c) Hi
- d) Nothing will be printed
<details><summary> <b>Show Answer</b> </summary>
 
**Ans:** option a) is correct.

**Explanation:** The above code will result in syntax error as 'for' is a keyword in python and we cannot use keywords as variable or a class. 
  </details>

 ---
78. Which of the following statement is not assigning a numerical value 5 to variable var, if the original value of var is 0? 

- a) var = 5
- b) var += 5
- c) var *=5
- d) None
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) var *=5

**Explanation:** var *=5 will store the value 0 to var not 5, hence wrong.
  </details>

 ---
79. Jake knows how to create a variable and assign a integer value to it, but he don't know how to display all the values (greater then -1) which are lesser then that particular variable's value. Help Jake by writing the logic for it in the given spaces below.
```
n = 6
___#write the logic here___
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** 
```
for i in range(0,n):
    print(i)
```

**Explanation:** The for loop in python helps in running the loop for the range given. The above code will print the values from 0 till 5, not including 6.
  </details>

---
80. Predict the output of the following code.
```
for i in range(6, -3, -2):
    print(i, end=", ")
```
- a) 6, 3, 0, -3
- b) 6 3 0 -3
- c) 6, 4, 2, 0, -2
- d) error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c)

**Explanation:** The for loop in the above code will first take 6 as intial value and for each iteration it decrements the value by -2. Therefore it will print the values in reverse order untill -3. 
  </details>

---
81. What will be the output of the following code? 
```
age =50
if age > 45:
    if age > 65:
        print('old')
    else:
        print('middle')
else:
    print('young')
```
- a) old
- b) middle
- c) young
- d) None
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option b) is correct

**Explanation:** For age=50, the first if condition becomes true, but nested if becomes false resulting in executing the nested else statement.
  </details>
  
---
82. Which operators are used to combine clauses within an if statement?

- a) not
- b) or
- c) and
- d) Both b) and c)
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option d) is correct
  </details>

---
83. Predict the output of the following code.
```
i=0
while i<3:
  print(i, end=" ")
  i=i+1
else:
  print(4)
```
- a) 0 1 2 
- b) 0 1 2 4
- c) 0 1 2 3 4
- d) 1 2 3 4
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b)

**Explanation:** In python, we can write else part with for and while loop. So first while loop while executes untill it becomes false that is when i value becomes 3. After that else statement gets executed. 
</details>

---
84. Predict the output of the following code.
```
i=5
while(i<=8):
  print("i", end=" ")
  i+=1 
```
- a) 5 6 7 8
- b) 5 6 7
- c) i i i i
- d) i i i
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 

**Explanation:** Here in the print statement in while loop, 'i' is printed 4 times as it is of string type not int type.
</details>

--- 
85. Predict the output of the following code.
```
i=5
while(i<=8):
  print("i", end=" ")
  i+=1 
```
- a) 5 6 7 8
- b) 5 6 7
- c) i i i i
- d) i i i
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) 

**Explanation:** Here in the print statement in while loop, the value of 'i' is printed 4 times starting from 5 till 8.
</details>

---
86. For what value of n, in the below code, will execute the if block?
```
if n>=7 and n<8:
    print("Hello")
else:
    print("Hi")
```
- a) 6
- b) 7
- c) 8
- d) 10
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option b) is correct

**Explanation:** The only value of n that makes the if condition true is 7. 
</details>

---
87. Rohit wants to write a code that will print the table of any number given by user at run time. He got stuck after writing the 1st line, help him to write the whole code in provides space. 
```
number = int(input("Enter any number"))

# write your logic here 
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** 
```
for i in range(1,11):
    print(number,"*",i,"=",number*i)
```
</details>

---
88. Which condition will force to jump out of a loop when a number becomes 0 in python?

- a) if(number == 0)
- b) while(number!=0)
- c) elif( number==0)
- d) None
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 
</details>

---
89. Predict the output of the below code.
```
for i in range(2,10):   
    if (i%2==0):
        continue
        print(i, end=" ")
```
- a) 2 4 6 8 10
- b) 3 5 7 9
- c) 2 4 6 8
- d) Nothing is printed 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** option d) is correct.

**Explanation:** Whenever the if condition becomes true, it skips the below print statement because of continue. As there is no else part in the above code, the execution will again goes to for loop whenever if becomes false.
</details>

---
90. Predict the output of the below code.
```
for i in range(1,6):   
    if (i%2==0):
        break
        print(i, end=" ")
    print(i)
```
- a) 1
- b) 2
- c) 1 3 5
- d) 2 4 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) 1 

**Explanation:** The for loop will starts from 1 and goes till 5. In if block break statement is used which break the flow and jumps out of it whenever the if condition becomes true. So for i = 1, it prints the value as it is outside if block, then for i=2 the if condition becames true resulting in executing the break statement. 
</details>

---
91. What will be the output of following code?
```
for i in range(1,6):   
    if (i%2==0):
        break
        print(i)
print(i)
```
- a) 1
- b) 2
- c) 1 3 5
- d) 2 4 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 2 

**Explanation:** The for loop will starts from 1 and goes till 5. In if block break statement is used which break the flow and jumps out of it whenever the if condition becomes true. So for i = 1 it does not print anything as there is no print statement inside for loop after if block, then for i=2 the if condition becames true resulting in executing the break statement. Therefore the current value of i that is 2 is printed by print statement outside for loop.
</details>

---
92. What should be the arguments of a range() function that will print the values 10, 14 and 18 for the below code given?
```
for i in range(_,_,_):
    print(i)
```
- a) 10, 18, 4
- b) 11, 19, 4
- c) 10, 19, 4
- d) 10, 18, -4 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 

**Explanation:** For printing 10, 14 and 18 the range should starts with 10 and goes till the number greater then 18, that is till 19 with steps having 4. 
</details>

---
93. What will be the output of the following code?
```
for i in range(4):
    for j in range(3):
        if(i>3):
            print("Hello")
```
- a) It prints "Hello" three times.
- b) It prints "Hello" four times.
- c) It gives an error.
- d) it prints nothing.
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 

**Explanation:** The 'i' value in the for loop never goes beyond 3 so if condition will never becomes true. Hence no output is printed in console.
</details>

---
94. What will be the output of the below code?
```
matrix = [[1, 2, 3, 4],
[4, 5, 6, 7],
[8, 9, 10, 11],
[12, 13, 14, 15]]
for i in range(0, 4): 
    print(matrix[i][1], end=" ")
```
- a) 1 4 8 12
- b) 1 5 10 15
- c) 2 5 9 13
- d) 2 5 10 14 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 

**Explanation:** The print statement always chooses the 1st value of every list from the matrix. 
</details>

---
95. What will be the output of the below code?
```
matrix = [[1, 2, 3, 4],
[4, 5, 6, 7],
[8, 9, 10, 11],
[12, 13, 14, 15]]
for i in range(0, 4): 
    print(matrix[i][i], end=" ")
```
- a) 1 4 8 12
- b) 1 5 10 15
- c) 2 5 9 13
- d) 2 5 10 14 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is b) 

**Explanation:** The print statement prints the ith value from each list, one by one, starting from 0 till 3.
</details>

---
96. What will be the output of the below code?
```
matrix = [[1, 2, 3, 4],
[4, 5, 6, 7],
[8, 9, 10, 11],
[12, 13, 14, 15]]
for i in range(0, 4, 2): 
    print(matrix[i][i], end=" ")
```
- a) 1 4 8 12
- b) 1 5 10 
- c) 2 10
- d) 1 10  
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d)

**Explanation:** The print statement prints the ith value from 1st and 3rd list because in for loop the interval given is 2.
</details>

---
97. Predict the output.
```
if(10//2**2==2):
   print("hello")
else: 
   print("hi")
```
- a) hello
- b) hi
- c) hello hi
- d) Error 
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is a) hello

**Explanation:** The if condition becomes true as the following expression 10//2**2 is equal to 2 satisfied. Hence 'hello' is printed.
</details>

---
98. Predict the output of the following code.
```
list1 = [1, 2]
for i in list1:
    list1.append(i)
print(list1)
```
- a) [1, 2]
- b) [1, 2, 2, 1]
- c) [1, 2, 1, 2]
- d) None of the mentioned
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) 

**Explanation:** The for loop does not terminate as new element is being added to the list in each iteration. 
</details>

---
99. What will be the output of the below code?
```
list1 = [1, 2]
list2 = []
for i in list1:
    list2.append(i)
print(list1+list2)
```
- a) [1, 2]
- b) [1, 2, 2, 1]
- c) [1, 2, 1, 2]
- d) None of the mentioned
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is c) 

**Explanation:** The append() function will add all the values of list1 to an empty list list2. Then both list gets concatenate together through + operator. 
</details>

---
100. Predict the output of the following code. 
```
list1 = [1, 2]
list2 = []
for i in list1:
    list2.append(i)
print(list1+(list2+1))
```
- a) [1, 2, 1, 2]
- b) [1, 2, 2, 3]
- c) [1, 2, 3, 2] 
- d) Error
<details><summary> <b>Show Answer</b> </summary>
  
**Ans:** correct option is d) Error.

**Explanation:** The above code throws the "TypeError: can only concatenate list (not "int") to list". 
</details>

---




