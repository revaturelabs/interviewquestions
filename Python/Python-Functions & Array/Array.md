## Array

1.What are dynamic Arrays and how is it different from basics Arrays?
 
 <details><summary> <b>Show Answer</b> </summary>
  
- Dynamic arrays (also known as a growable array, resizable array or mutable array ) offer a big improvement, i.e., automatic resizing. 
- An array has a fixed size, so you always have to specify the number of elements your array will hold ahead of time. However, a dynamic array expands as you add more elements to it and you need not determine the size ahead of time.
  
  </details>
  
2.What are the differences between an array and a dictionary?

 <details><summary> <b>Show Answer</b> </summary>
  
**Arrays**:

- An Array is a sorted list of homogeneous elements.
- You have to set the size of an array before using it.
- Arrays can be dynamic in size.
- If you want to increase the array size, you have to use the ReDim statement.
  
**Dictionary**:
  
- A dictionary holds key-value pairs.
- You don't have to set the size for dictionaries.
- There is no dynamic concept for dictionaries.
- You can add an element in dictionary without the need for any statement.
  
  </details>
  
3.How will you access individual elements in an Array? State an Example.

 <details><summary> <b>Show Answer</b> </summary>
  
- In python, index numbers are used for accessing individual elements in an array.
  
```python
c = ["Fan", "Van", "Bat"]
x = c[0]
print(x)
```
  
**Output**:

Fan

<details><summary> <b>Explanation</b> </summary>
  
-In the above program, index numbers are used and the index numbers starts from 0 and ends with n-1
  
  </details>
  </details>
  
4.Write a python program to find the largest and smallest numbers in an array?
  
  <details><summary> <b>Show Answer</b> </summary>
  
  ```python
arr = []
n = int(input("enter size of array : "))
for x in range(n):
    x=int(input("enter element of array : "))
    arr.append(x)
largest = arr[0]
smallest = arr[0]
for i in range(n):
    if arr[i]>largest:
        largest = arr[i]
    if arr[i]<smallest:
        smallest = arr[i]        
print(f"largest element in array is {largest}")
print(f"smallest element in array is {smallest}") 
```

**Output**:
                        
enter size of array : 4

enter element of array : 540545

enter element of array : 304

enter element of array : 2094398

enter element of array : 3298
                        
largest element in array is 2094398
                        
smallest element in array is 304 
                        
 </details>
  
 5.Can a particular index value be used in python?
  
<details><summary> <b>Show Answer</b> </summary>
     
- Yes, the values can be changed using index numbers.

  <details><summary> <b>Example</b> </summary>   
   
```python    
Juice = ["Fanta", "Vicks", "Bovento"]
Juice[1] = "Sprite"
print(Juice)
```
    
**Output**: 
 
['Fanta', 'Sprite', 'Bovento']
  
  </details>
  </details>
  
6.Mention some advantages and disadvantages of Arrays.
  
<details><summary> <b>Show Answer</b> </summary>
  
**Advantages**:

- Multiple elements of Array can be sorted at the same time.
- Using the index, we can access any element in O(1) time.
  
**Disadvantages**:

- You need to specify how many elements are you going to store in your array ahead of time and we can not increase or decrease the size of the Array after creation.
- You have to shift the other elements to fill in or close gaps, which takes worst-case O(n) time.
  
  </details>
  
7.Write a python Program to remove duplicates from Array?
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
def Remove(duplicate):
	final_list = []
	for num in duplicate:
		if num not in final_list:
			final_list.append(num)
	return final_list
duplicate = [2, 4, 10, 20, 5, 2, 20, 4]
print(Remove(duplicate))
```
  
**Output**:
  
[2, 4, 10, 20, 5]  
  
 <details><summary> <b>Explanation</b> </summary> 
   
-We have a numbers of ways to solve these types of problems. We have opted for only one approach.  
-We can use 'not in' in the list to find out the duplicate items. We create a result list and insert only those that are not already 'not in'. 
  
  </details>
  </details>
  
8.Mention some of the built-in methods that you can use on lists/arrays.  
  
<details><summary> <b>Show Answer</b> </summary>
  
- 1.append()	Adds an element at the end of the list
  
- 2.clear()	Removes all the elements from the list
  
- 3.copy()	Returns a copy of the list
  
- 4.count()	Returns the number of elements with the specified value
  
- 5.extend()	Add the elements of a list (or any iterable), to the end of the current list
  
- 6.index()	Returns the index of the first element with the specified value
  
- 7.insert()	Adds an element at the specified position
  
- 8.pop()	Removes the element at the specified position  
  
  </details>
  
9.Write a python code to add an element at the end of array(list).
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
arr = [1,2,3,4,5]
num=int(input("Enter a number to insert in array at end :"))
arr.append(num)
print("Array after inserting",num,"at end",arr)  
```
  
**Output**:
  
Enter a number to insert an array at the end :56
  
