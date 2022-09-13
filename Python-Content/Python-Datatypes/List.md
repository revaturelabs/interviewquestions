## List

1.What is a list in python? Are list and Array same? If not, how list and array are different?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- List is a part of Collections in python. It has been used to store mulitple items in a single variable. An empty List is created by square brackets [], we can place the elements inside that `[]` separated by commas.     
- No, list and array both are not same in python. Although, list and array both are used to store elements in it, but still some differences are there:   
    
- i) List consists of elements of different types, for eg. [1, 2, "a", 4.5], whereas Array can store elements of same type only. 
- ii) List is a built-in data type in python and so anyone can directly use it, whereas for using Array we have to `import` the array module. 
- iii) List is preferred for shorter sequence of data items, and on the other hand, arrays are preferred for data items of longer sequence. 
- iv) We can print List without any loop, but for printing elements of an array a loop is required.
    
    </blockquote>
</details>

---

2.What are the methods frequently used when dealing with list in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- [For this type of question, only tell the methods that you have used while working with List because the interviewer might ask the next question based on your response.]   
   
- List provides different kinds of built-in methods that anyone can use for list manipulations. Some of the methods are mentioned below:  
    
i) `append()` : it is used to add element to the end of a list.  
    
ii) `insert()` : it is used to add element at a given position/index in a list.  
    
iii) `extends()` : it is used to add the specified list elements or any iterable to the end of list.  
    
iv) `count()` : this will return the number of times an item appears in a list.  
    
v) `clear()` : it is used to remove all elements from a list.  
    
vi) `index()` : it will return the lowest index of mentioned item.  
    
vii) `pop()` : by default,it removes and return the last element from the list. If index is specified, it removes the item present in that index.  
  
viii) `remove()` :  it removes the specified element from a list.  
  
ix) `sort()` : it will sort the list in ascending or descending order.  
    
x) `reverse()` : it reverses the order of elements present in a list.  
   
    </blockquote>
</details>  

---

3. In pyhton, how can you differentiate `pop()`, `remove()` and `del` in list?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>  
  <blockquote>
  
i) `del` is a keyword, whereas `remove()` and `pop()` is a method of a list.  
    
ii) For deleting element, `del` and `pop()` uses the index, whereas `remove()` uses value as parameter.  
   
iii) `del` and `remove()` does not return any value, whereas `pop()` returns the removed value.   
    
iv) `del` can delete any number of values from a list or a whole list at a time, whereas `pop()` and `remove()` deletes only one value from a list.  
    
For example: 
  
```python
l = [1, 3 , 3, 2, 4, 7]
del l[0]   # deletes the 0th index value
print(l)
l.pop()   # removes the last element by default
print(l)
l.remove(3) # removes the element mentioned
print(l)
```
    
**Output**:
  
> [3, 3, 2, 4, 7]
  
> [3, 3, 2, 4]
  
> [3, 2, 4]

</blockquote>
    </details>

---

4.How can you differentiate `append()`, `insert()` and `extend()` methods of a list in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> `append()` can be used when we have to add or insert single element in the end of list.  
    
> `insert()` can be used to add an element at desired postion in a list by passing index value along with element as a parameter.  
    
> `extend()` can be used when we have to add more then one element at the end of a list. It appends each element of an iterable such as list and tuple.  
  
For example: 

```python
l = [1, 3, 3, 2]
l.append(4)   # adding element at last
print(l)
l.insert(2,7)  # index, element
print(l)
l.extend([6,9,5])  # passing another list
print(l)
```
  
**Output**: 
  
> [1, 3, 3, 2, 4]
  
> [1, 3, 7, 3, 2, 4]
  
> [1, 3, 7, 3, 2, 4, 6, 9, 5]

  </details>

---

5.What do you mean by mutable object? what are the mutable and immutable datatypes in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Mutable means we can change the values of an object and it will directly reflect back to original object. 
> Immutable means we can't change the values of an object and it will directly reflect back to original object. 
> In python, Str (character/string), Tuple, Int, Float, Bool are of immutable type, whereas List, Set and Dict are of Mutable type.
  
</details>

---

6.How to iterate over the list of elements? Give a code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- To iterate over list in python, we can use any loop.
  
```python  
# Code using for loop
l = [1, 3, 3, 2]
for i in l:
   print(i) 
```
  
```python  
# Code using for loop and range() 
l = [1, 3, 3, 2]
for i in range(len(l)):
   print(l[i]) 
```
  
```python  
# Code using while loop
l = [1, 3, 3, 2]
i = 0
while i<len(l):
   print(l[i])
   i += 1 
```
                
```python                
# Code using list comprehension
l = [1, 3, 3, 2]
[ print(i) for i in l]
```

                </blockquote>
                </details>

---
  
7.What is the output of the following code?
  
