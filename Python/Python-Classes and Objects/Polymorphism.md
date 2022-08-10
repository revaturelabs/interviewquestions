# Polymorphism 


1. Explain polymorphism in Python? What are its type?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Polymorphism in python states that we can use the same function with same signature in both parent and child class. It allows the object to have multiple forms. Unlike other programming languages, python does not support compile time polymorphism, that is method overloading. If there are two functions with same name in a class, the last function specified will override the earlier one. It only supports the run time polymorphism, that is, method overriding.    
  
For example: 
```python3
#[method overriding]
class Bird:
  def intro(self):
    print("There are many types of birds.")
     
  def flight(self):
    print("Most of the birds can fly but some cannot.")
   
class sparrow(Bird):
  def flight(self):
    print("Sparrows can fly.")
    
obj1 =sparrow()
obj1.intro()     #output: There are many types of birds.
obj1.flight()   # it overrides the flight method of Bird class function.  #output: Sparrows can fly.  
```
</details>

---
2. Does python support method overloading and method overriding?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Python doesn't support method overloading but it supports method overriding. That is, we can define the same function in child and parent class with same signature and child's function overrides the parent class function. But when we define multiple functions with same name with different signatures and trying to call both with different number of argument passing, it executes the later one but gives error for trying to call the other functions as in namespace there will always be a single entry against each function name. let's see this with an example.   

#Example 1 
```python3
def add(a,b):
    return a+b 

def add(a,b,c):
    return a+b+c

print(add(2,4))
print(add(2,4,6))
```

> After writing and calling the above two methods together, we are getting `"TypeError: add() missing 1 required positional argument: 'c'"`. But if we commented the first calling function i.e add() with two arguments and call only the last function, it will execute and gives the output as 12. 
```python3
def add(a,b):
    return a+b 

def add(a,b,c):
    return a+b+c
# print(add(2,4))
print(add(2,4,6))   # output: 12 
```
</details>

---
3. What do you mean by method overriding?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Method overriding comes under runtime polymorphism and has the abilty by which a parent or base class functions can be redefined again in child or derived class. The method present in both parent and child should be same with same number of arguments.  
</details>

---
4. Which of the following holds true for polymorphism in python?

a) Ability to hide the complexity of code.  
b) Ability to inherit properties from base to subclass.  
c) Ability to restrict the access of data members from one class to another.   
d) Ability to override the functionality of parent class in child class.   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> In python, Polymorphism allows the child class to make changes in the functions present in parent class. 
  </details>
</details>

---
5. State True of False: "Polymorphism provides a default implementation of function overloading in python".

a) True    
b) False    

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> Suppose, if we define two functions with same name and different argument list in python, and when we try to call the first function, it will give error in the program. But, when we try to call the second function, it doesn't give the error and overrides the prior function and generates the output. 
  </details>
</details>

---
6. Predict the output of the following Code.
```python3
class Vehicle:
    def wheel(self):
        print("It can have 2 or more wheels")
        
class Car(Vehicle):
    def wheel(self):
        print("It has 4 wheels")

obj = Car()
obj.wheel()
```
a) It can have 2 or more wheels    
b) It has 4 wheels    
c) It has 4 wheels    
&emsp;It can have 2 or more wheels     
d) None of the above     

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> option is b) 
<details><summary> <b>Explanation</b> </summary> 
  
> Car class overrides the wheel() method of Vehicle class and therefore when calling the wheel() method of Car using object of Car class, it prints the statement present inside it. 
  </details>
</details>

---
7. Predict the output of the below code.
```python3
class Vehicle:
    def intro(self):
        print("It is a part of Vehicle class")
        
    def wheel(self):
        print("It can have 2 or more wheels")
    
class Car():
    def wheel(self):
        print("It has 4 wheels")

obj = Car()
obj.intro()
obj.wheel()
```
a) It has 4 wheels    
b) It is a part of Vehicle class  
&emsp;It can have 2 or more wheels  
c) It is a part of Vehicle class  
&emsp;It has 4 wheels  
d) Error   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> The above code will throw an `AttributeError` because Car class object is trying to call the method present inside Vehicle class which is not possible, as there is no relationship between Car and Vehicle class.
  </details>
