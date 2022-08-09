# Scopes in python [in class] 


1. What do you mean by global scope in python?
<details><summary> <b>Show Answer</b> </summary> 
  
> The object name that are defined in a main program or in a module comes under global scope. These are outside any function or block of code. It can access the builtin namespace objects. 
</details>

---
2. What do you mean by local scope in python?
<details><summary> <b>Show Answer</b> </summary> 
  
> The variable names defined in a class, function, loop or in any block of code are comes under local scope. These variables cannot be accessed by outer Namespace in python. Local namespace can access the global namespace objects and built-in namespace. 
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
<details><summary> <b>Show Answer</b> </summary> 
  
> option is d) 
<details><summary> <b>Explanation</b> </summary> 
  
> The first print statement, before method calling, prints the value of global variable i.e 40. And when the show() method is called the print statement present inside it will also prints the value of x as 40 not 20, because x= 20 is a class variable which must be accessed by using classname before variable name. Therefore it will also takes the global variable value i.e 40 in this case also. Hence the output.
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
<details><summary> <b>Show Answer</b> </summary> 
  
> Option a)
<details><summary> <b>Explanation</b> </summary> 
  
> When this code run, it will executes the print statement, which is outside the class, first. That print statement is accessing the class variable using class name so, 10 will be printed. Now when show() method is called it prints the value of x as 40 because it is accessing the global variable. 
  </details>
</details>

---
5. What will be the output of the following code?
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
<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> When this code runs, it will first print the value of global variable x as 40. After that, when show() method is called it will print the value of instance variable x which is 20. Hence the output.
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
<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> The above code will print 10 as an output, because inside show() method, the print statement is printing the value of current instance of the class which is x= 10 at that moment. Here x= 20 is a local variable of show() method, therefore it is not printed.
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
<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> As self is not defined outside the class, we will get the NameError. 
  </details>
</details>

---
8. State True and False: " When we assign a value to variable inside the function, it becomes a global variable".

a) True  
b) False  
<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> When we assign a value to variable inside the function, it becomes a local variable not global. 
  </details>
</details>

---
9. What happens if the global variable you wish to access has the same name as a local variable? 

a) It will result in Error  
b) The local variable is shadowed   
c) The global variable is shadowed  
d) None of the above  
<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
</details>

---





