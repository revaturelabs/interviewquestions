## Error Detection

1. Find the error in the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Game {
	public static void main(String[] args) {
		Game g;
		g.playCricket();
		
		
	}
	void playCricket() {
		System.out.println("I am a Batsman");
	}

}

```

<details><summary><b>Show Answer</b></summary>
	
<blockquote>

 The above code creates a compile-time error, The object "g" is declared but not initialized, and It is not possible to use an object of a class without Initializing it.
	
</blockquote>

</details>

---

2. What is the error in the following code snippet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
public class Child extends Parent, Grandparent{
	// code
}
```
<details><summary><b>Show Answer</b></summary>
<blockquote>

 Compilation error is caused because a class can extend only one parent class.
</blockquote>

</details>

---

3.  What is the error in the following code snippet?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

private class Main{
	// code	
}

```

<details><summary><b>Show Answer</b></summary>

<blockquote>

Compilation error is caused because a class can be public, abstract and final but not private unless it's a nested class.

</blockquote>
	
</details>



## Technical

1. Which of the following can be declared private?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A. Class
- B. Interface
- C. Nested Class
- D. None of the above

<details><summary><b>Show Answer</b></summary>

 > C
	
<details><summary><b>Explanation</b></summary>
	
<blockquote>
Classes and interfces can not be declared private, nested classes can be declared private.
</blockquote>

</details>
</details>

---

2. What are the parameters and arguments?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A. parameters: list of variables in the method declaration.
     Arguments:  Values that are passed when a method is invoked.
- B. parameters: list of variables in the method declaration.
     Arguments:  Values that are passed when a method is invoked.
     
<details><summary><b>Show Answer</b></summary> 
	
 > A 
</details>

---

3. What is the implicit superclass for all java classes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A. Arrays
- B. Collections
- C. Object
- D. None of the above

<details><summary><b>Show Answer</b></summary>

> C
	
<details><summary><b>Explanation</b></summary> 
	
<blockquote>
The default constructor of any class calls the no-arg constructor of the superclass, So, java provides an implicit super class "Object" which has a default constructor.
	</blockquote>

</details>
</details>

---

4. What are the benefits of using Objects?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	
<blockquote>
	
- Modularity: the source code for every object can be maintained independently and once an object is created it can be easily propagated inside the system.
- Information hiding: since an object is used to implement methods, the internal working of the class can be hidden using an object.
- Code - reusability:  once an object is created, it can be reused anywhere in the program.
- Pluggability and debugging: if an existing object fails to satisfy the requirements of the developer or causes any abnormality in the code, it can be 
	  deleted.
</blockquote>
	
</details>

---

5. Variables declared in an interface are?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A. public, static and final
- B. private and final
- C. public and final
- D. Default or public, static.


<details> <summary><b>Show answer</b></summary>

 > A
	
<details><summary><b>Explanation</b></summary>

<blockquote>
	
- final: variables in an interface are accessed by many classes and its not ideal, if any of the classes appends the value of the variable. to avoid this
	 variables are declared final.
- public: interfaces are accessed by any class present in any package, so to support this all variables are declared public.
- static: interface itself can't be initialized, so objects of a class are used to access variables, but if a class is imcomplete, an object cant be created.
	   All variables are static so that they can be accessed without an object.
</blockquote>

</details>
</details>

---

6. choose the right answer.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

1.local class   <br>                               
2.Anonymous class  <br>                           
3.lambda expression <br>                          
4.Nested class <br>

<br>
a.  Used to group classes that are reliable with each other, to increase encapsulation and to maintain cohesive, concise and readable code.<br>
b. Used to create a simple instance of a functional interface.<br>
c. Used when you need to use a local class only once.<br>
d. Used to create more than one instance of a class, and to add new fields and methods to the class.<br>
<br>


- A. 1-b, 2-d, 3-b, 4-c
- B. 1-d, 2-b, 3-a, 4-c
- C. 1-d, 2-c, 3-b, 4-a
- D. 1-b, 2-c, 3-d, 4-a

<details>
	<summary><b>Show Answer</b></summary>
	
> C

</details>

---

7. How to destroy an object in java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b>Show Answer</b></summary>

>  An object can not be directly destroid in java. by setting all the references to object as null, the object is eligible for garbage collection.

</details>

---

8. How many object references are present after executing the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

String s = "Revature";
String[] arr = new String[10];
arr[0] = s;
s=null;

```

