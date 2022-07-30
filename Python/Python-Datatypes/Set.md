## Set

126)What is the difference between list and set?

Ans:List:[]
    List is Mutable and ordered/indexed.
    List allows duplicate values.
    It can stroe any data type str,list,set,tuple,int and dictionary.
  Set:{}
    Set is Mutable and unordered.
    Set not allow duplicate values.
    Inside of dictionary key can be int,str,and tuple only values can be of any data type int,str,list,tuple,set and dictionary.

127)How will you add list items into a Set?

Ans:In python we can use the update() method of a set, to add list of items into a set.
Example:
sample_set = {"Yellow", "Orange", "Black"}
sample_list = ["Blue", "Green", "Red"]
sample_set.update(sample_list)
print(sample_set)

Output:
{'Green', 'Yellow', 'Red', 'Black', 'Orange', 'Blue'}

128)How will you return a new set of identical items from these two sets?
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
Ans:
  For that we have Intersction() method of a set.
set1 = {10, 20, 30, 40, 50}
set2 = {30, 40, 50, 60, 70}
print(set1.intersection(set2))

Output of the Above program is:
{40,50,60}
    
129)What will be the output of the following code?
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
Ans:
Output:
{(9, 5), (9, 6), (10, 6), (8, 5)}


130)How will you remove items 10, 20, 30 from the set at once?
set1 = {10, 20, 30, 40, 50}
Ans:
In python we use difference_update() method of a set.
s1 = {10, 20, 30, 40, 50}
s1.difference_update({10, 20, 30})
print(1)

Output:
40,50

131)Write a program to Check if two sets have any elements in common. If yes, display the common elements.
Ans:
set1 = {10, 20, 30, 40, 50}
set2 = {60, 70, 80, 90, 10}
if set1.isdisjoint(set2):
  print("Two sets have no items in common")
else:
  print("Two sets have items in common")
  print(set1.intersection(set2))

Output:
Two sets have items in common
{10}

132)What are the methods you frequently used when dealing with set in python?

Ans:Set provides different kinds of built-in methods that anyone can use for Set manipulations. Some of these methods are mentioned below:
i) add(): it is used to adds an element to the set
ii) clear(): it removes all the elements from the set
iii) copy(): it returns a copy of the set
iv) difference(): it returns a set containing the difference between two or more sets
v) difference_update(): it removes the items in this set that are also included in another, specified set
vi) discard(): it remove the specified item
vii)intersection(): it returns a set, that is the intersection of two other sets
viii)issubset():it returns whether another set contains this set or not
ix)issuperset():it returns whether this set contains another set or not
x)pop():it removes an element from the set
xi)remove(): it removes the specified element
xii)union():it return a set containing the union of sets
xiii)update(): Update the set with the union of this set and others

133)What is the difference between pop() and remove()?

Ans:
pop():
 it is used to removes an element from the set.
example:
fruits = {"apple", "banana", "cherry"}
x = fruits.pop()
print(x)

Output:
apple(it removes random element from set)
remove():
 it is used to removes the specified element.
example:
fruits = {"apple", "banana", "cherry"}
fruits.remove("cherry")
print(fruits)

Output:
{"apple","banana"}

134)How to iterate over the set of elements?Write a code for that.
Ans:
To iterate over set in python we can use any loop.
i)using for loop

set={"a","b","c"}
for x in set:
 print(x)
Output:
b
c
a

135)What is the use of copy() method? 
Ans:
The copy() method used to copies the set.
Example:
fruits = {"ant", "bat", "cat"}
x = fruits.copy()
print(x)
Output:
{'ant','bat','cat'}

136)Can you zip 2 sets together?
Ans:
Yes,but the values from each set may not be joined in order.
example:
z = zip({1,2,3},{'a','b','c'})
print(list(z))

Output:
[(1, 'b'), (2, 'c'), (3, 'a')]

137)Can a set be accessed by index?
Ans:
No.Set can't be accessed by index,if your trying to access a set by index will throw an error.
example:
s={1,2,3}
print(s[0])

Output:
TypeError: 'set' object is not subscriptable

138)Can you Update a set to equal the intersection of it and another set.
Ans:
In python intersection_update() updates the first set to be equal to the intersection.
example:
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1.intersection_update(s2)
print(s1)

Output:
{4,5}

This can also be done with the &= operator.

s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1 $= s2
print(s1)

Output:
{4,5}

139)Can you remove the intersection of a 2nd set from the 1st set.
Ans:
In python difference_update() removes the intersection from the first set.
example:
s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1.difference_update(s2)
print(s1)

Output:
{1, 2, 3}

The operator -= also works.

s1 = {1,2,3,4,5}
s2 = {4,5,6,7,8}
s1-=(s2)
print(s1)

Output:
{1,2,3}

140)Write a Python program to create a shallow copy of sets.

Note : Shallow copy is a bit-wise copy of an object. A new object is created that has an exact copy of the values in the original object.
Ans:

s1 = set(["Red", "Green"])
s2 = set(["Green", "Red"])
#A shallow copy
setr = s1.copy()
print(setr)

Output:
{'Green','Red'}

Pictorial Representation  of the above code:
s1     s2
    |
    |
 s1.copy()
    |
 A Shallow copy
  Red Green
