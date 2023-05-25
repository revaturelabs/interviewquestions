## Technical

1. What is REST?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Representational state transfer (REST) is an abstraction of the architecture of the world wide web. REST is an architectural style to design networked applications.
- REST makes communication between remote computers easy by using the simple HTTP protocol which supports for CRUD (Create, Read, Update, and Delete) operations on the server

</blockquote> 

</details>

---

2. What is a REST API?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A REST API, also called a RESTful API, is an API that follows REST principles. 
- In a REST API, all data are treated as resources, each one represented by a unique uniform resource identifier (URI). 
- For example, the **Twitter API** makes each tweet an available resource that can be retrieved by clients. Clients can also use Twitter’s API to post tweets and perform other actions on the site.

</blockquote>

</details>

---

3. What are the most used HTTP methods supported by REST?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `GET` is only used to request data from a specified resource. Get requests can be cached and bookmarked. It remains in the browser history and has length restrictions. GET requests should never be used when dealing with sensitive data.
- `POST` is used to send data to a server to create/update a resource. POST requests are never cached and bookmarked and do not remain in the browser history.
- `PUT` replaces all current representations of the target resource with the request payload.
- `DELETE` removes the specified resource.
- `OPTIONS` is used to describe the communication options for the target resource.
- `HEAD` asks for a response identical to that of a GET request, but without the response body.

</blockquote>

</details>

---

4. What is a Resource in REST?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- In REST, every accessible piece of content on the server is labelled as a resource. 
- A resource is an object with a type, associated data, a relationship with other resources on the server, and a list of methods that can be used with it. 
- For example, a resource could be an HTML or text file, a data file, an image or video, or an executable code file.

- A resource is identified with a uniform resource identifier or URI. Clients access resources by including their URIs in HTTP requests.

</blockquote>

</details>

---

5. Can you list out the REST design principles?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

REST APIs follow six design principles:

- Client-server Separation
- Stateless
- Cacheable
- Layered System
- Uniform Interface
- Code on Demand (optional)

</blockquote>

</details>

---

6. Can you brief me on the Client-server Separation principle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The application which is requesting the resource is called the client, and the application which has the resource is called the server. 
- When the client requests a request to the server, the server sends a response to the client. The server can’t initiate a request to the client. 
- In a RESTful API, the client and server are always kept independent of each other. This ensures that both the client and the server can be scaled independently.

</blockquote>

</details>

---

7. What is the stateless principle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- In a RESTful API, each request needs to contain the data that is necessary to process it. Servers aren’t allowed to store any data related to the client. 
- No session or authentication state is stored on the server. 
- If the client requires authentication, then the client needs to authenticate itself before sending a request to the server.

</blockquote>

</details>

---

8. Can you brief us on the cacheable principle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- In REST APIs, the resources should be able to cache themselves either on the client or on the server. - When a client requests a resource from the server, the response from the server will contain the information on whether the resource can be cached or not and for how long. 
- The main idea of caching is to improve the performance of the client by reducing the bandwidth required to load the resource.

</blockquote>

</details>

---

9. What is a layered system in Rest?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- In REST APIs, there can be multiple intermediaries between the client and the server. It isn’t always necessarily true that the client connects directly to the server and requests a resource. 
- There can be multiple systems in between them that are responsible for handling security, traffic, balancing the load, redirection, etc. 
- The client or the server doesn’t have any information about how many systems are in between them.

</blockquote>

</details>

---

10. Can you brief us on the uniform interface in Rest?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- All communications between the client and server must follow the same protocol. For REST, this protocol is HTTP. 
- A uniform interface simplifies integrations because every application is using the same language to request and send data.

</blockquote>

</details>

---

11. What is messaging in RESTful web services?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A client sends a message in form of an HTTP Request and the server responds in form of an HTTP Response. This technique is termed Messaging. These messages contain message data and metadata i.e., information about the message itself.

</blockquote>

</details>

---

12. What is addressed in RESTful web services?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Addressing refers to locating a resource or multiple resources lying on the server. It is analogous to locating a postal address of a person.

</blockquote>

</details>

---

13. What is CRUD?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- CRUD stands for “Create, Read, Update, Delete.” These are the four basic actions that can be performed on databases through a REST API. Each action corresponds to an HTTP request method:

  - Create = POST
  - Read = GET
  - Update = PUT
  - Delete = DELETE

</blockquote>

</details>

---

14. What are the main parts of an HTTP request?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

HTTP requests are sent by the client to the API. They request data or perform some action on the server. 

There are five main components of an HTTP request in REST:

- **Start line**: Indicates the intended action of the request and includes:
- **a request method**: that indicates the HTTP request method to be performed on the resource (i.e., GET, POST, PUT, DELETE).
- **a URI** that identifies the requested resource on the server.
- **the HTTP version** being used, which signals which version the API should respond with.
- **HTTP Request Header**: Lists metadata about the request, such as the user agent, file formats the client will accept, format of the request body, language, caching preferences, etc.
- **HTTP Request body**: Contains any data associated with the request. This is only necessary if the request is to modify data on the server with the POST or PUT methods.

