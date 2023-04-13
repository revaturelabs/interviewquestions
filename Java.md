
1. Do you know about Java 8?

<details> <summary>Show Answer</summary>
 
<blockquote>

Java 8 is a major release of the Java programming language and its development kit (JDK).It introduced several new features and enhancements to the language, including:

**1. Lambda Expressions:** Lambda expressions provide a concise way of representing an anonymous function in Java. They enable the use of functional programming concepts and allow developers to write more concise and readable code.

**2. Streams:** Streams provide a new way of processing collections in Java. They allow developers to easily perform operations such as filtering, mapping, and reducing on collections with a declarative syntax.

**3. Functional Interfaces:** Functional interfaces are interfaces that have exactly one abstract method. They are used in conjunction with lambda expressions to provide a functional programming style in Java.

**4. Default Methods:** Default methods allow interfaces to have implementation code, which makes it easier to evolve interfaces without breaking existing implementations.

**5. Date and Time API:** Java 8 introduced a new Date and Time API, which is more comprehensive and flexible than the old java.util.Date and java.util.Calendar classes.

**6. Method References:** Method references provide a way to refer to a method without invoking it. They are used along with lambda expressions to simplify code.

**7. Optional:** Optional is a new class in Java 8 that represents a value that may or may not be present. It provides a more elegant way of handling null values and helps to avoid NullPointerExceptions.


- These features aim to improve the readability and conciseness of Java code, as well as make it easier to write parallel code and take advantage of multicore processors. Additionally, Java 8 includes various API improvements and performance optimizations.
  
</blockquote>

</details>

---

2. What are optional objects?

<details> <summary>Show Answer</summary>
 
<blockquote>

- In Java, an `Optional` object is a container object that may or may not contain a non-null value. It is a way of representing a value that may or may not exist, without using null references.
- The purpose of `Optional` is to provide a way to explicitly indicate that a value may be absent, and to avoid NullPointerExceptions. It forces the developer to consider the possibility that a value may not be present and to handle that case explicitly, rather than relying on a null check.
- 


  
</blockquote>

</details>

---

3. Sort elements in a String ArrayList. – Alphabetically - By String length

<details> <summary>Show Answer</summary>

<blockquote>

In Java, this can be achieved by using `Collections.sort()` method and Comparator to compare the string lengths.

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;

public class SortArrayList {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("banana");
        list.add("apple");
        list.add("orange");
        list.add("kiwi");
        list.add("pear");


        Comparator<String> lengthComparator = new Comparator<String>() {
            @Override
            public int compare(String s1, String s2) {
                return Integer.compare(s1.length(), s2.length());
            }
        };
        Collections.sort(list, lengthComparator);
        Collections.sort(list);

        System.out.println("Sorted alphabatically and by string length: " + list);
    }
}