Array after inserting 56 at end [1, 2, 3, 4, 5, 56]
  
  </details>
  
10.Does python have built-in support for Arrays?

<details><summary> <b>Show Answer</b> </summary>

- Python does not have built-in support for Arrays.
- But in python, Lists can be used instead of Arrays.

**Example**:

```python
fruits = ['apple', 'banana', 'cherry']
fruits.pop(1)
print(fruits)
```
</details>
  
11.Write a python Program to find a missing number in array?

<details><summary> <b>Show Answer</b> </summary>
  
```python
arr = []
n = int(input("enter size of array : "))
for x in range(n-1):
    x=int(input("enter element of array : "))
    arr.append(x)
sum = (n*(n+1))/2;
sumArr = 0
for i in range(n-1):
    sumArr = sumArr+arr[i];
print(int(sum-sumArr)) 
```
  
**Output**:
  
enter size of array : 3

enter element of array : 1

enter element of array : 2
  
3
  
  </details>
  
12.Which of the following must be used to declare an array?
  
- A.brackets[]
- B.parenthesis()
- C.curly braces{}
- D.pipes ||
  
<details><summary> <b>Show Answer</b> </summary>
  
  **Ans**:
  
  A.brackets[]
  
  </details>
  
13.Elements in an array are accessed _____________
  
- A.randomly
- B.sequentially
- C.exponentially
- D.logarithmically
  
<details><summary> <b>Show Answer</b> </summary>
   
**Ans**:
   
A.randomly
   
<details><summary> <b>Explanation</b> </summary>  
   
- Elements in an array are accessed randomly. In Linked lists, elements are accessed sequentially.

</details>
</details>
  
14.Write a Program to check if two arrays are equal in Python?
  
<details><summary> <b>Show Answer</b> </summary>
  
```python  
arr1=[1,2,3,4,5]
arr2=[1,3,4,5,7]
if len(arr1) == len(arr2):
    print("array is equal")
else:
    print("array is not equal")   
```
  
**Output**:
  
  array is equal
  
</details>
    
15.Write a python program to find the sum of array (list) elements.
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
size=int(input("Enter the number of elements: "))
arr=[]
sum=0
for i in range(0,size):
    elem=int(input("give value for index "+str(i)+": "))
    arr.append(elem)
    sum+=elem
print("sum of array elements = ",sum)
```
  
**Output**:
  
Enter the number of elements: 4

give value for index 0: 678

give value for index 1: 454

give value for index 2: 6

give value for index 3: 433
  
sum of array elements =  1571
  
  </details>
  
16. Write a Python program to get the number of occurrences of a specified element in an array.
  
<details><summary> <b>Show Answer</b> </summary>
  
```python
from array import *
array_num = array('i', [1, 3, 5, 3, 7, 9, 3])
print("array: "+str(array_num))
print("Number of occurrences: "+str(array_num.count(3)))
```
<details><summary> <b>Output</b> </summary>  
  
array: array('i', [1, 3, 5, 3, 7, 9, 3])
  
Number of occurrences: 3
  
  </details>
  </details>
  
17.Write a python program to delete any	given element of an array(list).
  
<details><summary> <b>Show Answer</b> </summary>  

```python
size=int(input("enter the number of elements: "))
arr=[]
for i in range(0,size):
    elem=int(input("give value for index "+str(i)+": "))
    arr.append(elem)
num=int(input("enter a number to remove from array : "))
arr.remove(num)
print("after removing",num,"=",arr)
```
  
**Output**:
 enter the number of elements: 5

give value for index 0: 24

give value for index 1: 2456

give value for index 2: 78

give value for index 3: 567

give value for index 4: 3467

enter a number to remove from array : 78
  
after removing 78 = [24, 2456, 567, 3467] 
  
  </details>
  
18.What would be the output of the following code?
  
```python
arr=[1,2,3,4,5]
arr2 = [i for i in arr1]
print(arr2)
```
  
<details><summary> <b>Show Answer</b> </summary>  

**Output**:
  
arr2 = [i for i in arr1]

NameError: name 'arr1' is not defined
  
</details>
  
19.Write a Python program to create an array that contains six integers ans also to print all the members of the array.
  
<details><summary> <b>Show Answer</b> </summary>    
  
```python
from array import array
my_array = array('i', [10, 20, 30, 40, 50])
for i in my_array:
    print(i)
```
  
  **Output**:
  
  10  
  
  20
  
  30
  
  40
  
  50
  
  </details>
  
20.What will be the output for the following code?
  
> names.append("May")

- A.Would add "names" to the list called "May"
- B.Would remove "May" from the list called "names"
- C.Would add "May" to the list called "names"
- D.Would add "May" to the list called "append"
  
<details><summary> <b>Show Answer</b> </summary>   
  
**Ans**:
  
  C.Would add "May" to the list called "names"
  
  </details>  
  