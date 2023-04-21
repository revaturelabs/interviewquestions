## Technical

1. What is MVC (Model View Controller)?Can you explain its life cycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

MVC is a framework for building web applications using an MVC (Model View Controller) design:

- The Model represents the data.
- The View displays the data.
- Controllers act as an interface between Model and View components to process all the business logic and then render the final output to view.
- Below is the flow of the request processing in MVC:

![MVC](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/MVC.PNG)

</blockquote>

</details>

---

2. What are the advantages of MVC over Web Forms?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Below are the advantages of MVC:

1. `SOC (SEPARATION OF CONCERNS)` - Separation of Concerns is one of the core advantages of ASP.NET MVC. The MVC framework provides a clean separation of the UI, Business Logic, Model or Data. Meaning is view is not dependent on controller and controller is not dependent on view. In Web forms one aspx file will have one aspx.cs file, which means UI(aspx) is TIGHTLY COUPLED with logic (.aspx.cs).

2. `MULTIPLE VIEW SUPPORT` - Due to the separation of the model from the view, the user interface can display multiple views of the same data at the same time.

3. `CHANGE ACCOMMODATION` - User interfaces tend to change more frequently than business rules (different colors, fonts, screen layouts, and levels of support for new devices such as cell phones or PDAs) because the model does not depend on the views, adding new types of views to the system generally does not affect the model. As a result, the scope of change is confined to the view. In Web forms one aspx file will have one aspx.cs file, which means UI(aspx) is TIGHTLY COUPLED with logic (.aspx.cs). In MVC one view can interact with multiple controllers and one controller can interact with multiple views therefore no TIGHT coupling.

4. `MORE CONTROL` - The ASP.NET MVC framework provides more control over HTML, JavaScript, and CSS than the traditional Web Forms.

5. `TESTABILITY` - ASP.NET MVC framework provides better testability of the Web Application and good support for test driven development too.

6. `LIGHTWEIGHT` - ASP.NET MVC framework doesn’t use View State and thus reduces the bandwidth of the requests to an extent.

7. `FULL FEATURES OF ASP.NET` - One of the key advantages of using ASP.NET MVC is that it is built on top of the ASP.NET framework and hence most of the features of the ASP.NET like membership providers, roles, etc can still be used.

</blockquote>

</details>

---

3. What are the different return types of a controller action method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

1. `VIEWRESULT` - This return type is used to return a webpage from an action method.
2. `PARTIALVIEWRESULT` - This return type is used to send a part of a view that will be rendered in another view.
3. `REDIRECTRESULT` - This return type is used to redirect to any other controller and action method depending on the URL.
4. `REDIRECTTOROUTERESULT` - This return type is used when we want to redirect to any other action method.
5. `CONTENTRESULT` - This return type is used to return HTTP content type like text/plain as the result of the action.
6. `JSONRESULT` - This return type is used when we want to return a JSON message.
7. `JAVASCRIPTRESULT` - This return type is used to return JavaScript code that will run in the browser.
8. `FILERESULT` - This return type is used to send binary output in response.
9. `EMPTYRESULT` - This return type is used to return nothing (void) in the result.

</blockquote>

</details>

---

4. What are filters and their types in MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

ASP.NET MVC Filter is a custom class where you can write custom logic to execute before or after an action method executes.

For example, here is the code of Authorize filter. If any request will try to access this action method DoAdminStuff, first this authorization filter will check that Roles In the request are of Admin, then only it will allow. So, this filter run before the execution of the action method.

``` C#

[Authorize]

public class AuthorizeController:Controller
{
    [Authorize(Roles="Admin")]
    public ActionResult DoAdminStuff()
    {
        return View();
    }
}
```
- Types of Action Filters are :

![Filters](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Filters_MVC.PNG)

</blockquote>

</details>

---

5. What is Authentication and Authorization in ASP.NET MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- Authentication is the process of obtaining some sort of credentials (username, password) from the users and using those credentials to verify the USER'S IDENTITY. 

- Authorization is the process of allowing an authenticated user ACCESS to resources.

**Authentication is always done before Authorization.**

![Auth](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Authentication_Authorization.PNG)

</blockquote>

</details>

---

6. What is the difference between ViewData, ViewBag & TempData?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- ViewData & ViewBag are used to pass data from **CONTROLLER TO VIEW**.
- TempData is used to pass data from **CONTROLLER TO CONTROLLER**.
- ViewData REQUIRES TYPECASTING for complex data types whereas ViewBag **DOESN’T REQUIRE TYPECASTING** for the complex data type

</blockquote>

</details>

---

7. What is Bundling and Minification in MVC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

**BUNDLING** - It lets us combine multiple JavaScript (.js) files or multiple cascading style sheet (.css) files, so that they can be downloaded as a unit, rather than making individual HTTP requests.
**MINIFICATION** - It squeezes out whitespace and performs other types of compression to make the downloaded files as small as possible. 

</blockquote>

</details>

---

8. What are the folders in ASP.NET MVC Application Solutions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

**Understanding the folders**:

When you create a project a folder structure gets created by default under the name of your project which can be seen in solution explorer. Below i will give you a brief explanation of what these folders are for.

**Model**
This folder contains classes that is used to provide data. These classes can contain data that is retrived from the database or data inserted in the form by the user to update the database.

**Controllers**
These are the classes which will perform the action invoked by the user. These classes contains methods known as "Actions" which responds to the user action accordingly.

**Views**
These are simple pages which uses the model class data to populate the HTML controls and renders it to the client browser.

**App_Start**
Contains Classes such as FilterConfig, RoutesConfig, WebApiConfig. As of now we need to understand the RouteConfig class. This class contains the default format of the url that should be supplied in the browser to navigate to a specified page.

</blockquote>

</details>

---

9. What is View? Explain its types?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In ASP.NET Core, a view is a user interface component that is responsible for rendering data to the user. Views are used to generate the HTML that is sent to the client's web browser, and they are typically defined using a combination of HTML and server-side code.

There are two main types of views in ASP.NET Core:

**Razor Views**: Razor views are the most common type of view in ASP.NET Core. They are defined using a combination of HTML and Razor syntax, which allows server-side code to be embedded directly into the HTML.

**Razor Pages**: Razor Pages are a newer type of view in ASP.NET Core that allow developers to define UI and server-side logic in a single file. Unlike Razor views, which are typically divided into separate view and controller files, Razor Pages combine both the view and the controller into a single file.

</blockquote>

</details>

---
 