</blockquote>

</details>

---

15. What are the main parts of an HTTP response?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- HTTP responses are sent by the API to the client. They inform the client that the requested action was (or was not) completed and deliver any requested resources. There are four main components of an HTTP response:

- **HTTP version**: The version of HTTP version used.
- **Status line**: Indicates the status of the request with an HTTP response status code.
- **HTTP Response Header**: Lists metadata about the response, such as the date, server, user agent, file formats of the returned resources, caching information, etc.
- **HTTP Response body**: Contains the resource data that was requested by the client and is also called the payload.

</blockquote>

</details>

---

16.What is a URI?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

URI stands for uniform resource identifier. In REST, a URI is a string that identifies a resource on a web server. Each resource has its own unique URI which, when included in an HTTP request, allows clients to target that resource and perform actions on it. The process of targeting a resource with its URI is called “addressing.”

The format of a URI is as follows:

`<protocol>://<service-name>/<ResourceType>/<ResourceID>`

</blockquote>

</details>

---

17. What is caching?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- Caching refers to storing server response in the client itself so that a client does need not to make server requests for the same resource again and again. 
- A server response should have information about how caching is to be done so that a client caches the response for a period or never caches the server response.

</blockquote>

</details>

---

18. What is the payload?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- `Payload` refers to the data in the body of the HTTP request and/or response messages in GET or POST requests.

- For example, if you request a specific tweet from the Twitter API, the payload comprises the document containing the tweet text and any associated files for rendering the tweet on a page.

- Payload can also be included in the HTTP request with the POST method. If you want to post a tweet through Twitter's API, the tweet text that you send in your POST request is the payload.

</blockquote>

</details>

---

19. What is the purpose of the HTTP Status Code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

HTTP Status code are standard codes and refers to predefined status of task done at server.

HTTP Status Code:
- **200** – OK, shows success.
- **201** – CREATED, when a resource is successfully created using POST or PUT request. Return the link to a newly created resource using the location header.
- **204** – NO CONTENT, when the response body is empty.
- **304** – NOT MODIFIED, used to reduce network bandwidth usage in case of conditional GET requests.
- **400** – BAD REQUEST, states that invalid input is provided.
- **401** – FORBIDDEN, states that the user is not having access to the method being used.
- **404** – NOT FOUND, states that the method is not available.
- **409** – CONFLICT, states conflict situation while executing the method.
- **500** – INTERNAL SERVER ERROR, states that the server has thrown some exception while executing the method.

</blockquote>

</details>

---
    
20. What is HATEOAS in REST?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

HATEOAS stand for Hypermedia as The Engine of the Application State. It provides links to resources so that client does not have to manually bookmark the links. Below is an example.
    
```JS
{
"id":1,
"message":"Hello World",
"author":"Dhiraj",
"href":"/messages/1"
}
```

</blockquote>

</details>

---
    
21. Differentiate between SOAP and REST?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
    
SOAP: 	
Simple Object Access Protocol 
SOAP is a protocol used to implement web services.   
SOAP supports only XML transmission between the client and the server.  
SOAP uses service interfaces for exposing the resource logic.
    
REST: 
Representational State Transfer
REST is an architectural design pattern for developing web services
REST supports data of multiple formats like XML, JSON, MIME, Text, etc.
REST uses URI to expose the resource logic.
    
</blockquote>

</details>

---
    
22. What are Idempotent methods? How is it relevant in RESTful web services domain?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
    
Idempotent methods ensure that the responses to a request if called once or ten times or more than that remain the same. This is equivalent to adding any number with 0.
REST provides idempotent methods automatically. GET, PUT, DELETE, HEAD, OPTIONS, and TRACE are the idempotent HTTP methods. POST is not idempotent.
    
</blockquote>

</details>

---
    
23.What are the differences between PUT and POST in REST?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
    
PUT methods are used to request the server to store the enclosed entity in request. In case, the request does not exist, then new resource has to be created. If the resource exists, then the resource should get updated.
    
POST method is used to request the server to store the enclosed entity in the request as a new resource.
    
</blockquote>

</details>

---
    
24.What is different between REST API and RESTful API?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
 
 REST is an architectural pattern used for creating web services.The data format of REST is based on HTTP.
 RESTful API is used to implement that pattern. The data format of RESTful is based on JSON, HTTP, and Text.  
    
</blockquote>

</details>

---
    
25.Explain media type formatters.
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
In web API, media type formatters are classes that are responsible for serialization data. Here, serialization generally means a process of translating data into a format that can be transmitted and reconstructed later.  Because of serializing request/response data, Web API can understand request data format in a better way and send data in a format that the client expects. It simply specifies data that is being transferred among client and server in HTTP response or request.     
    
