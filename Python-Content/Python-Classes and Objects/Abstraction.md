# Abstraction 


1. Explain Abstraction? How to achieve abstraction in python? Give an example. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Abstraction refers to hiding of unnecessary data from the user and showing only the relevant part in order to reduce complexity and increase the efficiency of program. For example,let's take social media platforms where we share photos, chat, etc., with friends without knowing how all these happens in background.    
  
> We can achieve abstraction in python by creating abstract classes in our program. 
  
> By default, python doesn't provide any implementation to create abstract class. There is a module in python that provides the way to create abstract classes and that module name is `ABC`[Abstract Base Classes]. Let's see an example that clears all the doubt.    
```python3
# example for abstract class
from abc import ABC, abstractmethod
 
class Vehicle(ABC):
 
    @abstractmethod
    def sound(self):
        pass
 
class Car(Vehicle):
 
    # overriding abstract method
    def sound(self):
        print("Zoom-Zoom...!!") 

c = Car()
c.sound()  # output: Zoom-Zoom...!!
```
</details>

---
2. Does python have a interface concept?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> In python, there is no concept of interface. Python doesn't have any interface keyword like it has for class. So, we can only use the abstract base class that let us define abstract methods inside it and those methods should be implemented by derived classes.

</details>

---
3. What is an abstract base class in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> Abstract base class provides a way to declare methods without implementation, and these methods must be implemented by derived classes. It has an advantage of hiding irrelevant or complex implementation from user. We cannot create object for abstract base class in python. 
</details>

---
4. Which of the following is true regarding abstract class in python?  

a) Abstract classes can be instantiated.    
b) Abstract classes can have only abstract methods.    
c) We can create abstract class using abstract keyword.    
d) Abstract classes can have both abstract methods and non-abstract methods.    

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> Option d)
<details><summary> <b>Explanation</b> </summary>
  
> In abstract classes, we can create abstract methods along with non-abstract methods.
  </details>
</details>

---
5. Can we create abstract class by just passing `pass` inside method definition in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> We can directly create classes in python which have some methods without definition but, these classes are not called as abstract base class because python doesn't have default implementation of abstract classes. And there is no such keyword as abstract through which we can create a abstract class or method. To create a abstract class in python, we have to import `abc` module which provides the way to create abstract class which can have abstract and non abstract methods. 
</details>

---
6. Predict the output of the following code.
```python3
from abc import ABC, abstractmethod
class Abstract(ABC):
 
    @abstractmethod
    def path(self):
        pass
    
    def show(self):
        print("Reached NY")
        
class Derived(Abstract):
    def path(self):
        print("60 km away from NY")

obj = Derived()
obj.path()
```
a) Reached NY  
b) 60 km away from NY  
c) Error  
d) Nothing is printed   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> option b) 
<details><summary> <b>Explanation</b> </summary>
  
> Derived class called its own method path() and hence, statement inside path() method is executed. Hence, we got the output as "60 km away from NY".
  </details>
</details>

---
7.  Predict the output of the following code.
```python3 
from abc import ABC, abstractmethod
class Abstract(ABC):
 
    @abstractmethod
    def path(self):
        pass
    
    def show(self):
        print("Reached NY")
        
class Derived(Abstract):
    def path(self):
        print("60 km away from NY")

obj = Derived()
obj.show()
```
a) Reached NY  
b) 60 km away from NY  
c) Error  
d) Nothing is printed   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> Option a)
<details><summary> <b>Explanation</b> </summary>
  
> Object of Derived class called the show() method of Abstract class and as show() method is a non-abstract method of Abstract class, its inside statement gets executed.
  </details>
</details>

---
8. Predict the output of the below code.
```python3
from abc import ABC, abstractmethod
class Abstract(ABC):
 
    @abstractmethod
    def path(self):
        pass
    
    def show(self):
        print("Reached NY")
        
class Derived(Abstract):
    def path(self):
        print("60 km away from NY")

obj = Abstract()
obj.show()
```
a) Reached NY  
b) 60 km away from NY  
c) Error  
d) Nothing is printed  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c)
<details><summary> <b>Explanation</b> </summary>
  
> After executing the above code, we will get the Error stating that Abstract class cannot be instantiated as it is abstract base class in python.
  </details>
</details>

---
9. What is the output of the following code?
```python3
from abc import ABC, abstractmethod
class Abstract(ABC):
 
    @abstractmethod
    def path(self):
        pass
    
    def show(self):
        print("Reached NY")
        
class Derived(Abstract):
    pass

obj = Derived()
obj.path()
```
a) Reached NY   
b) pass  
c) Error, because Derived class is an abstract class.  
d) Nothing is printed   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option c)
<details><summary> <b>Explanation</b> </summary>
  
> We will get the ```TypeError: Can't instantiate abstract class Derived with abstract methods path```. This is because we have not provided any implementation to path() method of Abstract class in Derived class. Therefore, derived class also becomes abstract class. 
  </details>
</details>

---
10. What is the output of the following?
```python3
from abc import ABC, abstractmethod
class Abstract(ABC):
 
    @abstractmethod
    def path(self):
        pass
    
    def show(self):
        print("Reached NY")
        
class Derived(Abstract):
    
    def path(self):
        pass

obj = Derived()
obj.path()
```
a) Reached NY   
b) pass  
c) Error, because Derived class is an abstract class.  
d) Nothing is printed   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> Option d)
<details><summary> <b>Explanation</b> </summary>
  
> The path() method of Derived class has implemented the path() method of Abstract class by just providing `pass` statement in the method definition. `pass` is a null statement in python and so, nothing is printed in the console [output screen].
  </details>
</details>

---
11. Which module is required to be imported for creating abstract class in python? 

a) ast  
b) abc  
c) re  
d) sys   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>
  
> option b) `abc` 
</details>

---



