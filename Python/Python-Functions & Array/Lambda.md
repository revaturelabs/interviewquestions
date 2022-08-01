## Lambda
1.What is lambda function?

<details><summary> <b>Show Answer</b> </summary>
  
Lambda function is an anonymous function is a function that is defined without a name.Lambda functions can have any number of arguments but only one expression. The expression is evaluated and returned. Lambda functions can be used wherever function objects are required.

Syntax:
   lambda arguments: expression
  
**Example**:
  
```python
double = lambda x: x * 2
print(double(5))
```
**Output**:
10
</details>

2.Look at the code carefully and Predict the output of the following code.

<details><summary> <b>Show Answer</b> </summary>
  
```python
list = [1, 5, 4, 6, 8, 11, 3, 12]
new_list = list(filter(lambda x: (x%2 == 0) ,list))
print(new_list)
```
**Output**:
  
new_list = list(filter(lambda x: (x%2 == 0) ,list))
  
TypeError: 'list' object is not callable
  
</details>

3.Debug the following code and give the correct code?

```python
#Type your answer here.
i=6
L=
print(L(i))
```
<details><summary> <b>Hint</b> </summary>
  You can start your function as following: lambda x: 
  
And then write your statement after the colon (:)
  
  </details> 

<details><summary> <b>Show Answer</b> </summary>
  
```python
i=6
L = lambda x: x+2
print(L(i))
```
**Output**:
  
  8
</details>

4.What is the difference between function and lambda function?


<details><summary> <b>Show Answer</b> </summary>
The functionality of both functions and lambda functions are similar. But, we need to write some extra code in normal functions compared to lambda functions for the same functionality.

Lambda functions come in handy when there is a single expression.
  
**Example**:
  
  *Function*:
  
```python
def absolute_value(num):
    if num >= 0:
        return num
    else:
        return -num
print(absolute_value(2))
print(absolute_value(-4))
```
  
 *Lambda function*: 
  
```python
i=6
L = lambda x: x+2
print(L(i))
```
  
</details>

5.What will be the output of the following code?

```python
i=10
f = lambda z z*11
print(f(i))
```

<details><summary> <b>Show Answer</b> </summary>
  
  **Output**:
  
  SyntaxError: bad input on line 4
  Because in line 4 ':' is missing
  
 **Ans**:
  
  ```python
i=9
f = lambda z: z*11
print(f(i))
```
**Output**:
  
  99
  
 </details>
 
 6.What will be the output of the following code?
 
 ```python
min = (lambda x, y: x if x < y else y)
print(min(101*70, 102*8))
```
- A.827
- B.999
- C.816
- D.797

<details><summary> <b>Show Answer</b> </summary>
  
**Ans**:
  
C.816
  
</details>

7.Does lambda contains return statements?

- A.True
- B.False

<details><summary> <b>Show Answer</b> </summary>
  
**Ans**:
  
  B.False

<details><summary> <b>Explanation</b> </summary>  
  
 lambda definition does not include a return statement. it always contains an expression which is returned. Also note that we can put a lambda definition anywhere a function is expected. We don’t have to assign it to a variable at all.

  </details>
  </details>
  
8.Write a lambda function which takes two arguments: a and b and returns the multiplication of them: a*b.

<details><summary> <b>Show Answer</b> </summary>
  
```python
i=int(input())
j=int(input())
f = lambda a, b: a*b
print(f(i, j))
```
  
**Output**:
  
  i=5
  j=6
  30
  It's based on user input's.
  
  </details>
  
9.Write a python program to sort the given list in ascending order with lambda function.(Get input from user)
  
  <details><summary> <b>Show Answer</b> </summary>
  
  ```python
lst=list(map(int,input().strip().split()))
lst = sorted(lst, key=lambda x: x)
print(lst)
```
  
**Output**:
  
8 10 4 23 666
  
[4, 8, 10, 23, 666]
</details>

10.What will be the output of the following code?

```python
y = 6
z = lambda x: x ** y
print (z(7))
```
<details><summary> <b>Show Answer</b> </summary>
  
**Ans**:
  
117649
  
<details><summary> <b>Explanation</b> </summary>  
  
The lambda keyword creates an anonymous function. The x is a parameter, that is passed to the lambda function. The parameter is followed by a colon character. The code next to the colon is the expression that is executed, when the lambda function is called. The lambda function is assigned to the z variable.
The lambda function is executed. The number 7 is passed to the anonymous function and it returns 117649 as the result. Note that z is not a name for this function. It is only a variable to which the anonymous function was assigned.
  </details>
  </details>
  
