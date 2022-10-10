1. Difference between method and function

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- Method and a function are the **same, with different terms**.
- A method is a **function that belongs to a class**.
- A function is a group of reusable code which can be called anywhere in your program.

</blockquote>
</details>

--- 

2. Tell us about OOPs

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- **O**bject **O**riented **P**rogramming is a programming paradigm/model which revolves around the concept of **Objects**. 
- Objects can be considered as real-world instances of entities like class, that have **characteristics** and **behaviors**

**For example**, if we consider a car, then based on the OOPs model:

- Class: A specific car model, such as Audi A4, BMW I8, Maruti Suzuki Vitara Brezza, etc.
- Object: A specific car of any model, like the car you own
- Characteristics: What is the color of your car? What is the model of your car? etc
- Behavior: How to start the car? How to change the gear of the car? etc.

Characteristics are also known as data, attributes, or properties, and Behaviours are also known as the functions, procedures or methods, in the programming language.

</blockquote>
</details>

--- 

3. What are the pillars of OOP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

The Four Pillars of Object-Oriented Programming are
- Abstraction
- Encapsulation
- Inheritance
- Polymorphism

</blockquote>
</details>

--- 

3. What is polymorphism?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- The word poly means many and morphs means forms, So polymorphism means many forms.
- It's an ablility of an object to exhibit more than one form

For example: A man at the same time is a father, a husband, an employee. So the same person possesses different behavior in different situations. This is called polymorphism. 

</blockquote>
</details>

--- 

4. What is method overloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
<blockquote>
 
- Method Overloading is a feature that allows a class to have more than one method with the same name, but with different parameters.
- It is also known as Compile-time Polymorphism or Static Polymorphism 

**For example**: 
```java
public class SquaringDemo {
	
	public void square(int n) {
		System.out.println("Method with int argument called: " + n*n);
	}
	public void square(double n) {
		System.out.println("Method with double argument called: " +n*n);
	}
	public void square(float n) {
		System.out.println("Method with float argument called: " + n*n);
	}

	public static void main(String[] args) {
	  SquaringDemo obj = new SquaringDemo();
	  obj.square(4);
	  obj.square(4.567);
	  obj.square(4.567f);
	}
	/*Output:
	 * Method with int argument called: 16
	 * Method with double argument called: 20.857489
	 * Method with float argument called: 20.857489
	 */
}
```

</blockquote>
</details>

--- 

5. What is method overriding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

If there is a same method is defined in both the superclass and the subclass, then the subclass's method overrides the superclass's method. This is known as method overriding. It's also called as dynamic polymorphism or run-time polymorphism.

For example,
```java
class Animal {
   public void makeSound() {
      System.out.println("I am an animal.");
   }
}

class Dog extends Animal {
   @Override
   public void makeSound() {
      System.out.println("I am a dog!!, woof woof");
   }
}

class Cat extends Animal{
	@Override
	   public void makeSound() {
	      System.out.println("I am a cat!!, meow meow");
	   }
}
```
 
 
</blockquote>
</details>

--- 

6. Explain encapsulation

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Encapsulation is the way of binding the data (variables) and code acting on the data (methods) together as a single unit.  

For example, in a company, they are different sections like the accounts section, finance section, sales section etc. Consider a situation, a person from finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. 

In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

</blockquote>
</details>

--- 

7. What is an abstract class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
<blockquote>

Abstract Class allows us to achieve 0 - 100 % of abstraction in java. 

A class which is declared with the abstract keyword is known as an abstract class. It can have abstract and non-abstract methods (method with the body).

A method that doesn't have its body is known as an abstract method. We use the same abstract keyword to create abstract methods.

We cannot create an object for abstract classes. Though abstract classes cannot be instantiated, we can create subclasses from it. We can then access members of the abstract class using the object of the subclass. 

```java
abstract class Animal {
  //abstract method
  abstract void makeSound();
  //non abstract method
  public void eat() {
    System.out.println("I can eat.");
  }
}

class Dog extends Animal {

  // provide implementation of abstract method
  public void makeSound() {
    System.out.println("Bark bark");
  }
}

class Main {
  public static void main(String[] args) {

    // create an object of Dog class
    Dog d1 = new Dog();

    d1.makeSound();
    d1.eat();
  }
}
```

</blockquote>
</details>

--- 

8. Brief us on interfaces

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Interface allow us to achieve 100% abstraction in java. An interface is declared by using the `interface` keyword. Sll the methods in an interface are abstract (declared with the empty body), and all the fields are `public`, `static` and `final` by default.

Like abstract classes, we cannot create objects of interfaces.

To use an interface, other classes must implement it. We use the `implements` keyword to implement an interface. A class that implements an interface must implement all the methods declared in the interface.

