## Tuple

1.What is a Tuple? How tuple different from list in python?


- Tuple is a immutable datatype in python which is used to store elements separated by comma inside parentheses (). To create an empty tuple we can use () in python. 
For example: i) tuple1 =()  ii) tuple1 = (1, 2, 3) 

In python, both list and tuple looks similar as they both can store any type of data in it but there are some difference that makes both of them distinct. Some of the following differences are:

i) Lists in python are mutable, whereas tuples are immutable.
ii) We can use append() or insert() to add elements to a list, but in tuple append and insert are not present.
iii) We can use pop() or remove() to delete an element from the list, but in tuple we cannot delete elements.
iv) Use list when you have to perform manipulation operations on data such as insertion or deletion. Use tuple when you have frequently access the elements without changing. 
v) Using [] brackets we can create list. Using (), we can create tuple in python. 


102) What are the built-in methods present in tuple?
Ans: Tuple has 2 built-in methods in python:
i) count() - it returns the count of specified element in tuple.
ii) index() - it searches the specified value in a tuple and returns the position of that element where it found. 


103) How to add element to a Tuple?
Ans: We cannot add elements to a tuple directly since it is immutable but if we convert the tuple to a list then we can add element to that list using append() or extend() method and after adding we can convert that list back to tuple. 
For example: 
tuple1 =(1, 2, 3)
list1 =list(tuple1)
list1.append(4)
tuple1 =tuple(list1)
print(tuple1)    # output: (1, 2, 3, 4)
print(type(tuple1))  # output: <class 'tuple'>


104) Tuple does not have sort method to sort the elements compared to List, then how will you sort the elements of a tuple in python?
Ans: there are few ways by which we can sort the elements of tuple, let's see them 1 by 1. 

# Using sorted() method and type conversion 
tuple1 = (12, 4, 7, 21, 34, 2, 16)  
sorted_tuple= tuple(sorted(tuple1))  
print(sorted_tuple)  # output: (2, 4, 7, 12, 16, 21, 34)

# Using sort() method of list and type conversion 
tuple1 = (12, 4, 7 , 21, 34, 2, 16)  
lst = list(tuple1)
lst.sort()   
print(tuple(lst))  # output: (2, 4, 7, 12, 16, 21, 34) 


105) How to sort the elements of a tuple in descending order?
Ans: By passing reverse = True as argument of sort() method, we can sort the elements of a list. After that using type conversion we can convert the list to tuple. 

# Code 
tuple1 = (12, 4, 7 , 21, 34, 2, 16)  
lst = list(tuple1)
lst.sort(reverse =True)   
print(tuple(lst))


106) How to join two tuples together in Python?
Ans: We can use the '+' operator to join two tuples together. 
For example:
t1 = (12, 4, 7 , 21)
t2 = (34, 2, 16)
print(t1 + t2)  # output: (12, 4, 7, 21, 34, 2, 16)
 

107) How to print the reverse order of elements in a tuple? 
Ans: Using reverse() method of list and type conversion we can achieve our task. 
For example: 
t1 =(1, 5, 3, 9, 2)
lst = list(t1)
lst.reverse()
print(tuple(lst))   # output: (2, 9, 3, 5, 1)


108) What is the output of below code:
tuple1 = (10, 20, 30, 40, 50)
tuple1.pop(2)
print(tuple1) 

Options:
a) (10, 20, 40, 50)
b) (10, 30, 40, 50)
c) 30 
d) Error 

Ans: Correct option is d) Error. The reason for it is that Tuple is immutable in python i.e we cannot change the values of a tuple.


109) Select the correct statements out of following regarding Tuple. 

options: 
a) We can delete the element from a tuple but we cannot update elements of the tuple.
b) We cannot delete the tuple.
c) We cannot delete the items from the tuple
d) We cannot update items of the tuple. 

Ans: options c) and d) both are correct. We can delete the whole tuple by using del keyword so option b) is incorrect. Option a) is incorrect because we cannot remove, add or update items of a tuple. 


110) State True or False: A Python tuple can also be created without using parentheses.

a) True 
b) False

Ans: option a) is correct. We can create a tuple without parentheses but we have to seperate each element of tuple by comma ','. 


111) What will be the output of following code?
tuple1 = (10,)
print(tuple1 * 3)

options:
a) TypeError
c) (30)
b) (10, 10, 10)
c) (10, 20, 30) 

Ans: correct option is c) (10, 10, 10). We can use '*' operator to repeat the values of tuple n number of times.


112) What is the type of follwing code?
tuple1 = ("anu")
print(type(tuple1))

options:
a) list 
b) tuple
c) array
d) str

Ans: Correct option is d) str. The answer of following code is not tuple because in python if you have to create a tuple of single item only, then you need to add a comma after the item. 
If you missed the comma, the python will treat it as a string type (str class). 


113) Predict the output of the code.
tuple1 = 25, 20, 15, 10, 5 
a, b, c, d, e = tuple1
print(b)

