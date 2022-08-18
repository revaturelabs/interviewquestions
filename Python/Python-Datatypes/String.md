## String

1.What are `String literals`?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- A `string` literal is a sequence of zero or more characters enclosed in single quotes.
  
**Examples**:
  
"Hello,World"
    
'Revature'
  
</blockquote>
    </details>

---

2.How do you know if every word in a string that starts with a capital letter?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> The `istitle()` function checks if each word is capitalized or not.
  
**Example**:
  
```python  
print( 'The Dog'.istitle() ) #=> True
```
<details><summary> <b>Explanation</b> </summary>  
  
> In python, `istitle()` function is used to check whether the given string starts with a capital letter or not.
  
</details>
</details>

---
  
3.How will you combine two or more strings in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> In Python, you can concatenate two strings by simply using the `+` operator in between them. You can use the + operator to `concatenate` three or more strings as well.

**Example**:
  
  ```python
  
s="hello"
s1="world"
string=s+s1
print(string)
```
  
**Output**:
  
> helloworld
  
<details><summary> <b>Explanation</b> </summary>
  
> In the above program, we use `+` operator for combining two or more strings into a single string.
  
</details>
</details>

---

4.What is the output of the following code?

```python
s1="IndiaTraining people"
s2=""
s3=""
for x in s1:
     if(x=="s" or x=="n" or x=="p"):
           s2+=x
print(s2,end=" ")
print(s3)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> nnnpp
  
<details><summary> <b>Explanation</b> </summary>
  
> In the above program, it will check whether s,n and p characters are in the string or not.If it is there, it will print those characters.
  
  </details>
  
</details>

---

5.How will you count total number of characters in a string. Give an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python, `len()` function will return the length of a string.
  
**Example**:
  
```python
s="Revature"
print(len(s))
```
  
**Output**:
  
8

</details>

---
 
6.What would be the output for the following code?

```python
string1 = "HAPPY "
string2 = "LEARNING!!!"
print((string1 + string2)*3)
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> HAPPY LEARNING!!!HAPPY LEARNING!!!HAPPY LEARNING!!!

<details><summary> <b>Explanation</b> </summary>
  
> In the case of a string, the `*` operator is used to repeat a string.
  
</details>
</details>

---

7.How will you check if a string contains only string or not?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python, `isnumeric()` function returns True if all characters are numeric.
  
**Example**:

```python  
s="Revature123"
print(s.isnumeric())
```
  
**Output**:
  
False
  
</details>

---

8.Write a program to find the characters at an odd position in a string input by the user?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
```python  
string = input("Enter the string : ")
outputString = ''
for i in range(len(string)):
    if(i % 2 == 0):
        outputString = outputString + string[i]
print("Input string :  ", string)
print("String after odd charcater :", outputString)
```
  
**Output**:
  
Enter the string : PythonString
Input string :   PythonString
String after odd charcater : PtoSrn
  
<details><summary> <b>Explanation</b> </summary>
  
> In the above program, we initially used `len()` function to find the size of the string. Then, we want to find the odd position in string and we used `if` statements inside the `for` loop.
> If the position/index is not equal to 0 , those characters are stored into the single variable and then it will print the values.

</details>
</details>
  
---

9.Write a program  to replace all occurrence of sub-string in string?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
```python
  
inputStr = "is the is Python is Program is"
modifiedStr =  inputStr.replace('is', '')
print(modifiedStr)
```

**Output**:
  
> the  Python  Program
  
<details><summary> <b>Explanation</b> </summary>
    
> In python, we use `.replace()` function to replace one character with another character.
    
</details>
</details>

---

10.How will you Count Total numbers of upper case and lower case characters in input string?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
- In python, we are using `isupper()` to find upper case characters and `islower()` to find the lower case characters.
  
**Example**:
  
```python
  
string = input('Please enter the string: ')
upper_case= 0
lower_case = 0
for char in string:
 if char.isupper():
    upper_case+=1
 elif char.islower():
    lower_case+=1
print ("string entered by user : ", string)
print (" Total Upper case characters  : ", upper_case)
print ("Total Lower case Characters : ", lower_case)
```

<details><summary> <b>Explanation</b> </summary>
   
- If we want to count total number of upper case and lower case in the given string, we can use `isupper()` and `islower()` method.
   
</details>
</details>

---

11.What is the output of the following code?

