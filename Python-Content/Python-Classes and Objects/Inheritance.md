# Python Inheritance 


1. What do you mean by inheritance? Give example.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> Deriving the properties of one class to another is known as inheritance. In python, the class which takes the functionality of another class is known as child class or derived class and the class from which child class inherits is known as base class or parent class. For example, lets say human is a parent class and we inherit certain properties from it like ability to eat, think, drink, speak, etc.   

Syntax of Inheritance:
```
class Base:
  data members and member functions of base class
class Derived(Base):
   data members and member functions of derived class
```

Example in python:
```python3
class Human:
    def speak(self):
       print("speak") 
     
    def eat(self):
        print("eat")

class American(Human):
    def speak(self):
        print("English..")
    
    def eat(self):
        print("Bread and Cheese")
        
america = American()

america.speak()
america.eat()
``` 
</details>

---
2. Why inheritance is an important concept of OOPs in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> The key feature of inheritance is that it provides code re-usability. Means, we don't have to create the same code again and again instead we can simply inherit the properties of one class into another and use the functionality of base class to derive own functionlity in child class. 
</details>

---
3. What are the types of inheritance present in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> There are 5 types of inheritance in python:  
  
- Single inheritance 
- Multiple inheritance
- Multilevel inheritance
- Hierarchical inheritance
- Hybrid inheritance 
</details>

---
4. Explain single inheritance with an example.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
 
> When one class inherits the property of another class is known as single inheritance. Here only two classes are present, one is a child class and another one is a base class.     
  
For example: 
```python3
class Base:
    def fun(self):
        print("this is a parent class function")
        
class Derived(Base):
    def fun(self):
        print("this is a child class function")
    
obj = Derived()
obj.fun()
```
</details>

---
5. Explain multilevel inheritance with an example.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> When one derived class inherit the properties of another derived class is known as multilevel inheritance. For example, suppose there are three classes A, B and C. Class B inherits from class A and class C inherits from class B. Here A is a parent class of B and B is a parent class of C.  
 
Example in python:
```python3
class Base:
    def fun(self):
        print("hello i am from upper")
        
class Derived_1(Base):
    def fun1(self):
        print("hello i am from middle")

class Derived_2(Derived_1):
    def fun2(self):
        print("hello i am from lower")
    
obj = Derived_2()
obj.fun()     # output: hello i am from upper
obj.fun1()    # output: hello i am from middle
``` 
</details>

---
6. Explain multiple inheritance with an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> When a class inherit properties of more then 1 class then it is known as multiple inheritance. Here, there is only one derived class is present and base class can be two or more in number.   

For example:
```python3
class Father:
    def fun(self):
        print("I'm the Father")
        
class Mother:
    def fun1(self):
        print("I'm the Mother")

class Child(Mother, Father):
    def fun2(self):
        print("I'm the Child")
    
obj = Child()
obj.fun()   # output: I'm the Father
obj.fun2()  # output: I'm the Child 
```
</details>

---
7. Explain hierarchical inheritance with an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> When more then 1 derived class inherits from a single base class then it is known as hierarchical inheritance. There can be any number of derived class but only single base class is present.   

For Example: 
```
class Father:
    def fun(self):
        print("I'm the Father of two")
        
class Child_1(Father):
    def fun1(self):
        print("I'm the elder child")

class Child_2(Father):
    def fun2(self):
        print("I'm the younger child")
    
obj1 = Child_1()
obj2 = Child_2()
obj1.fun1()     # output: I'm the elder child
obj2.fun2()     # output: I'm the younger child 
```
</details>

---
8. Explain hybrid inheritance with an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> When in a program there are more then 1 type of inheritance is applied then that is called hybrid inheritance.  

For example: 
```python3
class GrandFather:
    def fun(self):
        print("I'm the Father of two")
        
class Child_1(GrandFather):
    def fun1(self):
        print("I'm the elder child")

class Child_2(GrandFather):
    def fun2(self):
        print("I'm the younger child")

class GrandChild(Child_1, Child_2):
    def fun3(self):
        print("I'm the grandchild")
    
obj1 = Child_1()
obj2 = Child_2()
obj3 = GrandChild()
obj1.fun1()   # output: I'm the elder child
obj2.fun2()   # output: I'm the younger child
obj3.fun()    # output: I'm the Father of two
```
</details>

