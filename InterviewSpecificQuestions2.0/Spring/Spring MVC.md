## Technical

1. What is DispatcherServlet in the Spring MVC application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In the case of Spring MVC, DispatcherServlet is the front controller. 
- DispatcherServlet acts as an entry and exit point for any request received by the rom client. 
</blockquote> 

</details>

---

2. How DispatcherServlet handle requests &responses in the Spring MVC application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Whenever a request comes it first goes to the DispatcherServlet where it then tries to identify its handler method (the methods defined in the specific controller to handle the requests) using Handler mapping.
- Once the handler mapping returns the controller the DispatcherServlet knows the controller which can handle the request and goes there for further request processing.
- Once the controller returns the view the DispatcherServlet goes to the view resolver to identify where the view is located.
- DispatcherServlet then grabs the view and returns as the final l response.
</blockquote> 

</details>

---

3. How is the Spring MVC DispatcherServlet registered in the web.xml file?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Since DispatcherServlet is one type of Servlet the web.xml file configuration is the same as normal servlet.
- Additionally, as DispatcherServlet is our front controller we need to ensure that all the incoming requests should be routed to it using "/" url pattern.
```xml
<servlet>
    <servlet-name>dispatcher</servlet-name>
    <servlet-class>
        org.springframework.web.servlet.DispatcherServlet
    </servlet-class>
</servlet>
<servlet-mapping>
    <servlet-name>dispatcher</servlet-name>
    <url-pattern>/</url-pattern>
</servlet-mapping>
```
- If we are using `the spring-boot-starter-web` starter, DispatcherServletauto-configured to the URL pattern "/". So, we don't need to do any additional configuration in the web.xml file. 

</blockquote> 

</details>

---
4. How to change the default context path URL pattern of DispatcherServlet in Spring MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- It's very simple, we need to change two properties inside the application.properties file.
```
server.servlet.context-path=/admin
spring.mvc.servlet.path=/v2
```
- With the above customizations, DispatcherServlet is configured to handle the URL pattern /v2 and the rcontext Path will be /admin. 
- Thus, DispatcherServlet listens at http://localhost:8080/admin/v2/.


</blockquote> 

</details>

---

5. Can we have a `@RestController` class with multiple `@GetMapping` methods? Justify your Answer.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Yes, we can have one `@RestController` class with multiple `@GetMapping` methods.
- Defining not only Get but any HTTP method-compliant mappings purely depend on the context of the application and its use cases.
- Below three GetMappings can be defined inside one UserRestController.
```java
@RestController
public class UserRestController{
    @GetMapping(path="/users/")
    public ResponseEntity<UserInfoDTO> getUserByUsername(@RequestParam String username) {
    }
    // GET user details by username: <protocol>://<hostUrl>/users?username=<username>

    @GetMapping(path="/users")
    public ResponseEntity<List<UserInfoDTO>> getAllUsers() {
    }
    // GET all user details: <protocol>://<hostUrl>/users

    @GetMapping(path="/users/{id}")
    public ResponseEntity<UserInfoDTO> getUserById(@PathVariable Long id)
    // GET user details for specific userid: <protocol>://<hostUrl>/users/<userid>
}
```
</blockquote> 

</details>

---
6. How can you configure Spring MVC to handle both "/" and "/welcome" request mappings to land on the "index" view?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@RequestMapping` annotation in Spring MVC has a String[] value parameter, so we can specify multiple values like the below to return the index view of the rom controller class as below:
```java
@RequestMapping(value={"/", "welcome"})
public String homePage(){
  return "index";
}
```
</blockquote> 

</details>

---
7. How does the @Controller annotation work in both Spring MVC and RESTful applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The @Controller annotation in Spring is used to mark a class as a controller component. In Spring MVC applications, the @Controller annotation is used to handle requests and generate responses based on the MVC pattern. It is typically used to handle user interactions, perform business logic, and return views or templates.

- In RESTful applications, the @Controller annotation can also be used to handle requests and generate responses, but with a different approach. Instead of returning views or templates, the @Controller methods in RESTful applications typically return data in a format such as JSON or XML. The response is usually based on the requested resource or the requested operation (GET, POST, PUT, DELETE, etc.).

- In both Spring MVC and RESTful applications, the @Controller annotation provides a convenient way to define request-handling components and map them to specific URLs. However, the specific behavior and response type can vary depending on the application context.

</blockquote> 

</details>

---
8. What does @Controller & @RestController returns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- @Controller returns a view in the Spring MVC application.
- @RestController returns an object as a response instead of a view.

</blockquote> 

</details>

---
9. What is the use of @ResponseBody in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- @ResponseBody is a Spring annotation which binds a method return value to the web response body. 
- It is not interpreted as a view name. 
- It uses `org.springframework.http.converter Interface HttpMessageConverter<T>` to convert the return value to the HTTP response body, based on the content type in the request HTTP header.
</blockquote> 

</details>

---

10. What is the use of `@RequestBody` in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@RequestBody` annotation request body to method parameters. 
- We use the `@RequestBody` annotation to have the request body read and deserialized into an Object through an `HttpMessageConverter`. 
- Additionally, automatic validations can be applied by annotating the argument with @Valid annotation.
</blockquote> 