```python
input_string ="Consultancy"
reversed_str =''.join(reversed(input_string))
print('reversed string =',reversed_str)
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> reversed string = ycnatlusnoC

<details><summary> <b>Explanation</b> </summary>

> In python, to reverse a string, we can use built-in function reversed or else we can use `negative index ([::-1])`.
  
</details>
</details>

---

12.Write a program to Extract URL From A String In Python?
  
  ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

 ```python
  
import re
def URLsearch(stringinput):
    regularex = r"(?i)\b((?:https?://|www\d{0,3}[.]|[a-z0-9.-]+[.][a-z]{2,4}/)(?:[^\s()<>]+|(([^\s()<>]+|(([^\s()<>]+)))))+(?:(([^\s()<>]+|(([^\s()<>]+))))|[^\s`!()[]{};:'\".,<>?«»“”‘’]))" 
    urlsrc = re.findall(regularex,stringinput) 
    return [url[0] for url in urlsrc]
textcontent = 'text :a software website find contents related to technology https://devenum.com https://google.com,http://devenum.com'
print("Urls found: ", URLsearch(textcontent))
```
  
**Output**:
  
> Urls found:  ['https://devenum.com', 'https://google.com,http://devenum.com']
  
<details><summary> <b>Explanation</b> </summary>
  
> If we want to extract the url from string, we can use `regex`.
  
  </details>
  
</details>
  
---

13.Does creating a string twice (with two distinct variable names) result in one or two objects being stored in memory?
  
  ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> For example, writing animal = 'dog' and pet = 'dog'.
> It only creates one.
> Here we can see this example,

 ```python
animal = 'dog'
print( id(animal) )
#=> 4441985688
pet = 'dog'
print( id(pet) )
#=> 4441985688
```
  
</details>
  
---
  
14.How will you remove whitespace from the left, right or both sides of a string?
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python, we can use `lstrip()`, `rstrip()` and `strip()` to remove whitespace from the ends of a string.
  
**Example**,
 
```python
string="  Whitespace of strings  "
print(string.lstrip())
print(string.rstrip())
print(string.strip())
```
  
**Output**:
  
Whitespace of strings  
  Whitespace of strings
Whitespace of strings

<details><summary> <b>Explanation</b> </summary>
  
> For removing whitespace from the ends of the string, we can use `.strip()` functions.
> `.lstrip()` -used to remove whitespace from left side of the string.
> `.rstrip()` -used to remove whitespace from right side of the string.
  
  </details>
  </details>
  
  ---
  
15.Select the correct output for the following code?

 ```python 
str1=str("Python_programming")
str2="Python_programmIng"
print(str1 == str2)
print(str1 is str2)
```
  
 A. True
    False
  
 B. False
    False
  
 C. False
    True
  
 D. True
    True
  
  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> Option B is the correct one
  
<details><summary> <b>Explanation</b> </summary>
  
> In case of a string, `==` and `is` operators are used to check whether the given strings are equal or not.
  
  </details>
  </details>
  
  ---

16.What is `slicing` and what is the use of that?
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> `Slicing` in Python is a feature that enables accessing parts of sequences like `strings, tuples, and lists`. 
> You can also use them to modify or delete the items of mutable sequences such as lists. `Slicing` enables writing `clean, concise, and readable code`.
  
**Syntax**: 
  
`slice(stop) slice(start, stop, step)`
  
</details>
  
---

17.What are the difference between **==** and **is** operators in python?

  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
** == **:
  
 - In python, this operator is equality operator.
 - The == operator is used when the values of two operands are equal, and then the condition becomes `True`.
  
**Example**:

```python  
s1="hi"
s2="hi"
print(s1 == s2)
```  
 
**Output**:
  
 It returns True.
  
**is** :
  
 - In python, this operator is Identity operator.
 - The `is` operator evaluates to true if the variables on either side of the operator point to the same object and false otherwise.
  
**Example**:
  
```python
list_1 = ['a', 'b', 'c']
list_2 = list_1
list_3 = list(list_1)
print(list_1)
print(list_2)
print(list_3)
print(list_1 is list_2)
print(list_1 is list_3)
```
  
**Output**:
  
> True
  False
  
<details><summary> <b>Explanation</b> </summary>
  
- Here you can see (list_1 is list_3) is `False` because list_1 and list_3 are pointing to two different objects , even though their contents might be the same. So, we can say `is` will return True if two variables point to the same object and `==` ,if the objects referred by the variables are equal.

 <blockquote> 
</details>
</details>
  
---
  
18.Predict the output of the following code.
  
```python  
str="Software engineer"
print(str[2 : 10 : 2])
```
  
  ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> fw
  
<details><summary> <b>Explanation</b> </summary>
  > In the above program, we use `slicing` operator and this is used to cut the strings based on the values.
  
  </details>
</details>
  
  ---

19.What is the output of the following code?

```python
str1 = "Revature"
print(str1[1:4], str1[:5], str1[4:], str1[0:-1], str1[:-1])
```
   
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
   
<details><summary> <b>Show Answer</b> </summary>
  
> eva Revat ture Revatur Revatur

<details><summary> <b>Explanation</b> </summary>
  
 > We can use a slice operator [] to get a substring.
  
**Syntax**: 
  
> s[start : end]

  </details>
  </details>
  
  ---
  
20.What is the difference between `indexing` and `slicing`?

<details><summary> <b>Show Answer</b> </summary>
  <blockquote>
  
 - **Indexing**: Indexing is used to obtain individual elements.
           - Indexing returns one item.
           - Indexing starts from `0`. Negative Indexing starts from `-1`.
 - **Slicing**: Slicing is used to obtain a sequence of elements.
           - Slicing returns new list.
           - We can specify range of indexes.

 - Indexing and Slicing can be done in Python Sequence types like `list, string, tuple, range objects.
    
   </blockquote>

  </details>
  
  ---
  
