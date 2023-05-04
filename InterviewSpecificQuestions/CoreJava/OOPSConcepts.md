1. What is the difference between method and function?

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

2. Explain OOPs.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- **O**bject **O**riented **P**rogramming is a programming paradigm/model which revolves around the concept of **Objects**. 
- Objects can be considered as real-world instances of entities like class, that have **characteristics** and **behaviors**

**For example,**, if we consider a car, then based on the OOPs model:

- Class: A specific car model, such as Audi A4, BMW I8, Maruti Suzuki Vitara Brezza, etc.
- Object: A specific car of any model, like the car you own
- Characteristics: What is the color of your car? What is the model of your car? etc.
- Behavior: How to start the car? How to change the gear of the car? etc.

Characteristics are also known as data, attributes, or properties, and Behaviors are also known as the functions, procedures, or methods, in the programming language.

</blockquote>
</details>

--- 

3. What are the pillars of OOPs?

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

4. What is polymorphism?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- The word poly means many and morphs means forms, so polymorphism means many forms.
- It's an ability of an object to exhibit more than one form

For example: A man at the same time is a father, a husband, an employee. So, the same person possesses different behavior in different situations. This is called polymorphism. 

</blockquote>
</details>

--- 

5. What is method overloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
<blockquote>
 
- Method Overloading is a feature that allows a class to have more than one method with the same name, but with different parameters.
- It is also known as Compile-time Polymorphism or Static Polymorphism 

**For example,**: 
```java
public class SquaringDemo {
	
	public void square(int n) {
		System.out.println("Method with int argument called: " + n*n).
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

6. Explain Encapsulation.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Encapsulation is the way of binding the data (variables) and code acting on the data (methods) together as a single unit.  

For example, in a company, they are different sections like the accounts section, finance section, sales section etc. Consider a situation, a person from finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. 

In encapsulation, the variables of a class will be hidden from other classes and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

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
 
Interface allow us to achieve 100% abstraction in java. An interface is declared by using the `interface` keyword. All the methods in an interface are abstract (declared with the empty body), and all the fields are `public`, `static` and `final` by default.

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
| Abstract class can have final, non-final, static, and non-static variables. | Interface has only static and final variables.                                                       |
| The `abstract` keyword is used to declare abstract class.                  | The `interface` keyword is used to declare interface.                                                |
| n abstract class can be extended using keyword `extends`.                  | An interface can be implemented using keyword `implements`.                                          |
| Members can be private, protected, default or public.                      | Members of an interface are public by default.                                                        |
 
</blockquote>
</details>

--- 

10. What is Abstraction? or Describe abstract in OOP (or) What does Abstraction do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Abstraction is an important concept of object-oriented programming that allows us to hide unnecessary details and only show the needed information.

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
 
Inheritance in Java is a concept that acquires the properties from one class to other classes: for example, the relationship between father and son. Inheritance in Java is a process of acquiring all the behaviors of a parent object.

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

The JDBC API is an excellent example. It exists of almost only interfaces. The concrete implementations are provided as "JDBC drivers". This enables you to write all the JDBC code independent of the DB vendor. You can just change the JDBC driver without changing any line of Java code (except of any hardcoded DB-specific SQL code) whenever you'd like to switch of DB vendor.
 
 
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

23. Can you change the scope of a method or class using inheritance?

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

24. What are the benefits of abstraction?

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

25. What is the difference between class and object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
	
 
| Class                                                                     | Object                                                                                      |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Class is a blueprint or template from which objects are created.          | Object is an instance of a class.                                                           |
|  Class is a group of similar objects.                                     | Object is a real-world entity such as pen, laptop, mobile, bed, keyboard, mouse, chair etc. |
|  When a class is created, no memory is allocated.                         | Objects are allocated memory space whenever they are created.                               |
| The class has to be declared first and only once.                         | An object is created many times as per requirement.                                         |
| It is declared with the class keyword                                     | It is created with a class name and a \`new\` keyword in Java.                              |
| Class does not contain any values which can be associated with the field. | Each object has its own values, which are associated with it.                               |

</blockquote>
</details>

--- 

26. How can we change the super class method according to the requirements of sub class in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It can be done by method overriding , which is a type of polymorphism. It can modify a super class method in the sub class.

</blockquote>

</details>

---

27. Can an interface extends another interface in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

 Yes, an interface can extend another interface in Java.

</blockquote>

</details>

---

28. What happens if a class has implemented an interface but has not provided implementation for that method defined in Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

The class has to be declared with an abstract modifier, which will be enforced by the Java compiler.

</blockquote>

</details>

---

29. Can we declare a class as Abstract without having any abstract method?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, we can create an abstract class by using abstract keyword before class name even if it doesn’t have any abstract method. If a class has even one abstract method, it must be declared as abstract otherwise it will give an error.

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

31. How can we stop inheriting a class from other class in Java?

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

32. Can we use a default constructor of a class even if an explicit constructor is defined?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. Java provides a default no argument constructor if no explicit constructor is defined in a class. But if an explicit constructor has been defined, default constructor can’t be invoked, and developer can use only those constructors which are defined in the class.

 </blockquote>

</details>

---

33. Is it possible to change the value of any variable defined in the class implementing an interface?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

No, we can’t change the value of any variable of an interface in the implementing class as all variables defined in the interface are by default public, static and Final. final variables are like constants which can’t be changed later

  </blockquote>

</details>

---

34. What part of memory (Stack/Heap) is cleaned in garbage collection process?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

Heap. Because when Java programs run on the JVM, objects are created on the heap,

  </blockquote>

</details>

---

35. Can we achieve method overloading by changing the return type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

No, we cannot achieve method overloading through return type in Java.

</blockquote>

</details>

---

36. Can we extend a String class?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, String is a final class, therefore we cannot extend or inherit it.

</blockquote>

</details>

---

37. Explain about inner class in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, we can define a class inside a class, and they are called nested classes. Any nested class which is non-static are known as inner class. 

</blockquote>

</details>

---

38. What is the difference between a constructor and a method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In object-oriented programming, a constructor and a method are both types of functions, but they serve different purposes.

A constructor is a special type of method that is called automatically when an object is created. Its purpose is to initialize the object's instance variables and set them to some default or initial values. Constructors are usually named after the class and have no return type.

A method, on the other hand, is a function that is defined within a class and operates on the object's data. Methods can be used to manipulate the object's data, perform calculations, or perform any other action that is necessary for the object to function properly. Methods can take parameters and return values, and they can be called by the object or by other parts of the program that have access to the object.

In summary, a constructor is used to initialize an object's state when it is created, while a method is used to perform operations on the object's state after it has been created.

</blockquote>

</details>

---

39. How do you call another constructor from a constructor? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, you can call another constructor of the same class using the this keyword and the constructor's parameters. Here's an example:

```java
public class MyClass {
   private int myValue;

