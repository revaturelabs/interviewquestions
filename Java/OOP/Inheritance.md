## Real-Time Applications

1. Harry potter's Invisibility cloak was passed down to him by his father James and James potter got it from his father Henry potter, this is a clear example for?  



- A.Hybrid Inheritance
- B.Multilevel Inheritance
- C.Simple Inheritance
- D.Multiple Inheritance

<details><summary> Show Answer </summary>
  <b>Ans</b>: B
  
  <b>Explanation</b>: Invisibility cloak is a family heirloom for potters, A property is passed down from one class(generation) to another, this is a clear example of multilevel inheritance
</details>




2. English language vocabulary is comprised of old germanic, French, and Latin words, this is an example for?    ![EASY](Easy%20(2).jpg)

- A.Hybrid Inheritance
- B.Multilevel Inheritance
- C.Simple Inheritance
- D.Multiple Inheritance

<details><summary> Show Answer </summary>
  <b>Ans</b>: D
  
  <b>Explanation</b>: English vocabulary is inherited from germanic, French, and Latin, one class inherits the properties of multiple classes, and this is an example of multiple inheritances.
</details>



## Technical

1. How is Multiple Inheritance implemented in java?

<details>
<summary><b> Show Answer</b></summary>

Ans: In java, a class can not extend more than one class. To achieve multiple Inheritance, one can create multiple interfaces and create a class that implements multiple Interfaces.
</details>

2. What is Hybrid Inheritance?
<details>
<summary><b> Show Answer</b></summary>

Ans: Simple inheritance, multilevel inheritance, and multiple inheritances are the different types of Inheritance in java, combining two or many of these is considered Hybrid Inheritance.
</details>

3. What is Multilevel Inheritance?
<details>
<summary><b> Show Answer</b></summary>

<b>Ans</b>:  A superclass is extended by a subclass and the subclass is extended by another subclass. The US government provides funds to Texas and the Texas government provides funds to Austin, here funds are an object, and the US, Texas, and Austin are classes.
</details>

4. What is simple Inheritance?
<details>
<summary><b> Show Answer</b></summary>

<b>Ans</b>: the relation between a superclass which gets extended by a single subclass is called Simple Inheritance.
</details>

5. Differentiate Aggregation and Inheritance.
<details>
<summary><b> Show Answer</b></summary>

<b>Ans</b>: 
Aggregation: Has-a Relationship is implemented in aggregation.
Inheritance: Is- a Relationship is implemented in Inheritance.
</details>

6. How can a subclass use the private fields of a super class?

<details>
  <summary> Show Answer </summary>
  
  <b>Ans: </b> A subclass can access the private members of the super class in two possible ways:<br>
  
  1. If public or protected methods of the superclass have access to the private fields, then the sub class can have access to the private fields.
  2. If the superclass has a public or protectd nested class then the sub class can access all the private members of superclass usiing the nested class.
  
  
</details>

## Problem solving

1. What is the output of the following code?

``` java
package web;

import java.util.*;

public class Main{
  
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

<details><summary> Show Answer </summary>
  <b>Ans</b>: A
  
  <b>Explanation</b>:  
</details>





## Error Detection

1. What is the output of the following code?

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

<details><summary> Show Answer </summary>
  <b>Ans</b>: C
  
  <b>Explanation</b>: Class KIA is trying to inherit the final class Car. It's not possible to inherit a final class.
</details>

2. What is the output of the following code?
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

<details><summary> Show Answer </summary>
  <b>Ans</b>: A
  
  <b>Explanation</b>: final class can not be inherited but no object is created for the subclass and no subclass methods are implemented, So there is no error in the code.
</details>

3. What is the error in the following code snippet? correct the error.

``` java

Object o = new Main();
Main m = o;


``` 

<details><summary> Show Answer</summary>
  
<b>Ans:</b> 
  - the above code is an example for object casting and the line 2 creates an error, even if object o is of type Main, JVM can not recognize it and an explicit type      cast should be added to avoid copiletime error.
  
 ``` java
  
  Main m = (Main) o;
  
  ```
  
  - After adding the type cast, if the object o is not of type main, a runtime error occurs.
  
  

</details>

4. The object declared in the below code snippet is type casted but it may or may not be of type Main, How does a pogrammer avoids runtime error?

``` java

Main m = (Main) o;

```

<details><summary>Show Answer</summary>

  <b>Ans: </b> In order to avoid any runtime error the decleration can be enclosed in a simple condition which checks the instance of object o.
  
  ``` java
  if( o instanceof Main)
	{
			Main m = (Main) o;
	}
  
  ```

</details>






