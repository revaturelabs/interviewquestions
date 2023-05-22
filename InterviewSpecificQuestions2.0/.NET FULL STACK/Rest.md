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
