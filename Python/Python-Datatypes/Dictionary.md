## Dictionary

141)What do you mean by python dictionary? How does it work?
Ans:
  Python dictionary objects are data types that are enclosed in curly braces '{}' and havkey and value pairs and each pair is seperated by a comma(,).
  Dictionary is mapped. Meaning since it has key and value pair, a meaningful key can save a lot of trouble for coders, like using an address key to save all the addresses, an id key for all id’s and so on.
Example:
# Creating a dictionary
# var_name = {key:value} or var_name = dict({key:value})
user_info = {'name': 'Naveen', 'education': 'B.Tech', 'age': 23}
# Print type
print("Variable user_info is a {}.".format(type(user_info)))
# Print Dictionary
print(user_info)
# Now to get a specific information just fetch it using key.
print(user_info['name'])

Output:
Variable user_info is a <class 'dict'>.
{'name': 'Naveen', 'education': 'B.Tech', 'age': 23}
Naveen

142)How will you get keys and values of dictionary?
Ans:
  In dictionary comes with keys() method that will provides all list of the keys in dictionary.
example:
user_info = {'name': 'Naveen', 'education': 'B.Tech', 'age': 23}
print(user_info.keys())

Output:
dict_keys(['name','education','age'])

In dictionary comes with values() method that will provides all list of the keys in dictionary.
example:
user_info = {'name': 'Naveen', 'education': 'B.Tech', 'age': 23}
print(user_info.values())

Output:
dict_values(['Naveen', 'B.Tech', 23])

In Dictionary using items() method that returns list consisting of key and value pair.
example:
user_info = {'name': 'Naveen', 'education': 'B.Tech', 'age': 23}
print(user_info.items())

Output:
dict_items([('name', 'Naveen'), ('education', 'B.Tech'), ('age', 23)])

143)Are dictionaries mutable?What do you mean by mutable?
Ans:
 Yes,the python dictionary is a mutalbe object.
 Mutable means we can change,add or remove key-value pairs after assigning.
example:
 # Mutable Dict
student_info = dict({'id': 12,'nationality': 'China','data_enrolled': 2015,'gender': 'Male'})
print("Student info original: ", student_info)
# We made a mistake while gender registration
# Lets correct it
# Lets change the gender to female
student_info['gender'] = 'Female'
print("Student info after corrections: ", student_info)

Output:
Student info original:  {'id': 12, 'nationality': 'China', 'data_enrolled': 2015, 'gender': 'Male'}
Student info after corrections:  {'id': 12, 'nationality': 'China', 'data_enrolled': 2015, 'gender': 'Female'}

144)What is the difference between list.pop() and dictionary.pop()?
Ans:
The pop() method in list the last item in the list, however, the pop() method in the dictionary can remove a specified item. The dict.popitem() would be the equivalent of list.pop(). 
example:
recurrence_dict = {'current_location': 'Usa','job': 'sofware engineer','older_location': 'Canada'}
print("Before popping: ", recurrence_dict)
# Lets remove the last item
recurrence_dict.popitem()
print("After popping: ", recurrence_dict)

Output:
Before popping:  {'current_location': 'Bangaluru', 'job': 'sofware engineer', 'older_location': 'Chennai'}
After popping:  {'current_location': 'Bangaluru', 'job': 'sofware engineer'}

145)How will you merge more than one dictionary?
Ans:
 In python dictionary can be merger as {**dict_1, **dict_2, …,**dict_n}.In python 3.9 its can be merged using "|" operator.
Example:
# Merge Dictionary
dict_1 = {'name': 'Harini', 'age': 27, 'location': 'kerala'}
dict_2 = {'job': 'software engineer'}
# Merge dict using ** argument
dict_merged_1 = {**dict_1, **dict_2}
print("using ** argument :",dict_merged_1)
# Python 3.9 has new feature merge "|" operator
dict_merged_2 = dict_1 | dict_2
print("using | operator :",dict_merged_2)

Output:
using ** argument : {'name': 'Harini', 'age': 27, 'location': 'kerala', 'job': 'software engineer'}
using | operator : {'name': 'Harini', 'age': 27, 'location': 'kerala', 'job': 'software engineer'}

