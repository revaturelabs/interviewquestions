1.Define Servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets can be defined as a small Java program that runs within a Web server.It receive and respond to requests from Web clients like **HTTP**(HyperText Transfer Protocol).It can also access a library of HTTP-specific calls which includes portability, performance, reusability, and crash protection.They are often used to provide rich interaction functionality within the browser for users like clicking link, form submission.

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

We have to create a Java class that extends `javax.servlet.http.HttpServlet` and import the classes from `servlet.jar` or `servlet-api.jar`.These will be needed to compile the servlet.A servlet does not have a `main()` method, unlike a regular Java program, and just like an applet. It has some methods of a servlet that are called upon by the server for the purpose of handling requests. It invokes the servlet’s `service()` method, every time the server sends a request to a servlet.

To handle requests that are appropriate for the servlet, a typical servlet must override its `service()` method. The `service()` method allows 2 parameters: these are the request object and the response object. The request object is used to inform the servlet about the request, whereas the response object is used to then give a response.

</blockquote>

</details>
  
 ---
  
4.What is the need of Http servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A Http servlet typically does not override the `service()` method. However, it actually overrides the `doGet()` to handle the GET requests and the `doPost()` to handle POST requests. Depending on the type of requests it needs to handle, an HTTP servlet can override either or both of these methods. 

</blockquote>

</details>
  
---
  
5.How do you create a  server-side functionalities in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets can be added in HTML pages with the server-side include (SSI) functionality. A page can be preprocessed by the server to add the output from servlets at some points within the page, in the servers that support servlets.
	
```java

<SERVLET CODE=ServletName CODEBASE=http://server:port/dir
           initParam1=initValue1 
           initParam2=initValue2>
<PARAM NAME=param1 VALUE=val1>
<PARAM NAME=param2 VALUE=val2>
   SERVER SIDE FUNCTIONALITIES
</SERVLET>
	
```

</blockquote>

</details>

---
  
6.Explain  'init' and 'destroy' methods in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Servlets init method is used to initialise a servlet.When the web container loads and instantiates the servlet class and before it delivers requests from clients, the web container initializes the servlet. To customize this process to allow the servlet to read persistent configuration data, initialize resources, and perform any other one-time activities, you override the init method of the Servlet interface.When a servlet container determines that a servlet should be removed from service (for example, when a container wants to reclaim memory resources or when it is being shut down), the container calls the destroy method of the Servlet interface.

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

- The life cycle of a servlet can be implemented by `init( )`, `service( )`, and `destroy( )` methods.
When a user enters a Uniform Resource Locator (URL) to a web browser.The browser then generates an HTTP request for this URL. This request is then sent to the appropriate server.The Http request is received by the web server. The server maps this request to a particular servlet. 

- The servlet is dynamically retrieved and loaded into the address space of the server.The server invokes the `init( )` method of the servlet. This method is invoked only when the servlet is first loaded into memory. It is possible to pass initialization parameters to the servlet so it may configure itself.

- The server invokes the `service( )` method of the servlet. This method is called to process the HTTP request. You will see that it is possible for the servlet to read data that has been provided in the HTTP request. It may also formulate an HTTP response for the client.The servlet remains in the server’s address space and is available to process any other HTTP requests received from clients. The `service( )` method is called for each HTTP request.

- The server may decide to unload the servlet from its memory. The server calls the `destroy( )` method to relinquish any resources such as file handles that are allocated for the servlet. Important data may be saved to a persistent store. The memory allocated for the servlet and its objects can then be garbage collected.

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

- We can create and compile the servlet source code.Then, copy the servlet’s class file to the proper directory, and add the servlet’s name and mappings to the proper `web.xml` file.
- Start Tomcat.
- Start a web browser and request the servlet.

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



</details>
	
</blockquote>
</details>


---