</details>

---
8. Predict the output of the below code.
``` python3
class Vehicle:
    def intro(self):
        print("It is a part of Vehicle class")
        
    def wheel(self):
        print("It can have 2 or more wheels")
    
class Car(Vehicle):
    def wheel(self):
        print("It has 4 wheels")

obj = Car()
obj.intro()
obj.wheel()
```
a) It has 4 wheels  
b) It is a part of Vehicle class  
&emsp;It can have 2 or more wheels  
c) It is a part of Vehicle class  
&emsp;It has 4 wheels  
d) Error    

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c) 
<details><summary> <b>Explanation</b> </summary> 
  
> The Car class is a child class of Vehicle class, so it can access the methods present inside that class. Because of that intro() method of Vehicle class got executed when using the object of Car class and wheel() of Car class is executed, not of Vehicle, because of method overriding.
  </details>
</details>

---
9. What will be the output of the following code?
```python3
class Test:
    def __init__(self, a):
        self.a = a
        
    def add(self):
        self.a = 20
        return self.a
        
class Test1(Test):
    def add(self):
        self.a= self.a+10
        return self.a
        
obj = Test1(11)
print(obj.add()) 
```
a) 11  
b) 21  
c) 30   
d) 31   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> In the above code, the Test1 class method add() overrides the Test class method. Also while initalizing the value of a was 11 and after adding it with 10 in add(), it becomes 21 and hence the output.
  </details>
</details>

---
10. What is the output of the below code?
```python3
class Test:
    def __init__(self, a):
        self.a = a
        
    def add(self):
        self.a = 20
        return self.a
        
class Test1(Test):
    def add(self):
        self.a= a+10
        return self.a
        
obj = Test1(11)
print(obj.add())
```
a) 11  
b) 21  
c) 20   
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d) 
<details><summary> <b>Explanation</b> </summary> 
  
> The above code on execution will throw the `NameError`, as there is no 'a' variable defined in class Test1. 
  </details>
</details>

---
11. Predict the output of the following code.
```python3
class Test:
    def __init__(self, a):
        self.a = a
        
    def assign(self):
        return self.a
        
class Test1(Test):
    def __init__(self, a):
        super().__init__(a)
        
    def assign(self):
        return self.a

class Test2(Test1):
    def __init__(self, a):
        super().__init__(a)
        
    def assign(self):
        return self.a
        
obj1 = Test(11)
obj2 = Test1(12)
obj3 = Test2(13)
for i in (obj1, obj2, obj3):
    print(i.assign(), end=" ")
```
a) 11 11 11    
b) 11 12 11    
c) 11 12 13     
d) Error    

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> obj1, obj2, obj3 all three objects belongs to different classes and when assign() method is called using these objects, the statement present inside these is executed and hence we get the values as 11, 12 and 13.
  </details>
</details>

---
12. Which of the following is true about method overriding in python?  

a) Private method in a parent class can be overridden in a child class.  
b) Public method in a parent class can be overridden in a child class.  
c) Method Overriding is not possible in python.  
d) Any method of parent class can be overridden in a child class.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> option a) , c) and d) are incorrect because method overriding is possible in python and private methods of a base class cannot be overridden in a child class. 
  </details>
</details>

---
13. Predict the output of the below code?
```python3
class Test:
    
    def multiply(self, a, b):
        return a*b
    
    def multiply(self, a, b, c):
        return a*b*c
        
obj1 = Test()
print(obj1.multiply(10,20))
```
a) 20  
b) 10  
c) 200  
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> The above code will throw a `TypeError` because the default way of method overloading is not possible in python. Here, the later function overrides the previous function at the run time and so, three arguments are required to pass to multiply() method and not two at the time of calling. 
  </details>
</details>