21. Mention few String methods in Python?
    
    ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
   > - `endswith()`	Returns true if the string ends with the specified value
   > - `format()`	Formats specified values in a string
   > - `isalpha()`	Returns True if all characters in the string are in the alphabet
   > - `isidentifier()`	Returns True if the string is an identifier
   > - `partition()`	Returns a tuple where the string is parted into three parts
  
  </details>
  
  ---
  
22.What is the output of the following code?

```python  
str = "RevatureLearningProcess"
print(str[: :-1])
print(str[-7: -1: 2])
print(str[3 : 14 : 3])
```
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  <blockquote>

 ssecorPgninraeLerutaveR
  
 Poe
  
 aren
  
<details><summary> <b>Explanation</b> </summary>
> In the above program, we will get some part of string characters as we use `slicing()` method.    

</details>
    </details>
  
---
  
23.Which method should we use to convert the String "welcome to the beautiful world of python" to "Welcome To The Beautiful World Of Python".
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
 > - `title()`-method
 > - For this, we can use `title()` method.
  
<details><summary> <b>Show Explanation</b> </summary>
  
> The `title()` function `capitalize()` the first letter of every word of the String.
  
  </details>
  </details>

  ---
  
24. Mention few Escape Characters in python?
  
  ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> - \'	Single Quote	
> - \\	Backslash	
> - \n	New Line	
> - \r	Carriage Return	
> - \t	Tab	
> - \b	Backspace	
> - \f	Form Feed	
> - \ooo	Octal value	
> - \xhh	Hex value
  
</details>
  
---

25.Debug the code and give the correct output for that code.

```python  
str="Hello World!"
#Type your answer here.
lst=
print(lst)
```
  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Hint</b> </summary>
  <blockquote>
  
- `.split()` method can be used to split strings based on a given character. It returns a list of split substrings.
  
 </details>  
  
<details><summary> <b>Show Answer</b> </summary>
  
Expected output:
  
> ['Hello','World!']
  
**Answer**:
 
```python 
str="Hello World!"
lst=str.split(" ")
print(lst)
```
 </blockquote> 
  </details>
  
  ---
  
26.Find the correct output of the following String operations.
  
```python  
str1='Welcome'
print(str1[:6] + ' to India')
```
  
 ![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
   
> Welcom to India
   
<details><summary> <b>Explanation</b> </summary>
  
> Here, we use slicing to get some part of string and then we use `+` operator for string combining.

  </details>
  </details>
  
  ---
  
27.What is the output of the following code?
  
 ```python 
str1 = "My salary is 7000";
str2 = "7000!"
print(str1.isdigit())
print(str2.isdigit())
 ```
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>
  
> False
> False
  
<details><summary> <b>Explanation</b> </summary>
  
> `isdigit()` method checks if it contains the characters or not. If it has, it will return True or else it will return False.
  
  </details>
  </details>
  
---
