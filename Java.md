1. Why use Dependency injection?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dependency injection (DI) is a technique used in software engineering to make development of software applications easier. The DI uses loose coupling between different components, making it easier to modify individual parts without affecting the rest of the application.

Consider you are writing a code for an application where the various objects depend on each other. So, instead of having each object create and manage its own dependencies, you can use DI to create an object of those dependencies and pass them to each object whenever needed.

Since the dependencies are managed by the DI, users can modify them without needing to change the code in every object that uses them.

</blockquote>
  
</details>

---

2. Difference between RestController and Controller?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between RestController and Controller is that the `@RestController` is used for building RESTful web services that return data in JSON, XML or any other format and the `@Controller` is used when we are building a web application that return an HTML view.

</blockquote>
  
</details>

---

3. Functional interface in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A functional interface is a Java 8 feature and is also called as `Single Abstract Method`. It is an interface that has only one abstract method. Functional interfaces are commonly used with lambda expressions to create more concise and readable code.

Java includes some built-in functional interfaces, such as Runnable, Consumer, Comparable.

</blockquote>
  
</details>

---

4. What is the purpose of interfaces in Java? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An interface defined the set of methods that a class must implement. It is like a blueprint for a class. They are used to achieve abstraction in the application. Also by using interface we can achieve multiple inheritance in java.

</blockquote>
  
</details>

---

5. What is a singleton, and why do you use it?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Singleton is a type of bean object scope in which only one instance of bean is created. and this same instance will be shared globally for each request made for that bean.

</blockquote>
  
</details>

---

6. What is a class?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Class is a blueprint for creating objects. It defines the structure of an object by specifying methods and variables which the object will contain. Objects are created from class by using `new` keyword.

</blockquote>
  
</details>

---

7. What is object?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An object is an instance of class. It represents an real-world entity which have properties and behaviour specified by the class. An object is creted from class using `new` keyword. Each object have it's own unique identity and behaviour. Objects are the main block of object oriented programming. 

</blockquote>
  
</details>

---

8. How do you connect a spring application with a database?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To connect a database to our spring boot application first we have to add the driver dependency for that specific database. After adding the dependency we have to configure the database properties like url, username, password in our `application.properties` or `application.yml` file. Post which we have to create an Database access layer to interact with our database.

</blockquote>
  
</details>

---

9. How do you connect a spring application with a database?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To connect a database to our spring boot application first we have to add the driver dependency for that specific database. After adding the dependency we have to configure the database properties like url, username, password in our `application.properties` or `application.yml` file. Post which we have to create an Database access layer to interact with our database.

</blockquote>
  
</details>

---

10. How can I make so that a field in an entity class does not generate a colum?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To acheive this functinality we can use `@Transient` annotation. The `@Transient` annotation indicats JPA to exclude the annotated field while creating the database table.

</blockquote>
  
</details>

---

11. How do you create a controller in your spring application?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a controller in a Spring application. Create a class and annotate it with the `@Controller` annotation. You can also use `@RequestMapping` annotation above the controller class to define the base url for the class methods. 

</blockquote>
  
</details>

---

12. How does spring know if your request is post, get or put in your controller?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The spring determines the type of HTTP request POST, GET, PUT based on the HTTP method specified in the request. Spring checks the HTTP method and url pattern to map that request to a specific method. 

For example, If we send an GET request with a specific url. The spring will automatically map that request to a method which is having `@GetMapping` annotation with matching url pattern.


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

An abstract class is a class which contain abstract methods. The abstract class can not be instantiated and have to be extended by other class to use the methods of that class. While an interface serves as an contract that specifies a set of methods that a class must implement.

The difference between abstract class and interface is that the abstract class can contain both abstract and non-abstract methods while an interface can have only abstract methods. Since java 8, it can have static and default methods. Abstract class can have final, non-final, static and non-static variables while interface can only have static and final variables.


</blockquote>
  
</details>

---

15. Controller annotations for get mapping, post mapping?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

We can use `@GetMapping` annotation for get mapping and `@PostMapping` annotation for post mapping in spring.

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

In java we follow pass-by-value.

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