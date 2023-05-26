## Technical

1. How do you make a decision between choosing Spring or Spring Boot framework for the application?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- It’s simple, any console/desktop or web application that wants to leverage DI & other key features provided by Core Spring modules can use the Spring framework.
- Spring Boot framework was evolved on top of Spring framework to support microservices-based architecture on the cloud.
- Spring Boot framework is popularly used to develop Web/Enterprise Applications, RESTful API & Microservices.

</blockquote>

</details>

---
2. Why is it necessary to have a Service layer? Is it possible to directly invoke the Repository layer from the Controller layer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- There is no restriction from compiler, and we can call the Repository layer from the Controller layer directly.
- The layering helps to segregate the Spring application responsibilities and enables loose coupling between the objects.
- Service layer in the application facilitates communication between the Controller and the Persistence/Repository/DAO layer.
- Service layer usually holds business logic e.g. It may include validation logic.
- One Service layer may depend on multiple Repository layers to serve a specific business purpose.
- The method names in Service layer are usually named as per the business purpose they serve whereas method names in Repository are named as standard CRUD operations supported by that Repository.
- Hence, we need Service layer between DAO and Controller layer.
</blockquote> 

</details>

---
3. Is it secure to store sensitive passwords, such as database credentials, directly inside property files? Justify.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Since property file(s) are readable by anyone who has access to the codebase it is highly recommended not to keep the DB and other critical credentials inside property file(s).
- They are usually stored inside cloud environment variables or passed through command line arguments while executing the application.

``` java 
mvn spring-boot:run -Dspring-boot.run.jvmArguments='
-Dspring.datasource.url=jdbc:postgresql://localhost:5432/mydb 
-Dspring.datasource.username=admin 
-Dspring.datasource.password=gd123'

````
</blockquote> 

</details>

---
4. How can Spring Boot assist developers in monitoring the status of a production application on a daily basis? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- One of the routine tasks for a developer is to check the status of the already launched production application periodically.
- To simplify this task, Spring Boot provides a sub-project named Spring Boot Actuator.
- Spring Actuator exposes operational information about the executing application, including, metrics, info, dump, env, etc. 
- The information is accessed usually via HTTP endpoints, a few of which are listed below:
    - `/health` summarizes the health status of our application.
    - `/beans` returns all available beans in our BeanFactory.
    - `/envy returns the current environment properties. 
- To enable Spring Boot Actuator, we just need to add the spring-boot-actuator dependency to our maven package manager.

```XML
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
- To access the actuator endpoints using HTTP, we need to both enable and expose them.
- Only the /health and /info endpoints are exposed by default.
- We need to add the following configuration to expose all endpoints: 
`management.endpoints.web.exposure.include=*`

</blockquote> 
</details>

---
5. What is Spring profile and why do we use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Profiles provide a way to segregate parts of your application configuration and make it only available in certain environments. 
- Any `@Component`, `@Configuration` or `@ConfigurationProperties` can be marked with `@Profile` to limit when it is loaded.
```java
@Configuration
@Profile("prod")
public class ProductionConfiguration {
 // ...
}

@Configuration
@Profile("test")
public class TestConfiguration {
 // ...
}
```
- In the normal Spring way, you can use a `spring.profiles.active` environment property to specify which profiles are active. 
- You can specify the property in any of the usual ways, for example, you could include it in your application.properties:
`spring.profiles.active=test`
or specify on the command line using the switch `--spring.profiles.active=prod`.
</blockquote> 

</details>

---
6. How do you define multiple profiles in the Spring Boot application and also explain how to add an active profile?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The application development process undergoes different stages; the typical ones are development, testing, and production. 
- Spring Boot profiles help group parts of the application configuration and make it available only in certain environments.
- A profile is a set of configuration settings. 
- Spring Boot allows to definition profile of -specific property files in the form of `application-{profile}.properties`.
- We can define both profile-specific and default application.properties file in the application. (For example, if your application activates a profile named prod and uses YAML files, then both application.yml and application-prod.yml will be considered).
- The local/default profile (`application.properties`) is usually called `default`; all the beans that do not have a profile set belong to the `default` profile.
- Spring automatically loads the properties in an application.properties file for all profiles and the ones in profile-specific property files only for the specified profile. 
- The keys in the profile-specific property override the ones in the default property file.
- There are plenty of ways of defining active profiles in Spring Boot, including command line arguments, Maven settings, JVM system parameters, environment variables, spring.profiles.active property, and SpringApplication methods.
- We commonly set active profiles using the `spring the .profiles.active` property or command line argument.
- For Example, we have three profiles (`local/default`, `dev`, `prod`) and two profile-specific property files as below:
```
pom.xml
src
├── main
│   ├── java
│   │   └── com
│   │       └── revature
│   │           └── Application.java
│   └── resources
│       ├── application-dev.properties
│       ├── application-prod.properties
│       └── application.properties
└── test
    └── java
