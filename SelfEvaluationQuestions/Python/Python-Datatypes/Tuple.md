## Tuple

1.What is a Tuple? How tuple is different from list in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
- `Tuple` is an immutable datatype in python which is used to store elements and is separated by comma inside parentheses (). To create an empty `tuple`, we can use `()` in python. 
 
**Example**: 
 
  i) `tuple1 =()`  
 
  ii) `tuple1 = (1, 2, 3)`

- In python, both `list` and `tuple` looks similar as they both store any type of data in it but there are some difference that makes both of them distinct. Some of the following differences are:

 i) `Lists` in python are mutable, whereas tuples are immutable.
  
 ii) We can use `append()` or `insert()` to add elements to a list, but in `tuple`, `append` and `insert` are not present.
  
 iii) We can use `pop()` or `remove()` to delete an element from the `list`, but in `tuple` we cannot delete elements.
  
 iv) Use `list` when you have to perform manipulation operations on data such as insertion or deletion. Use tuple when you have frequent access to the elements without changing. 
  
 v) Using [] brackets, we can create `list`. Using `()`, we can create `tuple` in python. 

</blockquote>
  </details>

---

2.What are the built-in methods in `tuple`?
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
 
- `Tuple` has 2 built-in methods in python:
 
 i) `count()` - it returns the count of specified element in tuple.
 
 ii) `index()` - it searches the specified value in a `tuple` and returns the position of that element to where it is found. 

</blockquote>
  </details>

---

3.How to add an element to a `Tuple`?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> We cannot add elements to a `tuple` directly since it is immutable. But if we convert the `tuple` to a `list`, we can add element to that list using `append()` or `extend()` method. After adding, we can convert that list back to `tuple`. 
 
**Example**:
 
 ```python
tuple1 =(1, 2, 3)
list1 =list(tuple1)
list1.append(4)
tuple1 =tuple(list1)
print(tuple1)    # output: (1, 2, 3, 4)
print(type(tuple1))  # output: <class 'tuple'>
```

 </details>
 
 ---
 
4. If `Tuple` does not have sort method to sort the elements compared to `List`, then how will you sort the elements of a `tuple` in python?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
  
- There are few ways by which we can sort the elements of `tuple`,

 ```python
# Using sorted() method and type conversion 
tuple1 = (12, 4, 7, 21, 34, 2, 16)  
sorted_tuple= tuple(sorted(tuple1))  
print(sorted_tuple)  # output: (2, 4, 7, 12, 16, 21, 34)
```
 
```python 
# Using sort() method of list and type conversion 
tuple1 = (12, 4, 7 , 21, 34, 2, 16)  
lst = list(tuple1)
lst.sort()   
print(tuple(lst))  # output: (2, 4, 7, 12, 16, 21, 34) 
```
 
 </blockquote>
  </details>
 
 ---

5.How to sort the elements of a `tuple` in descending order?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
  
> By passing `reverse = True` as argument of `sort()` method, we can sort the elements of a `list`. After that, using type conversion, we can convert the `list` to `tuple`. 

```python 
# Code 
tuple1 = (12, 4, 7 , 21, 34, 2, 16)  
lst = list(tuple1)
lst.sort(reverse =True)   
print(tuple(lst))
```
 
 </details>
 
 ---

6.How to join two `tuples` together in Python?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
  
> We can use the `+` operator to join two `tuples` together. 
  
**Example**:
  
```python  
t1 = (12, 4, 7 , 21)
t2 = (34, 2, 16)
print(t1 + t2)  # output: (12, 4, 7, 21, 34, 2, 16)
```
  
 </details>
 
 ---

7.How to print the reverse order of elements in a `tuple`? 
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
 
> Using `reverse()` method of `list` and type conversion, we can achieve our task. 
 
**Example**:
 
```python 
t1 =(1, 5, 3, 9, 2)
lst = list(t1)
lst.reverse()
print(tuple(lst))   # output: (2, 9, 3, 5, 1)
```
 
 </details>
 
 ---
 
8.What is the output of below code:

 ```python
tuple1 = (10, 20, 30, 40, 50)
tuple1.pop(2)
print(tuple1) 
```
 
 A.(10, 20, 40, 50)
 
 B.(10, 30, 40, 50)
 
 C.30 
 
 D.Error 
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> Option  d) Error. 
 
<details><summary> <b>Explanation</b> </summary>
  
> The reason is `Tuple` is immutable in python i.e we cannot change the values of a `tuple`.

 </details>
 </details>
 
 ---

