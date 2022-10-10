## Technical

1. How you decide whether to choose either Spring or Spring Boot framework for application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Its simple, any console/desktop or web application that want to leverage DI & other key features provided by Core Spring modules can use Spring framework.
- Spring Boot framework was evolved on the top of Spring framework. to support microservices based architecture on cloud.
- Spring Boot framework is popularly used to develop Web/Enterprise Application, RESTful API & Microservices.
</blockquote>

</details>

---
2. Why we need `Service layer`? Can’t we call `Repository layer` directly inside `Controller layer`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- There is no restriction from compiler we can call Repository layer from Controller layer directly.
- The layering helps to segregate the Spring application responsibilities and enabling loose coupling between the objects.
- Service layer in application facilitates communication between the Controller and the Persistence/Repository/DAO layer.
- Service layer usually hold business logic e.g. It may include validation logic.
- One Service layer may depend on multiple Repository layers to serve specific business purpose.
- The method names in Service layer usually named as per business purpose they serve whereas method names in Repository are named as standard CRUD operations supported by that Repository.
- Hence we need Service layer between DAO and Controller layer.
</blockquote> 

</details>

---
3. Is it safe to keep the DB & other critical passwords directly inside property file(s)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Since property file(s) are readable by anyone who has access to codebase it is highly recommended not to keep the DB and other critical credentilas inside property file(s).
- They are usually stored inside cloud environment variables or passed through command line arguments while executing the application.
```
mvn spring-boot:run -Dspring-boot.run.jvmArguments='
-Dspring.datasource.url=jdbc:postgresql://localhost:5432/mydb 
-Dspring.datasource.username=admin 
-Dspring.datasource.password=gd123'
````
</blockquote> 

</details>

---
4. As a developer you need to check your production application status daily, how Spring Boot can help here?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- One of the routine taks for a developer is to check the status of already launched production application on periodic basis.
- To simplify this task Spring Boot provided sub-project named Spring Boot Actuator.
- Spring Actuator exposes operational information about the executing application this include- health, metrics, info, dump, env, etc. 
- The information is accessed usually via HTTP endpoints, few of which listed below:
    - `/health` summarizes the health status of our application.
    - `/beans` returns all available beans in our BeanFactory.
    - `/env` returns the current environment properties. 
- To enable Spring Boot Actuator, we just need to add the spring-boot-actuator dependency to our maven package manager.

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
- In order to access the actuator endpoints using HTTP, we need to both enable and expose them.
- Only the /health and /info endpoints are exposed by default.
- We need to add the following configuration to expose all endpoints: 
`management.endpoints.web.exposure.include=*`

</blockquote> 
</details>

---
5. What is Spring profile and why we use it?

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
- You can specify the property in any of the usual ways, for example you could include it in your application.properties:
`spring.profiles.active=test`
or specify on the command line using the switch `--spring.profiles.active=prod`.
</blockquote> 

</details>

---
6. How can you define multiple profiles in Spring Boot application? How to add active profile?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The application development process undergoes different stages; the typical ones are development, testing, and production. 
- Spring Boot profiles helps group parts of the application configuration and make it be available only in certain environments.
- A profile is a set of configuration settings. 
- Spring Boot allows to define profile specific property files in the form of `application-{profile}.properties`.
- We can define both profile specific and default application.properties file in application. (For example, if your application activates a profile named prod and uses YAML files, then both application.yml and application-prod.yml will be considered).
- The local/default profile (`application.properties`) is usually called `default`; all the beans that do not have a profile set belong to `default` profile.
- Spring automatically loads the properties in an application.properties file for all profiles, and the ones in profile-specific property files only for the specified profile. 
- The keys in the profile-specific property override the ones in the default property file.
- There are plenty of ways of defining active profiles in Spring Boot, including command line arguments, Maven settings, JVM system parameters, environment variables, spring.profiles.active property, and SpringApplication methods.
- We commanly set active profile using `spring.profiles.active` property or command line argument.
- For Example, we have three profiles(`local/default`, `dev`, `prod`) and two profile-specific property files as belows:
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
7. What happens when two profiles are set for property `spring.profiles.active` in Spring application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- If several profiles are specified, a last-wins strategy applies. 
- For example, if profiles prod,live are specified by the spring.profiles.active property (i.e. `spring.profiles.active=prod,live`), values in `application-prod.properties` can be overridden by those in `application-live.properties`.
</blockquote> 

</details>

---
8. Which `pom.xml` file inside Spring Boot framework defines versions of all preconfigured dependencies?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Boot framework has utilised the concept of parent and child pom file inheritance and defined all the dependencies specific to its release version under `spring-boot-dependencies` module.
- For example refer this link: https://repo1.maven.org/maven2/org/springframework/boot/spring-boot-dependencies/2.7.3/spring-boot-dependencies-2.7.3.pom

</blockquote> 

</details>

---
9. What is Bean Validation API? How we can use it in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- To restrict the input provided by the user in Spring MVC applications, the Spring >=4 supports and use `Bean Validation API`.
- The Bean Validation API is a Java specification which is used to apply constraints to the fields of a class via annotations. 
- Using Bean Validation API we can validate a length, number, regular expression, etc. as well as we can build custom validations.
- `Hibernate Validator` is most famous/used implementation of of the Bean Validation API sepcification.
- There are 3 types of variables that can be validated using Bean Validation API:
  - The request body,
  - Variables within the path (e.g. id in /api/{id}) and,
  - Query parameters.
- Spring Boot comes with the validation starter, which need to be included in `pom.xml` file which intern added `hibernate-validator` dependency as below:

```xml
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
  </dependency>
