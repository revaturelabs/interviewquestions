## Technical

1. What is ASP.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ASP.NET is a server-side technology used for developing dynamic websites and web applications on the internet. It also produces data-driven web applications.

</blockquote>

</details>

---

2. Is it possible to deploy the application without deploying the server source code?
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- It is certainly possible to do that with the help of the process of new precompilation which is also known as ‘precompilation for deployment’. 
- We can make use of aspnet_compiler.exe to make sure that the precompilation of the site is done. Besides, the process also builds every page in the web application in a single one with DLL and other placeholder files.

</blockquote>

</details>

---

3.  What is the ASP.NET Life Cycle, and list the types of Life Cycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- When ASP.NET pages run, it goes through several steps of the life cycle, which perform a series of actions like initialization, running, restoring, and rendering.

- Life Cycle is classified into two categories.

**Application Life Cycle**: The user requests for accessing the application.
**Page Life Cycle**: Page Life Cycle has phases like initialization, restoring, execution, and page rendering. 

</blockquote>

</details>

---

4.  What is ASP.NET MVC framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ASP.NET MVC is a web application framework for the .NET Platform used for building full-stack web applications using the Model-View-Controller pattern.

</blockquote>

</details>

---

5. What is the web.config file and what is it used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The web.config file is crucial because it contains the configuration settings for the application. It keeps your entire configuration separate from your code so you can easily change settings without code changes. It also allows you to potentially encrypt the configuration settings for increased security.

</blockquote>

</details>

---

6. What is an ASP.NET web API framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ASP.NET Web API is used purely for building backend web APIs which can be used by an array of clients, from the web to desktop to mobile. It forms the server component in the RESTful (Representational State Transfer) architecture.

</blockquote>

</details>

---

7. Can you explain the request flow in the ASP.NET MVC framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Request flow handles the request from the clients and passes it to the server. The request hits the controller coming from the client. 
- Controller plays its role and decides which model to use to serve the request further, passing that model to view which then transforms the model and generates an appropriate response that is rendered to the client.

</blockquote>

</details>

---

8. Could you explain the viewstate concept in ASP.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To make sure that the state between the postbacks is well maintained, ASP.NET offers a mechanism which is called view state. There are hidden form fields which are used for storing the objects stored on the client section and are returned to the server as soon as the postback occurs. 

</blockquote>

</details>

---

9. How can you detect if a viewstate has tampered with?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

By setting the EnableViewStateMac to true in the `@Page` directive. This attribute checks the encoded and encrypted viewstate for tampering.

</blockquote>

</details>

---

10.  What is Server control?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ASP.NET has Server Controls features, which provide facilities to manipulate the values of the controls on the Server-Side. This is especially helpful when we want to create validating and dynamic web forms.

</blockquote>

</details>

---

11.  How many types of Server controls are supported by ASP.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are mainly four different types of Server-side controls in ASP.NET :

- HTML server controls
- Web Server controls
- User controls
- Validation controls

</blockquote>

</details>

---

12. Can you differentiate Server.Transfer and Response.Redirect?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- In `Server.Transfer` page processing transfers from one page to the other page without making a round-trip back to the client’s browser. This provides a faster response with a little less overhead on the server. The client URL history list or current URL Server does not update in case of `Server.Transfer`.

- `Response.Redirect` is used to redirect the user’s browser to another page or site. It performs a trip back to the client where the client’s browser is redirected to the new page. The user’s browser history list is updated to reflect the new address.

</blockquote>

</details>

---

13. What is caching?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Caching is a technique used to increase performance by keeping frequently accessed data or files in memory. The request for a cached file/data will be accessed from the cache instead of the actual location of that file.

</blockquote>

</details>

---

14. What are the different types of caching?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ASP.NET has 3 kinds of caching:

- Output Caching,
- Fragment Caching,
- Data Caching.

</blockquote>

</details>

---

15. Can you list the events in the page life cycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Page_PreInit
- Page_Init
- Page_InitComplete
- Page_PreLoad
- Page_Load
- Page_LoadComplete
- Page_PreRender
- Render

</blockquote>

</details>

---

16.  Is it possible to create a web application with both webforms and MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes. We have to include the below MVC assembly references in the web forms application to create a hybrid application.

`System.Web.Mvc`

`System.Web.Razor`

`System.ComponentModel.DataAnnotations`

</blockquote>

</details>

---

17. What is Cross Page Posting?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

When we click submit button on a web page, the page posts the data to the same page. The technique in which we post the data to different pages is called Cross Page posting. This can be achieved by setting POSTBACKURL property of the button that causes the postback. Findcontrol method of PreviousPage can be used to get the posted values on the page to which the page has been posted.

</blockquote>

</details>

---

18. What is Query String in ASP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A query string is a method of transporting data from page to page using the browser URL. It is attached to the URL using the question mark symbol (?). For example, `http://xyz.com?userid=12334&pwd=rf5r5jm3smQ`

</blockquote>

</details>

---

19. What is tracing in .NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Tracing in .net enables one to follow the execution path of a page, debug the application and display diagnostic information at runtime. Trace messages can be accessed and manipulated from the code allowing for finer control to add more details. The tracing data is organized into a set of tables by ASP.NET. 

</blockquote>

</details>

---

20. What are Master Pages?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Master pages are a template that is used to create web pages with a consistent layout throughout your application. Master Pages contain content placeholders to hold page-specific content. When a page is requested, the contents of a Master page are merged with the content page, thereby giving a consistent layout.

</blockquote>

</details>

---

21. What is Razor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Razor is a view engine. The view engine is responsible for rendering the HTML page view to the browser. It is an advanced view engine, introduced with MVC3. Razor syntax is advanced, compact, and easy to learn. By default, ASP.NET MVC supports two view engines: ASPX and Razor.

</blockquote>

</details>

---

22. What is page processing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Page processing allows ASP.NET to execute the web server on the server by a technique called postback. It also enables ASP to create a seamless user experience where web applications are stateless.

</blockquote>

</details>

---

23. What is the use of the AutoEventWireup attribute in the Page directive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The AutoEventWireUp is a Boolean attribute that allows automatic wire-up of page events when this attribute is set to true on the page. It is set to True by default for a C# web form.

</blockquote>

</details>

---

24. What are the different Session state management options available in ASP.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In-Process and Out-of-Process are the two session state management options.

- In-Process stores the session in memory on the web server.
- Out-of-Process Session state management stores data in an external server. All objects stored in the session are required to be serializable.

</blockquote>

</details>

---

25. What is the difference between a session and an application object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The difference between session and application object is that all users share one Application object and with sessions, there is one session object for each user. Data stored in the application object can be shared by all the sessions of the application. Application object stores data in the key-value pair.
- Session object stores session-specific information and the information is visible within the session only. ASP.NET creates a unique SessionId for each session of the application. 
- SessionIDs are maintained either by an HTTP cookie or a modified URL, as set in the applications configuration settings. By default, SessionID values are stored in cookies.

</blockquote>

</details>

---