```python  
lst=[11, 100, 101, 999, 1001]
answer_1=lst[-1]
print(answer_1)
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>
  
> 1001
  
<details><summary> <b>Explanation</b> </summary>
  
> In this code, we are using negative indexing, and so we are getting last element from that list.
  
  </details>
  </details>

---
  
8.What is the use of `copy()` method? What happens if we directly assign one list to another using `=` operator?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>  
  <blockquote>
  
- `copy()` is a built-in method present in the list. Using `copy()`, we can shallow copy a list.  
  
**Example**: 

```python  
l1 = [1, 2, 3, 4]
l2 = l1.copy()
print(l2)   # output: [1, 2, 3, 4]
```
  
- If we use the `=` operator instead of `copy()` to copy 1st list elements to 2nd list, the output will be same when we print 2nd list. But the actual difference occurs when we try to `add, delete or change` a value in original list, and the new list that we have created using `copy()` method will not change and vise-versa. Whereas the changes will reflect to new list if we used '=' operator for copying the elements. Let's see one example to understand easily. 

```python  
original = [1, 3, 3, 2]
new = original
new_list = original.copy()
print(original)   # output: [1, 3, 3, 2]
print(new)        # output: [1, 3, 3, 2]
print(new_list)   # output: [1, 3, 3, 2]

new.append(4)
print(original)    # output: [1, 3, 3, 2, 4]
print(new)         # output: [1, 3, 3, 2, 4]

new_list.append(5)
print(new_list)    # output: [1, 3, 3, 2, 5]
print(original)    # output: [1, 3, 3, 2, 4]
```
  
    </blockquote>
  </details>

---
  
9.Why do we get `Indexerror: list index out of range` error in python?
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
- Sometimes when we try to get the element by index which is not valid i.e the element that we want to access doesn't have index position in the list, then we get the `Indexerror: list index out of range` error. 
  
**For example**: 
  
```python  
l = [2, 4]
for i in range(len(l)+1)
    print(l[i])  
``` 
  
- Here, we are trying to get the 3rd element from the list whose index value doesn't exist. So, we will get index out of range error in this code after printing 2, 4 in new line. 

  </blockquote>
  </details>

--- 

10.Predict the output of following code.

```python  
list1 = ['saran', 'shalini', 'sandy']
print (max(list1))
```
  
A.saran  
B.shan 
C.sandy  
D.error 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> Option b) shan. 
  
<details><summary> <b>Explanation</b> </summary>
  
> `max()` function in python returns the element with the highest value from an iterable. But if the elements of iterable[list, tuple, etc] are strings, then it compares alphabetically and returns the maximum from them. In this code, the first letter of each word is 's', so it checks the 2nd letter of each word and as 'h' is a greater value then 'a', it returns shan as output.

  </details>
  </details>

---

11.Predict the output of following code.

```python  
list1 = ["Hello", [2, 5, 7, 9, 3]]
print(list1[0][-3])
print(list1[1][2])
```
 
A. e    
&emsp;7   
B. H   
&emsp;5  
C. l   
&emsp;5  
D. l  
&emsp;7   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option d) l and 7 
  
<details><summary> <b>Explanation</b> </summary>
  
> First, print statement picks the 0th index value which is "Hello", after that for -3 index iterates over hello from the last and prints the 'l' letter from "Hello". The 2nd print statement picks the 1st index value from the list which itself is a list of [2, 5, 7, 9, 3] values, after that it finds the element at index 2 from that list and print its value which is 7. Hence, l and 7 will be printed.
  
  </details>
  </details>

---

12.Select all the correct options to join two Lists in Python.

```python  
list1 = [2, 5, 7, 9, 3]
list2 = [1, 4, 6, 8] 
```

A. new = list1 + list2    
B. new = extend(list1, list2)    
C. new = list1.extend(list2)    
D. new.extend(list1, list2)    

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Options are (a) and (c). 
  
<details><summary> <b>Explanation</b> </summary>
  
> `extend()` method takes 1 argument as parameter and not 2, so options b) and d) are eliminated there. The '+' operator can also be used to join two list in python.
  
  </details>
  </details>

---

13.Write a program to return duplicate/ repeated items from the List. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

```python  
list1 = [2, 5, 2, 5, 3]
dup =[]
new =[]
for i in list1:
    if i not in new:  
        new.append(i)
    else:
        dup.append(i)
print(dup)   # output: [2, 5]
```
  </details>
  
---

14.Write a program to remove duplicate items from the List.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
```python  
list1 = [2, 5, 2, 5, 3]
new =[]
for i in list1:
    if i not in new:
        new.append(i)
print(new)   # output: [2, 5, 3]
```
  </details>

---

15.Write a program to remove all consecutive duplicates from the list.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

```python
def solve(l):
      seen = -1
      ans = []
      for i in l:
         if i != seen:
            ans.append(i)
            seen = i
      return ans