11.What is map and filter in Python?

<details><summary> <b>Show Answer</b> </summary>
  
1.The map function takes each item in a given iterable and and includes all of them in a new lazy iterable, transforming each item along the way.
  
2.The filter function doesn't transform the items, but it's selectively picks out which items it should include in the new lazy iterable.

**Syntax of map() function**:
  
     map(function,sequence)
  
where,
- function – function argument responsible for applied on each element of the sequence
- sequence – Sequence argument can be anything like list, tuple, string  
  
**Syntax of filter() function**:
  
     filter(funtion, sequence)
  
where,
- function – Function argument is responsible for performing condition checking.
- sequence – Sequence argument can be anything like list, tuple, string
</details>

12.What is use of reduce() function in python?

<details><summary> <b>Show Answer</b> </summary>
  
In Python, the reduce() function is used to minimize sequence elements into a single value by applying the specified condition. The reduce() function is present in the functools module; hence, we need to import it using the import statement before using it.

**Syntax of reduce() function**:
  
   reduce(function, sequence)
  
  </details>
  
13.What is difference between filter and reduce in python?
  
<details><summary> <b>Show Answer</b> </summary>
  
**Filter**:
   - filter is used to spliting the data.
   - Function is a boolean condition that rejects all the items in the iterable object that are not true.
   - Syntax: filter(function,iterable object)
   - Example: All the even numbers from a list.
**Reduce**:
   - reduce function used to single output operations.
   - Breaks down the entire process of the applying the function into pair-wise operations.
   - Syntax: reduce(function,iterable object)
   - Example: Product of all the items in the list.
  
</details>

14.Write a python program to filter the negative numbers from the list.

<details><summary> <b>Show Answer</b> </summary>

```python  
lst1=list(map(int,input().strip().split()))
lst = list(filter(lambda x: x<0, lst1))
print(lst)
print(lst)
```
     
**Output**:
[12, -1, 9, 8, -0.5, -0.2, -100]
                                 
[-1, -0.5, -0.2, -100]
</details>
  
15.What will be the output of the following code?
  
```python
str1="Welcome to my new world"
lst = list(filter(lambda x: True if x.lower() in "aeiou" else False, str1))
print(lst)
```
  
<details><summary> <b>Show Answer</b> </summary>
  
**Ans**:
  
  ['e', 'o', 'e', 'o', 'e', 'o']
  
<details><summary> <b>Explanation</b> </summary>
 
  - You can use filter(f, list). Make sure your function is a logical statement to facilitate the filtering process.
  - Since filter() function will return an iterator, you can use list() function to convert it to a proper Python list.
  - To create a lambda function with logical expression you can implement something like this:

    **lambda x: True if x in ….else False**
  </details>
  </details>

16.Write a python program using map() and filter() functions add the values below 80. 
  
<details><summary> <b>Show Answer</b> </summary>  
  
 ```python
lst1=[1000, 50, 600, 700, 5000, 90000, 175]
lst2 = list(map(lambda x: x+2000, filter(lambda x: x<800, lst1)))
print(lst2)
```
<details><summary> <b>Explanation</b> </summary> 
  
- You can use filter(f, list). Make sure your function is a logical statement to facilitate the filtering process.
- Since filter() function will return an iterator, you can use list() function to convert it to a proper Python list.
- You can use filter() function inside your map() function:
  
  map(f, list)
  
  where list is a filter() function itself:
  
  map(f1, filter(f2,list))
  
</details>
 </details>                                                        
                                 
17.What will be the output of the following code?

```python
lst1=[22, 100, 19, 13, 11, 1, 4, 66]
lst2 = list(filter(lambda x: x%2 == 1, lst1))
print(lst2)
```
<details><summary> <b>Show Answer</b> </summary> 
  
[19, 13, 11, 1]

</details>

<details><summary> <b>Explanation</b> </summary>
  
  - You can use filter(f, list). Make sure your function is a logical statement to facilitate the filtering process.
  - Since filter() function will return an iterator, you can use list() function to convert it to a proper Python list.
</details>

18.What is the output of the following code?

```python
import functools
l=[1, 2, 3, 4, 5]
m=functools.reduce(lambda x, y:x if x>y else y, l)
print(m)
```
<details><summary> <b>Show Answer</b> </summary>
  
5 
  </details>
  
<details><summary> <b>Explanation</b> </summary>
The code shown above can be used to find the maximum of the elements from the given list. In the above code, this operation is achieved by using the programming tool reduce. Hence the output of the code shown above is 5.

</details>

