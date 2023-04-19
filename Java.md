1. Functional interface in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A functional interface is a feature introduced in Java 8 and is also called a `Single Abstract Method`. It is an interface that has only one abstract method. Functional interfaces are commonly used with lambda expressions to create more concise and readable code.

Java includes some built-in functional interfaces, such as Runnable, Consumer, and Comparable.

</blockquote>
  
</details>

---

2. What is the purpose of interfaces in Java? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An interface defined the set of methods that a class must implement. It is a blueprint for a class. They are used to achieve abstraction in the application. Also by using interface we can achieve multiple inheritance in java.

</blockquote>
  
</details>

---



3. What is a class?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A class is a blueprint for creating objects. It defines the structure of an object by specifying methods and variables that the object will contain. For example, a Car class can have attributes such as model, weight, and color, as well as methods such as start, stop, and brake. We can then use this blueprint to create objects for the Car class, with each object having its own values for the attributes. To create objects from a class, we use the `new` keyword.


</blockquote>
  
</details>

---

4. What is object?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An object is an instance of a class. It represents a real-world entity that has properties and behavior specified by the class. An object is created from a class using the `new` keyword. Each object has its own unique identity, state, and behavior. The state represents the data contained in the object, while the methods define the actions that can be performed on that state. Objects are the main building block of object-oriented programming. 

</blockquote>
  
</details>

---

5. Abstract class vs interface?  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An abstract class is a class that contains abstract methods. The abstract class can not be instantiated and have to be extended by other class to use the methods of that class. While an interface serves as a contract that specifies a set of methods that a class must implement.

The difference between an abstract class and an interface is that the abstract class can contain both abstract and non-abstract methods while an interface can have only abstract methods. Since Java 8, it can have static and default methods. An abstract class can have final, non-final, static, and non-static variables while an interface can only have static and final variables.


</blockquote>
  
</details>

---

6. Does Java allow static classes?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java allows a class to be a static only if that class in a inner class.Static classes are also known as `static nested classes`. The static inner classes can be accessed without initializing the outer class.The static class does not have access to the instance variables and methods of the outer class. 

</blockquote>
  
</details>

---

7. What are annotations and what are they good for?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Annotations in java provide metadata about the class, method, and interface. They are used to provide additional information to the compiler about a programming element like a method or class to provide additional functionality. In Java, annotations are represented using the `@` symbol followed by the annotation name.

</blockquote>
  
</details>

---

8. What is a deadlock?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A deadlock condition occurs when two or more threads are blocking the resources and waiting for each other to release the resource. Consider for example, If one thread acquires a lock on one resource and then attempts to lock another resource that is already locked by another thread that is waiting for the first thread to release the lock on the first resource. So in this condition, a deadlock occurs. To prevent deadlock conditions we can avoid nested locks.

</blockquote>
  
</details>

---

9. What are threads? What type of threads?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Threads are individual, lightweight, and the smallest unit of a given process. They are used to perform multiple tasks simultaneously, which increases the performance of a program. There are two types of threads: daemon threads and user threads. User threads are created by the Java application and are used to perform application-specific tasks. Daemon threads are low-priority threads created by the JVM that run in the background and support the user threads.

</blockquote>
  
</details>

---

10. What is an exception in Java?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An exception is an event that occurs during the execution of a program, which disrupts the normal flow of the program. When an exception occurs, the execution flow of the program is transferred from the normal flow to an exception handling mechanism which uses a `try-catch` block to handle the exception.

In Java, there are two types of exceptions: checked exceptions and unchecked exceptions. Checked exceptions are checked by the compiler at compile-time, while unchecked exceptions are not checked by the compiler. Examples of checked exceptions include `IOException`, `SQLException`, and `ClassNotFoundException`, while examples of unchecked exceptions include `NullPointerException`, `ArrayIndexOutOfBoundsException`, and `ArithmeticException`.

</blockquote>
  
</details>

---

