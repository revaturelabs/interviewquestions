1. Why use Dependency injection?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dependency injection (DI) is a technique used in software engineering to make development of software applications easier. The DI uses loose coupling between different components, making it easier to modify individual parts without affecting the rest of the application.

Consider you are writing a code for an application where the various objects depend on each other. So, instead of having each object create and manage its own dependencies, you can use DI to create an object of those dependencies and pass them to each object whenever needed.

Since the dependencies are managed by DI, users can modify them without needing to change the code in every object that uses them. 

</blockquote>
  
</details>

---

2. Difference between RestController and Controller?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between `@RestController` and `@Controller` is that the `@RestController` annotation is used for building RESTful web services that return data in JSON, XML or any other format, whereas the `@Controller` annotation is used when we are building a web application that returns an HTML view.

</blockquote>
  
</details>

---

3. Functional interface in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A functional interface is a feature introduced in Java 8 and is also called a `Single Abstract Method`. It is an interface that has only one abstract method. Functional interfaces are commonly used with lambda expressions to create more concise and readable code.

Java includes some built-in functional interfaces, such as Runnable, Consumer, and Comparable.

</blockquote>
  
</details>

---

4. What is the purpose of interfaces in Java? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An interface defined the set of methods that a class must implement. It is a blueprint for a class. They are used to achieve abstraction in the application. Also by using interface we can achieve multiple inheritance in java.

</blockquote>
  
</details>

---

5. What is a singleton, and why do you use it?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Singleton is a type of bean object scope in which only one instance of the bean is created, and this same instance is shared globally for each request made for that bean. The singleton bean scope is used for stateless beans that do not maintain any internal state, such as utility classes or service classes. The singleton scope offers benefits like improved performance, consistency, and simplicity in configuration.

</blockquote>
  
</details>

---

6. What is a class?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A class is a blueprint for creating objects. It defines the structure of an object by specifying methods and variables that the object will contain. For example, a Car class can have attributes such as model, weight, and color, as well as methods such as start, stop, and brake. We can then use this blueprint to create objects for the Car class, with each object having its own values for the attributes. To create objects from a class, we use the `new` keyword.


</blockquote>
  
</details>

---

7. What is object?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An object is an instance of a class. It represents a real-world entity that has properties and behavior specified by the class. An object is created from a class using the `new` keyword. Each object has its own unique identity, state, and behavior. The state represents the data contained in the object, while the methods define the actions that can be performed on that state. Objects are the main building block of object-oriented programming. 

</blockquote>
  
</details>

---

8. How do you connect a spring application with a database?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To connect a database to our spring boot application first, we have to add the driver dependency for that specific database. After adding the dependency we have to configure the database properties like URL, username, and password in our `application.properties` or `application.yml` file. Post which we have to create a Database access layer to interact with our database.

</blockquote>
  
</details>

---

9. How does jpa interact with the data base?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JPA stands for Java Persistence API. It is a standard interface for Object-Relational Mapping (ORM) tools to map Java objects to relational databases. The JPA interacts with the database using an EntityManager, which is responsible for managing the lifecycle of entities. JPA also provides a query language called JPQL (Java Persistence Query Language). The JPQL queries are then translated into SQL statements that are used to perform operations on the database.


</blockquote>
  
</details>

---

10. How can I make so that a field in an entity class does not generate a column?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To achieve this functionality we can use the `@Transient` annotation. The `@Transient` annotation indicates JPA to exclude the annotated field while creating the database table.

</blockquote>
  
</details>

---

11. How do you create a controller in your spring application?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a controller in a Spring application. Create a class and annotate it with the `@Controller` annotation. This class will have methods that handle incoming HTTP requests and return a response to the client. You can also use the `@RequestMapping` annotation above the controller class to define the base UR for the class methods.

</blockquote>
  
</details>

---

12. How does Spring know if your request is post, get, or put in your controller?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Spring framework determines the type of HTTP request (POST, GET, PUT) based on the HTTP method specified in the request. Spring checks the HTTP method and URL pattern to map that request to a specific method.

For example, if we send a GET request with a specific URL, Spring will automatically map that request to a method which has the `@GetMapping` annotation with a matching URL pattern.


