## Real-Time Applications

1. Harry potter's Invisibility cloak was passed down to him by his father James and James potter got it from his father Henry potter, this is a clear example for?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A.Hybrid Inheritance
- B.Multilevel Inheritance
- C.Simple Inheritance
- D.Multiple Inheritance

<details><summary> <b>Show Answer</b> </summary>
	
> B
 
<details>
  <summary><b>Explanation</b></summary> 
	
> - Invisibility cloak is a family heirloom for potters, A property is passed down from one class(generation) to another, this is a clear example of multilevel inheritance
</details>
</details>

---

2. English language vocabulary is comprised of old germanic, French, and Latin words, this is an example for? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A.Hybrid Inheritance
- B.Multilevel Inheritance
- C.Simple Inheritance
- D.Multiple Inheritance

<details><summary><b>Show Answer</b> </summary>
	
> D
  
<details>
  <summary><b>Explanation</b></summary> 
	
>  English vocabulary is inherited from germanic, French, and Latin, one class inherits the properties of multiple classes, and this is an example of multiple inheritances.
</details>
</details>

---


## Technical

1. How is Multiple Inheritance implemented in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b> Show Answer</b></summary>

> In java, a class can not extend more than one class. To achieve multiple Inheritance, one can create multiple interfaces and create a class that implements multiple Interfaces.
</details>

---
2. What is Hybrid Inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer</b></summary>

> Simple inheritance, multilevel inheritance, and multiple inheritances are the different types of Inheritance in java, combining two or many of these is considered Hybrid Inheritance.
</details>

---
3. What is Multilevel Inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer</b></summary>

> A superclass is extended by a subclass and the subclass is extended by another subclass. The US government provides funds to Texas and the Texas government provides funds to Austin, here funds are an object, and the US, Texas, and Austin are classes.	
>
> <img width="155" alt="Multilevel" src="https://user-images.githubusercontent.com/103101208/185297803-40ec0caf-43c1-4ec5-8345-a3d21f171b28.PNG">

</details>

---
4. What is single Inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer</b></summary>

> the relation between a superclass which gets extended by a single subclass is called single Inheritance.
> 
> <img width="173" alt="Single" src="https://user-images.githubusercontent.com/103101208/185297546-71804b70-cd2f-4bae-930a-6a61d4da839f.PNG">

</details>

---
5. Differentiate Aggregation and Inheritance.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer</b></summary>

> - Aggregation: Has-a Relationship is implemented in aggregation.
> - Inheritance: Is- a Relationship is implemented in Inheritance.
</details>

---
6. How can a subclass use the private fields of a superclass?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
  <summary> <b>Show Answer</b> </summary>
<blockquote>

- A subclass can access the private members of the superclass in two possible ways:<br>
  
 1. If public or protected methods of the superclass have access to the private fields, then the subclass can have access to the private fields.
 2. If the superclass has a public or protected nested class then the subclass can access all the private members of the superclass using the nested class.
  
 </blockquote> 
</details>

---
7. Which of the following is invalid in java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

- A.Multiple Inheritance of state
- B.Multiple inheritance of type
- C.Simple Inheritance 
- D.Multilevel Inheritance

<details><summary><b>Show Answer</b></summary>
	
> A

<details>
  <summary><b>Explanation</b></summary> 
	
> Multiple Inheritance of state is invalid in java because a class cant extend more than one class but it can implement multiple interfaces.


</details>
</details>

---
8. Why is a class restricted to extend a single class in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 
> If a class extends multiple classes the object of the class inherits all the fields of all the inherited classes, and inherited classes might have the same fields which are instantiated by different methods or constructors, it's not possible to set the precedence for all the methods and constructors, so the instantiation of the field is ambiguous. A class extend a single class, to avoid Multiple inheritances of state.

</details>

---
9. What is Multiple Inheritance of state and why is it not possible to implement it in java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>



> Exteding more than one class leads to multiple inheritance of state in java. If a class extends more than a single class, it inherits all the fields of superclasses, and if two classes have same fields and they are intialized by different constructors or methods of different classes, JVM can not give precidence to an Intilization. So, Multiple Inheritance of state is not possible in java.

</details>

---
10. What is Upcasting?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
	
<blockquote>
	
- A child class inherits all the properties of parent class so the child class can be implicitly upcasted to parent.
	
``` java
	
Parent p = new Child();
	
```
</blockquote>	
</details>

---
11. What is Downcasting?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
- A parent class may or may not have all the properties of Child class, so parent class can be ecplicily downcasted to Child class