11. The Difference Between a vector and ArrayList.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Vector is synchronized while ArrayList is not synchronized and is not thread-safe. The performance of vector is less than arraylist. Vector doubles its size when it needs to expand, whereas ArrayList increases by half of its size.

</blockquote>
  
</details>

---

12. The difference between a @bean and @component.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between `@Component` and `@Bean` is that `@Component` is a class-level annotation that allows Spring to automatically discover and register a bean, whereas `@Bean` is a method-level annotation that creates and returns an object that Spring should register as a bean. 

</blockquote>
  
</details>

---

13. Is java a pass-by-value or pass-by-reference.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In java is a pass-by-value. When a Java method is called, the values of the arguments are copied into the method's parameter variables. This means that changes made to the parameter variables within the method do not affect the original values of the arguments passed to the method. In case of an object reference, the reference itself is passed by value. This means that the value of the reference is copied into the parameter variable, but the object itself is not copied. Therefore, changes made to the object's state within the method are visible outside the method.



</blockquote>
  
</details>

---

14.  What is a stream api in Java. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Stream API is a feature introduced in Java 8. It  provids functional programming approach to processing collections of data. A Stream is a sequence of elements that can be processed in parallel or sequentially. It allows you to perform various aggregate operations, such as filtering, mapping, sorting, and reducing, on a collection of objects. The Stream API is designed to work with large data sets and can help improve the performance of your Java applications.

</blockquote>
  
</details>

---

15. Java Interfaces – How many can you implement? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An interface is a contract that specifies a set of methods that a class must implement. A class can implement multiple interfaces, But it should provide an implementation for all the methods defined in each of the interfaces.

</blockquote>
  
</details>

---

16. Java Classes – How many can you extend? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, a class can only extend one parent class. The `extends` keyword is used in Java to indicate that a class is inheriting another class. When a class extends another class, it inherits all the properties and methods of the inherited class.

</blockquote>
  
</details>

---

17. What is a copy constructor?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, a copy constructor is a constructor that creates a new object by copying the state of an existing object. It takes an object of the same class as its parameter and initializes the new object's state with the state of the original object.

</blockquote>
  
</details>

---

18. How do you copy an array?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To copy an array values form one array to another you can use a for loop which will iterate over the first array and will put the elements of first array into another array. orelse you can use `Arrays.copyOf` methods.

</blockquote>
  
</details>

---

19. Arrays vs ArrayList.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Array is a fixes size data structure while size of arraylist is dynamic. We have to specify the size of array at the time of creation while there is no need of specifying size of an arraylist. array can store primitive data types, while an ArrayList can only store objects. Arrays are faster as compared to arraylist.

</blockquote>
  
</details>

---

20. What is a Linked List?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A linked list is a data structure that consists of a sequence of nodes, where each node stores an element of data and a reference to the next node. The difference between linkedlist and arraylist is that the elements of arraylist are stored in continuous block of memory. While the elements of linkedlist are distributed in the memory.


</blockquote>
  
</details>

---

21. Linked List vs ArrayList?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are following differences between an arraylist and linkedlist.

- The elements of arraylist are stored in continuous block of memory while the elements of linkedlist are stored in distributed manner in memory.
- It is efficient to access an element in arraylist as compared to linkedlist as the arraylist uses an index-based lookup while in linkedlist we have to traverse through all the elements to get the desired element.
- The addition or removal of element in an linkedlist is efficient as compared to arraylist.
- The linked list is used when the user is going to frequently add or remove elements from the list. whereas the arraylist is prefered when the user wants to frequently access the elements.

</blockquote>
  
</details>

---

22. Do you know any thread safe collections?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java provides several thread-safe collections that can be used in multi-threaded applications where multiple threads can access the same collection concurrently. Stack, Vector, Hashtable these are some of the examples of thread safe collections.

</blockquote>
  
</details>

---

