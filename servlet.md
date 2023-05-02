1. Event and Listeners in Servlets?

<details> <summary>Show Answer</summary>
 
<blockquote>

Event and Listeners in Servlets?

In Java Servlets, an event is an action that occurs in a web application, such as a user submitting a form or clicking on a link. An event listener is an object that is notified when the event occurs. In other words, an event listener "listens" for events and performs some action in response to the event.

Servlets support the concept of events and listeners through the use of interfaces provided by the Servlet API. There are two main interfaces involved in handling events in Servlets:

**1. ServletContextListener:** This interface is used to receive notifications when the Servlet context is initialized or destroyed. A Servlet context is an object that represents a web application and is used to share information between Servlets.

**2. ServletRequestListener:** This interface is used to receive notifications when a Servlet request is created or destroyed. A Servlet request is an object that represents an HTTP request made to a web application.

- To use these interfaces, you need to implement them in your Servlet code and register the listeners with the Servlet container using either the web.xml file or annotations.
- Once the listeners are registered, they will receive notifications when the corresponding events occur, and can perform whatever actions are necessary in response. For example, a ServletContextListener could be used to initialize a database connection pool when the web application starts up, while a ServletRequestListener could be used to log information about each request made to the application.
  
</blockquote>

</details>

 ---

2. What is a servlet?

<details> <summary>Show Answer</summary>
 
<blockquote>

A Servlet is a Java class that runs on a web server and processes requests and responses between a client and a server. It is a server-side component that receives requests from web clients, processes them, and returns responses. Servlets are used to build dynamic web applications, such as e-commerce sites, social networking sites, and online banking systems. They follow the Java Servlet API, which provides a set of classes and interfaces that define the contract between the servlet container and the servlet. Servlets can handle HTTP requests and responses, session management, cookies, and more, making them a powerful tool for building web applications.

</blockquote>

</details>

 ---


