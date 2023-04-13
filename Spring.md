
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


4. CrudRepository vs JPARepository?

<details> <summary>Show Answer</summary>
 
<blockquote>



- The central interface in Spring Data repository is `Repository`. 
- Both CrudRepository and JPARepository are interfaces provided by Spring Data JPA to perform basic CRUD (Create, Read, Update, Delete) operations on entities in a database.
- The `CrudRepository` extends the `Repository`. It provides sophisticated CRUD functionality with methods like `save`, `findById`, `findAll`, `count`, `delete`, `existesById` etc.

- The `JpaRepository` extends the `CrudRepository` along with other repositories like  `ListCrudRepository`, `ListPagingAndSortingRepository`, and `PagingAndSortingRepository` etc.
- JpaRepository provides fine grained control over repository layer and it also as additional methods to perform more complex queries using the JPQL (Java Persistence Query Language) or native SQL queries like `findAll(Pageable)`, `findAll(Sort)`, `flush()` and `saveAndFlush(S)` etc.


  
</blockquote>

</details>

---

5. Default fetch type for ManyToOne?

<details> <summary>Show Answer</summary>
 
<blockquote>

The default fetch type for a `@ManyToOne` association in JPA (Java Persistence API) is `EAGER`. This means that when an entity containing a `@ManyToOne` association is fetched from the database, the associated entity is also fetched eagerly, by default.

The fetch type can be changed to `LAZY` explicityly by using the following code:

```java
@ManyToOne(fetch = FetchType.LAZY)
private OtherEntity otherEntity;
```
With LAZY fetch type, the associated entity will only be fetched from the database when it is actually accessed for the first time, which can help to improve performance by reducing unnecessary database queries.
  
</blockquote>

</details>

---

6. Code to specify fetch types?

<details> <summary>Show Answer</summary>
 
<blockquote>

The fetch type referes to the different ways of retreiving data from a database. There are two types:

1. `EAGER`: EAGER loading means that the associated entity or collection will be loaded immediately along with the owning entity. In other words, when an entity is retrieved from the database, its associated entities or collections are also retrieved from the database and loaded into memory.
2. `LAZY`: LAZY loading means that the associated entity or collection will not be loaded along with the owning entity. Instead, the associated entity or collection is loaded from the database only when it is actually accessed in the code.

The code to specify the fetch type is:

```java
import org.hibernate.FetchMode;
import org.hibernate.annotations.Fetch;

@Entity
public class Order {

    @OneToMany(fetch = FetchType.LAZY)
    private List<OrderItem> items;

    @OneToMany
    @Fetch(value = FetchMode.SELECT)
    private List<OrderNote> notes;

    // methods
}
```

In the above code `(fetch = FetchType.LAZY)` is used to specify the fetch mode as `LAZY` or `EAGER`. The `@Fetch(value = FetchMode.SELECT)` specifies the `LAZY` and `@Fetch(value = FetchMode.JOIN)` specifies `EAGER`.

  
</blockquote>

</details>

---

7. What does Spring MVC stand for and what does it do?

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

8. What is Spring Boot, what is your experience with it?

<details> <summary>Show Answer</summary>
 
<blockquote>

- Spring Boot is a Java-based open-source framework that is used to create standalone, production-ready applications quickly and easily. 
- It is built on top of the Spring framework and provides a simplified approach to building and deploying web applications, microservices, and APIs.
- Spring Boot reduces the amount of boilerplate code required to build an application, making it easier to get started with Spring development. 
- It also provides a range of features such as auto-configuration, which automatically configures the application based on the dependencies added to the project, and embedded servers, which allow applications to be deployed without the need for a separate server installation.
  
</blockquote>

</details>

---


9. Tell me about ORM

<details> <summary>Show Answer</summary>
 
<blockquote>

ORM stands for Object Relational Mapping. The integration of Spring with Hibernate, iBATIS and Toplink frameworks is called Spring with ORM framework.

## Advantages of Spring ORM

