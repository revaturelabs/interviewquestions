# Iterator in python


1. What is an iterator in python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Iterator allows to iterate or traverse through all the values of collection in python. It has two methods, `__iter__()` and `__next__()`. `iter()` method is similar to `init()` method, as it is used to initialize the objects but, it returns an iterator. `next()` method is used to get the next element of the iteration.   

For example:
```python3
l = [1,2,3]
m =iter(l)

print(next(m))   #output: 1
print(next(m))   #output: 2
print(next(m))   #output: 3 
```
or 
  
```python3
l = [1,2,3]
m =iter(l)

for i in m:
    if i<=len(l):
        print(i, end=" ")    #output: 1 2 3
```
</details>

---
2. How to create an iterator in python?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> To create a custom iterator in python, we can use `__iter__()` and `__next__()` method inside a class.

```python3
class Numbers:
    def __iter__(self):
        self.a = 1
        return self

    def __next__(self):
        if self.a <= 5:
            x = self.a
            self.a += 1
            return x
        else:
            raise StopIteration     # to stop the iteration.    

obj = Numbers()
itr = iter(obj)

for x in itr:
        print(x, end=" ")     # output: 1 2 3 4 5
```
</details> 

---
3. What is a StopIteration exception?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary> 
  
> In python, it is raised by `next()` method when there is no element to be present for iteration. 
  </details>

---
4. Which of the following exception is thrown by next() in python?

a) RuntimeError    
b) SystemExit    
c) StopIteration     
d) IndexError    
  
![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 
  
<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
</details>

---
5. Predict the output of the following code.
```python3
class Numbers:
    def __iter__(self):
        self.a = 8
        return self

    def __next__(self):
        if self.a <= 5:
            x = self.a
            self.a += 1
            return x
        else:
            raise StopIteration

obj = Numbers()
itr = iter(obj)

for x in itr:
        print(x, end=" ")
```
a) 5 6 7 8  
b) 8 7 6 5  
c) Error  
d) Nothing is printed  
                      
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
                      
<details><summary> <b>Show Answer</b> </summary> 
  
> Option d)
<details><summary> <b>Explanation</b> </summary> 
  
> As the current value of a is more than 5, it will raise `StopIteration` exception and prints nothing in output screen.
  </details>
</details>
  
---
6. Predict the output for the following code.
```python3
class Numbers:
    def __iter__(self):
        self.a = 3
        return self

    def __next__(self):
        if self.a <= 5:
            x = self.a
            self.a += 1
            return x
        else:
            raise StopIteration

obj = Numbers()
itr = iter(obj)

for x in itr:
        print(x, end=" ")
```
a) 3 4 5  
b) 5 4 3  
c) Error  
d) Nothing is printed   
                      
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
                      
<details><summary> <b>Show Answer</b> </summary> 
  
> Option a)
<details><summary> <b>Explanation</b> </summary> 
  
> The initial value of a is 3 and it will increment by 1 until it reaches 5 in `__next__()` method. Therefore, we will get 3, 4 and 5 as an output.  
  </details>
</details>

---
7. What is the use of `iter()` method in python?

a) It is used to initialize an object.  
b) It is used to throw an error.  
c) It is used to return an iterator.  
d) None of the above.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Option c)
<details><summary> <b>Explanation</b> </summary> 
  
> It returns an iterator and converts an iterable to an iterator. 
  </details>
</details>

---
8. What is the use of `next()` in python?

a) It is used to initialize an object.  
b) It is used to give next element from the iteration through iterator.  
c) It is used to return an iterator.  
d) It is used to throw StopIteration exception.  

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Option b)
<details><summary> <b>Explanation</b> </summary> 
  
> next() method, in python, returns the next element from iterator.
  </details>
</details> 
  
---