<details><summary><b>Show Answer</b></summary>
<blockquote>
	
one reference will be left after executing the code snippet(arr[0]--> s).
</blockquote>

</details>

---

9. Which of the following options best explains the folowing code snippet?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
interface Car{
        // code	
}

public class Audi implements Car{
	
	public static void main(String[] args) {
		Car c = new Audi();	
	}
	// code
  
}

```

A. Object for interfcae Car is created and it's reference is assigned to Class Audi.<br>
B. Object for interfcae Car is created and it's reference is assigned to itself.<br>
C. Object for Class Audi will be created and it's reference is assigned to itself.<br>
D. Object for Class Audi is created and it's refrence is assigned to the Interface.

<details><summary><b>Show Answer</b></summary>

> D

<details><summary><b>Explanation</b></summary>
	
<blockquote>

It is not possible to create an object for interface, an Object can be created only for classes and the reference can be assigned to an interface.

</blockquote>
</details>


</details>

---


10.  Write a code where an object is created for an Interface or abstract class.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	
<blockquote>
	
- Interfaces and Abstract classes cant be initialized because they have abstract methods, so its not possibel to create an object for an Interface,but while creating an anonymous class an object can be created for interface and abstract method.
	
``` java
	
interface Shape{
	void area();
	void circuference();
}

abstract class Dimension{
	abstract void visibility();
}

public class Circle {
	
	
	public static void main(String[] args) {
		Shape  c = new Shape() {

			@Override
			public void area() {
				System.out.println("3.14*r*r is the area of circle");
				
			}

			@Override
			public void circuference() {
				System.out.println("3.14*r*r is the circufrence of circle");
				
			}
			
			
		};
		
		Dimension d = new Dimension() {
			
			@Override
			void visibility() {
				System.out.println("A circle is 2D object or planar object");
				
			}
		};
		
		
		
	}
	
}

	
	
```
In the above code, obejcts c and d are created for interface Shape and abstract class Dimension.
</blockquote>
	
</details>

---

11. How to create an immutable class in java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer </b></summary>
<blockquote>
	
A class is considered as imputable if once an object is created, then its contents cant be modified.
	
An immutable class can be created by
1. Declaring all the feilds as private to avoid access. 
2. Declaring the class as final to avoid overriding of methods.
3. Declare class as final to avoid ineritance.
4. intializing data using a parameterized constructor.
5. retriving data using a getter method to avoid getting direct access to the object reference.

</blockquote>
</details>

---

12. How to represent an object as a string?

<details>
	<summary><b>Show Answer</b></summary>
	
> an object can be represneted as string using `toString()` method.

</details>


## Real-time Application

1. Consider that a code is created for the sole purpose of notifying the user that the battery is fully charged, this can be used by any device like a mobile, pc, AirPods etc. Which of the following implementations suits the best?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

- A. abstract class with a single abstract method and an anonymous class
- B. abstract class with a single abstract method and a local class.
- C. Interface with a single abstract method and an anonymous class.
- D. Interface with a single abstract method and lambda.

<details>
<summary><b>Show Answer</b></summary>
	
> D
<details><summary><b>Explanation</b></summary>
	
<blockquote>
A code with a single purpose translates to a class/ interface with a single method, functional interface is the best way to implement this scenario and lambda implementation in each device, makes the code concise, easily readable and maintainable.

</blockquote>
</details>
</details>