23. Do you know about any concurrent collections?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ConcurrentHashMap, CopyOnWriteArrayList, ConcurrentLinkedQueue, BlockingQueue, and ConcurrentSkipListMap these are some of the examples of concurrent collections.

</blockquote>
  
</details>

--- 

24. How do you make an arraylist synchronized?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To make an arraylist synchronized in java, we can use `Collections.synchronizedList()`
method to create a synchronized version of the arraylist. This method returns a thread-safe version of the original arraylist.

</blockquote>
  
</details>

---

25. What is a set?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `Set` in java is an unordered collection which do no allow duplicate values to be stored in it. We can implement the `Set` interface using `HashSet`, `LinkedHashSet`, `TreeSet`. The `LinkedHashSet` maintains the order of elements in which they were inserted and in `TreeSet` the elements are stored in sorted manner. To perform operations on set we can use methods like `add()`, `remove()`, `contains()`,and  `size()` 

</blockquote>
  
</details>

---

26. How are elements in TreeSets arranged?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The elements in a `TreeSet` are arranged in ascending order. The `TreeSet` internally implements a self-balancing binary search tree. So whenever an element is added into a tree set. It is inserted at the appropriate position in self-balancing binary search tree to maintain the sorted order.

</blockquote>
  
</details>

---

27. What is a Queue in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `Queue` is a collection interface that is used to store the elements in a particular order. The queue follows the first in first out principle. which means that the first element added to the queue is the first element to be get removed from the queue. In `Queue`, the elements are added from the tails and removed from the head.  

To perform operations on queue we can use methods like `offer()`, `poll()`, `peek()`, and `size()`. The queue can be implemented using `LinkedList`,  `ArrayDeque`, and `PriorityQueue`.

</blockquote>
  
</details>

---

28. What is a Stack?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`Stack` is a linear data structure that follows the last in first out principle. The last in first out principle states that the last element added to the stack is the first element to be removed. To perform operations on queue we can use methods like `push()`, `pop()`, `peek()`, and `empty()`. 

The `push()` method adds the element at the top of the stack. The `pop()` method removes and returns the top element from the stack. The `peek()` method will return the first element in the stack without removing it. The `empty()` method is used to check whether the stack is empty or not.

</blockquote>
  
</details>

---

29. Queue vs Stack?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The difference between queue and stack is that the queue follows the first in first out principal while the stack follows the last in first out principal. 

The new element which will get added to the Queue will be added at the end/tail of the stack. The new element which we add to the stack gets added at the top of the stack. 

Stacks are commonly used in programming for keeping track of function calls. while the queue is commonly used to manage tasks in a system, such as processing jobs.   

Stacks are used in algorithms such as Depth First Search (DFS). whereas the queue is used in the Breadth First Search algorithm.

</blockquote>
  
</details>

---
30. How to handle exceptions?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To handle an exception, java provides an exception handling mechanism called the `try-catch` block. The part of code which may throw an exception that code is written `try` block. In the `catch` block we write the code which will get executed when any exception occurs in the try block. we can have multiple `catch` blocks to handle different types of exceptions. with try and catch block java also provides a `finally` block which will get executed whether an exception occurs or not. The use of the `finally` block is optional. 

</blockquote>
  
</details>

---

31. Use of finally?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The finally block is used with the `try-catch` block for exception handling in Java. The finally block gets executed regardless of whether an exception occurs or not. It is mainly used to release resources such as network connections, and database connections.


</blockquote>

</details>

---

32. How do you do multi-threading?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Multithreading in java allows a program to perform multiple tasks concurrently, which can improve the performance of the application. Threads in Java can be created by using two ways. The first way to create a thread in Java is by implementing the `Runnable` interface and the second way is by extending the `Thread` class. 

</blockquote>

</details>

---

33. Volatile keywords?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `volatile` keyword in Java is used to indicate that a variable's value may be modified by multiple threads at the same time. Without the `volatile` keyword, different threads may create their own copy of that variable which will contain a different value for a different thread. This can lead to incorrect results. The `volatile` keyword helps to prevent this by forcing threads to always read the variable's value from main memory, rather than from a cached copy.