</details>

---
11. What is Content Negotiation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Content negotiation is the process of selecting one of the multiple possible representations to return to a client, based on client or server preferences.
- When a consumer sends a request, it can specify two HTTP Headers related to Content Negotiation `Accept` and `Content-Type`.
- `Content-Type` indicates the content type of the body of the request.
- `Accept` indicates the expected content type of the response.

</blockquote> 

</details>

---

12. What does “representation", "state" and "transfer" mean in Representational State Transfer (REST)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- To understand REST let us first understand the-    
  - What is a `resource`- 
    - The key abstraction of information in REST is a resource. 
    - There is no restriction on what a resource can be. 
    - Any information that can be named can be a resource: a document or image, a temporal service (e.g., "today's weather in Los Angeles"), a collection of other resources, a non-virtual object (e.g., a person), and so on.
  - What is a `representation`-
    - A JSON document can be used to represent the state of a particular resource. A resource can have many representations, such as JSON and/or XML documents, and the client can use content negotiation to request different representations of the same resource.
  - What is a `state transfer`-
    - The state of a given resource can be retrieved and manipulated using representations.


</blockquote> 

</details>

---
13. What is REST API versioning? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- API versioning is the process of transparently managing changes to your API.
- Versioning aims at effective communication around changes to API, so consumers/subscribers know what to expect from it. 
</blockquote> 

</details>

---
14. How do we provide a version to RESTful APIs in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- APIs only need to be up-versioned when a breaking change is made. Breaking changes include:
  - Change in the format of the response data for one or more calls
  - Change in the request or response type (i.e., changing an integer to a float)
  - Removing any part of the API.
- There are multiple ways to version RESTful API-
  - One controller class with multiple methods having separate versions for mapping URLs.
  - One controller class with one method having separate versions number passed as path variables.
  - One controller class with one method having separate versions number passed as a custom request header.
  - Multiple controller classes marked with version names with their method names. 
- Breaking changes should always result in a change to the major version number for an API or content response type.
- Non-breaking changes, such as adding new endpoints or new response parameters, do not require a change to the major version number.
- Example of using two controller classes serving different versions-
```java
@RestController
@RequestMapping("/api/v1")
public class ControllerV1 {
  //...
}

@RestController
@RequestMapping("/api/v2")
public class ControllerV2 {
  //...
}
```
</blockquote> 

</details>

---
15. Which object is used as a base context in the Spring MVC application? Why?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `WebApplicationContext` object is used as the base object in the Spring MVC application.
- WebApplictionContext is an extension of ApplicationContext `public interface WebApplicationContext extends ApplicationContext`.
- WebApplicationContext is a web-aware ApplicationContext i.e., it has Servlet Context information. 
- In one web application, there can be multiple WebApplicationContext. 
- In one web application, there can be multiple DispatcherServlet, one for handling request and returns view whereas another which handle REST request & responses. 
- Each DispatcherServlet is associated with a single WebApplicationContext. 
- The WebApplicationContext configuration file `*-servlet.xml` is specific to the DispatcherServlet and a web application can have more than one DispatcherServlet configured to handle the requests and each DispatcherServlet would have a separate `*-servlet.xml` file to configure.
</blockquote> 

</details>