---
9. Which of the following is the correct way of inheriting the `Company` class from `Department` class in python?

a) class Company : public Department  
b) class Department : protected Company  
c) class Department(Company)  
d) class Department extends Company   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> option c) 
<details><summary> <b>Explanation</b> </summary> 
  
> option a) and b) are used in C++ and option D) is used in Java to inherit one class from another. Hence option c) is correct.
  </details>
</details>

---
10. Which of the following correctly depicts the multi-level inheritance in Python?

a) class B(A):  
b) class B(A):    
&emsp;class C(B):  
c) class B(A):  
&emsp;class C(A):  
d) class C(A,B):  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> option b)
<details><summary> <b>Explanation</b> </summary> 
  
> Option a) depicts single inheritance, option c) depicts hierarchical inheritance, and option d) multiple inheritance.
  </details>
</details>

---
11. Which of the following correctly depicts the multiple inheritance in Python?

a) class B(A):  
b) class B(A):    
&emsp;class C(B):  
c) class B(A):  
&emsp;class C(A):  
d) class C(A,B):  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> option d)
<details><summary> <b>Explanation</b> </summary> 
  
> Option a) depicts single inheritance, option c) depicts hierarchical inheritance, and option b) multi-level inheritance.
  </details>
</details>

---
12. Which of the following correctly depicts the hierarchical inheritance in Python?

a) class B(A):    
b) class B(A):     
&emsp;class C(B):    
c) class B(A):  
&emsp;class C(A):  
d) class C(A,B):  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> option c)
<details><summary> <b>Explanation</b> </summary>
  
> Option a) depicts single inheritance, option d) depicts multiple inheritance, and option b) multi-level inheritance.
  </details>
</details>

---
13. Suppose class Department is a child of Company class, to invoke the `__init__()` in Company from Department, what line of code you will write?

a) `Company.__init__(self)` 
b) `Company.__init__(Department)`  
c) `Department.__init__(self)`  
d) `Department.__init__(Company)`  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option a)
<details><summary> <b>Explanation</b> </summary>
  
> To invoke the `__init__()` method of parent class from child class, we have to write `Parent_ClassName.__init__(self)` inside child class. 
  </details>
</details>

---
14.Which is not a type of inheritance?

a) Hybrid  
b) Single-level  
c) Double-level  
d) Multiple   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>
  
> option c) 
<details><summary> <b>Explanation</b> </summary>
  
> There is no double level inheritance present in python.
  </details>
</details>

---
15. Predict the output of the following code.
```python3
class Company():
    def show(self):
        print("Revature Company")
    
class Department(Company):
    def show(self):
        print("Training Department")
    
obj1 = Company()
obj2 = Department()
obj1.show() 
obj2.show()
```
a) Error  
b) Revature Company    
&emsp;Training Department  
c) Revature Company  
d) Training Department  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> obj1 and obj2 are referring to different classes and they are calling the show() method of different classes. 
  </details>
</details>

---
16. Predict the output of the following code.
```python3
class Company():
    def showName(self):
        print("Revature Company")
    
class Department(Company):
    def show(self):
        print("Training Department")
    
obj1 = Company()
obj2 = Department()
obj1.show()
obj2.showName() 
```
a) Revature Company  
&emsp;Training Department  
b) Training Department  
&emsp;Revature Company   
c) Error  
d) Nothing is printed  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option c) 
<details><summary> <b>Explanation</b> </summary>
  
> The above code Throws the AttributeError while calling `obj1.show()` because there is no show method present inside Company class. 
  </details>
</details>

---
17. Predict the output of the following code.
```python3
class Company():
    def showName(self):
        print("Revature Company")
    
class Department(Company):
    def show(self):
        print("Training Department")
    
obj1 = Company()
obj2 = Department()
obj2.showName() 
obj1.showName()
```
a) Revature Company  
&emsp;Training Department  
b) Revature Company  
&emsp;Revature Company   
c) Training Department  
&emsp;Revature Company   
d) Training Department   
&emsp;Training Department  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> Both obj1 and obj2 are referring to the same class method. And obj2 of Department class can refer to method of Company class because Department class inherits the Company in above code. 
  </details>
</details>