```

</blockquote> 

</details>

---
10. Explain few `hibernate-validator` Spring bean validation annotations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Few common validation annotations are listed below:
  - `@NotNull`: Field must not be null.
  - `@NotEmpty`: List field must not be empty.
  - `@NotBlank`: String field must not be the empty String (i.e. it must have at least one Character).
  - `@Min` and `@Max`: Numerical field is only valid when it’s value is above or below a certain value.
  - `@Pattern`: String field is only valid when it matches a certain regular expression.
  - `@Email`: String field must be a valid email address.
</blockquote> 

</details>

---
11. What does the `@Valid` annotation indicate in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `@Valid` annotation can be added to variables in a `RestController` mapping method to validate them. 
- In below code our POST request takes in a request body, and we're mapping that request body to a class InputForm.
- The `@Valid` annotation will tell Spring to go and validate the data passed into the controller i.e age is between 18 and 60 inclusive because of those Bean Validation API annotations (min and max).
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

12. What is use of `@ControllerAdvice` in Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@ControllerAdvice` is a specialization of the `@Component` annotation which allows to handle exceptions across the whole application in one global handling component.
- It basiclly intercepts exceptions thrown by methods annotated with `@RequestMapping` and similar.
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

13. What is use of `@ExceptionHandler` in Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `@ExceptionHandler` is an annotation used to handle a specific exception in controller and send custom response to the client.
- We need to have a method annotated with @ExceptionHandler which takes Exception Class (any exception which you want to handle) as argument, if any of these exception is raised in the controller, then this handler method will handle it.
- If we have two handler method in same controller say for example one handler for Exception and another handler for RuntimeException, then the handler method which is closer to Exception Class hirarchy is triggered. 
- For example,if NullPointerException is thrown then IOException handler method is triggered, which is the closest to the Exception class.
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
</cblockquote> 

</details>

---
14. Have you use HAL browser in Spring? How to use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- HAL stands for Hypertext Application Language.
- HAL is a simple format that gives a consistent and easy way to hyperlink between resources in your API.
- Adopting HAL make API explorable, and its documentation easily discoverable from within the API itself. 
- In short, it make API easier to work with and therefore more attractive to client developers.
- The HAL browser provides an in-browser GUI to traverse your Spring RESTful API.
- Below is the single dependency needed to integrate the HAL browser into our REST API. 

```xml
  <dependency>
	  <groupId>org.springframework.data</groupId>
	  <artifactId>spring-data-rest-hal-explorer</artifactId>
  </dependency>
```
- As long as we have above dependency, Spring will auto-configure the HAL browser, and make it available via the default endpoint.
- All we need to do now is press run and switch to the browser. The HAL browser will then be available on http://localhost:8080/
</blockquote> 

</details>

---
15. What is use of `ResponseEntity` class in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `ResponseEntity` represents an HTTP response, including headers, body, and status. 
- While `@ResponseBody` puts the return value into the body of the response, ResponseEntity also allows us to add headers and Http Status code.
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

16. What is Spring Boot ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Boot is a microservice-based framework and making a production-ready application in it takes very less time.

</blockquote>

</details>

---

17. What is the use of `@RestController`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`@RestController` is a convenience annotation for creating Restful controllers. It is a specialization of @Component and is autodetected through classpath scanning. It adds the @Controller and @ResponseBody annotations. It converts the response to JSON or XML.

</blockquote>

</details>

---