---
16. What is the difference between `applicationContext.xml` and `*-servlet.xml` in Spring Framework?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `applicationContext.xml` defines the beans that are shared among all the servlets. 
- If our application has more than one servlet, then defining the common resources in the `applicationContext.xml` would make more sense.
- `*-servlet.xml` defines the beans that are related only to specific DispatcherServlet. 
- All our Spring MVC controllers are defined in this file.
- There is nothing wrong in defining all the beans in the `*-servlet.xml` if we are running only one DispatcherServlet in our web application.
</blockquote> 

</details>

---

17. How are the HTTP requests are processed in the Spring MVC architecture?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- It all starts with the client, which sends a request to a specific URL.
-  When that request hits the web container like Tomcat it looks into web. xml and finds the Servlet or Filter which is mapped to that particular URL.
-  It the delegate that Servlet or Filter to process the request.


</blockquote> 

</details>

---

18. How would you declare which HTTP requests you would like a controller to process?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
In Spring MVC, you can declare which HTTP requests a controller should process by using the appropriate mapping annotations. Here are some common annotations used to specify the supported HTTP methods and request paths for a controller:

1. @RequestMapping: This annotation is used to map the controller methods to specific request paths. You can specify the path value as a string or use various attributes like `value`, `method`, `params`, `headers`, etc., to further refine the mapping. For example:
   ```java
   @RequestMapping(value = "/users", method = RequestMethod.GET)
   public String getUsers() {
       // Controller logic
   }
   ```

2. @GetMapping, @PostMapping, @PutMapping, @DeleteMapping: These annotations are shortcuts for mapping specific HTTP methods. They are alternative options to @RequestMapping with the `method` attribute set to the corresponding HTTP method. For example:
   ```java
   @GetMapping("/users")
   public String getUsers() {
       // Controller logic
   }
   ```

3. @RequestMapping with method-specific variants: Starting from Spring 4.3, you can use the method-specific variants of the @RequestMapping annotation for each supported HTTP method. For example:
   ```java
   @GetMapping("/users")
   public String getUsers() {
       // Controller logic
   }
   ```

4. @RequestMapping with multiple mappings: You can specify multiple request paths for a single controller method using an array of strings. The controller method will be invoked for any of the specified paths. For example:
   ```java
   @RequestMapping(value = {"/users", "/customers"}, method = RequestMethod.GET)
   public String getUsers() {
       // Controller logic
   }
   ```

By using these mapping annotations, you can precisely define which HTTP requests should be handled by specific methods in your controller. This allows for fine-grained control over request handling and enables you to build RESTful APIs or handle different types of requests in your application.

</blockquote> 

</details>

---

19. How would you specify HTTP status codes to return from your controller?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
In Spring MVC, you can specify the HTTP status codes to return from your controller methods using the `ResponseEntity` class or the `@ResponseStatus` annotation.

1. ResponseEntity: The `ResponseEntity` class allows you to customize the HTTP response, including the status code, headers, and response body. You can create a `ResponseEntity` object and return it from your controller method. For example:
   ```java
   @GetMapping("/users/{id}")
   public ResponseEntity<User> getUser(@PathVariable Long id) {
       User user = userService.getUserById(id);
       if (user != null) {
           return ResponseEntity.ok(user);  // 200 OK status code
       } else {
           return ResponseEntity.notFound().build();  // 404 Not Found status code
       }
   }
   ```

2. @ResponseStatus: The `@ResponseStatus` annotation is used to declare the default HTTP status code for a controller method. You can annotate the method with `@ResponseStatus` and specify the desired status code as an argument. For example:
   ```java
   @GetMapping("/users")
   @ResponseStatus(HttpStatus.OK)  // 200 OK status code
   public List<User> getUsers() {
       // Controller logic
   }
   ```

By using either `ResponseEntity` or `@ResponseStatus`, you can explicitly set the desired HTTP status code to return from your controller methods. This allows you to provide meaningful responses to clients and control the behavior of your application based on different scenarios or conditions.

</blockquote> 

</details>

---

20. What is the difference between @RequestMapping and @GetMapping?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
The `@RequestMapping` and `@GetMapping` annotations are used in Spring MVC to map HTTP requests to controller methods. The main difference between them lies in the specificity of the mapping they provide.

1. @RequestMapping: The `@RequestMapping` annotation is a versatile annotation that can be used to map HTTP requests to controller methods. It allows you to specify various attributes such as the HTTP method, request URL, request parameters, headers, and more. You can use `@RequestMapping` with a specific HTTP method (e.g., `RequestMethod.GET`, `RequestMethod.POST`) or without specifying a method to handle all HTTP methods. For example:
   ```java
   @RequestMapping(value = "/users/{id}", method = RequestMethod.GET)
   public User getUser(@PathVariable Long id) {
       // Controller logic
   }
   ```