</blockquote>
  
</details>

---

13. How were you transferring information through the controllers to your angular application? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To transfer data from contoller to angular application we can use `HTTPClient` service which will be used to make HTTP requests to the controller. The `HTTPClient` service return an `observable` which we can subscribe to get the data sent from the controller in our angular application.


</blockquote>
  
</details>

---

14. Abstract class vs interface?  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An abstract class is a class that contains abstract methods. The abstract class can not be instantiated and have to be extended by other class to use the methods of that class. While an interface serves as a contract that specifies a set of methods that a class must implement.

The difference between an abstract class and an interface is that the abstract class can contain both abstract and non-abstract methods while an interface can have only abstract methods. Since Java 8, it can have static and default methods. An abstract class can have final, non-final, static, and non-static variables while an interface can only have static and final variables.


</blockquote>
  
</details>

---

15. Controller annotations for get mapping, post mapping?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

We use the `@GetMapping` annotation for HTTP GET requests to map that request to a specific handler method in a controller, and the `@PostMapping` annotation for HTTP POST requests in Spring.

</blockquote>
  
</details>

---

16. Does Java allow static classes?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java allows a class to be a static only if that class in a inner class. The static inner classes can be accessed without initializing the outer class.  

</blockquote>
  
</details>

---

17. What are annotations and what are they good for?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Annotations in java provide metadata about the class, method, interface. They are used to provide additional information to compiler to provide additional functionality.

</blockquote>
  
</details>

---

18. What is a deadlock?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A dedlock condition occurs when two or more threads are blocking the resources and waiting for each other to release the resource. Consider for example, If one thread acquires lock on one resource and then attempts to lock another resource which is already locked by another threading which is waiting for first thread to release the lock on first resource. So in this condition deadlock occurs. To prevent deadlock condition we can avoid nested locks.

</blockquote>
  
</details>

---

19. What are threads? What type of threads?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Threads are individual, light-weight and smallest unit of a given process. There are two types of threads daemon threads and nondeamon thread. The deamon threads are lowpriority threads which runs in backgroundand supports the nondeamon threads.

</blockquote>
  
</details>

---

20. What is an exception in Java?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An exception is an event that occurs during the execution of a program, which disrupts the normal flow of the program's instructions.Exceptions are of two types, checked exceptions and unchecked exceptions. Checked exceptions are checked by the compiler at the compile-time, while unchecked exceptions are not checked by the compiler. Java provides try-catch block to handel the exceptions.

</blockquote>
  
</details>

---

21. Can spring use a server different from the embedded tomcat server?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Spirng support the usage of different servers other than the embedded Tomcat server. Inside the project dependencies you can configure the servers which you want to utilize.

</blockquote>
  
</details>

---

22. What is Spring and why do we use it?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Spring is a popular open-source framework for building robust and scalable applications in Java. Spring provided multiple feature like dependency injection, aspect-oriented programming, transaction management, and more. 

Spring is widely used for building web applications, microservices, and enterprise applications.


</blockquote>
  
</details>

---

23. The Difference Between a vector and ArrayList.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Vector is synchronized while ArrayList is not synchronized and is not thread-safe. The performance of vector is less than arraylist. Vector doubles its size when it needs to expand, whereas ArrayList increases by half of its size.

</blockquote>
  
</details>

---

24. The difference between a @bean and @component.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between `@Component` and `@Bean` is that `@Component` is a class-level annotation that allows Spring to automatically discover and register a bean, whereas `@Bean` is a method-level annotation that creates and returns an object that Spring should register as a bean. 

</blockquote>
  
</details>

---

25. How do you inject a dependency through the constructor ?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To inject a dependency through the constructor, create a constructor in a class and pass that dependency as a parameter to the constructor. Then, apply the `@Autowired` annotation above the constructor, Spring will automatically detect the dependency and inject it into the constructor when creating an instance of the class.

</blockquote>
  
</details>

---

26. Is java a pass-by-value or pass-by-reference.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In java is a pass-by-value.

</blockquote>
  
</details>

---

27. What is a stream api in Java. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Stream API is a feature introduced in Java 8. It  provids functional programming approach to processing collections of data.

</blockquote>
  
