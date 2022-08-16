## Module- Math , JSON,regex

1.Explain python modules?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>
  <blockquote>
  
 - A file containing Python definitions and statements is known as a module. In python, Variables, classes, and functions can all be defined in a module. 
 - Executable file may also be included in a module.

**Example**: 
 
- File name: `example.py` , is called a module, and its module name is example.
   
```python
def add(a,b):
    return a+b
print(add(8,6))
```
  
- The above module is the main file

File name: `main.py`

```python 
import example
example.add()
```
  
**Output**:

> 14
    
  
  </blockquote> 
</details>

---

2.Which one of these are used for storing and exchanging the data?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> - In python, `JSON` is a syntax for storing and exchanging data.
> - Python have an built-in package called json, which is used to work with `JSON` data.
> - Because, it is easy for humans to browse and write. It's simple for machines to analyze and generate.
 
**import the JSON module :**
 
`import json`
  
</details>

---

3.How can we import modules in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>
  
- In Python, the `import` statement is used to import the whole module. Also, we can import specific categories and functions from a module.
  
**Example**:
  
- `import module name`
  
- To import modules in Python, we use the Python `import` keyword. With the assistance of the import keyword, each **built-in** and **user-defined** modules are imported.

**Example**
  
```python  
import math
print(math.sqrt(5))
```
  
**Output**:
  
> 2.23606797749979  
  
</blockquote>
    </details>
  
---  
  
4.Can we import multiple modules in python. Give an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  
  
<details><summary><b>Show Answer</b></summary>
  
> - Yes, we can import multiple modules in python.
> - If we want to use more than one module, then we can import multiple modules. This is the simplest form to import a statement.

**Syntax**:
  
`import module1[,module2[,.. moduleN]`
  
```python
# Import two modules
import math, random
print(math.fact(5))
print(random.randint(10, 20))
```
  
**Output**:
  
> 120  
> 18

</details>
  
---

5.How will you import with renaming a module?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  
> If we want to use the module with a different name, we can use import_as statement. It is possible to import a particular method and use that method with a different name. 
Then, we can use that name in the entire program.

**Syntax**:  
  
`from module_name import name as alternae_name`
  
**Example**:
  
```python
#rename randint as number
from random import randint as number
print(number(100, 500))
```
  
</details>
  
  ---
  
6.How will you import all the modules in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
  
> If we want to `import` all the functions and attributes of a specific module, instead of writing all names and functions names ,we can import all using              <b> * </b>. 
 
**Syntax**:
  
 `import *`

**Example**:
 
```python
from math import  *
print(pow(5,2))
```
  
**Output**:
  
> 25.0
  
</details>

---

7.Write a regex program in python to extract the full email addresses from the sentence?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary> 

```python
import re
string=input("enter the string")
regex=r'\S+@\S+'
emails=re.findall(regex, string)
print(emails)
```

**Output**:
  
> enter the string: hi my mail id is kavina@yahooo.com 
  
> ['kavina@yahooo.com']
  
</details>

---

8.Write a python program to shuffle the given elements.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
  
```python
import random
String=['appt','cat','bat','mat','sat']
print("before shuffling:",String)
random.shuffle(String)
print("after shuffling",String)
```
 
**Output**:
 
> before shuffling: ['appt', 'cat', 'bat', 'mat', 'sat'] 
  
> after shuffling: ['sat', 'mat', 'bat', 'appt', 'cat']
  
</details>

---

9.Write a python program to find the words with exactly 8 letters using regular expression.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary> 

```python
import re
str='''Huge and tiny creatures are also an essential part of our ecosystem. 
Animals and other domesticated animals give humans food, fibre, and leather. 
A clean environment needs the help of wild creatures including birds, fishes, insects and honeybees to maintain its web of interconnected activity.'''
regex=r'\w{8}'
output=re.findall(regex, str)
print(output)
```

**Output**:

> ['creature', 'essentia', 'ecosyste', 'domestic', 'environm', 'creature', 'includin', 'honeybee', 'maintain', 'intercon', 'activity']
  
</details>

---

10.What is `dir()` function in modules?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
  
> - In python,`dir()` is a built-in function. This function is used to list all the members in current modules.
> - When we use this `dir()` function with any object(like list,tuple,set,...), it will return properties , attributes and methods.
  
**Syntax**:
  
`dir([object])`
  
**Sample code**:
  
```python
import re
print(dir(re))  
```
  
**Output**:
  
> ['A', 'ASCII', 'DEBUG', 'DOTALL', 'I', 'IGNORECASE', 'L', 'LOCALE', 'M', 'MULTILINE', 'Match', 'Pattern', 'RegexFlag', 'S', 'Scanner', 'T', 'TEMPLATE', 'U', 'UNICODE', 'VERBOSE', 'X', '_MAXCACHE', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '__version__', '_cache', '_compile', '_compile_repl', '_expand', '_locale', '_pickle', '_special_chars_map', '_subx', 'compile', 'copyreg', 'enum', 'error', 'escape', 'findall', 'finditer', 'fullmatch', 'functools', 'match', 'purge', 'search', 'split', 'sre_compile', 'sre_parse', 'sub', 'subn', 'template']

</details>

---

11.Write a python program to sort JSON keys and write them into a file.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  
> - In python, to sort JSON keys, first we need to import the JSON.
> - After importing the json data, we need to write into a file. Then, we should open a file and dump the data into a single file.
  