---
14. Predict the output of the below code.
```python3
class Test:
    
    def multiply(self, a, b):
        return a*b
    
    def multiply(self, a, b, c):
        return a*b*c
        
obj1 = Test()
print(obj1.multiply(10,20,2))
```
a) 20  
b) 400  
c) 200  
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> As three arguments are passed to multiply() method of Test class, last method implementation is executed and we will get the result as multiplication of 10, 20 and 2 , which is 400.   
  </details>
</details>

---
15. Predict the output of the following code.
```python3
class Test:
    
    def multiply(self, a, b):
        return a*b
        
class Test1(Test):
    
    def multiply(self, a, b, c):
        return a*b*c
        
obj1 = Test1()
print(obj1.multiply(10,20))
```
a) 10  
b) 30  
c) 200  
d) Error  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> According to method overriding, parent class and child class method should have the same name with same number of arguments but, the multiply() method of Test class and multiply() method of Test1 class have different number of arguments, which leads to an error. While calling the mutliply() of Test1, 3 arguments are required but, only 2 passed. 
  </details>
</details>

---
16. Jack is trying the polymorphism concept in his code for the first time, he remembered something about method overriding and is able to create one method, in Parent class `Animal`, named as "leg()" and has given the implementation of leg() method. He also created one more class named as `Human` which inherited the Base class Animal. But he forgets what to write in Human class to complete the concept of method overriding and how to create an object of that class. Help Jack in solving his problem, and you have to create a leg() method in Human class which prints "Humans have legs" and create an object for the Human class to call leg() method. Given below has some code written, and write your logic in the spaces provided. 
```python3
class Animal:
    
    def leg(self):
        print("Not all Animals have legs")
        
class Human(Animal):
___________________
`````

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
```python3
class Animal:
    
    def leg(self):
        print("Not all Animals have legs")
        
class Human(Animal):
    
    def leg(self):
        print("Humans have legs")
        
obj1 = Human()
obj1.leg()
```
</details>

---
17. Create a class that shows the concept of method overloading in python?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Default implementation of method overloading is not possible in python, but we can implement and show overloading by passing default arguments to methods. Let's see how to do it. 
```python3
class Overloading:
    
    def add(self, x, y, z = 0):
        return x + y + z

obj = Overloading()
print(obj.add(10, 20))        # output: 30
print(obj.add(10, 20, 30))    # output: 60
```
> Here, we have passed different number of arguments at the time of calling, and we are getting different output as well for that. 
</details>

---
18. Show the polymorphism concept by using '+' operator inside a class. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> In python '+' operator is not only used to add values together but, it can also be used to concatenate two or more string values. Let's understand this better through a code.
```python3
class Operator:
    
    def add(self, x, y):
        return x + y
    
    def concatenate(self, a, b):
        return a + b

obj = Operator()
print(obj.add(10, 20))
print(obj.add("Akshay"," Bhadauria"))
```
</details>

---
19. Can `len()` function be used in polymorphism in python? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> In python, len() is used to find the length of different datatypes like string, list, tuple, etc. The below code will show how we can use len() function with different types of data.
```python3
print(len("Akshay"))           #Output: 6
print(len([1, 2, 3, 4]))       #Output: 4
print(len((1.5, 2.8, 3.3)))    #Output: 3 
```
> Different types of values are present in different print statements. First it is a string, then it is a list, and at last it is a tuple. The len() function is returing the length of these values. 
</details>

---
20. What is the use of polymorphism in python?

a) It allows to use the same code again and again.  
b) Programs that uses the polymorphism concepts takes less space in memory.   
c) We can hide the complexity through polymorphism.  
d) It allows the methods to have different implementation according to the class.   

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> It provides the way to create same method in different classes with different implementation. 
  </details>
</details>

---
21. Which of the following operator overloads the `__add__()` function?

a) +  
b) +=  
c) -  
d) -=  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option a)
</details>

---
22. Which operator is overloaded by the `__or__()` function?

a) ||  
b) |  
c) //  
d) /  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> The function __or__() overloads the bitwise OR operator '|'.
  </details>
</details>

---


