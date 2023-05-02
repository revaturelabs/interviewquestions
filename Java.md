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

An interface defines the set of methods that a class must implement. It serves as a blueprint for a class. Interfaces are utilized to achieve abstraction in the application as they only contain the method signature, not the method definition. Additionally, interfaces allow multiple inheritance in Java. By using an interface, we can define the method separately from the signature, resulting in independent methods and classes that achieve Loose Coupling. Overall, interfaces are essential for abstraction, multiple inheritance, and loose coupling in Java applications.

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

In Java, Vector and ArrayList are both classes used for storing and manipulating collections of objects, but they follwing differences:
- Synchronization: Vector is synchronized, meaning that it is thread-safe and can be accessed by multiple threads simultaneously. but ArrayList is not synchronized.
- Performance: Vector is generally slower than ArrayList.
- Capacity: Vector doubles its size when it needs to expand, while ArrayList increases its size by half of its current size.
- Enumeration: Vector has an enumeration interface that allows it to be used with older Java classes whereas ArrayList does not have an Enumeration interface.

</blockquote>
  
</details>

---
12. Have you used any design patterns? What are they?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A software design pattern is a reusable solution to a commonly occurring problem in software design. TI is not specific to any particular programming language or software system. Rather, it is a general concept or approach to solving a problem. There are multiple design patterns like Singleton pattern, Factory pattern, Adapter pattern, Observer pattern etc.


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

To copy an array values form one array to another you can use a for loop which will iterate over the first array and will put the elements of first array into another array. orelse you can use `Arrays.copyOf()` methods.

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

Serialization is the process of converting an object into a stream of bytes so that it can be stored in a file or sent over a network. In Java serialization is achieved by implementing the `Serializable` interface, which is a marker interface with no methods. To convert back the serialized bytes back to the object java use a process called `Deserialization`. We can not serialize all the objects. The objects that contain non-serializable fields or methods such as open file handles or network connections, cannot be serialized. 

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

The StringBuffer is thread-safe while the StringBuilder is not thread-safe. So, we can use StringBuffer in multi-threaded environment. The performance of the StringBuffer is low as compared to StringBuffer. The StringBuffer was introduced in Java 1.0, while StringBuilder was introduced in Java 1.5.

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

Java provides a wide range of built-in data structures that are used to store, and organize data efficiently. It is wide range of data structures, like `Array`, `ArrayList`, `LinkedList`, `HashSet`, `TreeSet`, `HashMap`, `TreeMap` etc.

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

67. how to write to a file.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To write inside a file java uses a `File` class which is present inside the `java.io` package. This class is ued to handle file related operations in java. Like creating or deleting files and directories. To write to a file, you first create a `File` object representing the file you want to write to, and then create a `FileWriter` object and pass the object of `File` to it. Once you have the `FileWriter` object, you can use its `write()` method to write text to the file.

For example,

```java
import java.io.*;
import java.util.*;

public class test {
 
    public static void main(String[] args) 
    {
       
        File file = new File("C:/file.txt");
        FileWriter writer;
        try {
            writer = new FileWriter(file);
            writer.write("Hello, World!");
            writer.close();
        } 
        catch (Exception e) {
    
            e.printStackTrace();
        }

    }
}

```

</blockquote>

</details>

---


68. what is mvc.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

MVC stands for Model-View-Controller, which is a software design pattern. 

- The Model represents the data and business logic of the application. It is responsible for managing data and performing calculations on it.
- The View represents the user interface of the application. It is responsible for displaying data to the user and receiving input from them.
- The Controller acts as an intermediary between the Model and the View. It processes user input and updates the Model and View accordingly.

By separating the application into these components, makes it easier to maintain and modify the application.

</blockquote>

</details>

---


69. Tell me some String methods;

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `String` class provides many methods for manipulating strings. The `String` class includes methods like `length()`, `charAt()`, `substring()`, `trim()`, `toLowerCase()`, `toUpperCase()` etc. 

</blockquote>

</details>

---