list1 = [2,5,2,5,5,5]
print(solve(list1))	
```
  </details>
  
---

16.Write a program to find the frequency of elements in a list.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
```python  
list1 = ['apple', 'orange', 'apple', 'mango', 'apple', 'orange']
freq = {}   
for i in list1:
   if i in freq:
      freq[i] += 1
   else:
      freq[i] = 1
print(freq)
```
  </details>

---

17.How to take user input in the List in Python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> There are many ways through which one can take input from user in list:

**Example 1**:  
    
```python  
lst = []
n = int(input("Enter number of elements : "))
for i in range(n):
    elmt = int(input())
    lst.append(elmt) 
print(lst)
```
    
**Example 2 [Using map]**:  
    
```python  
n = int(input("Enter number of elements : "))
lst = list(map(int,input().split()))[:n]
print(lst)
```
      
**Example 3 [Using List Comprehension]**   
    
```python  
lst = []  
lst = [int(i) for i in input().split()]
print(lst) 
```
  </details>
 
---

18.What is the output of the following list operation?

```python
sampleList = [10, 20, 30, 40, 50]
print(sampleList[-2])
print(sampleList[-4:-1])
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. 40  
&emsp;[20,30,40]  
B. error  
C. lst index out of range  
D. No output  

<details><summary> <b>Show Answer</b> </summary>
  
> option A.  40  
  
<details><summary> <b>Explanation</b> </summary>
  
> Use the range of negative indexes to search from the end of the list.
  
  </details>
  </details>

---

19.Write a python program to find the max,min number from the list(take input from user).

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

  <details><summary> <b>Show Answer</b> </summary>
    
```python
listlang = []
numbers = int(input('enter the number of items in list '))
for num in range(numbers):
    item = int(input('Entered number '))
    listlang.append(item)
print('entered list =',listlang)
print("Max number = :", max(listlang), "\nMin number :", min(listlang))
```
  </details>
 
---

20.What is the output of the following list operation?

```python  
aList = [10, 20, 30, 40, 50, 60, 70, 80]
print(aList[2:5])
print(aList[:4])
print(aList[3:])
```
  
A. [20, 30, 40, 50]    
&emsp;[10, 20, 30, 40]  
&emsp;[30, 40, 50, 60, 70, 80]  
B. [30, 40, 50]  
&emsp;[10, 20, 30, 40]  
&emsp;[40, 50, 60, 70, 80]  
C. [10, 20, 30, 40]  
&emsp;[50, 60, 70, 80]  
D. None of the above  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option B
  
<details><summary> <b>Explanation</b> </summary>
  
> Python list collection is ordered and changeable. The list also allows duplicate members. To get a sublist out of the list, we need to specify the range of indexes.  To get a sublist, we need to specify where to start and where to end the range.

> Syntax: list[start:end] If start is missing it takes 0 as the starting index

  </details>
  </details>
  
---
21.Predict the output of the following code.(Removing the last item of a list)

```python  
lst=[55, 777, 54, 6, 76, 101, 1, 2, 8679, 123, 99]
#  Type your code here.
print(lst)
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
<details><summary> <b>Hint</b> </summary>
  
> Use the `.remove()` method and inside parenthesis, we can type the value you’d like to remove.
 
  </details>
  
**Solution**:
  
```python  
lst=[55, 777, 54, 6, 76, 101, 1, 2, 8679, 123, 99]
#  Type your code here.
lst.remove(99)
print(lst)
```
  
**Output**:
  
[55, 777, 54, 6, 76, 101, 1, 2, 8679, 123]
  
  </details>
  
---

22.Write a python program to generate a number list between two ranges.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

```python  
listnum = list(range(1, 7))
print ("list between two range : " ,listnum)
```
  
**Output**:
  
> list between two range :  [1, 2, 3, 4, 5, 6]
  
  </details>

---
23.What will be the correct output for the following code?
 
```python  
listnum = [45,67,12,14,56,87]
list =listnum[::-1]
print (list)
```
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> [87, 56, 14, 12, 67, 45]
  
<details><summary> <b>Explanation</b> </summary>
  
> Here,we are using negative indexing to reverse a list.
  
  </details>
  </details>

--- 

24.Can you write a piece of code for intersecting two list?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
```python  
listnum = ['C++',2,3,6,7,5,'C#']
listnum1 = ['C++',5,6,7,'C#']
intersect_res = [item for item in listnum if item in listnum1]
print('intersect of two list =',intersect_res)
  ```
  
**Output**:
  
> intersect of two list = ['C++', 6, 7, 5, 'C#']
  </details>

---

25.What is the output of the following code?

```python
my_list = ["Hello", "Python"]
print("-".join(my_list))
```
  
A. HelloPython-  
B. Hello-Python  
C. -HelloPython  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b
  
<details><summary> <b>Explanation</b> </summary>

> The join() method will join all items in a list into a string, using a hyphen character as a separator.
  
  </details>
  </details>

---