</details>

---

28. Java Interfaces – How many can you implement? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In java we can implement multiple interfaces in the same class.

</blockquote>
  
</details>

---

29. Java Classes – How many can you extend? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In java we can extend only one class.

</blockquote>
  
</details>

---

30. What is a copy constructor?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A copy constructor is a special constructor that allows you to create a new object by copying the values of an existing object.

</blockquote>
  
</details>

---

31. How do you copy an array?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To copy an array values form one array to another you can use a for loop which will iterate over the first array and will put the elements of first array into another array. orelse you can use `Arrays.copyOf` methods.

</blockquote>
  
</details>

---

32. Arrays vs ArrayList.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Array is a fixes size data structure while size of arraylist is dynamic. We have to specify the size of array at the time of creation while there is no need of specifying size of an arraylist. array can store primitive data types, while an ArrayList can only store objects. Arrays are faster as compared to arraylist.

</blockquote>
  
</details>

---

33. What is a Linked List?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A linked list is a data structure that consists of a sequence of nodes, where each node stores an element of data and a reference to the next node. The difference between linkedlist and arraylist is that the elements of arraylist are stored in continuous block of memory. While the elements of linkedlist are distributed in the memory.


</blockquote>
  
</details>

---

34. Linked List vs ArrayList?
 
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

35. Do you know any thread safe collections?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ConcurrentHashMap, CopyOnWriteArrayList, ConcurrentLinkedQueue, BlockingQueue, and ConcurrentSkipListMap, Vector, HashTable these are some of the examples of thread safe collections.

</blockquote>
  
</details>

---

36. Do you know about any concurrent collections?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ConcurrentHashMap, CopyOnWriteArrayList, ConcurrentLinkedQueue, BlockingQueue, and ConcurrentSkipListMap these are some of the examples of thread safe collections.

</blockquote>
  
</details>

--- 

37. How do you make an arraylist synchronized?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To make an arraylist thread-safe in java, we can use `Collections.synchronizedList()`
method to create a synchronized version of the arraylist. This method returns a thread-safe version of the original arraylist.

</blockquote>
  
</details>

---

38. What is a set?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A set in java is an unordered collection which do no allow duplicate values to be stored in it. We can implement the set using HashSet, LinkedHashSet, TreeSet. In LinkedHashSet the order of elements is maintained and in treeset the elements are stored in sorted manner. To perform operations on set we can use methods like `add()`, `remove()`, `contains()`,and  `size()` 

</blockquote>
  
</details>

---

39. How are elements in TreeSets arranged?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The elements in a tree set are arranged in ascending order. The tree set internally implements a self-balancing binary search tree. So whenever an element is added into a tree set. It is inserted at the appropriate position in self-balancing binary search tree to maintain the sorting order.

</blockquote>
  
</details>

---

40. What is a Queue in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A Queue is a collection interface which is used to store the elements in a particular order. The queue follows first in first out principle. which means that the first element added to the queue is the first element to be get removed from the queue. In queue the elements are added from the tails and removed from the head.  

To perform operations on queue we can use methods like `offer()`, `poll()`, `peek()`, and `size()`. The queue can be implemented using `LinkedList`,  `ArrayDeque` and `PriorityQueue`.

</blockquote>
  
</details>

---

41. What is a Stack?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Stack is a linear data structure which follows last in first out principal. The last in first out principal stats that the last element added to the stack is the first element to be removed. To perform operations on queue we can use methods like `push()`, `pop()`, `peek()`, and `empty()`. 

The `push()` methods adds the element at the top of stack. The `pop()` methods removes and returns the top element from the stack. The `peek()` methods will return the first element in the stack without removing it. The `empty()` method is used to check whether the stack is empty or not.

</blockquote>
  
</details>

---

42. Queue vs Stack?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The difference between queue and stack is that, the queue follows first in first out principal while the stack follows last in first out principal. 

The new element which will get added in the stack will be added at the end/tail of the stack. The new element which we add in stack gets added at the top of the stack. 

Stacks are commonly used in programming for keeping track of function calls. while the queue is commonly used to manage tasks in a system, such as processing jobs.   

Stacks are used in algorithms such as Depth First Search (DFS). whereas the queue is used in Breadh First Search algotithm.

