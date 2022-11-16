## Technical

1. Which access modifier is used to override the method of an Interface?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

- A.public
- B.private
- C.protected
- D.default

<details markdown="1">
<summary><b>Show Answer</b></summary>

> A
  
<details markdown="1">
  
<summary>Explanation</summary>
  
> All the methods in an interface are public by default and It is not possible to alter the access modifier while overriding the method.
    
</details>
  
</details>

---

2. What is Marker Interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



<details markdown="1">
  <summary><b>Show Answer</b></summary>


    
> Marker Interfaces are empty Interfaces (no fields or methods).
> Marker interfaces are used to pass the information to JVM that a certain object of a class can implement methods like Serializable, Cloneable etc.

  </details>
</details>

---

3. Is it possible to create an Object for the Interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



<details markdown="1">
<summary><b>Show Answer</b></summary>
	
>  No 
<details markdown="1">
  
  <summary>Explanation</summary> 
    
> Interfaces contain abstract methods, Which means only method declarations are present but not implementation.so,there is no purpose of an Object, But one can create an Object for a class that implements Interface and reference it to the Interface. 

  </details>
</details>

---

4. What methods can be created in an Interface?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

- A.abstract
- B.static
- C.Default
- D. All the above

<details markdown="1">
<summary><b>Show Answer</b></summary> 
	
 > D
<details markdown="1">
  
  <summary>Explanation</summary> 
    
> Interface is used to implement abstraction, so abstract methods are allowed in an Interface.
> Default methods are allowed to avoid the issue of mandatory implementation of all methods in an Interface.
> static methods are generally used to create helper methods,static methods are referenced to the interface, rather than the class that implements the interface.

  </details>
</details>

---

5. Give an example where default methods are created in an Interface.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details markdown="1">

  <summary><b>Show Answer</b> </summary>  
  
> Consider that there is an interface implemented by 4 classes and a new method should be added to the interface, but all the previous classes should implement the new method, which creates trouble for the developer. So, the new method can be added as a default method. A default method in the interface can be overridden by a class based on the requirement. 
    

   </details>
   
---


6. Give an example where static methods are created in an Interface.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details markdown="1">

  <summary><b>Show Answer</b> </summary>  
  
> Static methods are introduced in java 8 and static methods are added to integrate helper methods into the interface instead of creating a new class and facing cohesion issues.
    

   </details>
   
 ---


7. Consider that a class extends the interface Elevator, Which of the following is true?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



``` java
interface  Electrical{
	void controlLight();
	void controlAC();
}

interface Mechnical{
	void pullUp();
	void pullDown();
}

interface Elevator extends Electrical, Mechnical{
	
	int goUP();
	int goDown();

}

```

- A. The concreate class that implemnets Elevator, must override the methods of evelator, overriding methods of Electrical and Mechanical is optional.
- B. The concreate class that implements Elevator, must override all the methdos of all the interface.
- C. class can not implement Elevator because an interface can not extend more than one interface.
- D. It is not mandatory to override any method of any interface.

<details markdown="1">
	
<summary><b>Show Answer</b></summary>
	
> B
	
<details markdown="1">

<summary><b>Explanation</b></summary>
	
> If a class implements an Elevator, all the methods of Elevator, Mechanical and  Electrical are inherited by the class, all the methods other than default and static should be overridden in the class.

</details>
</details>

---

8. How can complete abstraction be achieved by interface but not by an abstract class?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



<details markdown="1">

<summary><b>Show Answer</b></summary>
	
> - Interface contains an abstract class with no implementation, whereas abstract class contain both abstract and non-abstract methods with concrete implementation, so complete abstraction can be achieved by an interface	
> - But from java 8 interface can contain default and static methods.

</details>

---

9. Explain Multiple Inheritance of implementation using Interfaces.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details markdown="1">

<summary><b>Show Answer</b></summary>
	
> A class can Inherit multiple Interfaces with the same method names and this might cause a conflict while overriding the methods of the interface.
> To resolve this issue interfaces can have default methods with the same method name and JVM has some rules implement the default methods.