   // First constructor
   public MyClass(int value) {
      myValue = value;
   }

   // Second constructor that calls the first constructor
   public MyClass() {
      this(0); // Calls the first constructor with value = 0
   }
}
```
In the example above, the second constructor calls the first constructor using the this keyword and passing in the value 0. This means that when an object is created using the second constructor, it will have a default value of 0 for the myValue field.

You can also use the super keyword to call a constructor from the superclass if the class you're defining is a subclass. In that case, the super keyword is used instead of this. For example:

```java
public class MySubClass extends MyClass {
   public MySubClass() {
      super(10); // Calls the superclass constructor with value = 10
   }
}
```
In this example, the MySubClass constructor calls the superclass constructor with a value of 10 using the super keyword.

</blockquote>

</details>

---
40. What is the difference between the super keyword and this keyword regarding local variables 


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, the super and this keywords are used to refer to different things, including local variables.

The this keyword is used to refer to the current instance of the class and is used to access instance variables and methods. When used with local variables, this is used to disambiguate a local variable from an instance variable with the same name. For example:

```java
public class MyClass {
    private int myVariable;

    public void myMethod(int myVariable) {
        this.myVariable = myVariable; // Use "this" to access the instance variable
        int localVariable = myVariable; // Use the local variable with the same name
    }
}
```
In this example, this.myVariable refers to the instance variable myVariable of the class MyClass, while int localVariable = myVariable creates a new local variable with the same name as the parameter.

On the other hand, the super keyword is used to refer to the parent class of the current class and is not used to access local variables. The use of super is limited to accessing the parent class's constructors, methods, and instance variables.

In summary, this is used to refer to the current instance of the class and can be used to disambiguate local variables from instance variables with the same name, while super is used to refer to the parent class of the current class and is not used to access local variables.

</blockquote>

</details>

---

41. What is constructor overloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Constructor overloading in Java refers to the practice of defining multiple constructors for a class with different parameters. When a class has multiple constructors, each constructor can be called with a different set of arguments to create objects with different initial states.

Constructor overloading is similar to method overloading, which allows multiple methods with the same name but different parameters to be defined in a class.

Here's an example of constructor overloading in Java:

```java
public class MyClass {
    private int myValue;