</blockquote>
  
</details>

---
43. How to handle exceptions?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To handel exception, java provides an exception handling mechanism called `try-catch` block. The part of code which may throw an exception that code is written `try` block. In the `catch` block we write the code which will get executed when any exception occurs in try block. we can have multiple `catch` blocks to handel different types of exceptions. with try and catch block java also provides `finally` block which will get executed wheather an exception occurs or not. The use of `finally` block is optional. 

</blockquote>
  
</details>

---

44. Spring annotations for exception handling?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The spring framework have following annotations to handel exceptions

- `@ControllerAdvice`: This annotation is used to define global exception handlers that apply to all controllers.

- `@ExceptionHandler`: It is used to define methods that handle specific exceptions thrown by controllers or services.

- `@ResponseStatus`: This annotation is used to define the HTTP status code that should be returned when a specific exception is thrown.

- `@RestControllerAdvice`: This annotation is used to define global exception handlers for RESTful web services.

</blockquote>

</details>

---

45. Use of finally?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The finally block is used with `try-catch` block for exception handling in java. The finally block gets executed regardless of whether an exception occurs or not. It is mainly used to release resources such as network connectionds, database connections.

</blockquote>

</details>

---

46. How do you do multi-threading?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Multithreding in java allows a program to perform multiple tasks concurrently, which can improve performance of the application. Threads in java can be created by using two ways. The first way to create an thread in java is by implemention the `Runnable` interface and the second way is by extending the `Thread` class. 

</blockquote>

</details>

---

47. Volatile keywords?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `volatile` keyword in java is used to indicate that a variable's value may be modified by multiple threads at the same time. Without the `volatile` keyword, different threads may create their own copy of that variable which will contain different value for differnt thread. This can lead to incorrect results. The `volatile` keyword helps to prevent this by forcing threads to always read the variable's value from main memory, rather than from a cached copy.

</blockquote>

</details>

---

48. Serialization in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Serialization in Java is the process of converting an object into a stream of bytes so that it can be stored in a file or sent over a network. In java serialization is achieved by implementing the `Serializable` interface, which is a marker interface with no methods. To convert back the serialized bytes back to the object java use a process called `Deserialization`. We can not serialize all the objects. The objects that contain non-serializable fields or methods such as open file handles or network connections, cannot be serialized. 

</blockquote>

</details>

---

50. What are hashes in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, hashes usually refer to the hash codes generated by the `hashCode()` method in object. The `hashCode()` method returns an integer value that is often used as an index in hash tables or for other purposes that require a unique identifier for an object. 

</blockquote>

</details>

---

51. What is JDBC?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JDBC stands for Java Database Connectivity. It is a Java API which is used to interact with relational databases. JDBC provides a standard set of interfaces that allow the user to connect to a database and retrieve or modify data in the database. 

</blockquote>

</details>

---

52. How do you make a connection to the database using jdbc?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To make a connection to the database using jdbc first we have to load the JDBC driver for the database you want to connect to using the `Class.forName()` method. then we can create a create a `Connection` object using the `DriverManager.getConnection()` method and providing the URL, username, and password for the database. Then create a `Statement` using the `Connection.createStatement()` method. Then we can use `executeQuery()` method to run the queries on the database and fetch the result. The result received by the database can be stored in `ResultSet` object.

</blockquote>

</details>

---

53. What are servlets?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Servlets are Java-based server-side components that are used to generate dynamic web content. The servlets run on a web server and respond to incoming requests from client side, by generating dynamic web content. Servlets are commonly used to create web applications such as online shopping sites, social media platforms, and other interactive web applications.

</blockquote>

</details>

---

54. What are Java Server Pages?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JavaServer Pages (JSP) is a technology used to create dynamic web pages in Java. It allows you to combine static HTML with Java code to generate dynamic content on the server-side, which is then sent to the client-side for display in a web browser.

JSP pages can be used to create a wide variety of web-based applications, including e-commerce sites, content management systems, social media platforms, and more.

JSP pages can also be combined with other Java technologies, such as JavaBeans, servlets, and tag libraries, to create even more powerful web-based applications.

</blockquote>

</details>

---