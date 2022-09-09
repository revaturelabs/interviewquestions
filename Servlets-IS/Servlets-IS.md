1.Define Servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets can be defined as a small Java program that runs within a Web server.It receive and respond to requests from Web clients like HTTP(HyperText Transfer Protocol).It can also access a library of HTTP-specific calls which includes portability, performance, reusability, and crash protection.They are often used to provide rich interaction functionality within the browser for users like clicking link, form submission.

</blockquote>

</details>

---

2.What are the functionalities of Servlets in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets provide a number of functionalities which includes power, integration, efficiency, safety, portability, endurance, elegance, extensibility, and flexibility. It is convenient in modifying regular HTML and we can write the servlet code into the JSP.It includes java features like multithreading, exception handling and it has a separate layer of business logic in the application.

</blockquote>

</details>

---

3.How do you create a servlet in a web application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We have to create a Java class that extends javax.servlet.http.HttpServlet and import the classes from servlet.jar or servlet-api.jar.These will be needed to compile the servlet.A servlet does not have a main() method, unlike a regular Java program, and just like an applet. It has some methods of a servlet that are called upon by the server for the purpose of handling requests. It invokes the servlet’s service() method, every time the server sends a request to a servlet.

To handle requests that are appropriate for the servlet, a typical servlet must override its service() method. The service() method allows 2 parameters: these are the request object and the response object. The request object is used to inform the servlet about the request, whereas the response object is used to then give a response.

</blockquote>

</details>
  
 ---
  
4.What is the need of Http servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A Http servlet typically does not override the service() method. However, it actually overrides the doGet() to handle the GET requests and the doPost() to handle POST requests. Depending on the type of requests it needs to handle, an HTTP servlet can override either or both of these methods. 

</blockquote>

</details>
  
---
  
5.How do you create a  server-side functionalities in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets can be added in HTML pages with the server-side include (SSI) functionality. A page can be preprocessed by the server to add the output from servlets at some points within the page, in the servers that support servlets.

<SERVLET CODE=ServletName CODEBASE=http://server:port/dir
           initParam1=initValue1 
           initParam2=initValue2>
<PARAM NAME=param1 VALUE=val1>
<PARAM NAME=param2 VALUE=val2>
   SERVER SIDE FUNCTIONALITIES
</SERVLET>

</blockquote>

</details>

---
  
6.Explain  'init' and 'destroy' methods in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Servlets ​​init method is used to initialise a servlet.When the web container loads and instantiates the servlet class and before it delivers requests from clients, the web container initializes the servlet. To customize this process to allow the servlet to read persistent configuration data, initialize resources, and perform any other one-time activities, you override the init method of the Servlet interface.When a servlet container determines that a servlet should be removed from service (for example, when a container wants to reclaim memory resources or when it is being shut down), the container calls the destroy method of the Servlet interface.

</blockquote>

</details>

 ---
  
 7.How does a servlet get access and examine all its init parameters?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `public String ServletConfig.getInitParameter(String name)`:This method returns the value of the named init parameter or if the named init parameter does not exist it will return null. The value returned is always a single string. The servlet then interprets the value.

- `public Enumeration ServletConfig.getInitParameterNames()`:This method returns the names of the servlet's initialization parameters as an Enumeration of String objects, or an empty Enumeration if the servlet has no initialization parameters. This is often used for debugging.

</blockquote>

</details>

---
  
8.Define Servlet chaining?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet Chaining is a way where the output of one servlet is piped to the input of another servlet, and the output of that servlet can be piped to the input of yet another servlet and so on. Each servlet in the pipeline can either change or extend the incoming request. 

</blockquote>

</details>
  
---
  
9.Explain the Life Cycle of a Servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The life cycle of a servlet can be implemented by init( ), service( ), and destroy( ) methods.
When a user enters a Uniform Resource Locator (URL) to a web browser.The browser then generates an HTTP request for this URL. This request is then sent to the appropriate server.The Http request is received by the web server. The server maps this request to a particular servlet. 

- The servlet is dynamically retrieved and loaded into the address space of the server.The server invokes the init( ) method of the servlet. This method is invoked only when the servlet is first loaded into memory. It is possible to pass initialization parameters to the servlet so it may configure itself.

- The server invokes the service( ) method of the servlet. This method is called to process the HTTP request. You will see that it is possible for the servlet to read data that has been provided in the HTTP request. It may also formulate an HTTP response for the client.The servlet remains in the server’s address space and is available to process any other HTTP requests received from clients. The service( ) method is called for each HTTP request.

- The server may decide to unload the servlet from its memory. The server calls the destroy( )
method to relinquish any resources such as file handles that are allocated for the servlet.
Important data may be saved to a persistent store. The memory allocated for the servlet and
its objects can then be garbage collected.

</blockquote>

</details>
  
---

10.Define Servlet Reloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

