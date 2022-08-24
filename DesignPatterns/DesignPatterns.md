1.How can you describe a design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Design patterns are the reusable solutions that solve common problems of software development. These problems include repetitive code, redundant functions and logic etc. These help to save considerable effort and time required for the developers while developing software. Design patterns are commonly used in object-oriented software products by incorporating best practices and promoting reusability for developing robust code.Defining  a pattern name and the classification of design pattern in which the pattern would fall to.Defining a Problem and its corresponding solution.The variations and language-dependent alternatives for the problem that needs to be addressed.The real-time use cases and the efficiency of the software that uses these patterns.
</blockquote>

</details>

---

2. How Inversion of Control can be used as a design pattern ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Inversion of control is a pattern used to decouple the dependencies between layers and components in the system. The Dependency-Injection (DI) pattern is an example of an IoC pattern that helps in removing dependencies in the code. For example, Consider we have a class A that makes use of class B as shown below:

```java

public class A{
   private B b;
   
   public A(){
       this.b = new B();
   }
}

```

Here, we have a dependency between classes A and B. If we had the IoC pattern implemented, we would not have used the new operator to assign value to the dependent variable. It would have been something as shown below:

```java

public class A {
   private IocB b;
   public A(IocB b) {
       this.b = b;
   }
}

```

We have inverted the control of handing the dependency of instantiating the object of class B to the IoC class IocB.

</blockquote>

</details>

---

3. How can you describe the SOLID Principles of the design pattern?

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

4. What do you understand by the Open-Closed Principle (OCP)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


The Open close principle states that any class, component or entity should be open for extension but closed for modification. A class can be extended via Inheritance, Interfaces, Composition whenever required instead of modifying the code of the class. Consider an instance where we have a class that calculates the area of a square. Later, we get the requirement of calculating the area of a rectangle. Here, instead of modifying the original class, we can create one base class and this base class can be extended by the new class rectangle.

</blockquote>

</details>

---

5. What are the design patterns used in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Decorator pattern are used by the Wrapper classes.
- Singleton pattern is used in classes like Calendar and Runtime.
- Factory pattern is used for methods like Integer.valueOf methods in wrapper classes.
- Observer pattern is used for handling event frameworks like awt, swing etc

</blockquote>

</details>

---



---