    // Constructor with no parameters
    public MyClass() {
        myValue = 0;
    }

    // Constructor with one parameter
    public MyClass(int value) {
        myValue = value;
    }

    // Constructor with two parameters
    public MyClass(int value1, int value2) {
        myValue = value1 + value2;
    }
}
```

In this example, MyClass has three constructors: one with no parameters, one with one parameter, and one with two parameters. Each constructor sets the value of myValue based on the arguments passed to it. This allows objects of MyClass to be created with different initial states depending on which constructor is used.

Constructor overloading can be useful when you want to provide different ways to create objects of a class with different initial states, or when you want to provide default values for some of the object's fields.


</blockquote>

</details>

---

42. Can constructors be private?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, constructors can be made private in Java. When a constructor is declared as private, it can only be accessed from within the class, which means that objects of the class cannot be created from outside the class.

One use case for private constructors is to implement the Singleton design pattern. In the Singleton pattern, a class is designed to have only one instance, and the constructor is made private to prevent multiple instances from being created. The Singleton pattern is often used for objects that represent system resources or settings that should not be duplicated.

Here's an example of a class with a private constructor that implements the Singleton pattern:

```java
public class MySingleton {
    private static MySingleton instance = new MySingleton();

    private MySingleton() {
        // Private constructor
    }

    public static MySingleton getInstance() {
        return instance;
    }