</details>

---


10. What is Multiple Inheritance of type using Interfaces?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details markdown="1">

<summary><b>Show Answer</b></summary>
	
> A class can implement multiple interfaces, and multiple objects can be created referencing those interfaces, this is called Multiple Inheritance of type.
> Consider that a class implements more than one interface with default methods of the same name, the issue with the implementation of methods can be resolved by defining the type of reference while creating the object for the class.
	

</details>

---

11. Is it possible to override the static method of an interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



<details markdown="1">

<summary><b>Show Answer</b></summary>
	
> No, static methods can not be overridden, if a method is created in the class that implements the method with the same name as the static method in the interface, it's considered method hiding.
	

</details>

---



## Error Detection

1. Identify the error in the following code snippet.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



``` java
interface Elevator{
	
	int goUP();
	int goDown();
	final void stop();
}

```

<details markdown="1"><summary><b>Show Answer</b></summary>
	
> Compile-time error

	
<details markdown="1"><summary><b>Explanation</b></summary>
	
> Methods in the interface can be abstract or default or static.
> Methods in the interface can not be final, because final methods can not be overridden. Interfaces are created so they can be implemented by a class and the methods of an interface should have the possibility to be overridden.

</details>

</details>

---

2. Identify the error in the following code snippet.
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



``` java



interface Shape{
	void area();
	void circumference();
}

public class Circle implements Shape{
	
	
	public static void main(String[] args) {
		Shape  c = new Shape() {

			@Override
			public void area() {
				System.out.println("3.14*r*r is the area of circle");
				
			}

			@Override
			public void circumference() {
				System.out.println("3.14*r*r is the circufrence of circle");
				
			}
			
			
		};
		
	}
	
}

```

<details markdown="1">
	<summary><b>Show Answer</b></summary>
	
> A compile-time error
<details markdown="1">
<summary><b>Explanation</b></summary>
	
> Even though the anonymous inner class overrides all the methods of the interface, The class Circle doesn't override them.

</details>
</details>





## Scenario Based

1. KIA launched 4 car models named seltos, carnival, Carens and sonnet with features like Front and Side Airbags, Highline Tyre Pressure Monitor, Hill assist control etc. from the 5th model KIA wants to add a new feature of autopilot and self-driving. Which of the following implementations best represents the scenario?
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



- A. A KIA interface with all features as abstract methods and models as classes that implement the KIA interface.
- B. A KIA Class with methods and features as abstract methods and models is the class that inherits the KIA.
- C. A KIA interface with all features as abstract methods except for the new feature( autopilot) which is a default method and all models as classes that implement Kia.
- D. None of the above.

<details markdown="1">
	
<summary><b>Show Answer</b></summary>
	
> C
	
<details markdown="1">
	
<summary><b>Explanation</b></summary>
	
	
> KIA(interface) has some models(Classes) that had some features till model 4 ( abstract methods in the interface ), from model 5 a new feature autopilot( method) is being added to upcoming KIA car models. but the previous models don't support the autopilot( override the method) so the new feature is added as a default method which can be used by upcoming models.
	
	

</details>

</details>

---
2. ISRO invented many rockets from PSLV to GSLV with different features and purposes but one constant feature is the Vikas engine. which implementation best represents the scenario?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)



- A. An interface with features of the rocket, classes that implement the interface( rocket model), and a default method for the Vikas engine.
- B. An interface with features of the rocket, classes that implement the interface( rocket model), and an abstract method for the Vikas engine.
- C. An interface with features of the rocket, classes that implement the interface( rocket model), and a static method for the Vikas engine.
- D. None of the above.

<details markdown="1">
	
<summary><b>Show Answer</b></summary>
	
> C
	
<details markdown="1">
	
<summary><b>Explanation</b></summary>
	
	
> ISRO Rockets is an interface with basic features of a rocket, PSLV, GSLV etc are the models(Classes) that satisfy the basic features. Vikas engine( method) is a constant feature for the rockets that are launched and about to be launched in the future, it can't be overridden, So it's declared as static.
	
	

</details>

</details>


