70. what is typecasting.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Typecasting is the process of converting a value of one data type to another data type. There are two types of typecasting implicit and explicit. In Implicit typecasting a smaller data type is converted to a larger data type. For example, converting an int to a long or a float to a double. The implicit typecasting happens automatically.In Explicit typecasting, also known as narrowing conversion, a larger data type is converted to a smaller data type. It requires the programmer to specify the type to which the value is going to be cased. For example, converting a double to an int.

</blockquote>

</details>

---


71. what is interpreter.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An interpreter is a computer program that translates and executes code written in a high-level programming language. The program gets executed line by line as the interpreter reads it. Unlike a compiler, which translates the entire program into machine code before execution, an interpreter works in real-time. Interpreters are often used in scripting languages like Python, JavaScript, and Ruby.

</blockquote>

</details>

---


72. why string are immutable.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, strings are immutable, which means that once a string object is created we cannot modified it. The immutability of strings provides benefits such as thread safety and increased security since they can be safely shared across threads and are not susceptible to modification by malicious code. Additionally, immutable strings can be more efficient than mutable strings when performing operations such as comparison or concatenation. The use of immutable strings also allows Java to cache frequently used string objects for better performance and reduced memory usage.


</blockquote>

</details>

---


73. static method in Java.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A static method is a method which belongs to a class and can be called directly using the class without creating an object of that class. To define a method as a static method, `static` keyword is used in the method signature. Static methods are often used for utility functions, factory methods, or defining constants associated with a class. The static methods cannot access non-static members of a class and cannot be overridden by subclasses.

</blockquote>

</details>

---


74. Can you provide an example of calling an overridden method?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Here is the example to call an overridden method in java.

```java

class Animal {
    public void makeSound() {
        System.out.println("The animal makes a sound");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow");
    }
}

public class Main {
    public static void main(String[] args) {
       
        Animal obj= new Cat();       
        obj.makeSound();     
    }
}
```

In this example, we define an Animal class with a makeSound method, and a Cat class that extends Animal and overrides the makeSound method. In the main method, we create a Cat object that is referred to as an Animal. When we call obj.makeSound(), the overridden makeSound method in the Cat class is called, and it prints "Meow" to the console. This demonstrates how calling an overridden method in Java works.


</blockquote>

</details>

---


75. Can you provide an example of calling a parent class's method?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Here is the example to call an parent class method from child class in java.

```java
 class Animal {
    public void makeSound() {
       System.out.println("The animal makes a sound");
    }

}
 

public class Test extends Animal {


    public static void main(String[] args) {
       Test test = new Test();
       test.makeSound(); 
    }
}


```


</blockquote>

</details>

---


76. How do you write an XML file?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To write an XML file:

- Decide on the structure of your XML file.
- Open a text editor or an XML editor.
- Start with the XML declaration at the beginning of the file: <?xml version="1.0" encoding="UTF-8"?>, which identifies the file as an XML file.
- Create the root element of the XML file with a start and end tag.
- Inside the root element, create other elements and add attributes and values to them.
- Save the file with an `.xml` file extension.
- Validate the XML file using an XML validator.

</blockquote>

</details>

---


77. What's the difference between a Set and a Map and why would you utilize one over the other.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between a `Set` and `Map` is that a `Set` is an unordered collection of unique elements. It is used to store a collection of objects where duplicates are not allowed. Whereas `Map` is an object that stores elements in key-value pairs where the keys are unique. We would use a `Set` when we need to store a collection of unique elements without any specific order. For example, If we want to store unique emails of employees, we can use a `Set` to ensure that there are no duplicates. On the other hand, we would use a `Map` when we need to retrieve values based on their associated keys. For example, when we need to store a collection of student records, where each record is associated with a unique student ID.

</blockquote>

</details>

---


78. What is the Collection framework in Java


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Collection framework in Java is a set of interfaces and classes that provides a way to handle groups of objects. It consists core interfaces like `Collection`, `List`, `Set`, `Map`,and `Queue` and  implementation class of those interfaces like `ArrayList`, `HashSet`, and `TreeMap`. It have advantages such as improved code readability, increased reusability of code, and enhanced performance.

