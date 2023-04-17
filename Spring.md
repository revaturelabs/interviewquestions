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

In Spring, the term "bean scope" refers to the lifecycle of a bean and indicates how many instances of the bean should be created and managed by the Spring container.

following are the types of bean scopes in spring:

- `Prototype`: In this scope, a new instance of the bean is created every time it is requested from the container.

- `Request`: In this scope, a new instance of the bean is created for each HTTP request. This scope is only applicable for web applications.

- `Session`: In this scope, a new instance of the bean is created for each HTTP session. This scope is only applicable for web applications.

- `Global Session`: This scope is similar to the session scope, but it is used in a portlet context where multiple portlets share the same session.

- `Application`: In this scope, a single instance of the bean is created for the entire lifecycle of the application.

- `WebSocket`: In this scope, a new instance of the bean is created for each WebSocket session. This scope is only applicable for WebSocket-based applications.


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

In AOP a JoinPoint is a point during the execution of a program where the aspect code can be attached into the program's execution. A JoinPoint can be thought of as a hook or an event in the program's execution where an aspect can intervene and perform its function. Examples of JoinPoints include method calls, method executions, field accesses, and exception handling.  

</blockquote>

</details>

---

20. What are JDBC Templates?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JDBC Templates are a part of the Spring Framework that provides a higher-level abstraction layer over the JDBC API. The JDBC Template encapsulates the common database operations, such as connecting to the database, creating statements, executing queries, and handling exceptions. It simplifies the use of JDBC and reduces the amount of boilerplate code needed for database operations.


</blockquote>

</details>

---

