## Boolean

1.What is boolean data type in python?

<details><summary> <b>Show Answer</b> </summary>
  
- The Python Boolean type is one of Python's built-in data types.  Boolean is a primitive data type that takes either "true" or "false" values. So anything that returns the value "true" or "false" can be considered as a boolean example. Checking some conditions such as "a==b" or "a<b" or "a>b" can be considered as boolean examples.
  
  </details>

2.What will be the output of the following code?

```python  
class truth:
    pass
x=truth()
print(bool(x))
```
  
- A.False
- B.True
- C.pass
- D.error

<details><summary> <b>Show Answer</b> </summary>
  
B.True
  
<details><summary> <b>Explanation</b> </summary>
  
> If the truth method is not defined,the object is considered true.Hence the output of the code is true.
  
  </details>
  </details>

3.What is the use of bool() function?

<details><summary> <b>Show Answer</b> </summary>
  
- Python bool() function is used to return or convert a value to a Boolean value i.e., True or False, using the standard truth testing procedure. 

**Syntax**: 
  
> bool([x])

These are the few cases, in which Python’s bool() method returns false.Except these all other values return True. 

- If a False value is passed.
- If None is passed.
- If an empty sequence is passed, such as (), [], ”, etc
- If Zero is passed in any numeric type, such as 0, 0.0 etc
- If an empty mapping is passed, such as {}.
- If Objects of Classes having __bool__() or __len()__ method, returning 0 or False
  
  </details>

4.Predict the output of the following code?

```python  
class myclass():
  def __len__(self):
    return 0
myobj = myclass()
print(bool(myobj))
```
  
<details><summary> <b>Show Answer</b> </summary>
  
False
  
<details><summary> <b>Explanation</b> </summary>
  
- One more value, or object in this case, evaluates to False, and that is if you have an object that is made from a class with a __len__ function that returns 0 or False.
  
  </details>
  </details>
  
5.Predict the output of the code?

```python  
print(['hello','morning'][bool('')])
```
  
<details><summary> <b>Show Answer</b> </summary>
  
> hello
  
<details><summary> <b>Explanation</b> </summary>
  
 - The line of code shown above can be simplified to state that 'hello' should be printed if the argument passed to the boolean function amounts to zero, else 'morning' will be printed.
  
  </details>
  </details>

6.What will be the output of the following code?
  
```python  
l=[1,0,2,0,'hello','',[]]
l2=list(filter(bool,l))
print(l2)
```
  
<details><summary> <b>Show Answer</b> </summary>
  
  **Output**:
  
[1,2,'hello']
  
<details><summary> <b>Explanation</b> </summary>
  
> The code shown above returns a new list containing only those elements of the list l which do not amount to zero.Hence the output is:[1,2,'hello']
  
  </details>
  </details>

7.Write a program to check whether the given number is even or odd?(take input from user)

<details><summary> <b>Show Answer</b> </summary>
  
```python  
n=int(input())
if(n%2==0):
    print("even number")
else:
    print("odd number")
```
  
<details><summary> <b>Explanation</b> </summary>
  
> If the given number(user input) is divisible by 2 it will print the given number is even number. if it's not it will print the given number is odd.
  
  </details>
  </details>

8.What will be output of the following code snippet?
  
```python  
print(not(10>20) and not(10<0))
```                                
- A.True
- B.False
- C.Error
- D.No output

<details><summary> <b>Show Answer</b> </summary>
  
**Output**:
  
A.True
  
<details><summary> <b>Explanation</b> </summary>
  
- The expression not(10>20) returns False.The expression not(10<0) returns False.The and operation between false and false returns True.Hence the output is True.

  </details>
  </details>

9.What will be the output of the following code?
  
```python  
x = 200.60
print(isinstance(x, int))
```
  
- A.200
- B.True
- C.200.60
- D.False

<details><summary> <b>Show Answer</b> </summary>
  
**Option**: D.False
  
  </details>

10.Predict the output of the following code and give me the correct code?
  
```python  
def myFunction() :
  return True
myFunction()
```
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
def myFunction() :
  return True
print(myFunction())
```
  
**Output**:
 
True
  
  </details>
  
11.Can you tell me some advantages of boolean() data type?
  
<details><summary> <b>Show Answer</b> </summary>
  
- A boolean can be set to one of only two predefined values, which maps perfectly to what it is used for. You could use an integer as a boolean, but there are many more than two possible integer values. So you'd have to define which integer values should be considered “true” and which should be considered “false”.
- Advantages of the boolean retrieval model It is easy to implement.
- It is easy to understand why the document is retrieved or not. Users can determine whether the query is too specific or too broad. 
  
  </details>  