13.Explain Single-Thread Model in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- It is standard to have a single servlet instance for each registered name of the servlet. However, instead of this, it is also possible for a servlet to choose to have a pool of instances created for each of its names that all share the task of handling requests. These servlets indicate this action by implementing the `javax.servlet.SingleThreadModel` interface.
- A server loading the SingleThreadModel servlet should guarantee, "that no two threads will execute concurrently the service method of that servlet". Each thread uses a free servlet instance from the pool in order to achieve this. Therefore, any servlet using the SingleThreadModel isn’t needed to synchronize usage to its instance variables and is considered thread-safe.

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

- **Sharing information**: Sharing information involves two or more servlets sharing the state or even resources. A special case of sharing information is Session tracking.

- **Sharing control**: Sharing control involves two or more servlets sharing control of the request. For example, one servlet could receive the request but let another servlet handle some or all of the request-handling responsibilities
		

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
	
17.Explain the stages of inter-servlet communication?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- **Servlet manipulation** :When a servlet directly invokes the methods of another servlet. These servlets can get references to other servlets using `getServletNames()` and `getServlet(String name)`.

- **Servlet reuse**:When one servlet uses another’s abilities for its own purposes.This requires forcing a servlet load using a manual HTTP request.

- **Servlet collaboration**:When the cooperating servlets share information. Servlets can share information using the system properties list, using a shared object, or using inheritance
		
</blockquote>

</details>

  
---
  
18.What is Servlet API?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet API contains two packages which contains the classes and interfaces that are required to build servlets. These are `javax.servlet` and `javax.servlet.http`. The `javax.servlet` package contains a number of interfaces and classes that establish the framework in which servlets operate.The `javax.servlet.http` package contains a number of interfaces and classes that are commonly used by servlet developers and its functionality makes it easy to build servlets that work with http requests and responses.

</blockquote>

</details>

---
  
19.Explain the Servlet Interface?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

All servlets must implement the Servlet interface. It declares the `init( )`, `service( )`, and `destroy( )` methods that are called by the server during the life cycle of a servlet. These are invoked by the server.The `getServletConfig( )` method is called by the servlet to obtain initialization parameters. A servlet developer overrides the `getServletInfo( )` method to provide a string with useful information.This method is also invoked by the server.
		
</blockquote>

</details>
  
---
  
20.How can you differentiate ServletConfig and ServletContext Interface?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The **ServletConfig** interface allows a servlet to obtain configuration data when it is loaded.
The methods declared by this interface are given below:

- `ServletContext getServletContext( )`: It returns the context for this servlet.
- `String getInitParameter(String param)`:It returns the value of the initialization parameter named param.
- `String getServletName( )`:It returns the name of the invoking servlet.

The ServletContext interface enables servlets to obtain information about their environment.

- `void destroy( )`: It is Called when the servlet is unloaded.
- `ServletConfig getServletConfig( )`: It returns a ServletConfig object that contains any initialization
parameters.
- `String getServletInfo( )`: It returns a string describing the servlet.
- `void init(ServletConfig sc)throws ServletException`:It is invoked when the servlet is initialized. Initialization parameters for the servlet can be obtained from sc.An UnavailableException should be thrown if the servlet cannot be initialized.
- `void service(ServletRequest req,ServletResponse res)throws ServletException,IOException`:It is used to process a request from a client. The request from the client can be read from req. The response to the clientcan be written to res. An exception is generated if a servlet or IO problem occurs.
	
</blockquote>

</details>

---

21.What is ServletRequest and ServletResponse Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The ServletRequest interface enables a servlet to obtain information about a client request.The ServletResponse interface enables a servlet to formulate a response for a client.
		
</blockquote>

</details>

---

22.What is GenericServlet Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The GenericServlet class provides implementations of the basic life cycle methods for a servlet.It implements the Servlet and ServletConfig interfaces. In addition, a method to append a string to the server log file is available. The signatures of this method are `void log(String s)` and `void log(String s, Throwable e)` Where s is the string to be appended to the log, and e is an exception that occurred

</blockquote>

</details>

---