9.Select the correct statements out of the following regarding `Tuple`. 
 
 A.We can delete the element from a `tuple` but we cannot update elements of the tuple.
 
 B.We cannot delete the `tuple`.
 
 C.We cannot delete the items from the `tuple`.
 
 D.We cannot update items of the `tuple`. 
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 <details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- Options c) and d) both are correct.
  
- We can delete the whole tuple by using `del` keyword so option b) is incorrect. Option a) is incorrect because we cannot `remove`, `add` or `update` items of a `tuple`. 

</blockquote>
   </details>
 
 ---
 
10.State `True` or `False`: A Python `tuple` can also be created without using parentheses.

 A.True 
 
 B.False
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
- Option  A.`True`
 
<details><summary> <b>Explanation</b> </summary> 
 
- We can create a `tuple` without parentheses but we have to seperate each element of tuple by comma ','. 
 
 </blockquote>
  </details>
 
 </details>
 
 ---

11.What is the output of following code?
 
```python 
tuple1 = (10,)
print(tuple1 * 3)
```
 
 A.`TypeError`
 
 B.30)
 
 C.(10, 10, 10)
 
 D.(10, 20, 30) 
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
  
- Option C.(10, 10, 10) 

<details><summary> <b>Explanation</b> </summary>
  
- We can use `*` operator to repeat the values of `tuple` as n number of times.

 </blockquote>
 </details>
 </details>
 
 ---
 
12.What is the type of the following code?
 
 ```python
tuple1 = ("andro")
print(type(tuple1))
```

 A.`list` 
 
 B.`tuple`
 
 C.`array`
 
 D.`str`
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> Option D.str
 
<details><summary> <b>Explanation</b> </summary>
 
> The answer of above code is not `tuple` because in python if you have to create a `tuple` of single item, you need to add a comma after the item. 
> If you missed the comma, the python will treat it as a string type (str class). 

 </details>
 </details>
 
 ---
 
13.Predict the output of the code.
 
```python
tuple1 = 25, 20, 15, 10, 5 
a, b, c, d, e = tuple1
print(b)
```
 
 A.25
 
 B.20
 
 C.15
 
 D.5 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 
 
<details><summary> <b>Show Answer</b> </summary> 
 
> Option B.20
 
<details><summary> <b>Explanation</b> </summary>
 
> In python, we can create a `tuple` without parentheses. Also `tuple` unpacking is possible.
 
 </details>
 </details>
 
 ---
 
14.Debug the code and give the correct code.(To print the third element of the tuple.)

```python 
tuple=(11, 100, 101, 999, 1001)
#Type your answer here.
answer_1=
print(answer_1)
```
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>
 
 ```python
tuple=(11, 100, 101, 999, 1001)
answer_1=tuple[2]
print(answer_1)
```
 
<details><summary> <b>Explanation</b> </summary>
 
> 0,1,2 … Third element is index 2: [2]

</details>
 </details>
 
 ---
 
15.What will be the output of the following code?

```python 
Tuple1="yellow",20,"Red"
a,b,c=Tuple1
print(b)
```
 
 A.('yellow',20,'red')
 
 B.`TypeError`
 
 C.`yellow`
 
 D.No output
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> Option C.yellow
 
<details><summary> <b>Explanation</b> </summary>
 
> The `tuple` unpacking is also possible.
 
 </details>
 </details>
 
 ---

16.Write a python program to sort list of `tuples` by second element.
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
```python
 
listtuple= [('C#',1), ('Go',7), ('Basic',8), ('Python',60)]
print('original list of tuples =\n',listtuple)
listtuple.sort(key = lambda item:item[1])
print('after sorting by second item=\n',listtuple)
```
 
**Output**:
 
original list of tuples =
 [('C#', 1), ('Go', 7), ('Basic', 8), ('Python', 60)]
 
after sorting by second item=
 [('C#', 1), ('Go', 7), ('Basic', 8), ('Python', 60)]

<details><summary> <b>Explanation</b> </summary>
 
- This is the one way of approach only, you can do in your way.
 
 </blockquote>
  </details>
 </details>
 
 ---

17.Debug the code and give the output of the following code?
(sum of all the numbers in the tuple)
 
```python
tuple=(45,2,90,5,36,65)
output=
print("sum of the tuple:",output)
```
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Hint</b> </summary>
 
> `sum()` function will calculate the total sum inside the numbers of your `tuple`.
 
</details>
 
<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
```python
tuple=(45,2,90,5,36,65)
output=sum(tuple)
print("sum of the tuple:",output)
```
 
**Output**:
 
sum of the tuple: 243

  </blockquote>
 </details>
 
 ---

18.Write program to swap two `tuples` in python.

**Sample tuple**:
 