146)How will you convert list to a dictionary?
Ans:
In python as you know dictionary has key and value pair but the list does not. So, some cases of converting lists into dictionaries are.
i)For loop and Zip with two lists
example:
## List to dictionary
pets= ['dog','cat','guinea pig', 'parrot']
# Adding two list using zip and for loops
numbers =  [2,4,10,2]
pet_number_dict={}
for animal,num in zip(pets,numbers):
    pet_number_dict[animal]= num
print(pet_number_dict)

Output:
{'dog': 2, 'cat': 4, 'guinea pig': 10, 'parrot': 2}

ii)Zip, Comprehension with two lists
example:
## List to dictionary
pets= ['dog','cat','guinea pig', 'parrot']
# Add different values  using zip  and comprehension
pet_number_dict_2 = {animal:num for animal,num in zip(pets,numbers)}
print(pet_number_dict_2)

Output:
{'dog': 2, 'cat': 4, 'guinea pig': 10, 'parrot': 2}

147)What is the difference between duplicating dictionary with and without copy()?
Ans:
  It means is dict_2 = dict_1 vs. dict_2 = dict_1.copy(). When you are duplicating a dictionary object without a copy() method, you are not creating a new dictionary but pointing to the same dictionary object. So, when you make changes in the duplicate list it changes the original one too.
example:

# Duplicating dict with and without copy
list = {
'eggs': '1 karton',
'banana': '1 kg',
'milk': '1 ltr',
'sugar': '1 kg'
}
print("Original List before {}".format(list))
# Lets duplicate without copy
list_2 = list
# Lets make change to duplicate list
list_2['salt'] = '1 kg'
print("Original List after duplication {}".format(list))
print("Are the memory address of two dicts same? {}".format(id(list) == id(list_2)))

Output:
Original List before {'eggs': '1 karton', 'banana': '1 kg', 'milk': '1 ltr', 'sugar': '1 kg'}
Original List after duplication {'eggs': '1 karton', 'banana': '1 kg', 'milk': '1 ltr', 'sugar': '1 kg', 'salt': '1 kg'}
Are the memory address of two dicts same? True


Now we can do with copy() method.

# Duplicating dict with and without copy
to_buy_list = {
    'eggs': '1 karton',
    'banana': '1 kg',
    'milk': '1 ltr',
    'sugar': '1 kg'
 
}
print("Original List before {}".format(to_buy_list))
# Lets duplicate without copy
to_buy_list_2 = to_buy_list.copy()
# Lets make change to duplicate list
to_buy_list_2['salt'] = '1 kg'
print("Original List after duplication {}".format(to_buy_list))
print("Are the memory address of two dicts same? {}".format(
    id(to_buy_list) == id(to_buy_list_2)))

Output:
Original List before {'eggs': '1 karton', 'banana': '1 kg', 'milk': '1 ltr', 'sugar': '1 kg'}
Original List after duplication {'eggs': '1 karton', 'banana': '1 kg', 'milk': '1 ltr', 'sugar': '1 kg'}
Are the memory address of two dicts same? False

148)What will be output of following program?
d={(3,4,8):4,(5,6,9):3}
print('dictionary output:' ,d[3,4,9])

Ans:
output:
print('dictionary output:',d[3,4,9])
KeyError: (3, 4,9)

149)What module and function can be used to "pretty print" dictionary values?

Ans:
pprint is a python module that provides the capability to pretty print python data types.
First, declare an array of dictionaries. After, pretty print it using the function pprint.pprint().
Example:
import pprint
dictionary = [
  {'Name': 'John', 'Age': '23', 'Country': 'USA'},
  {'Name': 'Jose', 'Age': '44', 'Country': 'Spain'},
  {'Name': 'Anne', 'Age': '29', 'Country': 'UK'},
  {'Name': 'Lee', 'Age': '35', 'Country': 'Japan'}
]
pprint.pprint(dictionary)

