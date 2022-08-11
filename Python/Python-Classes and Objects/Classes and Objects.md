# Classes and Objects 


1. What do you understand by Object-Oriented Programming? What are its main features?
   
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
   
> Object-Oriented Programming refers to the programming style related with classes and objects. Here the object is a real world entity and a class is a blueprint to that object. For example, we can consider a 'Car' as a class and maruti suzuki or honda as an object.   
  
> Python is a OOP language.So,it supports all OOPs concepts such as Polymorphism, Inheritance, Encapsulation and Abstraction. Polymorphism in python defines method in child class have same name as method in parent class. Inheritance means the child class can inherits the properties from its parent class. Encapsulation is wrapping up of data and member functions together in same unit. And finally abstraction means hiding the irrelevent data from user showing only the important part or functionality. 
</details>

---
2. Why OOPs concepts important in programming?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> There are many reasons why one should go for programming languages that supports OOPs concepts like Python. Some of the reasons are: 
> - Problems can be divided into different parts making it simple to solve. 
> - Code reusibility increases thereby reducing redundancy.
> - Functions implementations will be hidden by user, making it more simpler to understand. For example, we can directly use the append() method of a list to add an item without knowing how append() method works internally. 
> - OOPs ensures Data Safety as well. 
</details> 

---
3. What do u mean by class and object in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> A class, in python, is a user defined datatype and also a blueprint of an object. Class provides a way of binding data and member functions together. An object is an instance of a class and a real world entity. For example, A gender can be considered as a class and male and female as an object of that class. 

Example in python:
```python3
class Gender:
    def fun1(self):
        print("I'm male..!!")
        
    def fun2(self):
        print("I'm female..!!")
    
male = Gender()
male.fun1()
```
</details>

---
4. What is a constructor in python? Give example.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Constructor is a method that is used to initialize the variable and are called when an object of a class is created. In python we can use the `__init__()` method that is a constructor, unlike in other programming language where both class name and constructor name should be same. The statements present inside the constructor are executed at the time of object creation. 

For Example:
```python3
class Student:
    name= "akshay"
    age =22
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show(self):
        print(self.name, end=" ")
        print(self.age)
obj = Student("rohit", 23)
obj.show()   # output: rohit 23 
```
</details>

---
5. Does python support constructor overloading? If yes, then how?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Python doesn't support constructor overloading i.e., we can not create two constructor, within same class, with different arguments. But there is a way in python through which we can make a constructor that can work in different way when we pass different number of arguments at the time of object creation. We can pass number of default arguments to `__init__()` method to make it as constructor overloading. 

For example: 
```python3
class Student:
    
    def __init__(self, name1, name2 =None, name3= None):   # using parameters name2 and name3 and assigning Default value None to both.
        self.name1 =name1
        self.name2 =name2
        self.name3 =name3 
    
    def getname(self):
        return self.name1, self.name2, self.name3

obj = Student("akshay")              # passing 1 argument
obj1 = Student("akshay", "rohit")    # passing 2 argument
print(obj.getname())           # output: ('akshay', None, None)
print(obj1.getname())          # output: ('akshay', 'rohit', None)
```
</details>

--- 
6. What is a self in class and python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> The self is a first parameter of every method in a class, and is used to refer the current class instance. There is no restriction in python to name it as self, it can be named whatever we like, but it has to be the first parameter of a method.   
  
For Example:
```python3
class Student:
    name= "akshay"
    age =22
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show(current):
        print(current.name, end =" ")  # here we used the name as current instead of self to refer the instance of a class.
        print(current.age)
obj = Student("rohit", 23)
obj.show()
```
</details>

---
7. State True and False: "self is a keyword in python".  

a) True  
b) False  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) False.
<details><summary> <b>Explanation</b> </summary>
  
> self is not a keyword in python, it is a parameter to a function and we can use any other name also in place of self, but it is advisable to use self as it increases the code readability. 
  </details>
</details>

---
8. Which of the following is the correct way of creating an object of a class `Student` in python?