23. How will you distinguish between the ServletInputStream and ServletOutputStream classes? 
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- ServletInputStream class extends InputStream. It is implemented by the servlet container and provides an input stream that a servlet developer can use to read the data from a client request. It defines the default constructor. In addition, a method is provided to read bytes from the stream as `int readLine(byte[ ] buffer, int offset, int size) throws IOException`. Here, buffer is the array into which size bytes are placed starting at offset. The method returns the actual number of bytes read or –1 if an end-of-stream condition is encountered.

- ServletOutputStream class extends OutputStream. It is implemented by the servlet container and provides an output stream that a servlet developer can use to write data to a client response. A default constructor is defined. It also defines the `print( )` and `println( )`methods, which output data to the stream.

</blockquote>

</details>

---

24. Explain how to read servlet parameters with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The ServletRequest interface includes methods that allow you to read the names and values of parameters that are included in a client request.The example contains two files. A web page is defined in parameters.html, and a servlet is defined in parametersservlet.java.

The html source code for parameters.htm is shown in the following listing. It defines a table that contains two labels and two text fields. One of the labels is Employee and the other is Phone. There is also a submit button. Notice that the action parameter of the form tag specifies a url. The url identifies the servlet to process the http post request.

```java

<html>
<body>
<center>
<form name="Form1"method="post" action="http://localhost:8080/servlets-examples/servlet/parametersservlet">
<table>
<tr>
<td><B>Employee</td>
<td><input type=textbox name="e" size="20" value=""></td>
</tr>
<tr>
<td><B>Phone</td>
<td><input type=textbox name="p" size="20" value=""></td>
</tr>
</table>
<input type=submit value="Submit">
</body>
</html>

```

The source code for parametersservlet.java is shown in the following listing. The `service( )` method is overridden to process client requests. The `getParameterNames( )` method returns an enumeration of the parameter names. These are processed in a loop. You can see that the parameter name and value are output to the client. The parameter value is obtained via the `getParameter( )` method.

```java

import java.io.*;
import java.util.*;
import javax.servlet.*;
public class ParametersServlet extends GenericServlet {
public void service(ServletRequest request,ServletResponse response)throws ServletException, IOException {
PrintWriter pw = response.getWriter();
Enumeration e = request.getParameterNames();
while(e.hasMoreElements()) {
String pname = (String)e.nextElement();
pw.print(pname + " = ");
String pvalue = request.getParameter(pname);
pw.println(pvalue);
}
pw.close();
}
}

```

</blockquote>

</details>

---

25. What are HttpServlet request,response and session interfaces in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The HttpServletRequest interface enables a servlet to obtain information about a client request. The HttpServletResponse interface enables a servlet to formulate an HTTP response to a client. Several constants are defined. These correspond to the different status codes that can be assigned to an HTTP response. For example, SC_OK indicates that the HTTP request succeeded, and SC_NOT_FOUND indicates that the requested resource is not available.The HttpSession interface enables a servlet to read and write the state information that is associated with an HTTP session.

</blockquote>

</details>
	
---

26. What is a Cookie Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Cookie class encapsulates a cookie. A cookie is stored on a client and contains state information. Cookies are valuable for tracking user activities. For example, assume that a user visits an online store. A cookie can save the user’s name, address, and other information.The user does not need to enter this data each time he or she visits the store.

</blockquote>

</details>

---

27. How a servlet helps to create a cookie in user's machine?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A servlet can write a cookie to a user’s machine by using `addCookie( )` method of the HttpServletResponse interface. The data for that cookie is then included in the header of the http response that is sent to the browser. The names and values of cookies are stored on the user’s machine. Some of the information that is saved for each cookie includes the following:

- The name of the cookie
- The value of the cookie
- The expiration date of the cookie
- The domain and path of the cookie

The expiration date determines when this cookie is deleted from the user’s machine. If an expiration date is not explicitly assigned to a cookie, it is deleted when the current browser session ends. Otherwise, the cookie is saved in a file on the user’s machine.The domain and path of the cookie determine when it is included in the header of an HTTP request. If the user enters a URL whose domain and path match these values, the cookie is then supplied to the Web server. Otherwise, it is not.
There is one constructor for Cookie. It has the signature shown here: `Cookie(String name, String value)`
Here, the name and value of the cookie are supplied as arguments to the constructor