options:
a) 25
b) 20
c) 15
d) 5 

Ans: Correct option is b) 20. In python, we can create a tuple without parentheses. Also tuple unpacking is possible. 

114)Debug the code and give me a correct code.(To print the third element of the tuple.)

tuple=(11, 100, 101, 999, 1001)
#Type your answer here.
answer_1=
print(answer_1)

Ans:
tuple=(11, 100, 101, 999, 1001)
#Type your answer here.
answer_1=tuple[2]
print(answer_1)

Explanation:
 0,1,2 … Third element is index 2: [2]

115)What will be the output of the following code?

Tuple1="yellow",20,"Red"
a,b,c=Tuple1
print(b)

a)('yellow',20,'red')
b)TypeError
c)yellow
d)No output

Ans:
c)yellow
Explanation:
The tuple unpacking is also possible

116)Write a python program to sort list of tuples by second element.

Ans:
listtuple= [('C#',1), ('Go',7), ('Basic',8), ('Python',60)]
print('original list of tuples =\n',listtuple)
listtuple.sort(key = lambda item:item[1])
print('after sorting by second item=\n',listtuple)

Output:
original list of tuples =
 [('C#', 1), ('Go', 7), ('Basic', 8), ('Python', 60)]
after sorting by second item=
 [('C#', 1), ('Go', 7), ('Basic', 8), ('Python', 60)]

Explanation:
This is the one way of approach only you can do in your way.

117)Debug the code and give the output of the following code?
(sum of all the numbers in the tuple)

tuple=(45,2,90,5,36,65)
output=
print("sum of the tuple:",output)

Hint:
sum() function will calculate the total sum inside the numbers of your tuple.

Ans:
tuple=(45,2,90,5,36,65)
output=sum(tuple)
print("sum of the tuple:",output)

Output:
sum of the tuple: 243

118)Write program to swap two tuples in python.

Sample tuple:
tuple1=(11,22)
tuple2=(99,88)
Expected output:
tuple1:(99,88)
tuple2:(11,22)

Ans:
tuple1=(11,22)
tuple2=(99,88)
tuple1,tuple2=tuple2,tuple1
print('tuple1 value after swapping:',tuple1)
print('tuple1 value after swapping:',tuple2)

Output:
tuple1 value after swapping: (99, 88)
tuple1 value after swapping: (11, 22)

119)What is the output of the following tuple operation

aTuple = (100, 200, 300, 400, 500)
aTuple.pop(2)
print(aTuple)

a)(100,200,400,500)
b)(100,300,400,500)
c)AttributeError
d)No output

Ans:
option c:AttributeError

Explanation:
A tuple is immutable. Once a tuple is created, you cannot remove its items, but you can delete the tuple completely. If you try to remove the item from the tuple, you will receive an AttributeError: 'tuple' object has no attribute 'pop'.

120)A Python tuple can also be created without using parentheses

a)False
b)True

Ans:
option:b)True

Explanation:
A tuple can also be created without using parentheses. It is called tuple packing.

example:
tuple = "Yarn", 20, "Rabbit"
print(tuple)

121)Write a program to convert two list to dictionary in python?

Ans:
Team=["Training","Dev","Sales","Finance"]
Members=[38,50,33,79]
Office=dict(zip(Team,Members))
print(Office)

Output:
{'Training': 38, 'Dev': 50, 'Sales': 33, 'Finance': 79

122)What is the type of the following variable?

Tuple=("Engineer")
print(type(Tuple))

a)tuple
b)str
c)array
d)list

Ans:
option:b)str

Explanation:
   To create a tuple with a single item, you need to add a comma after the item. Otherwise, Python will not recognize the variable as a tuple, and it will treat it as a string type.
example:
Tuple=("Engineer")
print(type(Tuple))
Tuple1=("Software",)
print(type(Tuple1))
Output:
<class 'str'>
<class 'tuple'>

123)How will you find the duplicate tuple in list of tuple.

Ans:

Tuple= [('Python',5),('Java',3),('C#', 1), ('JS', 2), ('C#', 1), ('JS', 2),('React',1)] 
#finding the duplicate tuple
Output_tuple = list(set([item for item in Tuple if Tuple.count(item) > 1])) 
print(Output_tuple)

Output:
[('JS', 2), ('C#', 1)]

124)Counts the number of occurrences of item 50 from a tuple.
Sample tuple:
tuple = (50, 10, 60, 70, 50,67,89,160,145,67,50)

Ans:
tuple = (50, 10, 60, 70, 50,67,89,160,145,67,50)
print(tuple.count(50))

Output:
3
Explantion:
 To count the number of occurrences we used the count() method of a tuple.

125)Choose the correct way to access value 20 from the following tuple.

Tuple = ("Software",[10, 20, 30], (5, 15, 25))

a)Tuple[1:2][1]
b)Tuple[1:2](1)
c)Tuple[1:2][1]
d)Tuple[1][1]

Ans:
option:c)Tuple[1:2][1]