a) Student obj = new Student();  
b) obj Student = new Student();  
c) obj = Student()  
d) Student obj;  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c) obj =Student()
<details><summary> <b>Explanation</b> </summary>
  
> options a) and d) are incorrect because this is how we can create a object in java and c++ respectively, not in python.
  </details>
</details>

---
9. What is the output of the following code?
```python3
class Student:
    name= "Henry"
    age =22
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show(current):
        print(current.name, end =" ")
        print(current.age)

obj = Student("James", 23)
obj.show()
```
a) Henry 22    
b) James 23    
c) Error, because self is not used as a parameter in show().    
d) None    

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) James 23 
<details><summary> <b>Explanation</b> </summary>
  
> option b) is corrent because both the print statements inside show() method is pointing to the current instance of a class, using current parameter. 
  </details>
</details>

---
10. What is the output of the following code?
```python3
class Student:
    name= "Henry"
    age =22
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show(current):
        print(Student.name, end =" ")
        print(current.age)

obj = Student("James", 23)
obj.show()
```
a) Henry 22  
b) James 23  
c) Error, because self is not used as a parameter in show().  
d) Henry 23   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option d) Henry 23 
<details><summary> <b>Explanation</b> </summary>
  
> In show() method, the 1st print statement is referring the class variable using the class name `Student`. And in 2nd print statement it is referring to instance variable through current parameter. Hence option d) is correct. 
  </details>
</details>

---
11. Predict the output of the given code.
```python3
class Student:
    name = "Henry"
    age = 22
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show():
        print(self.name, end =" ")
        print(Student.age)
obj = Student("James", 23)
obj.show()
```
a) Henry 22  
b) James 23  
c) Error   
d) No output  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
  
> Option c)
  
<details><summary> <b>Explanation</b> </summary>
  
> The above code will generate TypeError as no parameter is being passed to show() method. Adding self in the show() method definition should resolve the problem. 
  </details>
</details>

---
12. What are the different access modifiers present in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python, There are 3 types of access modifiers:  
- public access modifier  
- private access modifier  
- protected access modifier   
  
- i) Public access modifier: In python, anything by default inside a class is public whether it is a data member or member function. These members of a class can be easily accessible from any part of the program.  
For example: name = "Henry"   
  
- ii) Protected access modifier: In python, if you want to declare any member of a class as protected then you have to use single underscore '_' symbol before the members of that class. These members of a class can only be accessible to the same class as well to the derived class.  
For example: _name = "Henry"  
  
- iii) Private access modifier:  In python, if you want to declare any member of a class as private then you have to use double underscore '__' symbol before the members of that class. These members of a class can only be accessible within a class.  
For example: __name = "Henry"  
</details>

--- 
13. In Python, all classes have a function known as____.

a) `__inti__()`  
b) `__init__()`  
c) `init`  
d) `__int__()`  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b) __init__()
<details><summary> <b>Explanation</b> </summary>
  
>  `__init__()` is a constructor in python, rest all are wrong. 
  </details>
</details>
  
---
14. Which keyword can be used to delete the objects of a class in python?

a) delete  
b) remove   
c) pop   
d) del   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option d)
<details><summary> <b>Explanation</b> </summary>
  
> Through `del` we can delete objects created for a class. 
For example:
```python3
class Student:
    def __init__(self, name, age):
        self.name= name
        self.age =age
        
    def show(self):
        print(self.name, end =" ")
        print(self.age)
obj = Student("James", 23)
obj.show()
del obj      # this will delete obj object of Student class
obj.show()   # this will throw "NameError: name 'obj' is not defined"
```
  </details>
</details>

---
15. Variable that is defined inside a method of a class and its value varies from object to object is known as?

a) Instance variable  
b) Class variable   
c) Method variable  
d) Block variable   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option a) 
<details><summary> <b>Explanation</b> </summary>
  
> An instance variable is a variable whose value varies from object to object. These variables are not shared by objects. 
  </details>
</details>

---
16. What is the difference between instance variable and class variable?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> **Instance variables** are declared inside the method or a constructor of a class. They are not shared by any objects. Every object has its own copy of the instance variable.    
    