2. @GetMapping: The `@GetMapping` annotation is a specialized form of `@RequestMapping` that is specifically used for handling HTTP GET requests. It is a shortcut for mapping HTTP GET requests and provides a more concise syntax. When you use `@GetMapping`, you don't need to explicitly specify the HTTP method as it is implied to be `RequestMethod.GET`. For example:
   ```java
   @GetMapping("/users/{id}")
   public User getUser(@PathVariable Long id) {
       // Controller logic
   }
   ```

In summary, `@RequestMapping` is a general-purpose annotation that can handle requests for any HTTP method, while `@GetMapping` is a specific annotation for handling HTTP GET requests. `@GetMapping` provides a more concise syntax and is commonly used when you only need to handle GET requests in your controller methods.

</blockquote> 

</details>

---

21. What is the purpose of using ViewResolver?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- A ViewResolver in Spring MVC is responsible for resolving the logical view name returned by a controller into an actual view implementation that will be used to render the response. 
- It helps in determining the specific view technology and template to be used for rendering the response based on the logical view name provided by the controller.

</blockquote> 

</details>

---

22. What are the advantages of using RestTemplate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
RestTemplate provides several advantages for making HTTP requests in a Spring application:

1. Simplified API: RestTemplate offers a straightforward and easy-to-use API for making HTTP requests, abstracting away the complexities of working directly with the HTTP protocol.

2. Versatility: RestTemplate supports various HTTP methods (GET, POST, PUT, DELETE, etc.) and allows customization of headers, query parameters, and request/response bodies.

3. Integration with Spring: RestTemplate integrates seamlessly with other Spring features like dependency injection, allowing for easy configuration and usage within a Spring application.

4. Request and response handling: RestTemplate handles serialization and deserialization of request and response bodies in different formats (e.g., JSON, XML) automatically.

5. Error handling: RestTemplate provides built-in error handling mechanisms, allowing for handling of different HTTP status codes and exceptions in a standardized way.

6. Extensibility: RestTemplate can be extended and customized to fit specific requirements by configuring interceptors, message converters, and error handlers.

7. Integration with third-party libraries: RestTemplate can be easily integrated with other third-party libraries, enabling seamless communication with external services.


</blockquote> 

</details>

---

23. How would you extract query and path parameters from a request URL in your controller?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    In a Spring MVC controller, you can extract query and path parameters from a request URL using the `@RequestParam` and `@PathVariable` annotations, respectively.

1. Query Parameters:
   - Use the `@RequestParam` annotation to extract query parameters from the request URL.
   - Specify the parameter name in the annotation's value attribute.
   - Optional: Use the `required` attribute to specify if the parameter is mandatory or not.
   - Example: `@RequestParam("paramName") String paramValue`

2. Path Parameters:
   - Use the `@PathVariable` annotation to extract path parameters from the request URL.
   - Specify the parameter name in the annotation's value attribute.
   - Example: `@PathVariable("paramName") String paramValue`

Here's an example of a controller method that extracts both query and path parameters:

```java
@Controller
@RequestMapping("/example")
public class ExampleController {

    @GetMapping("/path/{id}")
    public String handleRequest(@PathVariable("id") String id, @RequestParam("param") String param) {
        // Process the extracted path and query parameters
        // ...
        return "result";
    }
}
```

In the above example, the `id` path parameter is extracted using `@PathVariable`, and the `param` query parameter is extracted using `@RequestParam`. The extracted values can then be used within the controller method for further processing.

</blockquote> 

</details>

---

24.  How would you relate Spring MVC Framework to MVC architecture?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Spring MVC Framework is a web framework that follows the MVC (Model-View-Controller) architectural pattern. It provides a structured approach to building web applications by separating the application into three main components:

1. Model: The model represents the data and business logic of the application. It encapsulates the application's data and provides methods to access and manipulate that data.

2. View: The view is responsible for rendering the user interface and presenting the data to the user. It defines how the data from the model should be displayed.

3. Controller: The controller acts as an intermediary between the model and the view. It receives user requests, processes them, interacts with the model to retrieve or update data, and determines which view should be used to render the response.