</blockquote>

</details>

---


79. What is the differences between Strings, StringBuilder and StringBuffer, and which one between StringBuilder and StringBuffer is thread-safe.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Strings, StringBuilder, and StringBuffer are classes in Java used to manipulate character sequences and the main differences between them are Strings are immutable, while StringBuilder and StringBuffer are mutable. StringBuffer and StringBuilder both provide the same functionality to the use with differences like StringBuffer is thread-safe, while StringBuilder is not thread-safe. The performance of StringBuilder is high as compared to StringBuffer. Strings create a new object in memory every time they are modified, while StringBuilder and StringBuffer use a single buffer.

</blockquote>

</details>

---


80. can we override static methods. 


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, static methods cannot be overridden in Java. When a subclass defines a static method with the same signature as a static method in the superclass, the method in the subclass is not considered as an override of the method and the method in superclass gets executed whenever we call the method.

</blockquote>

</details>

---


81. Boxing and Unboxing


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Boxing is the process of converting a primitive data type into its corresponding object wrapper class. For example, converting an int variable into Integer. Whereas Unboxing is the process of converting an object of a wrapper class to its corresponding primitive data type. For example, converting an Integer object to an int. Unboxing is necessary when you want to use an object as a primitive data type.

- Boxing example,

```java
int i = 15;
Integer integer = Integer.valueOf(i);

```

- Unboxing example, 

```java

Integer integer = 10;
int i = integer.intValue();

```

</blockquote>

</details>

---


82. Explain and create a lamda.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A lambda expression is a type of anonymous function in Java that can be used to implement functional programming concepts.

Example for lambda expression,

```java

interface Calculator {
  int calculate(int x, int y);
}

Calculator addition = (int x, int y) -> x + y;

int result = addition.calculate(10, 20);
System.out.println(result); // Output: 30

```
In the above code, we first define a functional interface called Calculator that has one method called calculate(). Then we create a lambda expression called addition that implements the calculate() method by adding two numbers together.

</blockquote>

</details>

---


83. Create a linked list.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a linked list you can use `LinkedList` class from the `Collection` interface in Java, which will create a doubly-linked list data structure. 

For an example:

```java
import java.util.*;

public class LinkedListExample {
    public static void main(String[] args) {
        LinkedList<String> list = new LinkedList<>();

        list.add("Apple");
        list.add("Mango");
        list.add("Banana");

        System.out.println("LinkedList elements: " + list);

    }
}

```

In this example, we create a `LinkedList` object called list and add several elements to it using the `add()` method. We then print the elements of the list using the `println()` method.

</blockquote>

</details>

---


84. What are the OOPS.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

OOPs stands for `Object-Oriented Programming`. It is a methodology to design a program to simplify the application development process. There are four main pillers of OOPs including `Encapsulation`, `Inheritance`, `Polymorphism`, and `Abstraction`.  

</blockquote>

</details>

---


85. What is runtime polymorphism? 


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Runtime polymorphism allows a subclass to provide its own implementation of a method that is already defined by its parent class. In Java, this is achieved through method overriding. In method overriding, a method is cretated in subclass with the same name, return type, and parameters as a method in its parent class. At runtime, when the method is called on an object of the subclass the overridden method in the subclass is executed instead of the method in the parent class.

For example,

```java

class Animal {
    public void makeSound() {
        System.out.println("Animal makes sound");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow");
    }
}

public class Test {
    public static void main(String[] args) {
        Animal animal = new Cat();
        animal.makeSound(); // Output: Meow
    }
}


```

This is the example for runtime polymorphism. When we run the above code the overridden `makeSound()` methods gets executed. and we will receive an output as "Meow".

</blockquote>

</details>

---


86. What is upcasting in runtime polymorphism?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Upcasting is a process of casting a reference variable of a subclass to a reference variable of its parent class. This limits the access of the variable to the methods and properties of the parent class only.