Output:
[{'Age': '23', 'Country': 'USA', 'Name': 'John'},
 {'Age': '44', 'Country': 'Spain', 'Name': 'Jose'},
 {'Age': '29', 'Country': 'UK', 'Name': 'Anne'},
 {'Age': '35', 'Country': 'Japan', 'Name': 'Lee'}]

150)What will be the output of the following code?
dictlang = {'To': 6, 'GO': 89, 'Python': 4,'Rules':10}
cpydict = dictlang.copy()
print(id(cpydict) == id(dictlang))

Ans:
Output:
False

151)How will you delete a key from Dictionary?

Ans:
 In python for that we can use del keyword to delete a key from dictionary.
Example:
fruitsDict = {'Apple': 100,'Orange': 200,'Banana': 400,'pomegranate':600}
if 'Apple' in fruitsDict: 
    del fruitsDict['Apple']
print('Dictionary after deleting key =',fruitsDict)

Output:
Dictionary after deleting key = {'Orange': 200, 'Banana': 400, 'pomegranate': 600}

152)Write a program to get min and max keys corresponding to min and max value in dictionary?

Ans:
n = int(input("enter the number of values"))
FruitsDict = dict(input().split() for i in range(n))
print(FruitsDict)
print('min value key:',min(FruitsDict,key=FruitsDict.get))
print('max value key:',max(FruitsDict,key=FruitsDict.get))

Output: 
max and min values it's depends upon the user values

153)How to sum all elements of Dictionary?

Ans:
  In python using sum() method we can sum the dictionaries elements.
Example:
Fruit = {'Apple': 100, 'banana': 5,'orange':45,'Guava':60}
print('sum of dict elements = ',sum(Fruit.values()))

Output:
sum of dict elements = 210

154)What will be the output of the following program?

from heapq import nlargest
FruitDict = {'Apple': 600, 'Banana': 515,'Orange':214,'Guava':1116} 
two_highest_values = nlargest(2, FruitDict, key=FruitDict.get)
print(two_highest_values) 

Ans:
output:
['Guava','Apple']

155)How will you print dictionary as table?

Ans:
Dict_tab = {'Students':['Rack','Jack','John'],'Fruit':['Apple','Banana','Orange'],'Subject':['Phy','Math','English']}
for row in zip(*([key] + (value) for key, value in sorted(Dict_tab.items()))):
    print(*row)

Output:
Fruit Students Subject
Apple Rack Phy
Banana Jack Math
Orange John English

156)Write a Python program to sort a list alphabetically in a dictionary?

Ans:
num = {'n1': [2, 3, 1], 'n2': [5, 1, 2], 'n3': [3, 2, 4]}
sorted_dict = {x: sorted(y) for x, y in num.items()}
print(sorted_dict)

Output:
{'n1': [1, 2, 3], 'n2': [1, 2, 5], 'n3': [2, 3, 4]}

157)Look at the code carefully and tell me what will be the output of the following code?
students = {'kanika':{'class':'V',
        'rolld_id':2},
        'Harini':{'class':'V',
        'roll_id':3}}
for a in students:
    print(a)
    for b in students[a]:
        print (b,':',students[a][b])

Ans:
kanika
class : V
rolld_id : 2
Harini
class : V
roll_id : 3

158)Write a Python program to sort counter by value?
Sample data : {'Math':81, 'Physics':83, 'Chemistry':87}
Expected data: [('Chemistry', 87), ('Physics', 83), ('Math', 81)]

Ans:
from collections import Counter
x = Counter({'Math':81, 'Physics':83, 'Chemistry':87})
print(x.most_common())

Output:
[('Chemistry', 87), ('Physics', 83), ('Math', 81)]

159)What will be the output of the following code?
dict =  {'Alex': ['subj1', 'subj2', 'subj3'], 'David': ['subj1', 'subj2']}
dict_len = sum(map(len, dict.value()))
print(dict_len)

Ans:
Output:
AttributeError: 'dict' object has no attribute 'value'

160)What will be the output of the following code?

dict1 ={'English':'67%','Maths':'78%','Social_Science':'87%','EVS':'97%'}
print(dict1 .keys( ))

Ans:
Output:
dict_keys(['English', 'Maths', 'Social_Science', 'EVS'])