</blockquote>

</details>

---

34. Serialization in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Serialization in Java is the process of converting an object into a stream of bytes so that it can be stored in a file or sent over a network. In Java serialization is achieved by implementing the `Serializable` interface, which is a marker interface with no methods. To convert back the serialized bytes back to the object java use a process called `Deserialization`. We can not serialize all the objects. The objects that contain non-serializable fields or methods such as open file handles or network connections, cannot be serialized. 

</blockquote>

</details>

---

35. What are hashes in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, hashes usually refer to the hash codes generated by the `hashCode()` method in object. The `hashCode()` method returns an integer value that is often used as an index in hash tables or for other purposes that require a unique identifier for an object. 

</blockquote>

</details>

---

36. Explain what a comparator is;

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `Comparator` is a Java interface used to define custom sorting for objects in a collection. It provides a way to compare two objects based on specific properties and is used to sort collections. The interface contains a single method called `compare()` which compares two objects and returns an integer value indicating the order of the objects which is used to sort the objects. It returns a positive value if the second object should come before the first object and a negative value if the first object should come before the second object. It returns zero if both values are equal.


</blockquote>

</details>

---

37. ==  vs .equals() in java.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, the `==` operator compares objects based on their memory addresses, while the `.equals()` method compares objects based on their values. `==` returns true if the two objects are the same instance, while `.equals()` returns true if the two objects have the same values. It's recommended to use `.equals()` for comparing objects.

</blockquote>

</details>

---

38. SOLID principles.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

SOLID is a set of principles that helps in writing maintainable and extensible software. The five SOLID principles are Single Responsibility Principle, Open/Closed Principle, Liskov Substitution Principle, Interface Segregation Principle, Dependency Inversion Principle. 

</blockquote>

</details>

---

39. What are the new features of Java 8?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java 8 provides following new features:

- **Lambda expressions** : A new syntax for writing anonymous functions that simplifies the development of functional programming code.

- **Stream API**: The Stream API is used to process collections of data in a functional way, making it easier to work with large data sets.

- **Default methods**: Interfaces can now have default methods, which are implemented in the interface and inherited by implementing classes.

- **Date and Time API**: A new API that provides a more comprehensive and flexible way of handling dates and times.

- **Optional class**: A new class that provides a way to handle null values without the risk of NullPointerException.

- **Functional Interfaces**: Functional interfaces are interfaces that have exactly one abstract method.

- **Method References**: Method references is used to refer a method without invoking it. 

</blockquote>

</details>

---

40. What is the difference between an Arraylist and a HashSet?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The ArrayList is an ordered collection of elements where as the HashSet is unordered. In Arraylist we can add duplicate numbers but we can not add duplicate elements in HashSet. ArrayList provides fast access by index, whereas HashSet provides constant-time performance for basic operations. 

</blockquote>

</details>

---

41. What does the term asynchronous mean in Java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, asynchronous refers to a programming model where tasks are executed concurrently and independently from the main program flow. This means that instead of waiting for a task to get completed before moving on to the next one, the program can continue executing other tasks and receive a notification when the original task is finished. This approach is used to increase the efficiency of the application.

</blockquote>

</details>

---

42. How do you do unit test.
 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Unit testing is done on an individual part of a code, like a method. In unit testing, we write a code that will check if a particular method on which we are performing unit testing gives an expected output or not for different test cases. If the output matches the expected output then the test is passed otherwise it fails.

</blockquote>

</details>

---

43. What are generics?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Generics in Java allow you to create classes, interfaces, and methods that can work with different types of objects. You can define a generic type with a type parameter, like T, which represents a placeholder for a specific type that will be determined later. You can use this type parameter to create classes, methods, or interfaces that can be used with any data type, making your code more flexible, reusable, and type-safe.

</blockquote>

