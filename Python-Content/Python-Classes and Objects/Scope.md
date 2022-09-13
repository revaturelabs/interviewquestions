# Scopes in python [in class] 


1. What do you mean by global scope in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> The object name that is defined in a main program or in a module comes under global scope. They could be used outside any function or block of code. It can access the built-in namespace objects. 
</details>

---
2. What do you mean by local scope in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> The variable names defined in a class, function, loop or in any block of code comes under local scope. In python, these variables cannot be accessed by outer Namespace. Local namespace can access the global namespace objects and built-in namespace. 
</details>

---
3. Predict the output of the following code.
```python3
x = 40
class Test:
    x =20 
    def show(self):
        print(x)
    
obj = Test()
print(x)
obj.show()
``` 

a) 20    
&emsp;20   
b) 20     
&emsp;40  
c) 40     
&emsp;20  
d) 40    
&emsp;40   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> option is d) 
<details><summary> <b>Explanation</b> </summary> 
  
> Before method calling, the first print statement prints the value of global variable i.e 40. And when the show() method is called, the print statement present inside will also print the value of x as 40 not 20, because x= 20 is a class variable which must be accessed by using classname before variable name. Therefore, it will also take the global variable value i.e 40 in this case.
  </details>
</details>

---
4. Predict the output of the following code. 
``` python3
x = 40
class Test:
    x = 10
    def show(self):
        self.x = 20
        print(x)
    
obj = Test()
print(Test.x)
obj.show() 
```
a) 10     
&emsp;40   
b) 10    
&emsp;20   
c) 40     
&emsp;20   
d) 40    
&emsp;10   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option a)
<details><summary> <b>Explanation</b> </summary> 
  
> When this code is executed, it will execute the print statement, which is outside the class. That print statement access the class variable using class name and hence 10 will be printed. When show() method is called, it prints the value of x as 40 because it is accessing the global variable. 
  </details>
</details>

---
5. What is the output of the following code?
```python3
x = 40
class Test:
    x = 10
    def show(self):
        self.x = 20
        print(self.x)
    
obj = Test()
print(x)
obj.show()
```
a) 10     
&emsp;40   
b) 10    
&emsp;20   
c) 40     
&emsp;20   
d) 40    
&emsp;10   

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> When this code is executed, it will first print the value of global variable 'x' as 40. After that, when show() method is called, it will print the value of instance variable 'x' as 20.
  </details>
</details>

---
6. Predict the output of the following code.
```python3
x = 40
class Test:
    x = 10
    def show(self, x):
        x =20
        x= self.x
        print(x)
    
obj = Test()
obj.show(5)
```
a) 40  
b) 10  
c) 20  
d) 5  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> The above code will print 10 as an output, because inside show() method, the print statement prints the value of current instance of the class, which is x=10. Here, x= 20 is a local variable of show() method, and therefore it is not printed.
  </details>
</details>

---
7. What is the output of the below code.
```python3
x = 40
class Test:
    x = 10
    def show(self, x):
        self.x =x 
        return self.x
    
obj = Test()
print(self.x)
```
a) 40   
b) 10  
c) Error  
d) Nothing is printed  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> As self is not defined outside the class, we get the `NameError`. 
  </details>
</details>

---
8. State True and False: " When we assign a value to a variable inside the function, it becomes a global variable".

a) True  
b) False  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> When we assign a value to a variable inside the function, it becomes a local variable not global. 
  </details>
</details>

---
9. What happens if the global variable that has to access has the same name as a local variable? 

a) It will result in Error  
b) The local variable is shadowed   
c) The global variable is shadowed  
d) None of the above  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
 
> In python, if both global and local variable having the same name and we have to access them at the same time, in that situtaion your code will access the local variable.  
</details>
</details>

---