Media Type Formatter Class :
    
JsonMediaTypeFormatter
XmlMediaTypeFormatter
FormUrlEncodedMediaTypeFormatter	
JQueryMvcFormUrlEncodedFormatter
    
</blockquote>

</details>

---  
    
26.What are Web API filters?
    
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Filters are basically used to add extra logic at different levels of Web API framework request processing.  Different types of Web API filters are available as given below:

Authentication Filter: It handles authentication and authenticates HTTP requests. It also helps to authenticate user detail. It checks the identity of the user.
Authorization Filter: It handles authorization. It runs before controller action. This filter is used to check whether or not a user is authenticated. If the user is not authenticated, then it returns an HTTP status code 401 without invoking the action.
AuthorizeAttribute is a built-in authorization filter provided by Web API.
Action Filter: It is attributing that one can apply to controller action or entire controller. It is used to add extra logic before or after controller action executes. It is simply a way to add extra functionality to Web API services.
Exception Filter: It is used to handle exceptions that are unhandled in Web API. It is used whenever controller actions throw an unhandled exception that is not HttpResponseException. It will implement an “IExceptionFilter” interface.
Override Filter: It is used to exclude specific action methods or controllers from the global filter or controller level filter. It is simply used to modify the behavior of other filters for individual action methods. 
    
</blockquote>

</details>

---  
    
27.Who can consume Web API?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>  
    
 A large range of clients such as browsers, mobile devices, iPhone, etc., include or consume web API. It is also good for using along native applications that require web services but not SOAP support. It can also be consumed by any client that supports HTTP verbs such as GET, DELETE, POST, PUT.
    
</blockquote>

</details>

---  
    
28.How to register an exception filter globally?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote>  
    
One can register exception filter globally using following code:
GlobalConfiguration.Configuration.Filters.Add (new MyTestCustomerStore.NotImplExceptionFilterAttribute());   
    
</blockquote>

</details>

---  
    
29.What are the main return types supported in ASP. Net Web API?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
It supports the following return types:

HttpResponseMessage
IHttpActionResult
Void
Other types such as string, int, etc.  
    
</blockquote>

</details>

---   
    
30.What is ASP.NET Web API routing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
Routing is the most important part of ASP.NET Web API. Routing is a way how Web API matches a URI to an action. It is basically a process that decides which action and controller should be called. The controller is basically a class that handles all HTTP requests. All public methods of controllers are basically known as action methods or just actions. Whenever a Web API framework receives any type of request, it routes that request to action. 

There are basically two ways to implement routing in Web API as given below:
Convention-based routing: Web API supports convention-based routing. In this type of routing, Web API uses route templates to select which controller and action method to execute. 

Attribute-based routing: Web API 2 generally supports a new type of routing known as attribute routing. As the name suggests, it uses attributes to define routes. It is the ability to add routes to the route table via attributes. 

    
</blockquote>

</details>

---  
    
31.What is HttpConfiguration in Web API?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
 It is considered as the main class that includes different properties with help of which one can override the default behavior of Web API. 

Some properties are given below:

DependencyResolver: It sets or gets a dependency resolver for dependency injection.
Services: It gets web API services.
ParameterBindingRules: It gets a collection of rules for how parameters should be bound.
MessageHandlers:  It sets or gets message handlers.
Formatters: It sets or gets media-type formatters.   
</blockquote>

</details>

---
    
32.Can we return View from ASP.NET Web API method?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
 
No, we cannot return the view from the ASP.NET Web API method. ASP.NET web API develops HTTP services that provide raw data or information. ApiController in ASP.NET MVC application only renders data that is serialized and sent to the client. One can use a controller to provide normal views.
    
</blockquote>

</details>

---
    
33.What is content negotiation in ASP.Net Web API?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
Content negotiation is basically a process of selecting the best representation from multiple representations that are available for a given response. It simply allows one to choose rather than negotiate content that one wants to get in response. It is performed at the server-side. In simple words, it chooses the best media type for matters to return a response to an incoming request. 
    
</blockquote>

</details>

---
   
 34.What is CORS in Web API?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
ORS (Cross-Origin Resource Sharing) is basically a mechanism that allows one to make requests from one website to another website in a browser that is normally not allowed by another policy called SOP (Same Origin Policy). It supports secure cross-origin requests and data transfers among clients or browsers and servers. Here, cross-origin request means requests coming from different origins. CORS simply resolves the same-origin restriction for JavaScript. One can enable CORS for web API using the respective web API package or OWIN middleware. 
    
</blockquote>

</details>

---
    
35.Explain method to handle error using HttpError in Web API?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
    
<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
CreateErrorResponse is an extension method that can be used in Web API controller methods to return error codes and error messages. It creates an HttpError object and then wraps it inside an HttpResponseMessage object.    
    
</blockquote>

</details>

---