- Less coding:
The process of managing the transaction, creating session and calling session factory can be avoided. Directly a hibernate template object can be used.
- Easy to test:
Junit testing can be used with Spring
- Better Exceptional Handling
- Integrated Transaction management

### JDBC vs ORM

![JDBC](/resources/JDBC.PNG)
- In the traditional JDBC approach the data from the result set is assigned to the object explicitly.

![ORM](/resources/ORM.PNG)
- In ORM the entity class is mapped with the SQL table and an object of the entity class is obtained.
  
</blockquote>

</details>

---

10.   Ways to make multiple data sources/connections in Spring?

<details> <summary>Show Answer</summary>
 
<blockquote>

Spring Framework provides several ways to make multiple data sources/connections, Here are some of the ways:

**1. Using multiple configuration files:** You can define different configuration files for each data source, and load them using Spring's @Configuration annotation. This allows you to configure multiple data sources separately, and inject them into different parts of your application.

**2. Using the DriverManagerDataSource class:** Spring's DriverManagerDataSource class allows you to configure multiple data sources programmatically. You can create multiple instances of this class, each with its own set of connection details, and inject them into your application.

**3.Using Spring Boot:** If you're using Spring Boot, you can define multiple data sources in your application.properties or application.yml file. Spring Boot will automatically create DataSource beans for each data source, which you can then inject into your application.

**4. Using Spring Data JPA:** Spring Data JPA provides support for multiple data sources out of the box. You can configure multiple data sources in your application.properties or application.yml file, and use the @Qualifier annotation to specify which data source to use in each repository.
  
</blockquote>

</details>

---

11. What is the difference between Spring and Spring Boot?

<details> <summary>Show Answer</summary>
 
<blockquote>

### Spring vs SPringBoot

| Aspect              | Spring                                                    | Spring Boot                                                                                     |
| ------------------- | --------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Configuration       | Requires manual configuration setup for most components   | Includes pre-configured setup for many common components                                        |
| Dependencies        | Requires explicit management of dependencies and versions | Uses a dependency management plugin to manage dependencies and versions                         |
| Packaging           | Requires manual packaging of the application              | Includes tools to automatically package the application as a self-contained executable JAR file |
| Auto-configuration  | Doesn't have auto-configuration                           | Includes auto-configuration to automatically configure components based on classpath            |
| Embedded Containers | Requires manual configuration of an embedded container    | Includes embedded containers such as Tomcat by default                     |
| Annotation          | Needs more annotation for configuration                   | Requires less annotation for configuration                                                      |
| Ease of Use         | Less easy to use                                          | More easy to use                                                                                |

- Spring Boot builds on top of Spring to provide a more streamlined and easier to use experience for developers. It includes many pre-configured setups and auto-configuration features, reducing the amount of manual configuration required.

  
</blockquote>

</details>

---

12.   What does this "@Annotation" do in Spring?

<details> <summary>Show Answer</summary>
 
<blockquote>

`@Annotation` is a syntax used to declare annotations in java and spring. 

Few Examples for annotations in spring are:

- `@Autowired` annotation is used to automatically wire dependencies into a Spring bean.
- `@RequestMapping` annotation is used to map HTTP requests to controller methods.
- `@Transactional` annotation is used to mark a method as transactional.
- Spring also has stereotype annotations like:

**1. `@Component`**

`@Component` is the main Stereotype Annotation. It is a class-level annotation. `@Component` is used across the application to mark the beans as Spring's managed components.

**2. `@Service`**

It is a specialization of `@Component`. The business logic of an application is in the service layer, `@Service` annotation is used to indicate that a class belongs to the service layer.

**3. `@Repository`**

It is a specialization of `@Component`. It is very similar to the DAO pattern. DAO classes provide CRUD operations for database tables.

**4. `@Controller`**

It is a specialisation of `@Component`. The `@Controller` indicates that a particular class is a controller. It is mostly used with Spring MVC applications. It is used in combination with annotated methods based on the `@RequestMapping` annotation. The dispatcher scans the class and detects methods with `@RequestMapping`. 

  
</blockquote>

</details>

---