> **Class variables** are declared inside the class but outside any method. These variables are shared accross all the objects of a class. Any change to the class variable will reflect to all the objects of that class.     
    
For example: 
```python3
class Student:
    name ="Henry"      # class variable
    def __init__(self, name):
        self.name= name    # instance variable
        
    def show(self):
        print(self.name)

obj = Student("James")
print(Student.name)     # output: Henry
obj.show()         # output: James
```
</details>

---
17. Predict the output of the following code. 
```python3
class Student:
    name ="James"
    def __init__(self, name):
        self.name = name
        
    def show(self):
        print(self.name)
        
obj = Student()
obj.show()
```
a) It prints output as James  
b) It prints the garbage value  
c) Error as one argument is required while creating the object  
d) Error as show() function requires additional argument   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c) 
<details><summary> <b>Explanation</b> </summary>
  
> During object creation, 1 argument is requried because `__init__()` method has another argument name other than self. For example `obj= Student("Henry")`
  </details>
</details>

---
18. State True and False: "`__init__()` is a constructor and public method in python".  

a) True  
b) False  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b) False. 
<details><summary> <b>Explanation</b> </summary>
  
>  `__init__()` is a private method and a constructor in python. 
  </details>
</details>

---
19. John is creating a class named `Dog`, which has `__init__()` method that has one parameter as "name". He forgets how to create a "getName()" method that returns the name when the method is called and a "setName()" method which sets the value for 'name' parameter. Given below is an incomplete piece of code, help john to make his code working. Provide your logic in the given spaces.
```python3
class Dog:
    def __init__(self, name=None):
        self.name = name
        
    # write your logic here

obj = Dog()
obj.setName("puppy")
print(obj.getName())
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
``` python3
class Dog:
    def __init__(self, name=None):
        self.name = name
        
    def getName(self):
        return self.name
    
    def setName(self, name):
        self.name =name

obj = Dog()
obj.setName("puppy")
print(obj.getName())
```
</details>

---
20. Predict the output of the following code.
```python3
class Girl():

    def __init__(self, name):
      self.name = name

    def namePrint(self):
      print(self.name)

girl1 = Girl("Emma")
girl2 = Girl("Ava")
girl1.namePrint()
```
a) Emma  
b) Ava  
c) Emma     
&emsp;Ava     
d) Error  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option a) Emma
<details><summary> <b>Explanation</b> </summary>
  
> Only the girl1 object is calling the namePrint() method, so only the value stored in girl1 object is printed, that is "Emma".
  </details>
</details>

---
21. Which of the following statements is incorrect about the below code?
```python3
class Girl():

    def __init__(self, name):
      self.name = name

    def namePrint(self):
      print(self.name)

girl1 = Girl("Emma")
girl2 = Girl("Ava")
girl1.namePrint()
```
a) The `__init__` method is used to set initial values for attributes. 
b) 'self' is not needed in namePrint() method
c) girl1 and girl2 are two different instances of the Girl class.
d) girl2 has a different value for 'name' than girl1.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> 'self' is used to represent the current instance of the class and is compulsory to have self for every method inside the class in python. 
  </details>
</details>

---
22. Which of the following is wrong statement for OOPs in python?  

a) OOPs can hide complexity.  
b) Class can contain functions as well as data  
c) Constructor methods are required to initialize an object   
d) Ability to create a new class by extending an existing class. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option c).
<details><summary> <b>Explanation</b> </summary>
  
> A constructor is optional and can be used to set initial values for an object in python.
  </details>
</details>

---
23. The ______ is used to store the data members and functions together in python.

a) method    
b) class    
c) object    
d) instance    

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b) class
</details>

---
24. ______ is not a keyword, but by convention it is used to refer to the current instance of a class. 

a) this  
b) super  
c) init  
d) self   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option d) self.
</details>

---
25. State True or False: In order to extend a class, the child class should have access to all the data and functions of the parent class.

a) True  
b) False   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) False
<details><summary> <b>Explanation</b> </summary>
  
> The child class does not need access to the all the functions in parent class.
  </details>
</details>

---
26. Which of the following is wrong with respect to objects in python?  

a) Objects are real world enitites.  
b) Object is an instance of a class.  
c) We can create objects based on the number of methods present inside a class  
d) Python treats everything as objects including variables, functions, list, tuple, ect.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
 
> option c) 
<details><summary> <b>Explanation</b> </summary>
  
> There is no restriction in the number of objects that can be created for a class in python, but by convention it should be meaningful.
  </details>
</details>

---
27. How many objects and reference variables are there for the given python program?
```python3
class Student():
    print("hello-world")
    
