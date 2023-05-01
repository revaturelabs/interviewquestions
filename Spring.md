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

3. What is a singleton, and why do you use it?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Singleton is a type of bean object scope in which only one instance of the bean is created, and this same instance is shared globally for each request made for that bean. The singleton bean scope is used for stateless beans that do not maintain any internal state, such as utility classes or service classes. The singleton scope offers benefits like improved performance, consistency, and simplicity in configuration.

</blockquote>
  
</details>

---

4. How do you connect a spring application with a database?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To connect a database to our spring boot application first, we have to add the driver dependency for that specific database. After adding the dependency we have to configure the database properties like URL, username, and password in our `application.properties` or `application.yml` file. Post which we have to create a Database access layer to interact with our database.

</blockquote>
  
</details>

---

5. How does jpa interact with the data base?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JPA stands for Java Persistence API. It is a standard interface for Object-Relational Mapping (ORM) tools to map Java objects to relational databases. The JPA interacts with the database using an EntityManager, which is responsible for managing the lifecycle of entities. JPA also provides a query language called JPQL (Java Persistence Query Language). The JPQL queries are then translated into SQL statements that are used to perform operations on the database.


</blockquote>
  
</details>

---


6. How can I make so that a field in an entity class does not generate a column?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To achieve this functionality we can use the `@Transient` annotation. The `@Transient` annotation indicates JPA to exclude the annotated field while creating the database table.

</blockquote>
  
</details>

---

7. How do you create a controller in your spring application?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a controller in a Spring application. Create a class and annotate it with the `@Controller` annotation. This class will have methods that handle incoming HTTP requests and return a response to the client. You can also use the `@RequestMapping` annotation above the controller class to define the base UR for the class methods.

</blockquote>
  
</details>

---

8. How does Spring know if your request is post, get, or put in your controller?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The Spring framework determines the type of HTTP request (POST, GET, PUT) based on the HTTP method specified in the request. Spring checks the HTTP method and URL pattern to map that request to a specific method.

For example, if we send a GET request with a specific URL, Spring will automatically map that request to a method which has the `@GetMapping` annotation with a matching URL pattern.


</blockquote>
  
</details>

---

9. How were you transferring information through the controllers to your angular application? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To transfer data from contoller to angular application we can use `HTTPClient` service which will be used to make HTTP requests to the controller. The `HTTPClient` service return an `observable` which we can subscribe to get the data sent from the controller in our angular application.


</blockquote>
  
</details>

---

10. Controller annotations for get mapping, post mapping?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

We use the `@GetMapping` annotation for HTTP GET requests to map that request to a specific handler method in a controller, and the `@PostMapping` annotation for HTTP POST requests in Spring.

</blockquote>
  
</details>

---

11. Can spring use a server different from the embedded tomcat server?
 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Spring support the usage of different servers other than the embedded Tomcat server and can use different servers like Jetty, GlassFish, WebSphere, and others. To use a different server in Spring, you need to add the required dependencies to your project and make specific configuration changes based on the server you want to use.

</blockquote>
  
</details>

---

12. What is Spring and why do we use it?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Spring is a popular open-source Java framework used to build robust and scalable applications. It provides features like dependency injection, aspect-oriented programming, and transaction management. By using spring the developer have to write less boilerplate code,and can manage dependencies more easily. Spring is widely used for building web applications, microservices, and enterprise applications. 

</blockquote>
  
</details>

---

13. How do you inject a dependency through the constructor ?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To inject a dependency through the constructor, create a constructor in a class and pass that dependency as a parameter to the constructor. Then, apply the `@Autowired` annotation above the constructor, Spring will automatically detect the dependency and inject it into the constructor when creating an instance of the class.

</blockquote>
  
</details>

---

14. Spring annotations for exception handling?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The spring framework has the following annotations to handle exceptions

- `@ControllerAdvice`: This annotation is used to define global exception handlers that apply to all controllers.

- `@ExceptionHandler`: It is used to define methods that handle specific exceptions thrown by controllers or services.

- `@ResponseStatus`: This annotation is used to define the HTTP status code that should be returned when a specific exception is thrown.

- `@RestControllerAdvice`: This annotation is used to define global exception handlers for RESTful web services.

</blockquote>

</details>

---

15. Default scope of beans in Spring?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Singleton scope is the default scope of Bean in Spring. When a bean is defined as a singleton, the Spring container creates only one instance of that bean, and all requests for that bean will return the same instance. This can be very efficient in terms of performance and memory usage, as it avoids creating multiple instances of the same bean.

Spring also includes other bean scopes like `prototype`, `request`, `session`, and `global session`.

</blockquote>

</details>

---

16. Other type of Universal Bean Scope in Spring?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Spring, the term "bean scope" refers to the lifecycle of a bean and indicates how many instances of the bean should be created and managed by the Spring container. There are different types of bean scopes like `Prototype`, `Request`, `Session`, `Global Session`, `Application`, and `WebSocket`. 

</blockquote>

</details>

---