```python
import json
sampleData = {"id" : 1, "name" : "Ram", "age" : 29}
print("writing json data into a file")
with open("sampleData.json", "w") as write_file:
    json.dump(sampleData, write_file, indent=4, sort_keys=True)
print("writing JSON data into a file is done")
```
  
**Output**:
  
> writing json data into a file  
  
> writing json data into a file is done  

</details>

---

12.What is Short Label in python module?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
  <blockquote>
  
 1. `\w` - This is a Word class (alphanumeric).
 2. `\d` - This label is for Digits.
 3. `\s` - Space label is used for an whitespace.
 4. `\W` - This label is for a Non-word class.
 5. `\D` - This is for Non-digit.
 6. `\S` - This label is for a Non-space. 
  
</blockquote>
    </details>

---

13.Write a python program to check whether the given function is user-defined or not.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```python
import types
def function(): 
    return 1
print(isinstance(function, types.FunctionType))
print(isinstance(max, types.LambdaType))
print(isinstance(abs, types.LambdaType))
```
  
**Output**:
  
>True

>False

>False  
  
</details>

---

14.How can we use `re.split()` function in module?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary> 
  <blockquote>
  
 - In python, `re.split()` is used to define how many splits you want to perform.
 - For example, if maxsplit=3, then it will do 3 splits.
  
**Syntax**:

 `re.split(pattern,string,maxsplit=0,flags=0)`
  
 - In regular expression, pattern and strings are the mandatory ones.
 - maxsplit and flag functions are not mandatory.
  
 1.pattern: In regular expression pattern, function is used for splitting the string.

 2.string: The string we want to perform split.

 3.maxsplit: The number of splits you want to perform.It's based upon the split size.

 4.flags: There are no flages applied, by default.
    
</blockquote>
</details>

---

15.What is the difference between `string split()` method and `regex split()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

`string split()`:

1.The `string split()` method is used to split the string into a list of substring with single fixed delimiter.

2.In `string split()` method, we can't inculde the seperator.

3.**Example** 

```python
#string split method
string="Hello guys, Welcome to my new programming language"
output=string.split()
print(output)
```

**Output**:

- ['Hello', 'guys,', 'Welcome', 'to', 'my', 'new', 'programming', 'language']

**regex split()**:

 1.The regex split() method is also used to split the into a list of substring s with an multiple delimiters.

 2.In regex split() method we can include the seperator.

 3.**Example**

```python
# regex split() method
import re
string="Hello-guys, Welcome to my new programming|language"
output = re.split("[-|,|.|\s]+", string)
print(output)
```

**Output**:

- ['Hello', 'guys', 'Welcome', 'to', 'my', 'new', 'programming', 'language']
    
    </blockquote>
</details>

---

16.How can we replace one or more occurrences of a regex pattern in given string?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

 - In python, we can use `sub()` and `subn()` methods to search and replace a string.
 - Using these methods, we can replace one or more occurrences of a regex pattern in the target string with the given string.
 - We have some regex replacement operations,
  
 1.`re.sub(paatern,replacement,string)` - this operation is used to find and replace the **all** occurrences of pattern.

 2.`re.sub(pattern,replacement,string,count=1)` - this operation is used to find and replace only the **first** occurrences of pattern.

 3.`re.sub(pattern,replacement,string,count=n)` - this operation is used to find and replace the **first n** occurrences of pattern.
    
    
</blockquote>
</details>

---

17.What are the differences between Built-in modules and User-defined modules?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
  <blockquote>

**Built-in modules**:

 1.Built-in modules comes with default python installation.
    
 2.Built-in modules provides a lot od reusable code.
    
 3.Some built-in modules are,
    
 - datetime
 - os
 - math
 - random
 - sys
  
**User-defined modules**:

 1.The modules which are defined by user is called a user-defined module.

 2.User can create own modules which contains classes,functions ,variables,etc.

 3.User-defined modules are created as per our requirements.
   
   </blockquote>

</details>

---

18.How can we convert python object to JSON?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> In python, we have python object,which can convert object into a json by using `json.dumps()` method.

**Example**:

```python
import json
x = {
  "name": "Jack",
  "age": 30,
  "city": "London"
}
y = json.dumps(x)
print(y)
```

**Output**:

> {"name": "Jack", "age": 30, "city": "London"}

> When we convert python string to json, python objects are converted into the json.

Example :

dict-object,
  
list-array,
  
tuple-array...

</details>

---

19.What is the output of the following code?

```python
import re
string="""
>Belarus
>China
<$#%#$%
<#$#$$
<**&&^^
>[60,15]
>2000"""
Json_data=re.findall('>\w+', string)
print(Json_data)
```

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> ['>Belarus', '>China', '>2000']

<details><summary><b>Explanation</b></summary>

> The Ouptut of the code is (['>Belarus', '>China', '>2000']) starts with > sign. It will return only those statements.

</details>
</details>

---

20.Which of the following functions creates a python object?

 A.re.compile(str)
 
 B.re.assemble(str)
 
 C.re.regex(str)
 
 D.re.create(str)
 
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

> Option A.`re.compile(str)`

<details><summary><b>Explanation</b></summary>

> The function `re.compile(srt)` compiles a pattern of regular expression into an object of regular `expression. `re.compile(str)` is the only function that creates an object.

</details>
</details>

---
  
  
  