    // Other methods and fields
}
```

In this example, the MySingleton class has a private constructor, which means that objects of this class cannot be created from outside the class. Instead, the class provides a getInstance() method, which returns the only instance of the class that is created when the class is loaded. This ensures that only one instance of MySingleton exists throughout the lifetime of the program.

Note that if a class has only private constructors, it cannot be subclassed or extended.

</blockquote>

</details>

---

43. Why would we want constructors to be private?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are several reasons why we might want to make constructors private in Java:

To implement the Singleton pattern: Making the constructor private is often used to implement the Singleton pattern, where a class is designed to have only one instance.

To prevent object creation: In some cases, we might want to prevent objects of a class from being created. By making the constructor private, we can ensure that the class can only be used as a utility class or a container for static methods and fields.

To restrict subclassing: If a class has only private constructors, it cannot be extended or subclassed. This can be useful when we want to ensure that a class cannot be modified or overridden.

To control object creation: By making the constructor private, we can control how objects of a class are created. For example, we might want to ensure that objects are only created under certain conditions, or that certain initialization steps are performed before an object is created.

To implement a factory method pattern: In some cases, we might want to provide a factory method for creating objects of a class, rather than allowing direct instantiation with a constructor. By making the constructor private and providing a factory method, we can control how objects are created and provide additional functionality such as caching or pooling of objects.

Overall, making constructors private can be a useful tool for controlling object creation, preventing unwanted modifications, and implementing design patterns.

</blockquote>

</details>

---

44. Can we inherit private classes in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, it is not possible to inherit or extend a private class in Java. Private classes are only accessible within the class in which they are defined, and cannot be accessed or extended from outside the class.

</blockquote>

</details>

---

45. Java Classes – How many can you extend?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, a class can extend only one class at a time. This is known as single inheritance, where a subclass inherits the properties and behaviors of a single superclass.

Java was designed with single inheritance to avoid the problems of multiple inheritance, which can lead to ambiguity when two or more superclasses define methods or fields with the same name. Single inheritance simplifies the language and makes it easier to reason about the behavior of objects.

However, Java provides an alternative way to reuse code through interfaces, which allow a class to define a set of method signatures without implementing them. A class can implement multiple interfaces, which can be seen as a form of multiple inheritance, where a subclass inherits the method signatures and is required to provide implementations for them.

Here's an example to illustrate this:

```java
public class MyClass extends MySuperclass implements MyInterface1, MyInterface2 {
    // Code for MyClass
}
```

In this example, MyClass extends MySuperclass and implements two interfaces, MyInterface1 and MyInterface2. This allows MyClass to inherit the properties and behaviors of MySuperclass, while also defining the method implementations required by the interfaces.

So, to summarize, a class can extend only one class in Java, but it can implement multiple interfaces

</blockquote>

</details>

---

46. What is a marker interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, a marker interface is an interface that has no methods or fields, and is used only to mark or tag a class. A class that implements a marker interface indicates that it has some specific characteristic or capability that the interface represents.

Marker interfaces are also known as "tagging interfaces" or "trait interfaces". They are typically used for metadata purposes, where the presence or absence of an interface is used to control or influence the behavior of the program.

Here are some examples of marker interfaces in Java:

Serializable - This interface is used to mark a class as serializable, which means that its state can be saved to a stream and reconstructed later.

Cloneable - This interface is used to mark a class as cloneable, which means that it can be duplicated using the clone() method.

RandomAccess - This interface is used to mark a list as random-access, which means that its elements can be accessed in constant time.

Readable and Writable - These interfaces are used to mark classes as readable or writable, which means that they can be used with I/O streams.

Remote - This interface is used in Java RMI to mark classes as remote, which means that they can be accessed by remote clients.

Annotation - This interface is used to mark an annotation type, which is used to add metadata to Java code.

</blockquote>

</details>

---

47. Can an interface extend a class? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, in Java, an interface cannot extend a class. An interface is a completely separate construct from a class and cannot inherit from a class. In Java, an interface can only extend another interface, using the extends keyword.

The reason for this is that a class and an interface have different purposes and functionality in Java. A class defines the behavior and state of an object, while an interface defines a set of methods that a class must implement. Since a class and an interface serve different purposes, it is not possible to mix the two by allowing an interface to extend a class.

However, a class can implement multiple interfaces, allowing it to provide implementations for multiple sets of methods. This is a powerful feature of Java that allows for flexible and modular design.

</blockquote>

</details>

---

48. What is the difference between method overloading and method overriding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Method overloading and method overriding are two important concepts in object-oriented programming in Java. The main difference between them is that method overloading involves creating multiple methods with the same name in a class, but with different parameters, whereas method overriding involves creating a new implementation of a method in a subclass, with the same name and parameters as a method in its superclass.

Here are some more details about each concept:

Method Overloading:

Method overloading is a feature of Java that allows a class to have multiple methods with the same name, but with different parameters.
The methods must have different parameter lists, which can differ in terms of the number, order, and types of parameters.
Method overloading allows a class to provide multiple ways of calling the same method, depending on the types and number of arguments passed to it.
Method overloading is resolved at compile time, based on the number and types of arguments passed to the method.
Method Overriding:

Method overriding is a feature of Java that allows a subclass to provide a new implementation of a method that is already defined in its superclass.
The method in the subclass must have the same name and parameters as the method in the superclass.
Method overriding allows a subclass to provide a specialized implementation of a method that is tailored to its specific needs.
Method overriding is resolved at runtime, based on the actual type of the object that the method is called on.
In summary, method overloading involves creating multiple methods with the same name in a class, but with different parameters, while method overriding involves creating a new implementation of a method in a subclass, with the same name and parameters as a method in its superclass.

</blockquote>

</details>

---

49. Is Java strictly OOP ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Java is considered to be a strongly object-oriented programming language, meaning that it is designed around the principles of object-oriented programming (OOP).

In Java, everything is an object, including primitives like int and boolean, which are represented as wrapper classes such as Integer and Boolean. Java also supports all the key features of OOP, such as encapsulation, inheritance, and polymorphism.

However, Java also includes some features that are not strictly object-oriented, such as static methods and variables, which belong to the class rather than to any instance of the class. Java also has basic support for procedural programming, as it allows for the use of functions outside of classes.

So while Java is designed around the principles of OOP and is widely considered to be an object-oriented language, it also includes some non-OOP features and supports other programming paradigms.

</blockquote>

</details>

---