```java
interface Polygon {
  void getArea(int length, int breadth);
}

// implement the Polygon interface
class Rectangle implements Polygon {

  // implementation of abstract method
  public void getArea(int length, int breadth) {
    System.out.println("The area of the rectangle is " + (length * breadth));
  }
}

class Main {
  public static void main(String[] args) {
    Rectangle r1 = new Rectangle();
    r1.getArea(5, 6);
  }
}
```
 
</blockquote>
</details>

--- 

9. Difference between abstract classes and interfaces

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 | Abstract class                                                             | Interface                                                                                            |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Abstract class can have abstract and non-abstract methods.                 | Interface can have only abstract methods. Since Java 8, it can have default and static methods also. |
| Abstract class doesn't support multiple inheritance.                       | Interface supports multiple inheritance.                                                             |
| Abstract class can have final, non-final, static and non-static variables. | Interface has only static and final variables.                                                       |
| The `abstract` keyword is used to declare abstract class.                  | The `interface` keyword is used to declare interface.                                                |
| n abstract class can be extended using keyword `extends`.                  | An interface can be implemented using keyword `implements`.                                          |
| Members can be private, protected, default or public.                      | Members of a interface are public by default.                                                        |
 
</blockquote>
</details>

--- 

10. What is Abstraction? or Describe abstract in OOP (or) What does Abstraction do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Abstraction is an important concept of object oriented programming that allows us to hide unnecessary details and only show the needed information.

A practical example of abstraction can be motorbike brakes. We know what brake does. When we apply the brake, the motorbike will stop. However, the working of the brake is kept hidden from us.

The major advantage of hiding the working of the brake is that now the manufacturer can implement brake differently for different motorbikes, however, what brake does will be the same.

**Abstraction lets you focus on what the object does instead of how it does it.**

There are two ways to achieve abstraction in java
1. Abstract class (0 to 100% abstraction)
2. Interface (100% abstraction)

</blockquote>
</details>

--- 

11. What is inheritance? (or) Brief us on inheritance

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Inheritance in Java is a concept that acquires the properties from one class to other classes; for example, the relationship between father and son. Inheritance in Java is a process of acquiring all the behaviours of a parent object.

The parent-child relationship, also known as the **IS-A** relationship, is represented by inheritance.
 
</blockquote>
</details>

--- 


12. Brief us on encapsulation and access modifiers (or) How do you achieve encapsulation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Encapsulation can be achieved by declaring all the variables in the class as private and writing public methods in the class to set and get the values of variables.

**Encapsulation = private data members + public getters or setters**
 
</blockquote>
</details>

--- 

13. How many constructors you used in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 Yes, a class can have multiple constructors that assign the fields in different ways.

</blockquote>
</details>

--- 

14. Can you do static overriding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

 We can declare static methods with the same signature in the subclass, but it is not considered overriding as there won’t be any run-time polymorphism. Hence the answer is **No**. 
 
</blockquote>
</details>

--- 

15. What are the types of Inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

There are 5 types of Inheritance. They are

1. Single Inheritance
2. Multi-level Inheritance
3. Hierarchical Inheritance
4. Hybrid Inheritance
5. Multiple inheritance 