---
18. Predict the output of the below mentioned code.
```python3
class Company():
    name = "Jack"
    def __init__(self):
        self.__name="James"
    
class Department(Company):
    def show(self):
        print(self.__name)
    
obj1 = Company()
obj2 = Department()
obj2.show()
```
a) James  
b) Jack  
c) Error, no use of obj1 object   
d) Error, accessing private class member in subclass can't possible   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option d)
<details><summary> <b>Explanation</b> </summary>
  
> '__name' is a private data member of Company class and private members of one class cannot be accessed in another class in python. 
  </details>
</details>

---
19. What is the output of the following code?
```python3
class Company():
    _name = "Jack"
    def __init__(self):
        self._name = "James"
    
class Department(Company):
    def show(self):
        print(self._name)
    
obj1 = Company()
obj2 = Department()
obj2.show()
```
a) James  
b) Jack  
c) Error, no use of obj1 object   
d) Error, accessing private class member in subclass can't possible   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>
  
> Option a) 
<details><summary> <b>Explanation</b> </summary>
  
> '_name'is a protected data member of Company class and protected members of one class can be accessed by another class through inheritance.
  </details> 
</details>

---
20. What `super()` do in python? ive example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> `super()` in python is a method, used in child class to access the functions defined in parent class. This helps in code reuseability as we don't have to implement the function of parent class again in child class.   
  
For example:
```
class School():
    def __init__(self):
        self.name = "Jack"
    
    def show(self):
        print(self.name)
    
class Student(School):
    def show(self):
        super().show()        # use of super()
    
obj2 = Student()
obj2.show()             # output: Jack
```
</details>

---
21. Which is a wrong statement regarding inheritance?

a) A class cannot inherits more then two classes in python  
b) protected members of a parent class can be accessed by child class.  
c) public members of a parent class can be used in child class and other classes also.  
d) In single inheritance one class inherits the other class.   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>
  
> Option a)
<details><summary> <b>Explanation</b> </summary>
  
> A class can inherits any number of classes in python. 
  </details>
</details>

---
22. Predict the output of the below code.
```python3
class Test:
    def __init__(self):
        self.a = 4
        
class Test2(Test):
    def __init__(self):
        super().__init__()
        self.b = 6

obj= Test2()
print(obj.a,obj.b)
```
a) 4  
b) 6  
c) 4 6  
d) Error, no attribute named "a" present in Test2 class.  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> c) 4 6 
<details><summary> <b>Explanation</b> </summary>
  
> `super()` is used to access the members of parent class in child class. 
  </details>
</details>

---
23. Predict the output of the below code.
```python3
class Test:
    def __init__(self):
        self.a = 4
        
class Test2(Test):
    def __init__(self):
        self.b = 6

obj= Test2()
print(obj.a,obj.b)
```
a) 4  
b) 6  
c) 4 6  
d) Error, no attribute named "a" present in Test2 class.  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option d)
<details><summary> <b>Explanation</b> </summary>
  
> The above code throws `"AttributeError: 'Test2' object has no attribute 'a'"`. 
  </details>
</details>
  
---
24. Which of the following is true regarding inheritance?

a) It is a part of Object Oriented Programming  
b) It gives the concept of accessing properties of one class to other.  
c) It reduces code repetition.  
d) All of the above.   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> option d)  
</details>

---
25. Which type of inheritance is shown in the below code?
```python3
class A:
    pass
class B(A):
    pass
class C(B,A):
    def show(self):
        print("hello")

obj =C()
obj.show()
```
a) Multiple Inheritance  
b) Hybrid Inheritance  
c) Multilevel Inheritance  
d) Single Inheritance  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> In the above code more than two types of inheritance is used, that is Single and Multiple. That is why it is a type of hybrid inheritance.
  </details>
</details>

---
26. What error will be shown if you run the below code and how to resolve that error?
```python3
class A:
    pass
class B(A):
    pass
class C(A,B):
    def show(self):
        print("hello")

obj =C()
obj.show()
```
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> TypeError: Cannot create a consistent method resolution order (MRO) for bases A, B. 

<details><summary> <b>Explanation</b> </summary>
  
> The reason for the above error is that, we are trying to inherit the class A before the class B in C class. And as A class is the parent of B class we should inherit the B class first than A class in class C. This will resolve the Error of the above code. Just change the line ```class C(A,B) to class C(B,A)```. 
  </details>