For example,

```java

class Animal {
    public void makeSound() {
        System.out.println("Makes sound");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow");
    }

    public void eat() {
        System.out.println("Eating...");
    }
}

public class Test extends Animal {
    public static void main(String[] args) {
        Animal animal = new Dog(); 
        animal.makeSound(); // Output: Meow

        //animal.eat(); // compile time error.
    }
}

```
In this example, we have a parent class Animal and a subclass Cat. We create an object of the Cat class and assign it to a variable of type Animal. This is an example of upcasting. In this example when we run the code It will give an output as "Meow" when the `makeSound()` method is called. But we can not call the `eat()` method using the object because the Animal class does not have any method like `eat()` and if we try to call it this will give us an compile time error.

</blockquote>

</details>

---


87. What is method overloading?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The method overloading allows a class to have multiple methods with the same name but different parameters. This means that two methods with the same name and different parameter types can coexist in the same class, as Java can differentiate between them based on their parameter types. The method overloading helps programmers to write more concise and flexible code.

For example,

```java

class MyClass {
    public int sum(int a, int b) {
        return a + b;
    }
    
    public double sum(double a, double b) {
        return a + b;
    }
}


public class Test{
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        System.out.println(obj.sum(1,2));        // output: 3
        System.out.println(obj.sum( 2.4,3.1));   // output: 5.5
        
    }
}


```
In this example, the MyClass class has two methods named as `sum()`, one that takes two integers as arguments and returns an integer, and another that takes two doubles as arguments and returns a double. When we execute this programme we will get output as 3 and 5.5 as in first scenario when will call the `sum()` method it executed the `sum()` method with parameter type as integer, and in the second `sum()` method call it executed the `sum()` method with parameter type double.

</blockquote>

</details>

---


88. What is garbage collection?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Garbage collection is used in Java to perform automatic memory management. It deletes the objects in memory that are no longer being used by the program, and freeup the space in memory. When an object is created, Java keeps track of its reference count. When an object is no longer referenced by the program, its reference count is reduced to zero, and it becomes eligible for garbage collection. The garbage collector periodically scan the heap for objects that have a reference count of zero and delete them. It helps prevent memory leaks and makes programming in Java more convenient and safe.

</blockquote>

</details>

---


89. What can you tell me about the final keyword?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `final` keyword is used to indicate that a variable, method, or class cannot be modified or extended once it has been initialized. When we apply `final` keyword to a  variable we can not change the value of assigned to that variable. When the `final` keyword is applied to method then that method can not be overridden. and when we apply `final` keyword to a class we can not extend the class which means that the class will not have any child class.



</blockquote>

</details>

---


90. What is the benefit of inheritance?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Inheritance is a core concept in object-oriented programming that allows classes to derive methods and variables from a parent class. It simplifies code structure, promotes code reusability, and saves time and efforts  as developers can leverage the existing functionality of a base class to create new classes with specific requirements.

</blockquote>

</details>

---

91. What is the HTTP Source Code?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

HTTP stands for Hypertext Transfer Protocol. It is the underlying protocol used by the World Wide Web for communication between servers and clients. HTTP source code refers to the set of rules and standards that define how HTTP messages are formatted, transmitted, and processed in between client and server. The developers need to understand HTTP source code to optimize their web pages, improve performance, and debug issues related to HTTP communication.

</blockquote>

</details>

---

92. Can you tell me about JDK?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JDK stands for Java Development Kit.it is a software development kit used by developers to create Java-based applications. It includes JVM, the Java Runtime Environment, and other tools and utilities needed to develop, debug, and run Java code.

</blockquote>

</details>

---


93. What is the JIT Compiler?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The JIT stands for Just-In-Time compiler is a component of the Java Virtual Machine (JVM) that compiles Java bytecode into machine code at runtime. It analyzes the bytecode as the program runs, identifies frequently executed sections of the code, then compiles these sections into machine code and stores the compiled code in a cache so that it can be executed more quickly in the future.This allows Java programs to achieve better performance.