```
</blockquote> 

</details>

---
7. What is the outcome when the spring.profiles.active property in a Spring application is configured with two profiles?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- If multiple profiles are specified for spring.profiles.active, the last profile in the list will override any previous ones. This means that the configurations and beans defined for the last profile will be active, while the configurations and beans associated with the earlier profiles will be ignored.

-It is important to be mindful of the order of the profiles in spring.profiles.active property, as it determines which profiles take precedence.

- For example, if profiles prod,live are 
specified by the spring.profiles.active property (i.e. `spring.profiles.active=prod,live`), values in `application-prod.properties` can be overridden by those in `application-live.properties`.

</blockquote> 

</details>

---
8. Which `pom.xml` file inside the Spring Boot framework defines versions of all pre-configured dependencies?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Boot framework has utilized the concept of parent and child pom file inheritance and defined all the dependencies specific to its release version under `spring-boot-dependencies` module.
- For example, refer to this link: https://repo1.maven.org/maven2/org/springframework/boot/spring-boot-dependencies/2.7.3/spring-boot-dependencies-2.7.3.pom

</blockquote> 

</details>

---
9. What is Bean Validation API and explain how do you implement it in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- To restrict the input provided by the user in Spring MVC applications, the Spring >=4 supports and uses `Bean Validation API`.
- The Bean Validation API is a Java specification which is used to apply constraints to the fields of a class via annotations. 
- Using Bean Validation API we can validate a length, number, regular expression, etc. as well, and build custom validations.
- `Hibernate Validator` is the most famous/used implementation of the Bean Validation API specification.
- There are 3 types of variables that can be validated using Bean Validation API:
  - The request body,
  - Variables within the path (e.g., id in /api/{id}) and,
  - Query parameters.
- Spring Boot comes with the validation starter, which needs to be included in `pom.xml` file and the intern added the `hibernate-validator` dependency as below:

```xml
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
  </dependency>
```

</blockquote> 

</details>

---
10. List some of the Spring bean validation annotations available in `hibernate-validator`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Few common validation annotations are listed below:
  - `@NotNull`: Field must not be null.
  - `@NotEmpty`: List field must not be empty.
  - `@NotBlank`: String field must not be the empty String (i.e., it must have at least one Character).
  - `@Min` and `@Max`: Numerical field is only valid when its value is above or below a certain value.
  - `@Pattern`: String field is only valid when it matches a certain regular expression.
  - `@Email`: String field must be a valid email address.


</blockquote> 

</details>

---
11. What is the use of `@Valid` annotation  in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `@Valid` annotation can be added to variables in a `RestController` mapping method to validate them. 
- In the below code our POST request takes in a request body, and we're mapping that request body to a class InputForm.
- The `@Valid` annotation will tell Spring to go and validate the data passed into the controller i.e., age is between 18 and 60 inclusive because of those Bean Validation API annotations (min and max).
```java
@RestController
public class ValidateFormController {
  @PostMapping("/validateInput")
  ResponseEntity<String> validateBody(@Valid @RequestBody InputForm inputForm) {
    return ResponseEntity.ok("valid");
  }
  // ...
}

public class InputForm {
  @Min(18)
  @Max(60)
  private int age;
  // ...
}
```

</blockquote> 

</details>

---

12. What is the use of `@ControllerAdvice` in the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@ControllerAdvice` is a specialization of the `@Component` annotation which allows handling exceptions across the whole application in one global handling component.
- It intercepts exceptions thrown by methods annotated with `@RequestMapping` and similar.
- All you need to have is a class annotated with @ControllerAdvice. 
- If any exception is raised in the defined controller [you can define to which packages this controller advice should listen for exception in base packages] then it is handled by ControllerAdvice.
```java
@ControllerAdvice(basePackages = "{com.revature.controller}")
public class RestApiExceptionHandlerAdvice {
    /** Handle all business exceptions here */  
}
```
</blockquote> 