</blockquote>

</details>

---

28. What is HttpServlet and HttpSessionEvent Class?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The HttpServlet class extends GenericServlet. It is commonly used when developing servlets`that receive and process HTTP requests. HttpSessionEvent encapsulates session events. It extends EventObject and is generated when`a change occurs to the session. It defines this constructor:`HttpSessionEvent(HttpSession session)`Here, session is the source of the event.HttpSessionEvent defines one method, `getSession( )`, which is shown here:`HttpSession getSession( )`.It returns the session in which the event occurred.

</blockquote>

</details>

---

29. Explain how it is possible to handle HTTP Requests in a servlet with examples?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The HttpServlet class provides specialized methods that handle the various types of http requests. A servlet developer typically overrides one of these methods. These methods are `doDelete( )`, `doGet( )`, `doHead( )`, `doOptions( )`, `doPost( )`, `doPut( )`, and `doTrace( )`. However, the GET and POST requests are commonly used when handling form input. 

- Handling HTTP GET Requests:We will develop a servlet that handles an HTTP GET request. The servlet is invoked when a form on a web page is submitted. The example contains two files. A web page is definedin ColorGet.htm, and a servlet is defined in ColorGetServlet.java. The HTML source code for ColorGet.htm is shown below. It defines a form that contains a select element and a submit button. Notice that the action parameter of the form tag specifies a URL. The URL identifies a servlet to process the HTTP GET request.

```java

<html>
<body>
<center>
<form name="Form1"
action="http://localhost:8080/servlets-examples/servlet/ColorGetServlet">
<B>Color:</B>
<select name="color" size="1">
<option value="Red">Red</option>
<option value="Green">Green</option>
<option value="Blue">Blue</option>
</select>
<br><br>
<input type=submit value="Submit">
</form>
</body>
</html>

```
The source code for ColorGetServlet.java is shown in the following listing. The doGet( ) method is overridden to process any HTTP GET requests that are sent to this servlet. It uses the getParameter( ) method of HttpServletRequest to obtain the selection that was made by the user. A response is then formulated.

```java

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class ColorGetServlet extends HttpServlet {
public void doGet(HttpServletRequest request,HttpServletResponse response)throws ServletException, IOException {
String color = request.getParameter("color");
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.println("<B>The selected color is: ");
pw.println(color);
pw.close();
}
}

```

- Handling HTTP POST Requests:We will develop a servlet that handles an HTTP POST request. The servlet is invoked when a form on a web page is submitted. The example contains two files. A web page is defined in ColorPost.htm, and a servlet is defined in ColorPostServlet.java.The HTML source code for ColorPost.htm is shown below. It is identical to ColorGet.htm except that the method parameter for the form tag explicitly specifies that the POST method should be used, and the action parameter for the form tag specifies a
different servlet.

```java

<html>
<body>
<center>
<form name="Form1"
method="post"
action="http://localhost:8080/servlets-examples/servlet/ColorPostServlet">
<B>Color:</B>
<select name="color" size="1">
<option value="Red">Red</option>
<option value="Green">Green</option>
<option value="Blue">Blue</option>
</select>
<br><br>
<input type=submit value="Submit">
</form>
</body>
</html>

```
The source code for ColorPostServlet.java is shown below. The `doPost( )` method is overridden to process any HTTP POST requests that are sent to this servlet. It uses the `getParameter( )` method of HttpServletRequest to obtain the selection that was made
by the user. A response is then formulated.

```java

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class ColorPostServlet extends HttpServlet {
public void doPost(HttpServletRequest request,HttpServletResponse response)throws ServletException, IOException {
String color = request.getParameter("color");
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.println("<B>The selected color is: ");
pw.println(color);
pw.close();
}
}

```

</blockquote>

</details>

---

30. Explain creating a cookie using a servlet with example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The html source code for AddCookie.htm is shown below. This page contains a text field in which a value can be entered. There is also a submit button on the page. When this button is pressed, the value in the text field is sent to AddCookieServlet via an HTTP POST request.