</details>

---
27. State True and False: "super() function makes the child class to inherit all the data members and member functions from its parent class in python". 

a) True   
b) False  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> Option a) 
<details><summary> <b>Explanation</b> </summary>
  
> We can use the super() function in child classes to inherit all the members of parent class.
  </details>
</details>

---
28. Suppose there are three classes, Animal, Dog, and Cat. Class Dog inherits properties from Animal class and class Cat also inherits properties from Animal class, than which type of inheritance can be depicted from the above scenario?

a) Multilevel Inheritance  
b) Multiple Inheritance  
c) Hierarchical Inheritance  
d) Hybrid Inheritance   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c)
<details><summary> <b>Explanation</b> </summary>
  
> In the above scenario, class Animal is a parent class of both Dog and Cat class. Also Dog and Cat both classes inherits from the same base class that is Animal class. So, Dog and Cat are derived classes of same base class, which is the definition of Hierarchical inheritance. 
  </details>
</details>

---
29. Suppose there are three classes, Father, Mother and Child. The Child class inherits properties from two classes, Father and Mother class, than which type of inheritance can be depicted from the above scenario? 

a) Multilevel Inheritance  
b) Multiple Inheritance  
c) Hierarchical Inheritance  
d) Hybrid Inheritance   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> option b) Multiple Inheritance. 
<details><summary> <b>Explanation</b> </summary>
  
> By the definition, Multiple inheritance states that one derived class can inherits properties from more than 1 base class. In the above scenario also, we can see that Child class  is a derived class which inherits all the properties from the 2 base classes, that is Father and Mother class. 
  </details>
</details>

---
30. Suppose there are three classes, Car, Maruti_Alto and Maruti_Arena. Maruti_Alto inherit the Car class and Maruti_Arena inherit the Maruti_Alto class, than which type of inheritance can be depicted from the above scenario? 

a) Multilevel Inheritance  
b) Multiple Inheritance  
c) Hierarchical Inheritance  
d) Hybrid Inheritance   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option a)
<details><summary> <b>Explanation</b> </summary>
  
> As we can see in the above scenario, when Maruti_Alto inherit the Car class, the Car class becomes the parent class and Maruti_Alto becomes the child class. But when Maruti_Arena inherit the Maruti_Alto class, the Maruti_Arena becomes the child class of Maruti_Alto, which was already a derived class of Car class. Therefore, the relation is of type multilevel inheritance. 
  </details>
</details> 

---
31. Predict the output of the following code.
```python3
class Test:
    def __init__(self, num1= 1):
        self.num1 = num1
        
class Test1(Test):
    def __init__(self,num2 = 2):
        super().__init__()
        self.num2 = num2+2

obj = Test1()
print(obj.num1, obj.num2)
```
a) 1 2  
b) 1 4  
c) 1 Error  
d) Nothing is printed  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> Simply the object of Test1 class is printing the values of num1 and num2.
  </details>
</details>

---
32. Predict the output of the below code.
```python3
class Test:
    def __init__(self, num1= 1):
        self.num1 = num1
        
class Test1:
    def __init__(self,num2 = 2):
        super().__init__()
        self.num2 = num2+2

obj = Test1()
print(obj.num1, obj.num2)
```
a) 1 2  
b) 1 4  
c) Error  
d) None of the above.  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c)
<details><summary> <b>Explanation</b> </summary>
  
> The above code will throw `"AttributeError: 'Test1' object has no attribute 'num1'"` because Test1 class is not a child of Test class and cannot inherit the things of Test class directly. 
  </details>
</details>

---
33. Predict the output of the following code.
```python3
class Sample:
    
    @staticmethod
    def sample(): 
        print("This sample will run first")
    
class Sample1(Sample):
    
    @staticmethod
    def sample(): 
        print("This sample will run second") 
    
Sample1.sample()
```
a) This sample will run first  
b) This sample will run second  
c) Error, because object is not created.  
d) None of the above  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option b)
<details><summary> <b>Explanation</b> </summary>
  
> In the above code, `@staticmethod` decorater is used which makes the function inside the class as Static and that can be accessed outside the class with the help of Class_Name. 
  </details>
</details>

---