17. What are prototype beans?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A prototype bean is a type of bean whose lifecycle is managed by the Spring IoC container in such a way that every time a bean is requested by the application, a new instance of the bean is created and returned. This means that each instance of the prototype bean will be completely independent and have its own state. Changes made to one instance of the bean will not affect other instances of the same bean.

</blockquote>

</details>

---

18. Types of advice in AOP?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

AOP stands for Aspect-Oriented Programming. It provides several types of advice to modify the behavior of target objects at runtime. The different types of advice in AOP are as follows:

- Before Advice: This advice is executed before the target method execution.

- After Advice: This advice is executed after the target method execution, regardless of whether the method execution was successful or resulted in an exception. 

- Around Advice: This advice intercepts the target method execution and allows the advice to control when and how the target method is executed. 

- After Returning Advice: This advice is executed after the target method execution has completed successfully and returned a result.

- After Throwing Advice: This advice is executed when the target method throws an exception. 

- Introduction Advice: This advice allows new methods and properties to be added to a target object at runtime.

</blockquote>

</details>

---

19. What is a JoinPoint?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In AOP a JoinPoint is a point during the execution of a program where the aspect code can be attached to the programme. It can be thought of as a hook or an event in the program's execution where an aspect can intervene and perform its function. Examples of JoinPoints include method calls, method executions, field accesses, and exception handling.  

</blockquote>

</details>

---

20. What are JDBC Templates?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The JDBC Templates are a part of the Spring Framework that provides a higher-level abstraction layer over the JDBC API. The JDBC Template encapsulates the common database operations, such as connecting to the database, creating statements, executing queries, and handling exceptions. It simplifies the use of JDBC and reduces the amount of boilerplate code needed for database operations.


</blockquote>

</details>

---

21. What is the lifecycle (this term confused me) of Dependency Injection?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dependency Injection (DI) is a design pattern used in software engineering to manage dependencies among objects. The lifecycle of Dependency Injection involves configuring a container with information about objects and their dependencies, injecting those dependencies into the objects, using the objects within the application, disposing of objects when they are no longer needed, and updating the container as necessary.

</blockquote>

</details>

---

22. What is CORS?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The CORS stands for Cross-Origin Resource Sharing. It is a security feature implemented in web browsers that restricts web pages from making requests to a different domain. It works by adding special HTTP headers to the response, which indicate which domains are allowed to make requests. This mechanism helps prevent unauthorized access to sensitive data.

</blockquote>

</details>

---

23. What is Lazy Loading?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Lazy Loading is a technique used in software development which enables the user to load the necessary information first and load the non-critical resources when they are required. This can optimize web page performance by loading only the visible portion of a web page initially, and additional content as the user scrolls down the page.

</blockquote>

</details>

---

24. Explain a design pattern you used befor.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

I have used Singleton design pattern. This pattern ensures that threr is only one object of a class is created, and that same object is shared across the application. The Single design pattern is implemented by creating a private constructor for the class and a static method that returns the single instance of the class. This pattern can be useful for things like database connections or logging, where you want to make sure that there is only one instance of the class.


</blockquote>

</details>

---

25. What is Springboot.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Spring Boot is a framework in Java that is used for building web applications and microservices. It is built on top of the popular Spring Framework. Using the spring boot framework we can easily configure Spring applications. It simplifies the process of application development by using its default tools. Spring Boot can quickly create a production-ready application and includes support for popular technologies like Spring Data and Spring Security.

</blockquote>

</details>

---

26. What is Spring JPA ?

<blockquote>

Spring JPA is a part of the Spring Framework that simplifies database access by providing a higher-level Object Relational Mapping (ORM) framework. The developers don't have to write boilerplate SQL code to perform operations on the database. It helps the developers to interact with databases more efficiently by providing features like entity mapping, CRUD operations, transactions, and querying using JPQL and Criteria API.


</blockquote>

</details>

---

27. Annotations used in Controller?

<blockquote>

In controller we use the annotations like `@Controller`, `@RequestMapping`, `@GetMapping`,`@PostMapping`, `@PutMapping`, `@DeleteMapping`, `@PathVariable`, `@RequestBody`, etc.

</blockquote>

</details>

---

28. What is @AutoWired?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `@Autowired` is a Spring annotation used for automatic dependency injection in spring. It allows Spring to automatically identify and inject the necessary dependencies (i.e., objects that a class needs to perform its functions) into a Spring-managed bean. By annotating a class property, constructor, or a setter method with @Autowired, Spring will automatically inject an instance of the required dependency when the bean is created. Spring uses type matching to determine which dependency to inject in the bean.

</blockquote>

</details>

---


29. Tell us about initialization in Spring?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

30. The difference between a @bean and @component.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between `@Component` and `@Bean` is that `@Component` is a class-level annotation that allows Spring to automatically discover and register a bean, whereas `@Bean` is a method-level annotation that creates and returns an object that Spring should register as a bean. 

</blockquote>
  
</details>

---

31. What is a controller;

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

32. Questions on Spring, how did you implement Spring JPA in your last project?; 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

33. What are dependency injections & the benefits of using them?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---