```java

<html>
<body>
<center>
<form name="Form1" method="post" action="http://localhost:8080/servlets-examples/servlet/AddCookieServlet">
<B>Enter a value for MyCookie:</B>
<input type=textbox name="data" size=25 value="">
<input type=submit value="Submit">
</form>
</body>
</html>

```

The source code for AddCookieServlet.java is shown below. It gets the value of the parameter named "data". It then creates a Cookie object that has the name "MyCookie" and contains the value of the "data" parameter. The cookie is then added to the header of the http response via the `addCookie( )` method.

```java

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class AddCookieServlet extends HttpServlet {
public void doPost(HttpServletRequest request,HttpServletResponse response)throws ServletException, IOException {
String data = request.getParameter("data");
Cookie cookie = new Cookie("MyCookie", data);
response.addCookie(cookie);
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.println("<B>MyCookie has been set to");
pw.println(data);
pw.close();
}
}

```

The source code for GetCookiesServlet.java is shown below. It invokes the `getCookies( )` method to read any cookies that are included in the HTTP GET request. The names and values of these cookies are then written to the HTTP response. Observe that the
`getName( )` and `getValue( )` methods are called to obtain this information.

```java

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class GetCookiesServlet extends HttpServlet {
public void doGet(HttpServletRequest request,HttpServletResponse response)throws ServletException, IOException {
Cookie[] cookies = request.getCookies();
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.println("<B>");
for(int i = 0; i < cookies.length; i++) {
String name = cookies[i].getName();
String value = cookies[i].getValue();
pw.println("name = " + name +"; value = " + value);
}
pw.close();
}
}

```

</blockquote>

</details>

---

31. What is Session Tracking?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
<blockquote>

Http is a stateless protocol. Each request is independent of the previous one. However, in some applications, it is necessary to save state information so that information can be collected from several interactions between a browser and a server. Sessions provide such a mechanism.A session can be created via the `getSession( )` method of HttpServletRequest. An HttpSession object is returned. This object can store a set of bindings that associate names with objects. The `setAttribute( )`, `getAttribute( )`, `getAttributeNames( )`, and `removeAttribute( )` methods of HttpSession manage these bindings.

</blockquote>

</details>


---

32. How do you create session using session tracking in servlets?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A new session is created if one does not already exist. The `getAttribute( )`method is called to obtain the object that is bound to the name "date". That object is a Date object that encapsulates the date and time when this page was last accessed. A Date object encapsulating the current date and time is then created. The `setAttribute( )` method is called to bind the name "date"
to this object.

```java

import java.io.*;
import java.util.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class DateServlet extends HttpServlet {
public void doGet(HttpServletRequest request,HttpServletResponse response)throws ServletException, IOException {
HttpSession hs = request.getSession(true);
response.setContentType("text/html");
PrintWriter pw = response.getWriter();
pw.print("<B>");
Date date = (Date)hs.getAttribute("date");
if(date != null) {
pw.print("Last access: " + date + "<br>");
}
date = new Date();
hs.setAttribute("date", date);
pw.println("Current date: " + date);
}
}

```

When you first request this servlet, the browser displays one line with the current date and time information. On subsequent invocations, two lines are displayed. The first line shows the date and time when the servlet was last accessed. The second line shows the current date and time.

</blockquote>

</details>

---

33. What is the difference between web server and application server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A web server responsibility is to handle Http requests from client browsers and respond with Html response. A web server understands Http language and runs on Http protocol. Apache Web Server is kind of a web server and then we have specific containers that can execute servlets and JSPs known as the servlet container and Application Servers provide additional features such as Enterprise JavaBeans support, JMS Messaging support, Transaction Management, etc.application server is a web server with additional functionalities to help developers with enterprise applications.

</blockquote>

</details>

---

34. Define MIME Type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