</details>

---

13. What is the use of `@ExceptionHandler` in the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `@ExceptionHandler` is an annotation used to handle a specific exception in the controller and send a custom response to the client.
- We need to have a method annotated with @ExceptionHandler which takes Exception Class (any exception that you want to handle) as an argument, if any of these exceptions are raised in the controller, then this handler method will handle it.
- If we have two handler methods in the same controller say for example one handler for Exception and another handler for RuntimeException, then the handler method which is closer to the Exception Class hierarchy is triggered. 
- For example, if NullPointerException is thrown then IOException handler method is triggered, which is the closest to the Exception class.
```java
@ControllerAdvice(basePackages = "{com.revature.controller}")
public class RestApiExceptionHandlerAdvice {
    @ExceptionHandler(value = BadRequestException.class)
    public ErrorMessage handleBadRequest(BadRequestException exception) {
        //code...
        return errMsg;
    }
    @ExceptionHandler(value = GatewayTimeoutException.class)
    public ErrorMessage handleGatewayTimeout(GatewayTimeoutException exception) {
        //code...
        return errMsg;
    } 
}
```
</blockquote> 

</details>

---
14. What is HAL browser in Spring? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- HAL stands for Hypertext Application Language.
- HAL is a simple format that gives a consistent and easy way to hyperlink between resources in your API.
- Adopting HAL make API explorable, and its documentation easily discoverable from within the API itself. 
- In short, it makes API easier to work with and therefore more attractive to client developers.
- The HAL browser provides an in-browser GUI to traverse your Spring RESTful API.
- Below is the single dependency needed to integrate the HAL browser into our REST API. 

```xml

  <dependency>
	  <groupId>org.springframework.data</groupId>
	  <artifactId>spring-data-rest-hal-explorer</artifactId>
  </dependency>

```
- If we have the above dependency, Spring will auto-configure the HAL browser, and make it available via the default endpoint.
- All we need to do now is press run and switch to the browser. The HAL browser will then be available on http://localhost:8080/

</blockquote> 

</details>

---
15. What is the use of the `ResponseEntity` class in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `ResponseEntity` represents an HTTP response, including headers, body, and status. 
- While `@ResponseBody` puts the return value into the body of the response, ResponseEntity also allows us to add headers and HTTP Status codes.
- It can be used in both `@RestController` and `@Controller`.
```java
 @RequestMapping("/handle")
 public ResponseEntity<String> handle() {
   URI location = ...;
   HttpHeaders responseHeaders = new HttpHeaders();
   responseHeaders.setLocation(location);
   responseHeaders.set("MyResponseHeader", "MyValue");
   return new ResponseEntity<String>("Hello World", responseHeaders, HttpStatus.CREATED);
 }
```
</blockquote> 

</details>

---

16. What is Spring Boot?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot is a microservice-based framework and making a production-ready application in it takes very less time.

</blockquote>

</details>

---

17. How does Spring Boot simplify the development of Spring applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot simplifies the development of Spring applications in several ways:

1. **Auto-configuration**: Spring Boot automatically configures various components based on the classpath dependencies and sensible defaults. This eliminates the need for manual configuration and reduces boilerplate code.

2. **Standalone executable JAR**: Spring Boot allows you to package your application as a self-contained, executable JAR file. This makes it easy to deploy and run the application without any additional setup or dependencies.

3. **Embedded server**: Spring Boot includes an embedded server (such as Tomcat, Jetty, or Undertow) which eliminates the need for deploying the application to an external server. This simplifies the deployment process and allows for rapid development and testing.

4. **Dependency management**: Spring Boot provides a robust dependency management system. It automatically manages the versions and dependencies of various libraries and frameworks, ensuring compatibility and reducing conflicts.

5. **Convention over configuration**: Spring Boot follows the principle of "convention over configuration," which means that it provides sensible defaults and configurations based on best practices. This reduces the need for explicit configuration and allows developers to focus on application logic rather than infrastructure setup.

6. **Integrated development experience**: Spring Boot integrates seamlessly with other Spring projects and libraries, providing a cohesive development experience. It offers out-of-the-box support for features like security, data access, caching, and more.

Overall, Spring Boot simplifies the development process by reducing the manual configuration, providing defaults and sensible defaults, and enabling rapid development and deployment. It allows developers to focus on writing business logic and building robust applications without getting bogged down by infrastructure and setup.