``` java
Child c= (Child) new Parent();
	
``` 
</blockquote>
	
</details>


---
12. Is it possible to override `main()` method?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
	
> No, `main()`  method is a static method and static methods can't be overriden.
	
</details>

---

13. Is it possible to inherit a constructor? justify your answer.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
	<summary><b>Show Answer</b></summary>
	
> No
> - Constructors should have the same name as the class, if a constructor is inherited it can't be named as the class and it will be considered as a method.
> - Using constructor all the private members of superclass can be accesed by the subclass. So, encapsulation can not be achived in java.
</details>

---

14. Is it possible to override a static method? justify your answer.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
	<summary><b>Show Answer</b></summary>
	
> No
> - A static method can not be overriden if a sub class has a method with the same name as the static method in super class, its considered as hiding.
> - unlike overloading, if static method is called in superclass, the superclass static method is invoked and if static method is called in subclass, the subclass static method is invoked.
</details>


## Problem solving

1. What is the output of the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
package web;

import java.util.*;

public class Olympics{
  
  public static void main(String[] args) {
    India i = new India();
    i.hostOlympics();
        
  }
  public void hostOlympics() {
    System.out.println("Summer Olympics and Winter Olympics");
  }

}

class India extends Olympics{

  public void hostOlympics() {
    
    System.out.println("We will host summer olympics in 2036"); 
    Olympics o = new Olympics();
    o.hostOlympics();
    
  }
}

class Japan extends Olympics{
  public void hostOlympics() {
    System.out.println("We hosted Olympics on 2021");
    
  }
}
```
- A. We will host the summer Olympics in 2036
     Summer Olympics and Winter Olympics

- B. Summer Olympics and Winter Olympics
     We will host the summer Olympics in 2036

- C. Summer Olympics and Winter Olympics

- D. We will host the summer Olympics in 2036

<details><summary><b>Show Answer</b></summary>
	
> A
  
<details>
<summary><b>Explanation</b></summary>
	
> ` i.hostOlympics()` invokes the method in India class. So, "We will host the summer Olympics in 2036" will be printed first and `o.hostOlympics()` invokes meythod in Olympics class. So, "  Summer Olympics and Winter Olympics" will be printed.
	
</details>
</details>


---


## Error Detection

1. What is the output of the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public final class Car{
    public static void main(String args[]){
        KIA k = new KIA();
      k.engine();

    }
    public void engine(){
        System.out.println(" I am  a Diesel engine");

    }

}
 class KIA extends Car{
    public void engine(){
        System.out.println("I am a Petrol engine");
    }

 }

```
- A. I am a Diesel engine
- B. I am a petrol engine
- C. Compile-time error
- D. Runtime error

<details><summary> <b>Show Answer</b> </summary>
	
 > C
  
<details><summary> <b>Explanation</b> </summary>
	
> Class KIA is trying to inherit the final class Car. It's not possible to inherit a final class.
</details>
</details>
	

---
2. What is the output of the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public final class Car{
    public static void main(String args[]){
        Car c = new Car();
      c.engine();

    }
    public void engine(){
        System.out.println(" I am  a Diesel engine");

    }

}
 class KIA extends Car{
    public void engine(){
        System.out.println("I am a Petrol engine");
    }

 }

```
- A. I am a Diesel engine
- B. I am a Petrol engine
- C. Compile-time error
- D. Runtime error

<details><summary><b>Show Answer</b> </summary>
 
> A
  
 
<details><summary><b>Explanation</b> </summary>
	
> Final class can not be inherited but no object is created for the subclass and no subclass methods are implemented, So there is no error in the code.
</details>
</details>

---
3. What is the error in the following code snippet? correct the error.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

Object o = new Main();
Main m = o;


``` 

<details><summary> <b>Show Answer</b></summary>
  
<blockquote>
  - the above code is an example for object casting and line 2 creates an error, even if object o is of type Main, JVM can not recognize it and an explicit type cast should be added to avoid compile time error.
  
 ``` java
  
  Main m = (Main) o;
  
  ```
  
- After adding the type cast, if the object o is not of type main, a runtime error occurs.
  
</blockquote>

</details>

---
4. The object declared in the below code snippet is type casted but it may or may not be of type Main, How does a programmer avoid runtime error?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

Main m = (Main) o;

```

<details><summary><b>Show Answer</b></summary>

<blockquote>
	
- To avoid any runtime error the declaration can be enclosed in a simple condition which checks the instance of object o.
  
  ``` java
  if( o instanceof Main)
	{
			Main m = (Main) o;
	}
  
  ```
</blockquote>

</details>