The "Content-Type" response header is known as MIME Type. Server sends MIME type to client to let them know the kind of data it’s sending. It helps client in rendering the data for user. Some of the mostly used mime types are `text/html`, `text/xml`, `application/xml` etc. We can use ServletContext `getMimeType()` method to get the correct `MIME` type of the file and use it to set the response content type. It’s very useful in downloading a file through servlet from the server.

</blockquote>

</details>

---

35. Explain Request Dispatcher?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

RequestDispatcher interface is used to forward the request to another resource that can be Html, Jsp or another servlet in the same application. We can also use this to include the content of another resource to the response. This interface is used for inter-servlet communication in the same context. There are two methods defined in this interface:
- `void forward(ServletRequest request, ServletResponse response)`:It forwards the request from a servlet to another resource (servlet, Jsp file, or Html file) on the server.
- `void include(ServletRequest request, ServletResponse response)`:It includes the content of a resource (servlet, Jsp page, Html file) in the response.
- We can get RequestDispatcher in a servlet using ServletContext `getRequestDispatcher(String path)` method. The path must begin with a / and is interpreted as relative to the current context root.

</blockquote>

</details>

---

36. What is difference between PrintWriter and ServletOutputStream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

PrintWriter is a character-stream class whereas ServletOutputStream is a byte-stream class. We can use PrintWriter to write character based information such as character array and String to the response whereas we can use ServletOutputStream to write byte array data to the response. We can use ServletResponse `getWriter()` to get the PrintWriter instance whereas we can use ServletResponse `getOutputStream()` method to get the ServletOutputStream object reference.

</blockquote>

</details>

---

37. How can we create deadlock situation in servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can create deadlock in servlet by making a loop of method invocation, we have to invoke `doPost()` method from `doGet()` method and `doGet()` method to `doPost()` method to create deadlock situation in servlet. 

</blockquote>

</details>

---

38. What is the use of servlet wrapper classes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet Http API provides two wrapper classes - `HttpServletRequestWrapper` and `HttpServletResponseWrapper`. These wrapper classes are provided to help developers with custom implementation of servlet request and response types. We can extend these classes and override only specific methods we need to implement for custom request and response objects. 

</blockquote>

</details>

---

39. What is HTTP Tunneling ? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

HTTP Tunneling is a technique by which, communications performed using various network protocols are encapsulated using the HTTP or HTTPS protocols. The HTTP protocol therefore acts as a wrapper for a channel that the network protocol being tunneled uses to communicate. The masking of other protocol requests as HTTP requests is HTTP Tunneling.

</blockquote>
</details>
	
---

40. How can you differentiate GenericServlet and HttpServlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

GenericServlet is protocol independent implementation of Servlet interface whereas HttpServlet is Http protocol specific implementation.we use servlet for creating web application by extending HttpServlet class. HttpServlet class extends GenericServlet and also provide some other methods specific to Http protocol.

</blockquote>

</details>

---

41. How to achieve thread-safety in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

HttpServlet `init()` method and `destroy()` method are called only once in the servlet life cycle, so we don't need to worry about their synchronization. But service methods such as `doGet()` or `doPost()` are getting called in every client request and since servlet uses multithreading, we should provide thread safety in these methods. If there are any local variables in service methods, we don't need to worry about their thread-safety because they are specific to each thread but if we have a shared resource then we can use synchronization to achieve thread-safety in servlets when working with shared resources. The thread safety mechanisms are similar to thread safety in standalone java application.

</blockquote>

</details>

---

42. How to invoke one servlet from another servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can use RequestDispatcher `forward()` method to forward the processing of a request to another servlet. If we want to include the another servlet output to the response, we can use RequestDispatcher `include()` method.

</blockquote>

</details>

---