In servlet reloading, the objects in classloader are developed to load a class just once. To solve this limitation and to load servlets multiple times, servers use custom class loaders. These custom class loaders load servlets from the default servlets directory.When a server dispatches a request to a servlet, it first checks if the servlet’s class file has changed on disk. If the change appears, then the server abandons the class that the loader used to load the old version and then creates a new instance of the custom class loader to load the new version. Old servlet versions can stay in memory indefinitely, but the old versions are not used to handle any more requests

</blockquote>

</details>

---
  
11.How can we get the name of the server and the port number for a particular request using a servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- A servlet can get the name of the server and the port number for a particular request with `getServerName()` and `getServerPort()` methods.

- `public String ServletRequest.getServerName()` and `public int ServletRequest.getServerPort()`
 are the methods and attributes of ServletRequest because the values can change for different requests if the server has more than one name is called as virtual hosting.

- The `getServerInfo()` and `getAttribute()` methods of ServletContext supply information about the server software and its attributes like `public String ServletContext.getServerInfo()`
`public Object ServletContext.getAttribute(String name)`

</blockquote>

</details>
  
---
  
12.How to create a servlet with example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- We can create and compile the servlet source code.Then, copy the servlet’s class file to the
proper directory, and add the servlet’s name and mappings to the proper web.xml file.
- Start Tomcat.Start a web browser and request the servlet.

```java

import java.io.*;
import javax.servlet.*;
public class HelloServlet extends GenericServlet {
public void service(ServletRequest request,ServletResponse response)throws ServletException, IOException {
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.println("<b>Hello!");
pw.close();
}
}

```

<details><summary><b> Explanation </b></summary>

The `javax.servlet` package contains the classes and interfaces required to build servlets.The program defines HelloServlet as a subclass of GenericServlet. The GenericServlet class provides functionality that simplifies the creation of a servlet. For example, it provides versions of `init( )` and `destroy( )` methods, which may be used to it. You need to supply only the `service( )` method.The `service( )` method which is inherited from GenericServlet is overridden. This method handles requests from a client. 
ServletRequest object enables the servlet to read data that is provided via the client request. ServletResponse object enables the servlet to formulate a response for the client.The call to `setContentType( )` establishes the MIME type of the Http response and the MIME type is text/html. This indicates that the browser should interpret the content as html source code. The `getWriter( )` method obtains a PrintWriter. Anything written to this stream is sent to the client as part of the http response. Then `println( )` is used to write some simple html source code as the http response. Compile this source code and place the HelloServlet.class file in the proper Tomcat directory and add HelloServlet to the web.xml file,Start the Tomcat and it must be running before you try to execute a servlet.Start a Web Browser and Request the Servlet.Start a web browser and enter the URL shown below:
`http://localhost:8080/servlets-examples/servlet/HelloServlet` and also `http://127.0.0.1:8080/servletsexamples/servlet/HelloServlet`
This can be done because 127.0.0.1 is defined as the IP address of the local machine.
The output of the servlet is shown in the browser display area. It will contain the
string Hello! in bold type.

</blockquote>

</details>

</details>


---

13.Explain Single-Thread Model in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

It is standard to have a single servlet instance for each registered name of the servlet. However, instead of this, it is also possible for a servlet to choose to have a pool of instances created for each of its names that all share the task of handling requests. These servlets indicate this action by implementing the `javax.servlet.SingleThreadModel` interface.
A server loading the SingleThreadModel servlet should guarantee, "that no two threads will execute concurrently the service method of that servlet." Each thread uses a free servlet instance from the pool in order to achieve this. Therefore, any servlet using the SingleThreadModel isn’t needed to synchronize usage to its instance variables and is considered thread-safe.

</blockquote>

</details>
  
---

    
14.How does Background Processing take place in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A thread that has been started by a servlet can continue to execute even after the response has been sent. This ability proves most useful for the tasks that are long-running, and whose incremental results should be made available to multiple clients. A background thread that has been started in `init()` performs continuous work. It also performs request-handling threads displaying the current status with `doGet()` method.

</blockquote>

</details>
  
---
  
15.How does Servlet collaboration take place?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets running together in the same server have many ways to communicate with one another. There are two main styles of servlet collaboration.

- Sharing information: Sharing information involves two or more servlets sharing the state or even resources. A special case of sharing information is Session tracking.

- Sharing control: Sharing control involves two or more servlets sharing control of the request. For example, one servlet could receive the request but let another servlet handle some or all of the request-handling responsibilities
		

</blockquote>

</details>
  
---
  
16.Explain Request parameters in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Http servlet gets its request parameters as a part of its query string or as encoded post data. A servlet used as a server-side includes its parameters equipped with PARAM tags.Although a servlet will receive parameters in an exceeding variety of various ways, every servlet retrieves its parameters the same way, by using `getParameter()` and `getParameterValues()` which is given below.

```java

public String ServletRequest.getParameter(String name)
public String[] ServletRequest.getParameterValues(String name)

```
		
</blockquote>

</details>
  
---

  