</details>

---

44. What does static mean in Java?
 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `static` keyword is used to define variables or methods that belong to a class rather than to any object of that class. This allows the user to accesss these vairables and methods directly using the class name without creating an object of that class.  

</blockquote>

</details>

---

45. What is JAVA

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java is a platform-independent object-oriented programming language. It can run on any computer or operating system that has a special program called a Java Virtual Machine (JVM) installed. It's used to build a wide range of software applications, including web and mobile apps, and is known for its ease of use, security features, and large developer community.

</blockquote>

</details>

---

46. difference between String and StringBuilder;


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The String is an immutable class in Java. where the StringBuilder is mutable. The performance of StringBuilder is faster than the String in operations like concatenation or modification. The String is a thread-safe class but the StringBuilder is not thread-safe.

</blockquote>

</details>

---

47. convert a string into a integer;

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To convert a string into an integer in Java, you can use the `parseInt()` method of the `Integer` class. Just pass the string as an argument to `parseInt()` method, and it will return an integer.

</blockquote>

</details>

---

48. explain how to start a thread.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To start a thread in java there are two ways. first one is to implment the `Runnable` interface and Then, create a new Thread object and pass an object of your class which is implementing the `Runnable` interface to the constructor, and call the `start()` method to start the thread.

The second way is to extends the `Thread` class. Then create an object of your class which is exting the `Thread` class and call the `start()` method.

</blockquote>

</details>

---

49. What is the difference between StringBuilder and StringBuffer?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The StringBuffer is thread-safe while the StringBuilder is not thread-safe. So, we can use StringBuffer in multi-threaded environment. The performance of the StringBuffer is low as compared to StringBuffer.

</blockquote>

</details>

---

50. What is an Optional in Java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Optional class in Java is used to handle the null values. It helps to avoid the null pointer exceptions in the case where a value may be missing. The Optional class has two possible states, "non-empty" if a value is present and "empty" if a value is not present. Optional allows us to write code that clearly expresses whether a value is optional or required, which makes the code easier to read and maintain.

</blockquote>

</details>

---

51. What is the benefit of Java 11.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java 11 has multiple benefits it improves the performance of the Java application as it introduced the Z garbage collector and removed some deprecated APIs. Java 11 has enhanced the security aspect of Java. Java 11 improved developer productivity by adding new APIs for working with strings and files, and improved HTTP client API.


</blockquote>

</details>

---

52. If I had a String variable a1 as "Hector" and wanted to concatenate a second String with no variable "Infosys", what will print out?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

When we concatinate both the strings the output will be "HecotorInfosys".

</blockquote>

</details>

---

53. Binary search algorithm

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The binary search algorithm is used to find an element in the sorted array. To implement the binary search algorithm it is important that the array should be sorted manner. The algorithm works by repeatedly dividing the search interval in half until the target element is found or not present in the array. The time complexity of the binary search is O(log n). 

</blockquote>

</details>

---

54. Map interface vs collection interface


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `Map` interface and the `Collections` interface are both part of the Java Collections Framework.

The `Collection` interface is used to represent a group of objects like a list. It provides a standard set of methods for adding, removing, and modifying elements in the list. The `Collection` interface is implemented by `ArrayList`, `LinkedList`, `HashSet`, and `TreeSet`.

The `Map` interface is used to store elements in key-value pair. Each key is associated with a value, and you can use the key to retrieve the value assigned to that key. The `Map` interface is implemented by `HashMap`, `TreeMap`, and `LinkedHashMap`.


</blockquote>

</details>

---

55. why java doesn't have pointers.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java was designed to be a safe and secure programming language. So, to restricted the direct access to memory to avoid common programming errors like memory leaks and buffer overflows. Instead, Java uses references, which are similar to pointers but with built-in safety features to ensure that objects are created, used, and destroyed safely and efficiently. This approach eliminates the possibility of accidentally modifying the wrong memory address, which can cause serious errors and security vulnerabilities.

