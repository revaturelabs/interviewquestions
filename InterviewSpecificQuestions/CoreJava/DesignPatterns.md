1.What is Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

- Design patterns are reusable solutions to general problems like include repetitive code, redundant functions and logic that software developers faced during software development.
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

Following are the components in the DAO Pattern.

- **Data Access Object Interface:** DAO interface describes the standard actions to be performed on a model objects.
- **Data Access Object concrete class:** This class implements a DAO interface. This class is accountable to get data from a data source which can be Xml/database or any other storage mechanism.
- **Model Object or Value Object:** This object is a plain old java object containing get/set methods to store data retrieved using DAO class.
</blockquote>
</details>

--- 

3. What is a singleton pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Singleton is a creational design pattern that lets you ensure that a class has only one instance, while providing a global access point to this instance.

Implementations of the Singleton have these two steps in common:

- Make the default constructor private, to prevent other objects from using the new operator with the Singleton class.
- Create a static creation method that acts as a constructor. Under the hood, this method calls the private constructor to create an object and saves it in a static field. All following calls to this method return the cached object.

If your code has access to the Singleton class, then it’s able to call the Singleton’s static method. So whenever that method is called, the same object is always returned.

</blockquote>
</details>

--- 

3. Describe the SOLID Principles.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- S - Single Responsibility Principle (SRP): The single responsibility principle ensures that every class or module should be accountable and responsible for only one functionality. There should be one and only one reason for changing any class.
- O - Open Closed Principle (OCP): Every class is open for extension but closed for modification. Here, we are allowed to extend the entities behaviour by not modifying anything in the existing source code.
- L - Liskov Substitution Principle(LSP): LSP principle states that the objects can be replaced by the subtype instances without affecting the correctness of the program.
- I - Interface Segregation Principle (ISP): The ISP principle states that we can use as many interfaces specific to the client’s requirements instead of creating only one general interface. Clients should not be forced to implement the functionalities that they do not require.
- D - Dependency Inversion Principle: Here, the high-level modules should not be dependent on the lower level modules or concrete implementations. Instead, they should be dependent on the abstractions.

</blockquote>

</details>

---


6.How are design principles different from design patterns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Design principles are those principles that are followed while designing software systems for any platform by making use of any programming language. SOLID principles are the design principles that we follow as guidelines to develop robust, extensible and scalable software systems. These apply to all aspects of programming.
- Design Patterns are the reusable template solutions for commonly occurring problems that can be customized as per the problem requirements. These are well-implemented solutions that are tested properly and are safe to use. Factory Design Pattern, Singleton pattern, Strategy patterns are a few of the examples of design patterns

</blockquote>

</details>

---


8.Explain  Factory Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Factory design pattern belongs to the category of Creational Design Patterns. Here, the objects are created without exposing the logic of creation to the client. The objects refer to the common interface.This pattern allows hiding the creation logic of the application by using interfaces and factory classes.It lets to test the seamlessness of the application by using mock or stubs.
Introduces loose coupling in the application by allowing flexibility in the implementation of methods when new classes are introduced

For example, Let’s consider 3 classes Square, Rectangle and Triangle. We will be using factory patterns to create objects of these three classes without exposing the creation logic by making use of ShapeFactory class. The Driver class would be passing the information like rectangle,square,triangle for getting the required object. 

- Create a Shape interface.

```java
   public interface Shape {
      void draw();
   }
```

- Create concrete classes Rectangle, Square, Triangle that implements the Shape interface.

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
      //the method will be used to get object of required shape
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

- Implement the Driver class and utilise the factory class for getting the object of the required type.

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

17.Explain MVC design pattern?

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