</blockquote>

</details>

---

18. How does Spring Boot handle application properties and configuration? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Spring Boot handles application properties and configuration by providing a convention-over-configuration approach. It looks for an `application.properties` or `application.yml` file in the `src/main/resources` directory by default. These files allow you to configure various properties such as server port, database connection details, logging settings, etc.

- Spring Boot also supports externalizing configuration to separate files outside the application's JAR file. It provides options to specify the location of these files and allows overriding properties using command-line arguments.

- Additionally, Spring Boot supports profile-specific configuration, allowing you to define specific configurations for different environments like development, testing, and production. It follows a specific order of precedence to resolve property conflicts and provides flexibility in managing configurations.

- Overall, Spring Boot simplifies application properties and configuration by providing a straightforward and flexible approach, allowing developers to easily customize and manage the behavior of their applications.


</blockquote>

</details>

---

19. What is the purpose of the @SpringBootApplication annotation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The `@SpringBootApplication` annotation is a convenience annotation in Spring Boot that combines multiple annotations to simplify the configuration of a Spring Boot application. It serves three main purposes:

1. `@Configuration`: It indicates that the class is a configuration class that defines beans and other Spring-related configurations.

2. `@EnableAutoConfiguration`: It enables automatic configuration of Spring beans based on classpath and property settings. It leverages Spring Boot's auto-configuration mechanism to automatically configure commonly used dependencies and features based on the dependencies present in the classpath.

3. `@ComponentScan`: It enables component scanning to automatically discover and register Spring beans in the application context. By default, it scans the current package and its sub-packages for components.

By using the `@SpringBootApplication` annotation on the main class of a Spring Boot application, you can configure the application with sensible defaults and enable features like auto-configuration and component scanning without writing a lot of boilerplate code. It provides a streamlined way to bootstrap a Spring Boot application and kickstart the application context.

</blockquote>

</details>

---



20. How does Spring Boot auto-configure various components in an application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 


- Spring Boot auto-configures various components in an application by leveraging classpath scanning, conditional configuration, external configuration, and auto-configured starter dependencies. 
- It scans the classpath for specific components, checks for conditions to enable/disable them, reads configuration properties from various sources, and provides starter dependencies that bring in required configurations. 
- This allows for automatic configuration with sensible defaults, reducing the need for manual configuration.

</blockquote>

</details>

---

21. What is the difference between Spring Boot's embedded container and an external container?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The difference between Spring Boot's embedded container and an external container is that the embedded container is included within the application itself and can be run as a standalone executable, while an external container is a separate server or runtime environment where the application needs to be deployed. 
- The embedded container eliminates the need for separate container setup and configuration, making it more convenient for development and deployment of Spring Boot applications.


</blockquote>

</details>

---

22. How does Spring Boot support the development of RESTful web services?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot provides built-in support for developing RESTful web services by integrating various components and features. It includes:
- **Spring MVC framework:** Spring Boot utilizes the powerful Spring MVC framework to handle HTTP requests and responses, allowing developers to define RESTful endpoints easily.
- **Auto-configuration:** Spring Boot automatically configures many aspects of the application, including the servlet container, message converters, exception handling, and content negotiation, simplifying the setup of RESTful services.
- **Spring Data REST:**Spring Boot integrates with Spring Data REST to automatically expose RESTful endpoints for CRUD operations on data repositories.
- **Embedded server:** Spring Boot includes an embedded server (such as Tomcat, Jetty, or Undertow) that allows developers to run and test RESTful services without the need for a separate server setup.
- **Content negotiation:** Spring Boot supports content negotiation, allowing the API to return different representations of the same resource based on the client's requested media type (JSON, XML, etc.).
- **Error handling:** Spring Boot provides convenient error handling mechanisms, allowing developers to define custom error responses and exception handling strategies for RESTful endpoints.
- **Actuator:** Spring Boot Actuator provides endpoints and monitoring capabilities for managing and monitoring RESTful services, such as health checks, metrics, and tracing.

Overall, Spring Boot's comprehensive support for configuration, auto-configuration, and integration with key Spring components makes it well-suited for developing RESTful web services with minimal boilerplate code and configuration.
</blockquote>

</details>

---

23. How can you package and deploy a Spring Boot application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

TTo package and deploy a Spring Boot application, you can follow these steps:

