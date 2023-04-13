
1. Use of @Configuration annotation?

<details> <summary>Show Answer</summary>
 
<blockquote>

Java Spring Framework, the `@Configuration` annotation is used to indicate that a class contains bean definitions that should be processed by the Spring container.

A class annotated with `@Configuration` is effectively a factory for creating beans, and its methods annotated with `@Bean` will create and configure individual beans. When the Spring container starts up, it will scan the application context for any `@Configuration` annotated classes and process them accordingly.
  
</blockquote>

</details>

---

2. Ways of creating beans in Spring? What annotations?

<details> <summary>Show Answer</summary>
 
<blockquote>

In spring framework, the beans can be created in three different ways:

1. XML configuration

The following syntax is used to define a bean

```XML
<bean id="..." class="...">
   <!-- dependencies and configuration for this bean go here -->
</bean>
```

2. `@Component` annotation

A bean will be registered for every class that has a `@Component` annotation in the Spring container with a bean id.

```java
package com.demo.annotationsconfig;

import org.springframework.stereotype.Component;

@Component
public class App {
}
```

3. `@Configuration` annotated class with `@Bean` annotated methods.

A class annotated with `@Configuration` is effectively a factory for creating beans, and its methods annotated with `@Bean` will create and configure individual beans.

```java
@Configuration
public class MyConfiguration {

    @Bean
    public MyBean myBean() {
        return new MyBean();
    }
}
```
  
</blockquote>

</details>

---

3. What does @Service annotation do?

<details> <summary>Show Answer</summary>
 
<blockquote>

**`@Service`:**

It is a specialization of `@Component`. The business logic of an application is in the service layer, `@Service` annotation is used to indicate that a class belongs to the service layer.
  
</blockquote>

</details>

---

4. Event and Listeners in Servlets?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

5. CrudRepository vs JPARepository?

<details> <summary>Show Answer</summary>
 
<blockquote>


  
</blockquote>

</details>

---

6. Default fetch type for ManyToOne?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

7. Code to specify fetch types?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

8. Do you know about Java 8?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

9. What are optional objects?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

10. Sort elements in a String ArrayList. – Alphabetically - By String length

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

11. What does Spring MVC stand for and what does it do?

<details> <summary>Show Answer</summary>
 
<blockquote>

## MVC Architecture

**Model:** The component that deals with all the data-related logic or business logic is Model

**View:** This component deals with the UI logic of the application.

**Controller:** It is an interface between Model and View. It is used to process business logic and incoming requests, manipulate data using the Model component and interact with the Views to give the final output.

## Spring MVC

Spring MVC makes the life of a programmer easier by providing a Front Controller to handle all the controllers.

The flow in Spring MVC is as follows

![SpringMVC Architectire](/resources/SpringMVC.PNG)

- The request from the client is taken to web.xml which sends the request to the DispatcherServlet.
- Based on the request, the request is sent to a specific controller.
- An XML file is created for spring MVC and all the controllers are annotated with the `@Controller` annotation.
- The response from the controller is model and view name.
- The DispatcherServlet interacts with the view template and sends the response.

- In this architecture, as the DispatcherServlet handles all the requests and sends the response there is no direct interaction between the client and the controllers.

- As DispatcherServlet interacts with the view template, at any point in time the developer can change the view from JSP to thymeleaf or any other view template easily.
  
</blockquote>

</details>

---

12. What is Spring Boot, what is your experience with it?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

13. What is your experience with Postman?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

14. Tell me about ORM

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

15. What is the difference between process variables and activity class variables?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

16. What are some best practices for creating interfaces?


<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

17. What is the difference between local variables and rule inputs?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

18. Have you used any testing frameworks? Ex. JUnit, Mockito

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

19. Ways to make multiple data sources/connections in Spring?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---
20. 4 pillars of OOP.

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---
