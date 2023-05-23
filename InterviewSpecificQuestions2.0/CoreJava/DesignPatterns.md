1.	What are Design Patterns? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

- Design patterns are reusable solutions to general problems including repetitive code, redundant functions, and logic that software developers faced during software development.
- Design patterns are commonly used in object-oriented software products by incorporating best practices and promoting reusability for developing robust code.

</blockquote>
</details>


---
2. What is DAO?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

DAO stands for Data Access Object. DAO Design Pattern is used to separate the data persistence logic in a separate layer. 

The following are the components of the DAO Pattern.

- **Data Access Object Interface:** DAO interface describes the standard actions to be performed on model objects.
- **Data Access Object concrete class:** This class implements a DAO interface. This class is accountable to get data from a data source which can be XML/database or any other storage mechanism.
- **Model Object or Value Object:** This object is a plain old java object containing get/set methods to store data retrieved using DAO class.
</blockquote>
</details>

--- 

3. What is a Singleton pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Singleton is a creational design pattern that lets you ensure that a class has only one instance while providing a global access point to this instance.

Implementations of the Singleton have these two steps in common:

- Make the default constructor private, to prevent other objects from using the new operator with the Singleton class.
- Create a static creation method that acts as a constructor. Under the hood, this method calls the private constructor to create an object and saves it in a static field. All following calls to this method return the cached object.

If your code has access to the Singleton class, then it’s able to call Singleton’s static method. So whenever that method is called, the same object is always returned.

</blockquote>
</details>

--- 

4. Describe the SOLID Principles.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- S - Single Responsibility Principle (SRP): The single responsibility principle ensures that every class or module should be accountable and responsible for only one functionality. There should be one and only one reason for changing any class.
- O - Open Closed Principle (OCP): Every class is open for extension but closed for modification. Here, we are allowed to extend the entity’s behavior by not modifying anything in the existing source code.
- L - Liskov Substitution Principle(LSP): LSP principle states that the objects can be replaced by the subtype instances without affecting the correctness of the program.
- I - Interface Segregation Principle (ISP): The ISP principle states that we can use as many interfaces specific to the client’s requirements instead of creating only one general interface. Clients should not be forced to implement the functionalities that they do not require.
- D - Dependency Inversion Principle: Here, the high-level modules should not be dependent on the lower-level modules or concrete implementations. Instead, they should be dependent on abstractions.

</blockquote>

</details>

---


5. How are design principles different from design patterns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Design principles are those principles that are followed while designing software systems for any platform by making use of any programming language. SOLID principles are the design principles that we follow as guidelines to develop robust, extensible, and scalable software systems. These apply to all aspects of programming.
- Design Patterns are reusable template solutions for commonly occurring problems that can be customized as per the problem requirements. These are well-implemented solutions that are tested properly and safe to use. Factory Design Patterns, Singleton patterns, and Strategy patterns are a few examples of design patterns

</blockquote>

</details>

---


6. Explain Factory Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Factory design pattern belongs to the category of Creational Design Patterns. Here, the objects are created without exposing the logic of creation to the client. The objects refer to the common interface. This pattern allows for hiding the creation logic of the application by using interfaces and factory classes. It lets to test the seamlessness of the application by using mock or stubs.
Introduces loose coupling in the application by allowing flexibility in the implementation of methods when new classes are introduced

For example, Let’s consider 3 classes Square, Rectangle, and Triangle. We will be using factory patterns to create objects of these three classes without exposing the creation logic by making use of ShapeFactory class. The Driver class would be passing information like rectangles, squares & triangles for getting the required object. 

- Create a Shape interface.

```java
   public interface Shape {
      void draw();
   }
```

- Create concrete classes Rectangle, Square, and Triangle that implements the Shape interface.

```java
 
   public class Rectangle implements Shape {
      @Override
      public void draw() {
         System.out.println("Showing Rectangle class");
      }
   }
   
   public class Square implements Shape {
      @Override
      public void draw() {
         System.out.println("Showing Square class");
      }
   }
  
   public class Triangle implements Shape {
      @Override
      public void draw() {
         System.out.println("Showing Triangle class");
      }
   }
```

- Create ShapeFactory class and create a method called getShape() for generating objects of the concrete classes defined above.

```java
   public class ShapeFactory {
      //the method will be used to get the object of the required shape
      public Shape getShape(String type){
         if(type == null){
            return null;
         } 
         if(type.equalsIgnoreCase("TRIANGLE")){
            return new Triangle();
         } else if(type.equalsIgnoreCase("SQUARE")){
            return new Square();
         } else if(type.equalsIgnoreCase("RECTANGLE")){
            return new Rectangle();
         }
         return null;
      }
   }
```

- Implement the Driver class and utilize the factory class for getting the object of the required type.

```java
   public class Driver {
      public static void main(String[] args) {
         ShapeFactory shapeFactory = new ShapeFactory();
         Shape triangle = shapeFactory.getShape("Triangle");
         triangle.draw();   
         Shape rectangle = shapeFactory.getShape("RECTANGLE");
         rectangle.draw();   
         Shape square = shapeFactory.getShape("SQUARE");
         square.draw();
      }
   }
// Output:
//   Showing Rectangle class
//   Showing Triangle class
//   Showing Squarue class
	
```
	
</blockquote>

</details>

---

7. Explain the MVC design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
MVC stands for Model-View-Controller. This pattern is used for separating the application’s concerns as listed below:

- Model - This represents the object (Java POJO) that carries the data. It can also consist of the logic of updating the controller in case the data changes.
- View - This represents the data visualization of the model.
- Controller - This is an interface between the Model and the View by controlling the flow of data into the model and updating the view whenever the model gets updated. This ensures that the model and the views are kept separate.

</blockquote>

</details>

---

8. What is the Observer design pattern?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Observer design pattern establishes a one-to-many dependency between objects, so that when one object changes its state, all its dependents are notified and updated automatically. It enables loosely coupled communication between objects, promoting maintainability and flexibility.

</blockquote>

</details>

---

9. What is the Strategy design pattern?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Strategy design pattern allows you to define a family of interchangeable algorithms and encapsulate each one as a separate class. It lets the algorithms vary independently from the clients that use them, promoting code reusability and flexibility.

</blockquote>

</details>

---

10. What is the Decorator design pattern?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Decorator design pattern attaches additional responsibilities to an object dynamically. It provides a flexible alternative to subclassing for extending functionality. The decorator wraps the original object and adds new behaviors without modifying its structure.

</blockquote>

</details>

---

11. What is the Builder design pattern?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Builder design pattern is used to create complex objects step by step. It separates the construction of an object from its representation, allowing the same construction process to create different representations. It provides a clean way to build objects with many optional parameters.

</blockquote>

</details>

---

12. What is the Iterator design pattern?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Iterator design pattern provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation. It encapsulates the traversal logic and provides a common interface for iterating over different types of collections.

</blockquote>

</details>

---

13. What is the Command design pattern?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Command design pattern encapsulates a request as an object, allowing you to parameterize clients with different requests, queue or log requests, and support undoable operations. It decouples the requester of a command from the object that performs the command.

</blockquote>

</details>

---

14. Why are design patterns important?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Design patterns provide proven solutions to recurring design problems, improve code maintainability, promote code reusability, and enhance software development efficiency.

</blockquote>

</details>

---

15. What are the three types of design patterns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The three types of design patterns are creational, structural, and behavioral patterns.

</blockquote>

</details>

---