43. What is difference between ServletResponse `sendRedirect()` and RequestDispatcher `forward()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- RequestDispatcher `forward()` is used to forward the same request to another resource whereas ServletResponse `sendRedirect()` is a two step process. In `sendRedirect()`, web application returns the response to client with status code 302 (redirect) with URL to send the request. The request sent is a completely new request.
- `forward()` is handled internally by the container whereas `sendRedirect()` is handled by browser.
- We should use `forward()` when accessing resources in the same application because it's faster than `sendRedirect()` method.
- In `forward()` method browser is unaware of the actual processing resource and the URL in address bar remains same whereas in `sendRedirect()` URL in address bar change to the forwarded resource.
- `forward()` can't be used to invoke a servlet in another context, we can only use `sendRedirect()` in this case.

</blockquote>

</details>

---

44. Why HttpServlet class is declared abstract?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

HttpServlet class provide Http protocol implementation of servlet but it's left abstract because there is no implementation logic in service methods such as `doGet()` and `doPost()` and we should override at least one of the service methods. 

</blockquote>

</details>


---


45. What are different methods of session management in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The session is a conversational state between client and server and it can consist of multiple request and response between client and server. Since Http and Web Server both are stateless, the only way to maintain a session is when some unique information about the session (session-id) is passed between server and client in every request and response.The common ways of session management in servlets are:

- User Authentication
- HTML Hidden Field
- Cookies
- URL Rewriting
- Session Management API

</blockquote>

</details>

---


46. What is URL Rewriting?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet API provides support for URL rewriting that we can use to manage session and it’s very easy to use and involves encoding the URL. Servlet URL Encoding is that it’s a fallback approach and it kicks in only if browser cookies are disabled. We can encode URL with HttpServletResponse `encodeURL()` method and if we have to redirect the request to another resource and we want to provide session information, we can use `encodeRedirectURL()` method.

</blockquote>

</details>

---

47. How does Cookies work in Servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Cookies are text data sent by server to the client and it gets saved at the client local machine. Servlet API provides cookies support through `javax.servlet.http.Cookie` class that implements Serializable and Cloneable interfaces. HttpServletRequest `getCookies()` method is provided to get the array of cookies from the request, since there is no point of adding Cookie to request, there are no methods to set or add a cookie to `request.HttpServletResponse addCookie(Cookie c)` method is provided to attach cookie in the response header, there are no getter methods for a cookie. 

</blockquote>

</details>

---

48. Why do we have servlet filters?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet Filters are pluggable java components that we can use to intercept and process requests before they are sent to servlets and response after servlet code is finished and before container sends the response back to the client.The servlet filter task are given below:

- Logging request parameters to log files.
- Authentication and authorization of request for resources.
- Formatting of request body or header before sending it to servlet.
- Compressing the response data sent to the client.
- Alter response by adding some cookies, header information etc.

</blockquote>

</details>

---

49. How to handle exceptions thrown by application with another servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The `doGet()` and `doPost()` methods throw ServletException and IOException. Since browser understand only html, when our application throw exception, servlet container processes the exception and generate a html response. Servlet API provides support for custom Exception and Error Handler servlets that we can configure in the deployment descriptor, the whole purpose of these servlets are to handle the Exception or Error raised by application and send html response that is useful for the user. We can provide a link to the application home page or some details to let the user know what went wrong. We can configure them in web.xml like below:

```java

<error-page>
	<error-code>404</error-code>
    <location>/AppExceptionHandler</location>
</error-page>
   
<error-page>
  	<exception-type>javax.servlet.ServletException</exception-type>
  	<location>/AppExceptionHandler</location>
</error-page>

```

</blockquote>

</details>

---

50. What is a deployment descriptor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The deployment descriptor is a configuration file for the web application and its name is `web.xml` and it resides in WEB-INF directory. Servlet container uses this file to configure web application servlets, servlet config params, context init params, filters, listeners, welcome pages and error handlers.

</blockquote>

</details>

---

51. How to make sure a servlet is loaded at the application startup?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlet container loads a servlet on the first client request.The servlet is heavy and takes time to loads, we might want to load it on application startup. We can use a load-on-startup element with servlet configuration in the `web.xml` file or use WebServlet annotation loadOnStartup variable to tell the container to load the servlet on system startup.

```
<servlet>
	<servlet-name>Revature</servlet-name>
	<servlet-class>com.Revature.servlets.Rev</servlet-class>
	<load-on-startup>4</load-on-startup>