</blockquote>

</details>

---

56.  Create functional interfaces and use a lambda expression to add two integers.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```java
interface IntegerMath {
    int operation(int a, int b);
}

public class Example {
    public static void main(String[] args) {
        
        IntegerMath addition = (a, b) -> a + b;
        
        int result = addition.operation(4, 5);
        System.out.println("The resultis " + result);
    }
}

```

</blockquote>

</details>

---



57. Did you ever run out of memory in Java? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java programs can run out of memory if they exceed the memory allocated to them by the Java Virtual Machine (JVM). Java throws `OutOfMemoryError` in this scenario. This can occur due to inefficient memory usage or memory leaks within the program. It is important to properly manage memory in Java programs to avoid such issues.

</blockquote>

</details>

---

58. Can you have a try block without a catch block.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, we cannot have a try block without a catch block in Java. A try block must be followed by at least one catch block or a finally block. If there is no catch block or finally block after a try block, the Java compiler will give a compile-time error.

</blockquote>

</details>

---


59. What IDE do you use for Java.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To execute Java programme we can use IDE like Eclipse, IntelliJ IDEA, NetBeans, Visual Studio Code with Java extensions, JDeveloper etc.

</blockquote>

</details>

---


60. What was added to the collections framework in java 8.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java 8 added several new features to the Collections framework, including Lambda expressions, the Streams API, default methods in interfaces, Optional class, enhancements to Map and Comparator interfaces, and more. These features make it easier to write expressive and efficient code for working with collections in Java.


</blockquote>

</details>

---


61. Throw vs Throws

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, the `throw` keyword is used to explicitly throw an exception from a method or block of code, while `throws` is used in the method signature to declare that the method may throw one or more types of exceptions. If a method can throw multiple exceptions, we can declare those exceptions in the method signature by separating them with commas.

</blockquote>

</details>

---


62. Explain the difference between a heap and a stack?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The heap and the stack are two separate areas of memory that are used for different purposes.

- Memory allocation: The heap is used for dynamic memory allocation, while the stack is used for automatic memory allocation.
- Data type: The heap is used for storing objects, while the stack is used for storing primitive types and method frames.
- Access: The heap is a shared resource that can be accessed by all threads in a program, while the stack is a per-thread resource that can only be accessed by the thread that owns it.
- Lifetime: Objects on the heap remain in memory until the garbage collector frees it or the program terminates, while data on the stack is freed when the method returns.

</blockquote>

</details>

---


63. What is the parent class of all classes in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `Object` class is the parent class of all classes in Java. Every class in Java implicitly or explicitly extends the `Object` class. The `Object` class provides some default methods to it's subclasses, such as `toString()`, `equals()`, and `hashCode()`.

</blockquote>

</details>

---

64. Inheritance in Java and how is it implemented?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, inheritance is a way for a class to inherit properties and behavior from another class called the superclass. Inheritance is implemented by using the `extends` keyword. When a class extends another class, it inherits all the properties and behaviors of that class, and can override or extend them as needed. 
For example, if we have an Animal class with an `eat()` method, and a Dog class that extends Animal, the Dog class automatically inherits the `eat()` method from Animal. 

```Java
public class Animal {
    public void eat() {
        System.out.println("This animal is eating.");
    }
}

public class Dog extends Animal {
    public void bark() {
        System.out.println("Woof!");
    }
}

```

Inheritance makes it easier to reuse code and create specialized classes.

</blockquote>

</details>

---


65. What data structures are used in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java there is wide range of data structures, like `Array`, `ArrayList`, `LinkedList`, `HashSet`, `TreeSet`, `HashMap`, `TreeMap` etc.

</blockquote>

</details>

---


66. Where primitive and an object get stored. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The primitive data types are stored in the memory stack. `int`, `double`, `boolean`, and `char` are the examples of primitive data type. whereas the Objects are stored in the heap memory.

</blockquote>

</details>

---