1. Build the application: Use your build tool (such as Maven or Gradle) to build the Spring Boot application. This will create an executable JAR or WAR file.

2. Configure the application: Set up the necessary configuration properties for your application, such as database connection details, logging settings, and any other required configurations. Spring Boot provides various ways to configure your application, including application.properties or application.yml files, environment variables, and command-line arguments.

3. Package the application: Use the build tool to package the application into a JAR or WAR file. This file will contain all the required dependencies and resources needed to run the application.

4. Deploy the application: Deploy the packaged application to your target environment, such as a server or cloud platform. The deployment process may vary depending on your deployment target. For example, you can deploy the application to a local server, containerize it using Docker, or deploy it to a cloud provider like AWS or Heroku.

5. Start the application: Once the application is deployed, start it using the appropriate command or deployment method. For executable JAR files, you can run the JAR using the `java -jar` command. For WAR files, deploy the WAR file to a servlet container or application server.

6. Verify the deployment: Test the deployed application to ensure it is running correctly. Access the application using the provided URL or endpoint and perform any necessary testing or validation.


</blockquote>

</details>

---

24. How does Spring Boot support database integration?


![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 


Spring Boot provides seamless integration with databases through its auto-configuration and data access features. It supports a wide range of databases, including relational databases like MySQL, PostgreSQL, and Oracle, as well as NoSQL databases like MongoDB and Redis.

To integrate with a database, you can simply add the necessary database driver dependencies to your project's build configuration. Spring Boot will automatically configure the data source based on the available dependencies and provide you with a pre-configured DataSource bean. You can then use this DataSource bean to establish connections and perform database operations using Spring's data access technologies like JDBC, JPA, or Spring Data JPA.

Additionally, Spring Boot provides convenient features for database schema creation, migration, and initialization. It supports various approaches for managing database migrations, such as using Flyway or Liquibase. You can also configure the data source properties, transaction management, and other database-related settings through Spring Boot's configuration options.

</blockquote>

</details>

---

25. What is Spring Boot starter concept and how does it simplify dependency management?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Spring Boot starter concept simplifies dependency management by providing a curated set of dependencies that are commonly used together to support specific features in a Spring Boot application. 
- By including a starter dependency, you get all the necessary libraries and configurations needed for that feature without manually managing individual dependencies. 
- It simplifies the setup process and ensures that all the required components are included automatically.

</blockquote>

</details>

---

26. How does Spring Boot handle logging and exception handling?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Spring Boot provides built-in support for logging and exception handling. It uses the common logging abstractions provided by SLF4J (Simple Logging Facade for Java) and allows you to configure logging through various properties. You can easily change the logging implementation or customize the logging behavior by adding dependencies and modifying configuration files.

- For exception handling, Spring Boot offers a default error handling mechanism that returns standard error responses for different types of exceptions. You can also customize the error handling by creating custom exception handlers or by using the `@ControllerAdvice` annotation to handle exceptions globally.

- Overall, Spring Boot simplifies logging and exception handling by providing defaults and conventions while allowing flexibility for customization when needed.

</blockquote>

</details>

---

27. What files would you use to configure Spring Boot applications?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In a Spring Boot application, you can use the following files to configure the application:

1. application.properties: This is a properties file where you can define key-value pairs to configure various aspects of the application.

2. application.yml: This is a YAML file that provides a more structured and human-readable format for configuration.

3. bootstrap.properties or bootstrap.yml: These files are used for configuring the Spring Boot bootstrap process.

4. application-{profile}.properties or application-{profile}.yml: These files allow profile-specific configuration.

5. logback.xml or log4j2.xml: These XML configuration files are used for configuring the logging framework.

These files can be used to configure properties such as server settings, database connections, logging levels, and more.

</blockquote>

</details>

---

28. How is Spring Boot different from legacy Spring applications?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot is different from legacy Spring applications in the following ways:

1. Convention over Configuration: Spring Boot follows the principle of "convention over configuration" where it provides sensible defaults and auto-configurations based on common use cases. This reduces the need for explicit configuration and boilerplate code.

2. Embedded Server: Spring Boot includes an embedded server (such as Tomcat, Jetty, or Undertow) by default, eliminating the need for separate server deployment and configuration.

3. Simplified Dependency Management: Spring Boot provides a powerful dependency management system that automatically resolves and manages dependencies, making it easier to manage and update libraries.

4. Auto-Configuration: Spring Boot auto-configures many components and frameworks based on the classpath and the application's dependencies. This eliminates the need for manual configuration and reduces the amount of code developers need to write.

5. Production-Ready Features: Spring Boot provides a range of features to support production-ready applications, such as health checks, metrics, and externalized configuration. These features make it easier to monitor, manage, and deploy applications in production environments.


</blockquote>

</details>

---


29. What is Spring Boot's support for caching? Explain how caching can be implemented in a Spring Boot application.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot provides built-in support for caching through integration with popular caching libraries such as Ehcache, Caffeine, and Redis. Caching can be implemented in a Spring Boot application by following these steps:

1. Include the caching dependency: Add the caching dependency to your project's build configuration (e.g., Maven or Gradle).

2. Enable caching: Annotate your Spring Boot application's main class with `@EnableCaching` to enable caching support.

3. Configure caching: Configure the caching behavior by creating a caching configuration class or using the built-in caching properties in `application.properties` or `application.yml` file. You can specify caching strategies, eviction policies, and other caching-related settings.

4. Annotate methods for caching: Use caching annotations such as `@Cacheable`, `@CachePut`, and `@CacheEvict` to define caching behavior for specific methods. These annotations allow you to cache method results, update cached values, or evict cache entries.

5. Specify cache names: Assign cache names to methods using the `value` or `cacheNames` attribute of the caching annotations. This allows you to organize cached data into different caches and apply different caching settings for each cache.

6. Configure cache storage: If using a specific caching library like Redis, configure the connection details and other cache-specific settings in the application's configuration file.


</blockquote>

</details>

---

30. What is the role of Spring Boot DevTools, and how does it improve the development experience?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Spring Boot DevTools is a module provided by Spring Boot that enhances the development experience by providing a set of tools and features. Some of its key roles and benefits include:

1. Automatic application restart: DevTools monitors classpath changes and automatically restarts the application whenever a change is detected. This eliminates the need for manual application restarts during development, saving time and improving productivity.

2. Live code reloading: DevTools enables live reloading of static resources, templates, and even Java classes. Changes made to these resources are immediately reflected in the running application without requiring a restart. This allows developers to see the effects of their code changes in real-time, making the development process faster and more efficient.

3. Enhanced error reporting: DevTools provides more detailed and accurate error messages during development. It captures and displays stack traces with source code snippets, making it easier to identify and debug issues quickly.

4. Developer-friendly defaults: DevTools configures the development environment with sensible defaults that optimize the development workflow. For example, it disables template caching, enables verbose logging, and configures automatic browser refreshing for Thymeleaf templates.

5. Additional development utilities: DevTools offers additional utilities like remote debugging support, property overrides, and environment-specific configuration files. These utilities help developers fine-tune their applications and streamline the development process.



</blockquote>

</details>

---

31.List the annotations that you use for Spring Boot application with its purpose?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In a Spring Boot application, the primary annotation you would use is `@SpringBootApplication`. This annotation is a combination of three annotations: `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`. It is typically applied to the main class of the application to indicate that it is a Spring Boot application.

Additionally, there are other annotations commonly used in Spring Boot applications, depending on the specific functionality you are implementing:

- `@RestController`: Used to annotate classes that handle RESTful requests and responses. It combines the `@Controller` and `@ResponseBody` annotations.
- `@Service`: Used to annotate classes that represent the service layer of the application.
- `@Repository`: Used to annotate classes that implement the data access layer, typically interacting with the database or other external data sources.
- `@Configuration`: Used to indicate that a class provides bean definitions and other configuration for the application context.
- `@Component`: Used to indicate that a class is a candidate for auto-detection as a Spring bean.

</blockquote>

</details>

---

32. What default connection pool does spring boot use?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Boot` uses `HikariCP` as the default connection pool.
- `HikariCP` has great performance and concurrency.

</blockquote> 

</details>

---

33. What connection pool does spring boot supports?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Boot supports various popular connection pool providers as listed below:
    - `HikariCP`
    - `Tomcat pooling Datasource`
    - `Commons DBCP2`
    - `Oracle UCP & OracleDataSource`
    - `Spring Framework’s SimpleDriverDataSource`
    - `H2 JdbcDataSource`
    - `PostgreSQL PGSimpleDataSource`
    - `C3P0`

</blockquote> 

</details>

---