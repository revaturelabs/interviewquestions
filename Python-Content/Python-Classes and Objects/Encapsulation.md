
# Encapsulation


1. What do you mean by encapsulation in python? How to achieve it? Give example. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Binding up of data members and member functions together into a single unit is known as encapsulation. A class is an example of encapsulation as it binds the variables and methods together. We can achieve encapsulation by declaring the data members of a class either as private or protected.   
  
For Example: 
```python3
class Student:
    def __init__(self, name, marks):
        self.name = name
        # private member
        self.__marks = marks

stu = Student('Rohan', 76)
print('Marks:', stu.__marks)
```
  
> In the above code, we will get the `"AttributeError: 'Student' object as no attribute __marks,because _marks is a private variable and we cannot access private variables directly outside the class. 
</details>

---
2. Give a real-time example of encapsulation.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Consider there are two companies that makes motercycles, one is `Hero` and other one is `Honda`. 
  Hero company has its own production unit and team, and Honda company also has its own production unit and team. They both are doing well in the market. If there's a situation, where Honda company wants to work with Hero company and wants to access the info of how Hero company production unit works. 
  As Honda company doesn't have the direct access of Hero company, they have to contact some of the higher officials to get the work done. This is what we can say encapsulation in real world is. Here all the datas related to Hero company can be wrapped into a single unit. Hero company will not give permission to anyone outside to access the data, the data has been hiden and secure from the outside world. 
</details>

---
3. Which statement out of the following is best for encapsulation?  

a) It gives ability to a child class to access properties from parent class.  
b) It has the ability to hide the unwanted complex implementation from the user.
c) It wraps up the data members and member functions of a class in a single unit.  
d) It gives different meaning to same function in different classes.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> option c) 
<details><summary> <b>Explanation</b> </summary> 
  
> Encapsulation is a way of binding all the members of a class together. 
  </details>
</details>

---
4. Predict the output of the following code.
```python3
class Test:
    def __init__(self):
        self.num1 = 5
        self.__num2 = 10
 
    def display(self):
        return self.__num2

obj = Test()
print(obj.num1)
```
a) 5 is printed  
b) 10 is printed  
c) Error, because num1 is not retured by display() method.  
d) Error, because __num2 is a private data member.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> option is a).
<details><summary> <b>Explanation</b> </summary> 
  
> num1 is a public variable of Test class. It can be accessed outside the class using objects of that class. 
  </details>
</details>

---
5. Predict the output of the following code.
```python3
class Test:
    def __init__(self):
        self.num1 = 5
        self.__num2 = 10
 
    def display(self):
        return self.__num2

obj = Test()
print(obj.__num2)
```
a) 5 is printed  
b) 10 is printed  
c) Error, because num1 is not retured by display() method.  
d) Error, because __num2 is a private data member.  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> option is d).
<details><summary> <b>Explanation</b> </summary> 
  
> As __num2 is private variable of Test class, we cannot access the variable through objects of that class. 
  </details>
</details>

---
6. Predict the output of the below code.
```python3
class Test:
    __num2=30
    def __init__(self):
        self.num1 = 5
        self.__num2 = 10
 
    def getNumber(self):
        print(Test.__num2)
    
    def setNumber(self):
        self.__num2 =20
        
obj = Test()
obj.getNumber()
```
a) 10  
b) 20  
c) 30  
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)

<details><summary> <b>Explanation</b> </summary> 
  
> Class variable's value is printed through getNumber() method using `Class_Name.variable_name`. 
  </details>
</details>

---
7. What is the output of the following code?
```python3
class Test:
    __num2=30
    def __init__(self, __num2):
        self.__num2 = __num2
 
    def getNumber(self):
        print(self.__num2)
    
    def setNumber(self, __num2):
        self.__num2 =__num2
        
obj = Test(10)
obj.setNumber(20)
obj.getNumber()
```
a) 10  
b) 20  
c) 30   
d) Error   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> The current instance value, that is 20, is printed using `self.variable_name` when calling getNumber() method.  
  </details>
</details>

---
8. What is the output of the following code?
```python3
class Test:
    __num2=30
    def __init__(self, __num2):
        self.__num2 = __num2
 
    def getNumber(self):
        print(__num2)
    
    def setNumber(self, __num2):
        self.__num2 =__num2
        
obj = Test(10)
obj.setNumber(20)
obj.getNumber()
```
a) 10  
b) 20  
c) 30   
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> option is d) Error
<details><summary> <b>Explanation</b> </summary> 
  
> In the above code, we will get `"NameError: name '_Test__num2' which is not defined"`. To resolve this error, we have to use either `class_name` or `self` before the `__num2` variable in print statement, according to our need. For example, `self.__num2`. 
  </details>
</details>

---
9. What do we call the Private members of a class that can be accessed through methods of a class?

a) __init__ / __del__  
b) getters / setters  
c) __iter__ / __eq__  
d) __repr__ / __str__  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b) 
<details><summary> <b>Explanation</b> </summary> 
  
> The motive of using `getters` and `setters`functions in a class is to get[return] and set[assign] the private variables of a class. 
  </details>
</details>

---
10. What is name mangling in python? Give example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> In python, when we have some attributes in one class that we don't want to use in child classes, then we make them as private by adding two underscores('__') in prefix of variable name. So, to access those variables outside the class, we use name mangling concept. To access those private class variables, we have to add `_classname` with that variable.   
  
For Example:
```python3
class Student:
    def __init__(self, name):
        self.__name = name    # __name is private
  
obj = Student("Jack")
print(obj._Student__name)    # using name mangling we get output as Jack. 
```
</details>

---
11. State True and False: "Private variables of a class cannot be accessed outside the class".  

a) True  
b) False   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> Using name mangling, we can access the private members of a class. For that, we have to write `ObjectName._ClassName__VariableName`. 
  For example: `obj._Student__name`, where obj is object name, Student is a class name and __name is a private variable.
  </details>
</details>

---
12. Which of these is a protected data member of a class in python?
```python3
class Test:
    def __init__(self):
        __num1 = 0
        self._num2 = 0
        self.__num3__ = 0
        __num4__= 0
```
a) __num1  
b) _num2  
c) __num3__  
d) __num4__  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b) 
<details><summary> <b>Explanation</b> </summary> 
  
> Variables with single underscore (_) are the protected variables of a class. 
  </details>
</details>

---
13. Predict the output of the following code.
```python3
class Apple: 
    def __init__(self):
        self.price = 500
        self.__quantity = 5
        
    def display(self):
        print(self.price, self.__quantity)
        
obj = Apple()
obj.display()
```
a) 500 5  
b) 500 Error  
c) Error  
d) Nothing is printed   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option a)
<details><summary> <b>Explanation</b> </summary> 
  
>  __quantity is a private variable of a class, and private variables can be printed using class methods. 
  </details>
</details>

---
14. State True or False: " Private and Protected class variables can be accessed by name mangling".

a) True  
b) False  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b) 
<details><summary> <b>Explanation</b> </summary> 
 
> Private variables can be accessed by name mangling but protected variables cannot. 
  </details>
</details>

---
15. Predict the output of the following code.
```python3
class Design:
    _shape = "Square"
    def __init__(self):
        self.colour = None
        self._shape = "Rectangle" 
 
    def display(self, s):
        self._shape = s
obj=Design()
print(obj._Design_shape)
```
a) Square  
b) Rectangle  
c) Error  
d) Nothing is printed   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
 
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> In the above code, we will get `AttributeError: 'Design' object as no attribute '_Design_shape'` because,  _shape is a protected member of Design class and we cannot access protected members outside the class using name mangling.  
  </details>
</details>

---



