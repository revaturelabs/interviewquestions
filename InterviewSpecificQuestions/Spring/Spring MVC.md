## Technical

1. What is DispatcherServlet in the Spring MVC application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In the case of Spring MVC, DispatcherServlet is the front controller. 
- DispatcherServlet acts as an entry and exit point for any request received by the rom client. 
</blockquote> 

</details>

---

2. How DispatcherServlet handle requests &responses in the Spring MVC application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Whenever a request comes it first goes to the DispatcherServlet where it then tries to identify its handler method (the methods defined in the specific controller to handle the requests) using Handler mapping.
- Once the handler mapping returns the controller the DispatcherServlet knows the controller which can handle the request and goes there for further request processing.
- Once the controller returns the view the DispatcherServlet goes to the view resolver to identify where the view is located.
- DispatcherServlet then grabs the view and returns as the final l response.
</blockquote> 

</details>

---

3. How Spring MVC DispatcherServlet is registered in the web.xml file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Since DispatcherServlet is one type of Servlet the `web.xml` file configuration is the same as normal servlet.
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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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

5. Can we have one `@RestController` class with multiple `@GetMapping` methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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
6. How do you ensure both "/" and "/welcome" request mappings land in the "index" view in Spring MVC applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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
7. Can `@Controller` annotation be used for both Spring MVC and RESTful applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Yes, `@RestController` is a convenience annotation that does nothing more than the `@Controller` and `@ResponseBody` annotations.
- Hence the following two controller definitions are the same:

```java
@Controller
@ResponseBody
public class RestControllerA { 

}

@RestController
public class RestControllerB { 

} 
```
</blockquote> 

</details>

---
8. What does `@Controller` & `@RestController` returns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@Controller` returns a view in the Spring MVC application.
- `@RestController` returns an object as a response instead of a view.

</blockquote> 

</details>

---
9. What is the use of `@ResponseBody` in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@ResponseBody` is a Spring annotation which binds a method return value to the web response body. 
- It is not interpreted as a view name. 
- It uses `org.springframework.http.converter Interface HttpMessageConverter<T>` to convert the return value to the HTTP response body, based on the content type in the request HTTP header.
</blockquote> 

</details>

---
10. What are MIME Types?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- MIME stands for Multi-purpose Internet Mail Extensions. 
- MIME types form a standard way of classifying file types on the Internet. 
- Internet programs such as Web servers and browsers all have a list of MIME types so that they can transfer files of the same type in the same way, no matter what operating system they are working in.
- A MIME type has two parts: a `type` and a `subtype`. They are separated by a slash (`/`) i.e., `type/subtype`. 
- For example, the MIME type for Microsoft Word files is an application and the subtype is ms-word. Together, the complete MIME type is application/ms-word.
- The entire list of MIME types is available under Internet Assigned Numbers Authority (IANA) website- https://www.iana.org/assignments/media-types/media-types.xhtml
- The MIME types & extensions can be found under-https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types 
</blockquote> 

</details>

---
11. What is the use of `@RequestBody` in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `@RequestBody` annotation request body to method parameters. 
- We use the `@RequestBody` annotation to have the request body read and deserialized into an Object through an `HttpMessageConverter`. 
- Additionally, automatic validations can be applied by annotating the argument with @Valid annotation.
</blockquote> 

</details>

---
12. What is the meaning of Content Negotiation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Content negotiation is the process of selecting one of the multiple possible representations to return to a client, based on client or server preferences.
- When a consumer sends a request, it can specify two HTTP Headers related to Content Negotiation `Accept` and `Content-Type`.
- `Content-Type` indicates the content type of the body of the request.
- `Accept` indicates the expected content type of the response.
</blockquote> 

</details>

---
13. What is RESTprotocol-dependentependent?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- REST is about resource state manipulation through their representations at the top of stateless communication between client and server. 
- It's a protocol-independent architectural style but, in practice, it's commonly implemented on top of the HTTP protocol.
</blockquote> 

</details>

---
14. What are “representation", "state" and "transfer" in Representational State Transfer (REST)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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
15. What is REST API versioning? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- API versioning is the process of transparently managing changes to your API.
- Versioning aims at effective communication around changes to API, so consumers/subscribers know what to expect from it. 
</blockquote> 

</details>

---
16. How do we provide a version to RESTful APIs in Spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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
17. Which object is used as a base context in the Spring MVC application? Why?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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
18. What is the difference between `applicationContext.xml` and `*-servlet.xml` in Spring Framework?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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

19. What is the difference between `@RequestParam` and `@PathVariable` in Spring MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`@RequestParam` is used to extract query parameters from the request URL, while `@PathVariable` is used to extract path variables from the URL. For example, in the URL `"/users?id=1"`, the id parameter can be extracted using `@RequestParam`, while in the URL `"/users/1"`, the `"1"` can be extracted using `@PathVariable`.

</blockquote>

</details>

---

20. What is the purpose of `@ModelAttribute` in Spring MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`@ModelAttribute` is used to bind HTTP request parameters to model objects. It can be used to pre-populate model objects with default values or to validate incoming data before processing it.

</blockquote>

</details>

---

21. What is the role of the `@Autowired` Annotation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The `@Autowired` annotation can be used with fields or methods for injecting a bean by type. This annotation allows Spring to resolve and inject collaborating beans into your bean.

</blockquote>

</details>

---

22. What is the ContextLoaderListener and what does it do? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The ContextLoaderListener is a listener that helps to bootstrap Spring MVC. As the name suggests, it loads and creates the ApplicationContext, so you don't have to write explicit code to do create it.

The application context is where Spring bean leaves. For a web application, there is is a subclass called WebAppliationContext.

The ContextLoaderListener also ties the lifecycle of the ApplicationContext to the lifecycle of the  ServletContext. You can get the ServletContext from the WebApplicationContext using the `getServletContext()` method.

</blockquote>

</details>

---

23. Describe the data flow of a request/response operation within a Spring MVC application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Request comes in to front controller, is dispatched to an appropriate controller which fetches the model requested, this bounces back through the front controller to a view template where the model data is woven into the UI view, this view object is then returned to the front controller, and the response is returned to the client.

</blockquote>

</details>

---

24. What is the purpose of BindingResult in Spring MVC validations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The BindingResult is an interface that contains the information of validations. For example :-

```Java
@RequestMapping("/helloagain")  
    public String submitForm( @Valid @ModelAttribute("emp") Employee e, BindingResult br)  
    {  
        if(br.hasErrors())  
        {  
            return "viewpage";  
        }  
        else  
        {  
        return "final";  
        }  
    }  

```

</blockquote>

</details>

---

25. What are the ways of reading data from the form in Spring MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The following ways to read the data from the form are: -

`HttpServletRequest interface` - The HttpServletRequest is a java interface present in `javax.servlet.http `package. Like Servlets, you can use HttpServletRequest in Spring to read the HTML form data provided by the user.
    
`@RequestParam annotation` - The @RequestParam annotation reads the form data and binds it automatically to the parameter present in the provided method.
    
`@ModelAttribute annotation` - The @ModelAttribute annotation binds a method parameter or its return value to a named model attribute

</blockquote>

</details>

---