**In java, multiple and hybrid inheritance is supported through interface only.**
 
 ![image](https://user-images.githubusercontent.com/70228962/193798049-81ea6a70-ea0e-4608-8789-d73370162d9a.png)

</blockquote>
</details>

--- 

16. When do you use Abstract Class and Interfaces?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

When we have the requirement of a class that contains some common properties or methods with some common properties whose implementation is different for different classes, in that situation, it's better to use Abstract Class then Interface.

Interfaces are a good choice when we think that the API will not change for a while.
Interfaces are also good when we want to have something similar to multiple inheritances since we can implement multiple interfaces.

The JDBC API is an excellent example. It exist of almost only interfaces. The concrete implementations are provided as "JDBC drivers". This enables you to write all the JDBC code independent of the DB vendor. You can just change the JDBC driver without changing any line of Java code (except of any hardcoded DB-specific SQL code) whenever you'd like to switch of DB vendor.
 
 
</blockquote>
</details>

--- 

17. Brief us on the types of Polymorphism

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

There are two types of polymorphism as below: 
1. Static Binding or Compile time Polymorphism or Method Overloading
2. Dynamic Binding or Runtime Polymorphism or Method overriding.
 
</blockquote>
</details>

--- 

18. Can the main method be overridden?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 No, we cannot override main method of java because a static method cannot be overridden.
 
</blockquote>
</details>

--- 

19. What are Constructors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

 A constructor in Java is a special method that is used to initialize objects. The constructor is called when an object of a class is created.
 
</blockquote>
</details>

--- 

20. What is a class? What is an object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
A class is a blueprint for the object. Before we create an object, we first need to define the class.

We can think of the class as a sketch (prototype) of a house. It contains all the details about the floors, doors, windows, etc. Based on these descriptions we build the house. House is the object.

Since many houses can be made from the same description, we can create many objects from a class.
 
</blockquote>
</details>

--- 

21. What is the benefit of inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- Inheritance helps in **code reuse**. The child class may use the code defined in the parent class without re-writing it.
- Inheritance makes the code flexible to change, as you will adjust only in one place, and the rest of the code will work smoothly.
- With the help of Inheritance, you can override the methods of the base class.
- The base class in Inheritance decides which data to be kept private, such that the derived class will not be able to alter it.
 
</blockquote>
</details>

--- 

22. Can we implement multiple inheritances in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Java does not support multiple inheritance using classes. It can be achieved or implemented using interfaces.
 
</blockquote>
</details>

--- 

24. Can you change the scope of a method or class using inheritance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 Yes, we can change the scope of the overridden method in the subclass. However, we cannot decrease the accessibility of the method. 

While changing the accessibility of the method,
  - private can be changed to protected, public, or default.
  - protected can be changed to public or default.
  - default can be changed to public.
  - public will always remain public.
 
</blockquote>
</details>

--- 

26. What are the benefits of abstraction?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>

- Helps to increase the security of an application or program as only essential details are provided to the user.
- Avoids code duplication and increases reusability. 
- It improves the maintainability of the application. It improves the modularity of the application.
</blockquote>
</details>

--- 

27. What is the difference between class and object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 +---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| Class                                                                     | Object                                                                                      |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| Class is a blueprint or template from which objects are created.          | Object is an instance of a class.                                                           |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| Class is a group of similar objects.                                      | Object is a real world entity such as pen, laptop, mobile, bed, keyboard, mouse, chair etc. |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| When a class is created, no memory is allocated.                          | Objects are allocated memory space whenever they are created.                               |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| The class has to be declared first and only once.                         | An object is created many times as per requirement.                                         |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| It is declared with the class keyword                                     | It is created with a class name and a `new` keyword in Java.                                |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+
| Class does not contain any values which can be associated with the field. | Each object has its own values, which are associated with it.                               |
+---------------------------------------------------------------------------+---------------------------------------------------------------------------------------------+

</blockquote>
</details>

--- 

10. How can we change the super class method according to the requirements of sub class in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It can be done by method overriding , which is a type of polymorphism. It can modify a super class method in the sub class.

</blockquote>

</details>

---

19. Can an interface extends another interface in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

 Yes, an interface can extend another interface in Java.

</blockquote>

</details>

---

22. What happens if a class has implemented an interface but has not provided implementation for that method defined in Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

The class has to be declared with an abstract modifier, which will be enforced by the Java compiler.

</blockquote>

</details>

---

28. Can we declare a class as Abstract without having any abstract method?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes we can create an abstract class by using abstract keyword before class name even if it doesn’t have any abstract method.If a class has even one abstract method, it must be declared as abstract otherwise it will give an error.

</blockquote>

</details>

---

30. Can we call the constructor of a class more than once for an object?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It’s called only once for an object automatically at the time of object creation using new keyword. we can’t invoke the constructor again for an object after its creation.

</blockquote>

</details>

---

33. How can we stop inherting a class from other class in Java?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If we want a class not to be extended further by any class, we can use the keyword `Final` with the class name.

In the following example, Stone class is Final and can’t be extended

``` java
public Final Class Stone {
	// Class methods and Variables
}
```

 </blockquote>

</details>

---

34. Can we use a default constructor of a class even if an explicit constructor is defined?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. Java provides a default no argument constructor if no explicit constructor is defined in a class. But if an explicit constructor has been defined, default constructor can’t be invoked and developer can use only those constructors which are defined in the class.

 </blockquote>

</details>

---

41. Is it possible to change the value of any variable defined in the class implementing an interface?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

No, we can’t change the value of any variable of an interface in the implementing class as all variables defined in the interface are by default public, static and Final. final variables are like constants which can’t be changed later

  </blockquote>

</details>

---

42. What part of memory (Stack/Heap) is cleaned in garbage collection process?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

Heap. Because when Java programs run on the JVM, objects are created on the heap,

  </blockquote>

</details>

---

45. Can we achieve method overloading by changing the return type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

No, We cannot achieve method overloading through return type in Java.

</blockquote>

</details>

---

46. Can we extend a String class?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, String is a final class, therefore we cannot extend or inherit it.

</blockquote>

</details>

---

54. Explain about inner class in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, we can define a class inside a class and they are called nested classes. Any nested class which is non-static are known as inner class. 

</blockquote>

</details>

---