The Spring MVC Framework provides the necessary infrastructure to support the MVC architecture. It handles the routing of incoming requests, maps them to appropriate controller methods, and manages the flow of data between the model, view, and controller.

By using the Spring MVC Framework, developers can easily implement the MVC pattern and benefit from the separation of concerns, modularity, and maintainability that it offers.

</blockquote> 

</details>

---

25. How is the right View chosen when it comes to the rendering phase?  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the Spring MVC framework, the right view is chosen during the rendering phase based on the configuration and the logical view name returned by the controller. The process involves the following steps:

1. The controller method processing the request returns a logical view name as a String. This logical view name represents the view that should be rendered for the response.

2. The logical view name is then resolved by a ViewResolver. The ViewResolver is responsible for mapping the logical view name to an actual view implementation.

3. The ViewResolver performs the necessary lookup and resolves the logical view name to an instance of the View interface.

4. Once the view is resolved, the rendering phase begins. The view is responsible for rendering the model data and generating the final response to be sent back to the client.

The selection of the right view depends on the ViewResolver implementation and the configuration in the Spring MVC application. Multiple ViewResolver implementations can be configured, each with its own strategy for resolving the logical view name.

By configuring different ViewResolver implementations or customizing the existing ones, developers can control the view resolution process and choose the appropriate view based on factors such as the requested media type, device type, or any other custom logic.

Overall, the Spring MVC framework provides flexibility in choosing the right view for rendering, allowing developers to customize the view resolution process to suit their specific application requirements.

</blockquote> 

</details>

---

26. Differentiate  between @RequestParam and @PathVariable? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The main difference between `@RequestParam` and `@PathVariable` in Spring MVC is how they extract data from the request.

- `@RequestParam` is used to extract query parameters or form data from the request URL. It allows you to specify the name of the parameter and whether it is required or optional. For example, `@RequestParam("id")` extracts the value of the "id" parameter from the request.

- `@PathVariable` is used to extract path variables from the request URL. It allows you to specify a placeholder in the request mapping URL and map it to a method parameter. For example, `@PathVariable("id")` extracts the value of the "id" variable from the URL pattern.

In summary, `@RequestParam` is used for query parameters or form data, while `@PathVariable` is used for extracting path variables from the request URL.

</blockquote> 

</details>

---

27. What is the difference between @Controller and @RestController annotations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
The main difference between the `@Controller` and `@RestController` annotations in Spring MVC is in the way the response is handled.

1. `@Controller`: This annotation is used to mark a class as a Spring MVC controller. It is typically used in traditional web applications where the controller's methods return a view name or a `ModelAndView` object. The returned value is processed by a view resolver to generate the final HTML response.

2. `@RestController`: This annotation is a specialized version of `@Controller` that is used for building RESTful web services. It combines the functionality of `@Controller` and `@ResponseBody`. When a method in a `@RestController` class is invoked, the return value is automatically serialized to JSON or XML (based on the `Accept` header) and sent back as the response body. This eliminates the need for explicit conversion of the response object to JSON or XML.

In summary, `@Controller` is used for traditional web applications where the response is typically a view, while `@RestController` is used for building RESTful web services where the response is serialized directly to JSON or XML.

</blockquote> 

</details>

---

28. How do you handle form submissions in Spring MVC?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring MVC, form submissions can be handled using the `@RequestMapping` annotation and the `ModelAttribute` annotation.

Here are the steps to handle form submissions in Spring MVC:

1. Create a form in your HTML view with input fields corresponding to the properties of your model object.
2. In your Spring MVC controller, create a method that maps to the form submission URL using the `@RequestMapping` annotation.
3. Add the `@ModelAttribute` annotation to a method parameter to bind the form data to a model object. This annotation binds the form fields to the corresponding properties of the model object.
4. Perform any necessary processing or validation on the form data.
5. Return a view name or a `ModelAndView` object to render the result of the form submission.

Here's an example:

```java
@Controller
public class MyController {

    @RequestMapping("/submitForm")
    public String handleFormSubmission(@ModelAttribute("myForm") MyFormModel formModel) {
        // Process the form data
        // Perform validation, business logic, etc.
        
        // Return the view name to render the result
        return "resultPage";
    }
}
```

In this example, the `handleFormSubmission` method maps to the URL "/submitForm". The `@ModelAttribute` annotation binds the form data to the `MyFormModel` object. After processing the form data, the method returns the view name "resultPage" to render the result.

