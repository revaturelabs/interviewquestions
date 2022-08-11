## Boolean

1.What is boolean data type in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> The Python Boolean type is one of Python's built-in data types.  Boolean is a primitive data type that takes either `true` or `false` values. So anything that returns the value `true` or `false` can be considered as a boolean example. Checking some conditions such as `a==b` or `a<b` or `a>b` can be considered as boolean examples.
  
</details>

---
  
2.What is the output of the following code?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

```python  
class truth:
    pass
x=truth()
print(bool(x))
```
  
A. False    
B. True    
C. pass    
D. error    

<details><summary> <b>Show Answer</b> </summary>
  
> Option B. True
  
<details><summary> <b>Explanation</b> </summary>
  
> If the truth method is not defined,the object is considered true. Hence, the output of the code is true.
  
  </details>
  </details>

---
  
3.What is the use of `bool()` function?
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
  
> Python `bool()` function is used to return or convert a value to a Boolean value that is `True` or `False`, using the standard truth testing procedure. 

**Syntax**: 

`bool([x])`
   
- These are the few cases, in which Python’s `bool()` method returns `false`. Except these, all other values return `True`. 

 - If a False value is passed it will print false.
 - If None is passed it will print false.
 - If an empty sequence is passed, such as (), [], ”, etc
 - If Zero is passed in any numeric type, such as 0, 0.0 etc
 - If an empty mapping is passed, such as {}.
 - If Objects of Classes having `__bool__()` or `__len()__` method, returning `0` or `False`
  
  </blockquote>
   </details>

---
  
4.Predict the output of the following code.

```python  
class myclass():
  def __len__(self):
    return 0
myobj = myclass()
print(bool(myobj))
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>
  
> False
  
<details><summary> <b>Explanation</b> </summary>
  
> One or more values or objects in this case evaluates to False, that is if you have an object that is made from a class with a __len__ function, it returns 0 or False.
  
  </details>
  </details>
 
---
  
5.Predict the output of the code.

```python  
print(['hello','morning'][bool('')])
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>
  
> hello
  
<details><summary> <b>Explanation</b> </summary>
  
> The line of codes shown above can be simplified that 'hello' should be printed if the argument is passed to the boolean function that amounts to zero. Else 'morning' will be printed.
  
  </details>
  </details>

---
6.What is the output of the following code?
  
```python  
l=[1,0,2,0,'hello','',[]]
l2=list(filter(bool,l))
print(l2)
```
  
  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
   
> [1,2,'hello']
  
<details><summary> <b>Explanation</b> </summary>
  
> The code shown above `returns` a new list that contains the elements of the list l which do not amount to zero. And, the output is:[1,2,'hello']
  
  </details>
  </details>

---
  
7.Write a program to check whether the given number is even or odd?(take input from user)
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
```python  
n=int(input())
if(n%2==0):
    print("even number")
else:
    print("odd number")
```
  
<details><summary> <b>Explanation</b> </summary>
  
> If the given number(user input) is divisible by 2, it will print the given number as even number. Else, it will print the given number as odd.
  
  </details>
  </details>

---
  
8.What is the output of the following code snippet?
  
```python  
print(not(10>20) and not(10<0))
```                                
A. True    
B. False   
C. Error    
D. No output    
                                
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)                                

<details><summary> <b>Show Answer</b> </summary>
  
> Option A.True
  
<details><summary> <b>Explanation</b> </summary>
  
> The expression `not(10>20)` returns `False`. And, the expression `not(10<0`) returns `False`. The `and` operation between `False` and `False` returns `True`. Hence, the output is `True`.

  </details>
  </details>

---
  
9.What is the output of the following code?
  
```python  
x = 200.60
print(isinstance(x, int))
```
  
A. 200    
B. True   
C. 200.60    
D. False    
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option D.False
  
  </details>

---
  
10.Predict the output of the following code and give the correct code.
  
```python  
def myFunction() :
  return True
myFunction()
```
  
  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
def myFunction() :
  return True
print(myFunction())
```
  
**Output**:
 
> True
  
</details>
 
---
  
11.Mention some advantages of `boolean()` data type?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
i) A `boolean` can be a set to one of the two predefined values, which maps perfectly to what it is used for. You could use an integer as a boolean, but there are many more than two possible integer values. So you'd have to define which integer values should be considered `True` and which should be considered `False`.
  
ii) Advantage of the boolean retrieval model is, it is easy to implement.   
  
iii) It is easy to understand whether the document can be retrieved or not. Users can determine whether the query is too specific or too broad.    

    </blockquote>
  </details>  

 ---