```

  
</blockquote>

</details>

---

4. What is your experience with Postman?

<details> <summary>Show Answer</summary>
 
<blockquote>

- Postman is a popular tool for API development, testing, and collaboration. It provides a user-friendly interface for making HTTP requests, and it supports a wide range of protocols and data formats, making it a versatile tool for working with APIs.

- Postman allows you to easily create and send requests, set headers and parameters, and view the responses. It also includes features for testing and debugging APIs, such as automatic testing scripts, debugging tools, and performance testing.

- Postman also allows you to collaborate with team members and share API documentation and test results. It integrates with version control systems like Git, allowing you to keep track of changes and collaborate on API development.
  
</blockquote>

</details>

---


5. What are some best practices for creating interfaces?


<details> <summary>Show Answer</summary>
 
<blockquote>

Creating interfaces in Java is a powerful feature that enables you to define a contract for the behavior of classes. Here are some best practices for creating interfaces in Java:

**1. Keep interfaces simple:** An interface should define only the necessary methods required for implementing a specific behavior. Avoid adding methods that are not essential or may be better implemented in a class.

**2. Use clear and concise naming conventions:** Naming conventions should be clear and concise to help other developers understand the purpose of the interface.

**3. Favor composition over inheritance:** Interfaces should be used to define contracts, not to provide implementations. Favor composition over inheritance to achieve a more flexible and maintainable codebase.

**4. Design for extension:** When designing interfaces, keep in mind the possibility of extending the interface in the future. Make sure the interface is designed to be easily extended without breaking existing implementations.

**5. Avoid duplicating code:** Interfaces should not duplicate code that is already defined in other interfaces or classes. Instead, use inheritance to reuse code and avoid code duplication.

**6. Document your interfaces:** Document your interfaces to provide clear and concise information on their intended use and the behavior of the methods defined in the interface.

**7. Use default methods with care:** Default methods were introduced in Java 8 to allow adding new methods to interfaces without breaking existing implementations. However, they should be used with care as they can lead to unexpected behavior and can make the code more complex.

Overall, creating interfaces in Java requires careful planning and consideration. Following these best practices can help ensure that your interfaces are well-designed, easy to use, and flexible for future changes.


</blockquote>

</details>

---

6. What is the difference between local variables and rule inputs?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
- Local variables in Java are declared within a block of code, such as a method or a loop, and are only accessible within that block. They can only be accessed from within the block of code where they are declared and are destroyed once the block of code is exited. Local variables in Java must be declared and initialized before they can be used.

- Rule inputs in Java are typically passed as parameters to a method or function. They are used to provide input or conditions to a set of rules, which then determine the appropriate output or action. Rule inputs in Java are similar to local variables in that they are only accessible within the block of code where they are declared, but they are typically declared as parameters to a method or function, rather than being declared within the method or function itself.

- Both local variables and rule inputs can be of different data types, such as int, float, String, or boolean, and can be used in calculations, comparisons, and other operations. However, their specific use cases and scope differ: local variables are used to store intermediate values within a specific block of code, while rule inputs are used to provide input or conditions to a set of rules or function.

  
</blockquote>

</details>

---

7. Have you used any testing frameworks? Ex. JUnit, Mockito

<details> <summary>Show Answer</summary>
 
<blockquote>
  
Yes, JUnit and Mockito are two commonly used testing frameworks in Java.

**JUnit:**

- It is a testing framework for Java that is used to write and run unit tests. It provides a set of annotations and assertions that allow developers to define and verify the behavior of their code in a systematic way. 
- With JUnit, developers can write test cases that verify the output of methods or the behavior of classes, and can automate the testing process, ensuring that their code is working as expected. 


**Mockito:** 

- It is a mocking framework for Java that is used to create mock objects for testing. 
- It allows developers to simulate the behavior of objects and dependencies, and to write test cases that focus on specific aspects of their code. 
- It provides a simple API for creating and configuring mock objects, and integrates seamlessly with JUnit, making it a popular choice for unit testing in Java. 
- It allows developers to isolate the code under test and test specific scenarios, without having to set up complex dependencies or write redundant test code.

Both JUnit and Mockito are essential tools for Java developers who want to ensure that their code is robust, reliable, and maintainable.

</blockquote>

</details>

---

8. 4 pillars of OOP.

<details> <summary>Show Answer</summary>
 
<blockquote>

The Four Pillars of Object-Oriented Programming are
**1. Abstraction:**

Abstraction is an important concept of object-oriented programming that allows us to hide unnecessary details and only show the needed information.

A practical example of abstraction can be motorbike brakes. We know what brake does. When we apply the brake, the motorbike will stop. However, the working of the brake is kept hidden from us.

The major advantage of hiding the working of the brake is that now the manufacturer can implement brake differently for different motorbikes, however, what brake does will be the same.

<i><b>Abstraction lets you focus on what the object does instead of how it does it.</b></i>

There are two ways to achieve abstraction in java
1. Abstract class (0 to 100% abstraction)
2. Interface (100% abstraction)


**2. Encapsulation:**


Encapsulation is the way of binding the data (variables) and code acting on the data (methods) together as a single unit.  

For example, in a company, they are different sections like the accounts section, finance section, sales section etc. Consider a situation, a person from finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. 

In encapsulation, the variables of a class will be hidden from other classes and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

**3. Inheritance:**
Inheritance in OOP is a concept that acquires the properties from one class to other classes: for example, the relationship between father and son. Inheritance in Java is a process of acquiring all the behaviors of a parent object.

The parent-child relationship, also known as the **IS-A** relationship, is represented by inheritance.

**4. Polymorphism:**

- The word poly means many and morphs means forms, so polymorphism means many forms.
- It's an ability of an object to exhibit more than one form

For example: A man at the same time is a father, a husband, an employee. So, the same person possesses different behavior in different situations. This is called polymorphism. 
  
</blockquote>

</details>

---

9. What's the difference between a hashSet and hashMap

<details> <summary>Show Answer</summary>
 
<blockquote>

### HashSet vs HashMap

| HashSet          | HashMap                                                |
| ---------------- | ------------------------------------------------------ |
| Data type        | Collection of unique objects                           | Collection of key-value pairs |
| Storage          | Hash table                                             | Hash table |
| Duplicates       | Not allowed                                            | Duplicate keys and values are allowed |
| Retrieval        | Only elements                                          | Value associated with a key |
| Null values/keys | Does not allow null elements                           | Allows null values and keys |
| Performance      | Constant time for add, remove, and contains operations | Constant time for put, get, and remove operations |
| Order            | Elements are not stored in any particular order        | No order is |
  
</blockquote>

</details>

---