Note that you need to have the necessary dependencies and configuration in your Spring MVC application for form handling, such as the `BindingResult` object for handling form validation errors.

</blockquote> 

</details>

---

29. What is the use of @ModelAttribute annotation in Spring MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The `@ModelAttribute` annotation in Spring MVC is used to bind method parameters or method return values to model attributes. It is primarily used for data binding and pre-population of model attributes in the controller. It helps in simplifying the data transfer between the controller and the view, reducing the boilerplate code required for data binding.

</blockquote> 

</details>

---

30. Explain the concept of RESTful web services in Spring MVC.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- RESTful web services in Spring MVC are a way to build web services that follow the principles of REST (Representational State Transfer).
-  They use standard HTTP methods (GET, POST, PUT, DELETE) to perform operations on resources. In Spring MVC, RESTful web services are implemented using the `@RestController` annotation, which combines the functionality of `@Controller` and `@ResponseBody`. 
- It allows developers to map URL patterns to controller methods, handle different HTTP methods, and return responses in different formats (such as JSON or XML).
- RESTful web services in Spring MVC promote statelessness, scalability, and simplicity in designing and implementing web services.

</blockquote> 

</details>

---

31. How do you configure view resolution in Spring MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To configure view resolution in Spring MVC, you can use the `ViewResolver` interface. The `ViewResolver` is responsible for resolving logical view names to actual view implementations.

In Spring MVC, you typically configure a `ViewResolver` bean in your application context configuration file. There are different implementations of `ViewResolver` available in Spring MVC, such as `InternalResourceViewResolver`, `UrlBasedViewResolver`, or `ThymeleafViewResolver`, depending on the view technology you are using.

Here is a simple example of configuring an `InternalResourceViewResolver` in Spring MVC XML configuration:

```xml
<bean id="viewResolver" class="org.springframework.web.servlet.view.InternalResourceViewResolver">
    <property name="prefix" value="/WEB-INF/views/" />
    <property name="suffix" value=".jsp" />
</bean>
```

In this example, the `InternalResourceViewResolver` is configured with a prefix and suffix. The prefix specifies the common prefix for all view names, and the suffix specifies the file extension of the view files. The logical view names will be resolved to JSP files located in the `/WEB-INF/views/` directory.

You can customize the `ViewResolver` configuration based on your specific needs and the view technology you are using.

</blockquote> 

</details>

---

32. What is the role of a HandlerInterceptor in Spring MVC?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The role of a HandlerInterceptor in Spring MVC is to intercept and modify the request and response at various stages of the request processing lifecycle. It allows you to add pre-processing and post-processing logic around the execution of a controller handler method.

The HandlerInterceptor interface defines three methods that you can implement:

1. preHandle: This method is called before the actual handler method is executed. It allows you to perform pre-processing tasks such as authentication, authorization, logging, or modifying the request attributes.

2. postHandle: This method is called after the handler method has been executed but before the view is rendered. It allows you to perform post-processing tasks such as modifying the model, adding additional attributes, or modifying the view before it is rendered.

3. afterCompletion: This method is called after the complete request has been processed, including the rendering of the view. It allows you to perform tasks such as resource cleanup or logging after the request has been fully processed.

By implementing the HandlerInterceptor interface and registering it with the Spring MVC framework, you can define custom logic that will be executed before and after the controller handler method. This gives you the ability to customize the request processing flow and add additional functionality to your application.

</blockquote> 

</details>

---

33. How do you handle file uploads in Spring MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To handle file uploads in Spring MVC, you can follow these steps:

1. Include the necessary dependencies in your project, such as Apache Commons FileUpload or Apache Commons IO.
2. Configure a `multipartResolver` bean in your Spring configuration file (e.g., XML or Java configuration).
3. Create a form in your view that includes an input field of type "file" to allow users to select a file for upload.
4. In your controller, use the `@RequestMapping` annotation with the appropriate HTTP method (e.g., POST) to handle the form submission.
5. Use the `@RequestParam` annotation to bind the uploaded file to a method parameter.
6. Process the uploaded file as needed, such as saving it to a specific location or performing further operations on it.

Spring MVC will automatically handle the file upload process and make the uploaded file available to your controller method. You can then perform any necessary operations with the uploaded file based on your application's requirements.

</blockquote> 

</details>

---