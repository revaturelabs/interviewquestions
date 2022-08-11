## Set

1.What is the difference between list and set?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>
	
 `List:[]`
    - List is Mutable and ordered/indexed.
    - List allows duplicate values.
    - It can store any data type like str,list,set,tuple,int and dictionary.
	
 `Set:{}`
    - Set is Mutable and unordered.
    - Set does not allow duplicate values.
    - Dictionary key can be int,str,and tuple, only values can be of any data type int,str,list,tuple,set and dictionary.
		
</blockquote>
</details>

---

2.How will you add list of items into a Set?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	<blockquote>
	
- In python, we can use the `update()` method of a set, to add list of items into a set.
	
**Example**:

```python
sample_set = {"Yellow", "Orange", "Black"}
sample_list = ["Blue", "Green", "Red"]
sample_set.update(sample_list)
print(sample_set)
```
	
**Output**:
	
> {'Green', 'Yellow', 'Red', 'Black', 'Orange', 'Blue'}
	
</blockquote>
		</details>	

---

3.How will you return a new set of identical items from these two sets?

```python
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> For that, we have `Intersction()` method of a set.
	
```python
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
print(set1.intersection(set2))
```
	
**Output**:
	
{40,50,60}
	
</details>

---

4.What is the output of the following code?

```python
set1={8,9}
set2={5,6}
set3=set()
i=0
j=0
for i in set1:
	for j in set2:
		set3.add((i,j))
		i+=1
		j+=1
print(set3)
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> {(9, 5), (9, 6), (10, 6), (8, 5)}

</details>

---

5.How will you remove items 10, 20, 30 from the set at once?

> set1 = {10, 20, 30, 40, 50}

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> In python, we use `difference_update()` method of a set.

```python	
s1 = {10, 20, 30, 40, 50}
s1.difference_update({10, 20, 30})
print(1)
```
	
**Output**:
	
40,50

</details>

---

6.Write a program to Check if two sets have any elements in common. If yes, display the common elements.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

```python	
set1 = {10, 20, 30, 40, 50}
set2 = {60, 70, 80, 90, 10}
if set1.isdisjoint(set2):
  print("Two sets have no items in common")
else:
  print("Two sets have items in common")
  print(set1.intersection(set2))
```
	
**Output**:
	
> Two sets have items in common
	
>  {10}

</details>

---

7.What are the methods you frequently use when dealing with set in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	<blockquote>
	
 - Set provides different kinds of built-in methods that anyone can use for set manipulations. Some of these methods are mentioned below:
	
 i) `add()`: it is used to add an element to the set
	
 ii) `clear()`: it removes all the elements from the set
	
 iii) `copy()`: it returns a copy of the set
	
 iv) `difference()`: it returns a set containing the difference between two or more sets
	
 v) `difference_update()`: it removes the items in this set that are also included in another, specified set
	
 vi) `discard()`: it removes the specified item
	
 vii)`intersection()`: it returns a set, that is the intersection of two other sets
	
 viii)`issubset()`:it returns whether another set contains this set or not
	
 ix)`issuperset()`:it returns whether this set contains another set or not
	
 x)`pop()`:it removes an element from the set
	
xi)`remove()`: it removes the specified element
	
xii)`union()`:it return a set containing the union of sets
	
xiii)`update()`: Update the set with the union of this set and others

</blockquote>
</details>

---
	
8.What is the difference between `pop()` and `remove()`?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	<blockquote>
	
- `pop()`:
   - it is used to remove an element from the set.
	
**Example**:
	
```python
fruits = {"apple", "banana", "cherry"}
x = fruits.pop()
print(x)
```
	
**Output**:
	
apple(it removes random element from set)
	
 `remove()`:
   - it is used to remove the specified element.
	
**example**:
	
```python	
fruits = {"apple", "banana", "cherry"}
fruits.remove("cherry")
print(fruits)
```
	
**Output**:
	
{"apple","banana"}
		
		</blockquote>
</details>

---

9.How to iterate over the set of elements? Write a code for that.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	<blockquote>
	
- In python, to iterate over set, we can use any loop.
	
i)using for loop

```python
set={"a","b","c"}
for x in set:
 print(x)
```
	
**Output**:
	
b
	
c
	
a

</blockquote>
		</details>

---
	
10.What is the use of `copy()` method? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> The `copy()` method is used to copies the set.
	
**Example**:
	
```python	
fruits = {"ant", "bat", "cat"}
x = fruits.copy()
print(x)
```
	
**Output**:
	
> {'ant','bat','cat'}
	
</details>

---

11.How will you zip 2 sets together?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> We can zip, but the values from each set may not be joined in order.
	
**Example**:
	
```python	
z = zip({1,2,3},{'a','b','c'})
print(list(z))
```
	
**Output**:
	
> [(1, 'b'), (2, 'c'), (3, 'a')]
	
</details>

---

12.Can a set be accessed by index?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> `No`. Set can't be accessed by index, and if your trying to access a set by index, it will throw an error.
	
**example**:

```python
s={1,2,3}
print(s[0])
```
	
**Output**:
	
TypeError: 'set' object is not subscriptable
	
</details>

---

13.Can you Update a set to equal the intersection of it and another set.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> In python, `intersection_update()` updates the first set to be equal to the intersection.
	
**Example**:
	
```python	
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1.intersection_update(s2)
print(s1)
```
	
**Output**:
	
> {4,5}

> This can also be done with the `&=` operator.

```python	
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1 $= s2
print(s1)
```
	
**Output**:
	
> {4,5}

</details>

---

14.Can you remove the intersection of a 2nd set from the 1st set.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> In python, `difference_update()` removes the intersection from the first set.
	
**Example**:
	
```python	
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1.difference_update(s2)
print(s1)
```
	
**Output**:
	
> {1, 2, 3}

- The operator **-=** also works.

```python	
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1-=(s2)
print(s1)
```
	
**Output**:
	
{1,2,3}
	
</details>

---

15.Write a Python program to create a `shallow copy` of sets.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
	
> Note : `Shallow copy` is a bit-wise copy of an object. A new object is created that has an exact copy of the values in the original object.

```python
s1 = set(["Red", "Green"])
s2 = set(["Green", "Red"])
#A shallow copy
setr = s1.copy()
print(setr)
```
	
**Output**:
	
> {'Green','Red'}
	

Pictorial Representation of the above code:
	
s1     s2
    |
    |
 s1.copy()
    |
 A Shallow copy
  Red Green
	
</details>

---