Student()
Student()
obj= Student()
```
a) 3 and 1  
b) 2 and 1  
c) 1 and 3  
d) 3 and 3  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option a) 
<details><summary> <b>Explanation</b> </summary>
  
> In the above code, 3 objects are present, two without reference variable and 1 with reference variable, `Obj = student()`. 
  </details>
</details>

---
28. Odd one out: Which is not comes under four pillers of OOPs in python?

a) Encapsulation  
b) Instantiation  
c) Inheritance   
d) Polymorphism   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) Instantiation.
<details><summary> <b>Explanation</b> </summary>
  
> 4 pillers of OOPs are, Abstraction, Polymorphism, Encapsulation, Inheritance. 
  </details>
</details>

---
29. Predict the output of the following code.
```python3
class Number():
    def __init__(self, num):
       self.num = num 
       num = 50
       
n = Number(60)
print(n.num)
```
a) 50  
b) 60  
c) Error  
d) None of the above  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) 60. 
<details><summary> <b>Explanation</b> </summary>
  
> In the above code, self is pointing to the current instance of the class which has the value 60. 
  </details>
</details>

---
30. Predict the output of the following code.
```python3
class Test:
    a = 10
    def __init__(self, a=0):
        self.a = a
        
    def assign(self, a):
        return self.a
        
obj1 = Test(11)
print(obj1.assign(12))
```
a) 10    
b) 11    
c) 12    
d) Error, too many 'a' variable used   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b) 11
<details><summary> <b>Explanation</b> </summary>
  
> assign() method returns the current instance variable's value, which is 11 at that time. Hence the output.
  </details>
</details>

---
31. Predict the output of the following code.
```python3
class Test:
    a = 10
    def __init__(self, a=0):
        self.a = a
        
    def assign(self, a):
        return Test.a
        
obj1 = Test(11)
print(obj1.assign(12))
```
a) 10  
b) 11  
c) 12  
d) Error, too many 'a' variable used 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option a) 10
<details><summary> <b>Explanation</b> </summary>
  
> assign() method returns the class variable's value, which is 10 at that time. Hence the output.
  </details>
</details>

---
32. Predict the output of the following code.
```python3
class Test:
    a = 10
    def __init__(self, a=0):
        self.a = a
        
    def assign(self, a):
        return Test.a
        
obj1 = Test(11)
print(obj1.assign(12))
```
a) 10  
b) 11  
c) 12  
d) Error, too many 'a' variable used   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option c) 12
<details><summary> <b>Explanation</b> </summary>
  
> assign() method returns the parameter's value of assign(), that was assign to it as 12 at the time of calling. Hence the output.
  </details>
</details>

---
33. State True and False: "It is mandatory to create a class with Starting letter in capital in python".

a) True  
b) False  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b) 
<details><summary> <b>Explanation</b> </summary>
  
> It is not mandatory to have a class with starting letter in uppercase but, it is recommended to make a class with starting letter in capital in python. 
  </details>
</details>

---
34. Predict the output of the following code.
```python3
class Dance:
    @staticmethod
    def moves():
        print("body moves started")

    def stop(self):
        print("body moves stoped")

Dance.stop()
```
a) body moves started    
b) body moves stoped    
c) Error    
d) Nothing will print     

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c) 
<details><summary> <b>Explanation</b> </summary>
  
> As stop() is not a Static method of Dance class, We can not access it without creating the object for it. 
  </details>
</details>

---


 