</blockquote>

</details>

---


94. What does JVM do?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JVM stands for Java Virtual Machine, and its main function is to execute Java bytecode. It provides a runtime environment in which Java applications can run on any platform, without the need for the developer to worry about the specific details of the underlying operating system. It manages memory, thread synchronization, security, and other runtime aspects of the Java application. It also includes components like the JIT compiler and class loader to optimize the performance of Java applications.

</blockquote>

</details>

---

95. What are Wrapper Classes?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Wrapper classes are the classes that allow primitive data types to be treated as objects. There is a wrapper class for each primitive data type, and they provide utility methods for converting between primitive data types and objects, as well as for performing various other operations on the data. Wrapper classes are useful in situations where an object is required, but only a primitive data type is available. Some examples of wrapper classes are `Boolean`, `Byte`,`Character`, `Short`, `Integer`,`Long`, `Float`, and `Double`.

</blockquote>

</details>

---

96. what is abstraction.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Abstraction in Java is the process of hiding the implementation details of a system or software component and focusing on the essential features. To implement abstractin in our applicatio we use abstract classes and interfaces. By using abstraction, we can create code that is more modular, maintainable, and extensible. It allows us to focus on the high-level design of a system, without getting bogged down in the details of implementation.

</blockquote>

</details>

---

97. How many memories are there in Java and what are they used for?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, there are mainly two types of memory: heap memory and stack memory. The heap memory is used for storing objects created during the runtime of a program, while stack memory is used for storing method calls and local variables. In addition to these, there are also other memory areas in Java, such as the Method Area, Runtime Constant Pool, and Native Method Stacks. Understanding the different types of memory in Java is important for writing efficient and scalable programs. 

</blockquote>

</details>

---

98. What kind of loop would you use for going from 1 to 10?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

We can use a for , while or do while loop to fulfill the requirement.

In the below example, We will write a code which will print numbers from 1 to 10 using for loop.

```java
import java.util.*;

public class Test{
    public static void main(String[] args) {
        
        for(int i=1;i<=10;i++){
            System.out.println(i);
        }
        
    }
}

```


</blockquote>

</details>

---

99. How do you declare a variable in java.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To declare a variable in Java, you need to specify its data type and name. The syntax for declaring a variable is `data_type variable_name;`.

for example: 
```java
int num;

```
The above exampole declares an integer variable named num with no initial value.

If you want to assign a value, you can do so in the declaration, like this: 

```java
int num = 10;
```

</blockquote>

</details>

---

100. What is JEE design patterns.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JEE (Java Enterprise Edition) Design Patterns are standard solutions to software design problems when building enterprise-level Java applications. They help developers create reliable and scalable software systems. Examples of these patterns include MVC, Singleton, DAO, Factory, Observer, Dependency Injection, Service Locator, and Front Controller.

</blockquote>

</details>

---

101. Can you code a program that reflects overloading


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

here is an example for method overloading:

```java
import java.util.*;

class DemoOverloading{
    public void printNumber(int num) {
        System.out.println("Printing integer number: " + num);
    }

    public void printNumber(double num) {
        System.out.println("Printing floating-point number: " + num);
    }

    public void printNumber(String num) {
        System.out.println("Printing string number: " + num);
    }
}

public class Test{
    public static void main(String[] args) {
        DemoOverloading obj = new DemoOverloading();
        obj.printNumber(10);
        obj.printNumber(10.0);
        obj.printNumber("10");  
        
        
    }
}

```

</blockquote>

</details>

---

102. What is an abstract class;


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An abstract class is a class that cannot be instantiated on its own but can be extended to create subclasses. It provides a blueprint for other classes and defines common characteristics and behavior that can be shared by multiple subclasses. The abstract class contains abstract and non-abstract methods, the abstract methods must be implemented in the subclasses that extend the abstract class. The keyword `abstract` is used to define an abstract class.

</blockquote>

</details>

---