```python
tuple1=(11,22)
tuple2=(99,88)
```
 
Expected output:
 
tuple1:(99,88)
 
tuple2:(11,22)
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>

```python
tuple1=(11,22)
tuple2=(99,88)
tuple1,tuple2=tuple2,tuple1
print('tuple1 value after swapping:',tuple1)
print('tuple1 value after swapping:',tuple2)
```
 
**Output**:
 
tuple1 value after swapping: (99, 88)
  
tuple1 value after swapping: (11, 22)

 </blockquote>
  </details>
 
 ---
 
19.What is the output of the following `tuple` operation

```python 
aTuple = (100, 200, 300, 400, 500)
aTuple.pop(2)
print(aTuple)
```
 
 A.(100,200,400,500)
 
 B.(100,300,400,500)
 
 C.`AttributeError`
 
 D.No output
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> Option C.`AttributeError`

<details><summary> <b>Explanation</b> </summary>
 
> A `tuple` is immutable. Once a `tuple` is created, you cannot remove its items, but you can delete the tuple completely. If you try to remove the item from the tuple, you will receive an `AttributeError: tuple` object has no attribute `pop`.

 </details>
 </details>
 
 ---
 
20.A Python `tuple` can also be created without using parentheses.

 A.`False`
 
 B.`True`
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> Option B.`True`

<details><summary> <b>Explanation</b> </summary>
 
> A tuple can also be created without using parentheses. It is called tuple packing.

**Example**:
 
```python
tuple = "Yarn", 20, "Rabbit"
print(tuple)
```
 
 </details>
 </details>
 
 ---
 
21.Write a program to convert two `list` to `dictionary` in python?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
```python 
Team=["Training","Dev","Sales","Finance"]
Members=[38,50,33,79]
Office=dict(zip(Team,Members))
print(Office)
````
 
**Output**:
 
{'Training': 38, 'Dev': 50, 'Sales': 33, 'Finance': 79}
 
<details><summary> <b>Explanation</b> </summary>
 
> To convert two `list` to `dictionary` in python we can use `zip()` method.
 
 </details>
 </details>
 
 ---
 

22.What is the type of the following variable?

```python
Tuple=("Engineer")
print(type(Tuple))
```
 
 A.`tuple`
 
 B.`str`
 
 C.array
 
 D.`list`
 
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>
 
- Option B.`str`

<details><summary> <b>Explanation</b> </summary>
 
- To create a `tuple` with a single item, you need to add a comma after the item. Otherwise, Python will not recognize the variable as a `tuple`, and it will treat it as a string type.
 
**Example**:
 
 ```python
Tuple=("Engineer")
print(type(Tuple))
Tuple1=("Software",)
print(type(Tuple1))
 ```
 
**Output**:
 
<class 'str'>
 
<class 'tuple'>
 
 </blockquote>
 </details>
 </details>
 
 ---
 

23.How will you find the duplicate tuple in list of `tuple`.
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 <blockquote>

```python 
Tuple= [('Python',5),('Java',3),('C#', 1), ('JS', 2), ('C#', 1), ('JS', 2),('React',1)] 
#finding the duplicate tuple
Output_tuple = list(set([item for item in Tuple if Tuple.count(item) > 1])) 
print(Output_tuple)
```
 
**Output**:
 
[('JS', 2), ('C#', 1)]
  
 <details><summary> <b>Explanation</b> </summary>
  
 >To find duplicate elements from `tuple`,convert the `tuple` into `set`.Because, `set` won't allows duplicates.
  
  </blockquote>
  </details>
 </details>
 
 ---

24.Counts the number of occurrences of item 50 from a tuple.
Sample tuple:
 
`tuple = (50, 10, 60, 70, 50,67,89,160,145,67,50)`
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
```python
tuple = (50, 10, 60, 70, 50,67,89,160,145,67,50)
print(tuple.count(50))
```
 
**Output**:
 
3
 
<details><summary> <b>Explanation</b> </summary>
 
> To count the number of occurrences we used the `count()` method of a `tuple`.

 </details>
 </details>
 
 ---
 
25.Choose the correct way to access value 20 from the following `tuple`.

> Tuple = ("Software",[10, 20, 30], (5, 15, 25))

 A.Tuple[1:2][1]
 
 B.Tuple[1:2](1)
 
 C.Tuple[1:2][1]
 
 D.Tuple[1][1]

<details><summary> <b>Show Answer</b> </summary>
 
> Option C.Tuple[1:2][1]
 
<details><summary> <b>Explanation</b> </summary>
 
 > If we want to access the value 20 from `tuple` we can use `slicing`.

 </details>
 </details>
 
 ---
 
 
