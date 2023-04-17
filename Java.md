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