</servlet> 
```

The load-on-startup value should be int, if it's a negative integer then servlet container will load the servlet based on client requests and requirement but if it's 0 or positive, then the container will load it on application startup. If there are multiple servlets with load-on-startup value such as 0,1,2,3 then lower integer value servlet will be loaded first.


</blockquote>

</details>

---

52. What is a WAR file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


The WAR(Web Application Resource) file specifies the web elements,Either a Servlet or JSP project can be converted into a war file. Moving one Servlet project from one place to another will be fast as it is combined into a single file.

</blockquote>

</details>

---

53. Explain MVC pattern.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Model-View-Controller (MVC) is a design pattern that divides a software application into three segments namely the Model, the View and the Controller.

- Model deals with the behaviour of the application. It contains the data and business logic of the application. It notifies views and controllers when there is a change in its state.
- View renders the information to the user so that it looks attractive and appealing. It takes information from the model using which it generates output.
- Controller takes input from a user and sends the command to model or view. It controls the flow of the application.

</blockquote>

</details>

---

54. Explain the different methods involved in the process of session management in servlets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The different methods involved in the session management in servlets are as follows:

- **User Authentication**: A user tries to access a protected resource, such as a JSP page. If the user has been authenticated, the servlet container makes the resource available; otherwise, the user is asked for a username and password

- **HTML Hidden Field**: The `<input type="hidden">` defines a hidden input field. A hidden field let web developers include data that cannot be seen or modified by users when a form is submitted. A hidden field often stores what database record that needs to be updated when the form is submitted

- **Cookies**: A small text file created by a website that is stored in the user’s computer either temporarily for that session only or permanently on the hard disk. Cookies provide a way for the website to recognize you and keep track of your preferences

- **URL Rewriting**: URL rewriting is an automatic process of altering a program written for manipulating the parameters in a URL (Uniform Resource Locator). URL manipulation is employed as a convenience by a Web server administrator. 

- **Session Management API**: Session Management API is built on top of the Request-Response methods for session tracking. Session Tracking is a way to maintain state/data of a user. It is also known as session management in servlet.

</blockquote>

</details>

---

55. What is a  Web Container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A web container or a Servlet container is used to interact with the Servlet and includes all the Servlet, JSP, XML files inside it. Web Container’s responsibility is to manage the life cycle of a servlet and to help to map the URL of a specific servlet. A web container is also used creates the object of a servlet.

</blockquote>

</details>

---

56. How a servlet works without the `main()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Servlets don’t have  a `main()` method. Because servlets are executed using web containers. When a client places request for a servlet, then the server hands the requests to the web container where the servlet is deployed.

</blockquote>

</details>

---

57. What is the difference between Context Parameter and Context Attribute?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Context Parameter is a value stored in the deployment descriptor, which is the `web.xml` and is loaded during the deployment process. Context Attribute is the value which is set dynamically and can be used throughout the application.

</blockquote>

</details>

---


58. How can you create a session in servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can create HttpSession object by calling the public method `getSession()` of HttpServletRequest. The below code shows how to create a session.

`HttpSession session = request.getSession();`


</blockquote>

</details>

---

59. Explain the working of `service()` method in a servlet.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The `service()` method is actually the main method that is expected to perform the actual task. The servlet container calls the `service()` method to handle requests coming from the client/browsers and to provide the response back to the client.Each time the server receives a request for a servlet, the server creates a new thread and calls for the service. The `service()` method checks the Http request type and calls the respective methods as required.

```java

public void service(ServletRequest request, ServletResponse response)throws ServletException, IOException{
}

```

The container calls the `service()` method and service method invokes `doGet(), doPost(), doPut(), doDelete(),` methods as needed. So you have nothing to do with `service()` method but you override either `doGet()` or `doPost()` depending on the request you receive from the client-end.

</blockquote>

</details>

---

60. How do you get the IP address of the client in servlet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

`request.getRemoteAddr()` is the code to get the client IP address in servlet.

</blockquote>

</details>

---
















  
