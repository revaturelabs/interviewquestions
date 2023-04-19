## Technical

1. What is Asp.Net Core?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

ASP.NET Core is a cross-platform, high-performance, open-source framework for building modern, cloud-enabled, Internet-connected apps. With ASP.NET Core, you can: Build web apps and services, Internet of Things (IoT) apps, and mobile backends.

</blockquote>

</details>

---

2. What is the role of `Program.cs` file in ASP.Net Core? (or) What is CreateHostBuilder/CreateDefaultBuilder ? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`Program.cs` fille is the entry point of application via `Main()` method. 

![Img1](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Program_cs.PNG)

`CreateHostBuilder` and `CreateDefaultBuilder` method prepare the default settings for web server for the application.

![Img2](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/ASPNET_CreateHostBuilder.PNG)

</blockquote>

</details>

---

3. What is the role of `Startup.cs` file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Inside `Program.cs` file, UseStartup method redirects the request to `Startup.cs` file. `Startup.cs` class does two things:

![starup.cs](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/startupcs.PNG)

1. It configures the SERVICES which are required by the app by using `ConfigureServices` Method.
2. It defines the app's REQUEST HANDLING PIPELINE as a series of middleware components by using `CONFIGURE` method.

</blockquote>

</details>

---

4. What is the role of `ConfigureServices` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `ConfigureServices` method called before the `Configure` method to configure the APP'S SERVICES.
- It is an OPTIONAL method.

For example, your application at some point can use Views then the below method `services.AddControllersWithViews()` will help in configuring that. Now it is not mandatory that every request will return the output as a view so therefore it is optional. A request may use it or may not.

```C#

// This method gets called by the runtime.
// Use this method to add services to the container.

public void ConfigureServices(IServiceCollection services)
{
    services.AddControllersWithViews();
}

```

</blockquote>

</details>

---

5. What is the role of `Configure` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `Configure` method specifies how the app responds to HTTP request and response. It is used to setup request pipeline.
- It is not optional.
- For example, in below example when the request will arrive, it will go through all the methods present inside `Configure` method one by one. Every request will go through all these methods or we also call them middleware 
so that’s why we say Configure methods are not optional where as `ConfigureServices` methods are optional.

``` C#
// This method gets called by the runtime
// Use this method to configure the HTTP request pipeline.

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if(env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }
    else
    {
        app.UseExceptionHandler("/Home/Error");
    }
    app.UseStaticFiles();
    app.UseRouting();
    app.UseAuthorization();

    app.UseEndPoints(endpoints =>
    {
        endpoints.MapControllerRoute(
            name:"default",
            pattern:"{controller=Home}/{action=Index}/{id?}"
        );
    });
}

```

</blockquote>

</details>

---

6. What is the difference between ConfigureServices & Configure method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- `ConfigureServices` is an optional method used to register dependent classes/services inside the DI container - `Configure` method specifies how the app responds to HTTP request and respond. It is used to add MIDDLEWARE components or to set request pipeline. It is not optional.
- `ConfigureServices` method called before the `Configure` method to configure the APP'S SERVICES

</blockquote>

</details>

---

7. What is Dependency Injection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

ASP.NET Core supports the dependency injection (DI) software design pattern, which is a technique for achieving Inversion of Control (IoC) between classes and their dependencies.

</blockquote>

</details>

---

8. Why to use Dependency Injection? (or) What problems does Dependency Injection solve?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Dependency injection decouples the two components or classes.

For example, A is a class here and B class is the dependency, so one way to use the 
dependency is to create the object like shown below:

``` C#

public class A
{
    public static void Main(String[] args)
    {
        B b =new B();
        int a =b.MethodB();
        Console.WriteLine(a);
    }
}

```

``` C#

public class B
{
    public int MethodB()
    {
        return 100;
    }
}

```

- But now if we want to replace MethodB of B class with MethodC then we have to change the main method also right? Which is a testing impact.
- So by using dependency injection we can use interfaces and design the classes in a manner that Main method needs not to be changed for any change in class B.
- That will decouple these classes and that is the main agenda of dependecy injection.

</blockquote>

</details>

---

9. What are the types of Dependency Injection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Dependency injection can be done in various ways. Below are the ways dependency injection can be done:

1. Constructor Injection
2. Property Injection
3. Method Injection

Dependency injection can be achieved with the help of any one of these injections.

</blockquote>

</details>

---

10. How to use Dependency Injection in views in ASP.Net Core?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A service can be injected into a view using the `@inject` directive. 
- For example, here IStudent is injected in the view.

``` C#
@{
    ViewData["Title"]="Home Page";
}
@inject WebApplication1.IStudent _student

<div class="text-center">
    <h1 class="display-4">Welcome</h1>
    Total Student: @_student.GetStudentCount();
</div>

```
</blockquote>

</details>

---

11. What is AddSingleton, AddScoped and AddTransient method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`AddSingleton` - AddSingleton method create only one instance when the service is requested for first time. And then the same instance will be shared by all different http requests.

For example, in below code the Logger instance will be shared between multiple requests.

``` C#

// This method gets called by the runtime.
// Use this method to add services to the container.

public void ConfigureServices(IServiceCollection services)
{
    services.AddSingleton<ILogger, Logger>();
    // services.AddSingleton<IPayment,Payment>();
    // services.AddTransient<IDataAccess,DataAccess>();
}

```

`AddScoped` - AddScoped method create single instance per request. For every individual request there will be a single instance or object.

In below code, AddScoped method will make sure that Payment class instance will remain specific to a specific request and will not be shared between multiple requests. 

``` C#

// This method gets called by the runtime.
// Use this method to add services to the conatiner.

public void ConfigureServices(IServiceCollection services)
{
    //services.AddSingleton<ILogger, Logger>();
    services.AddScoped<IPayment, Payment>();
    //services.AddTransient<IDataAccess,DataAccess>();
}

```

`AddTransient` - AddTransient instance will not be shared at all even with in the same request.
Every time a new instance will be created.

``` C#

// This method gets called by the runtime.
// Use this method to add services to the conatiner.

public void ConfigureServices(IServiceCollection services)
{
    //services.AddSingleton<ILogger, Logger>();
    //services.AddScoped<IPayment, Payment>();
    services.AddTransient<IDataAccess,DataAccess>();
}

```

</blockquote>

</details>

---

12. What is middleware in ASP.Net Core?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A middleware is nothing but a component (class) that is executed on EVERY REQUEST in the ASP.NET Core application. 

- We can set up the middleware in ASP.NET using the CONFIGURE method of our STARTUP class like shown below.
- All these methods – UseDeveloperExceptionPage, UseStaticFiles, UseRouting etc are middlewares.

``` C#
// This method gets called by the runtime
// Use this method to configure the HTTP requesr pipeline.

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if(env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }
    else
    {
        app.UseExceptionHandler("/Home/Error");
    }
    app.UseStaticFiles();
    app.UseRouting();
    app.UseAuthorization();
    app.UseEndpoints(endpoints =>
    {
        endpoints.MapControllerRoute(
            name:"default",
            pattern:"{controller=Home}/{action=Index}/{id?}");
    });

}

```

</blockquote>

</details>

---

13. How ASP.Net Core middleware is different from HTTPModule?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

If you have worked in asp.net webforms then you might have heard of HTTPModules.
Middleware almost behave similar to HTTPModule, as they both are the part of request pipeline

![Middleware_HttpModule](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/HttpModule_Middleware.PNG)

</blockquote>

</details>

---

14. What is Request Delgates?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Request delegates handle each HTTP request and are used to BUILD request pipeline by using RUN, MAP and USE extension methods. 

Below is the diagram of a request and the purpose of Use and Run method.

![Request_delegate](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Request_Delgate.PNG)

</blockquote>

</details>

---

15. What are the main JSON files available in ASP.Net Core?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`Global.json` - You can define the solution level settings in `global.json` file for example your application name and version.
`Launchsettings.json` – You can set the environment variables in this file. For example, set development or production environment in this file.
`Appsettings.json` – Configuration settings like database connection string can be set in this file. Similar to web.config in ASP.NET.
`Project.json` - ASP.NET Core uses Project.JSON file for storing all project level configuration settings. For example the nugget packages you have installed in the project.

</blockquote>

</details>

---

16. What is the difference between `Appsetting.Json` and `LaunchSetting.Json` file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`Appsetting.Json` store the configurations which are required when your application is running. For example, database connection string is used when application is running.

But `Launchsetting.Json` store the configuration which are required to start the application.For example, what will be application url, that can be configure here.

</blockquote>

</details>

---

17. What is caching in ASP.Net Core?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Caching refers to the process of storing frequently used data in cache, so that that data can be served much faster for any future requests. 

Below is the flow of the caching in normal scenarios

![caching](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Caching.PNG)

</blockquote>

</details>

---

18. What is CROSS-ORIGIN Requests (CORS) in ASP.NET Core? (or) Why CORS restriction is required? (or) How to fix CORS error?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

As the name suggests Cross Origin Resource Sharing – meaning the data or resource sharing between different or cross domains is not enabled by default. 

This is restricted.

Below are the cases when CORS will allow and disallow the response:

![Cases](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/CORS_Causes.PNG)

Above in first case the response will be fine, but in next four cases the response will not be sent:

1. First case is when you want to get the response from a different domain.
2. Second case is when you want to get the response from a subdomain.
3. Third case is when the domain is same, but you are requesting from http and the sender is https.
4. And in last case, if the port is different.


In all 4 cases above you will receive the below error:

![error](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/CORS_ERROR.PNG)

CORS is good because of security reason. Your API is secure by default otherwise any external website can try to access your data.

Now how to remove this CORS restriction? For that you have to do the two things:

1. Add Microsoft.AspNetCore.Cors nuget package to your project then
2. In startup class, edit the Configure and ConfigureServices method like this

![code](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/CORS_CODE.PNG)

</blockquote>

</details>

---

19. How Routing works in ASP.NET Core?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Routing in ASP.NET Core is the process of mapping incoming requests to the appropriate controller action method. ASP.NET Core routing works by using the Routing Middleware, which is responsible for matching incoming URLs to registered routes. Routing Middleware takes a URL and tries to find a matching route in the RouteCollection.

</blockquote>

</details>

---

20. How Logging works in .NET Core and ASP.NET Core?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Logging is an important feature of any application, and .NET Core and ASP.NET Core provide a powerful and flexible logging framework that makes it easy to log application events and errors.

The logging framework in .NET Core and ASP.NET Core is based on the ILogger interface, which defines a set of methods for logging different types of messages, including debug, information, warning, and error messages. To use the logging framework in your application, you need to create an instance of the ILogger interface and call the appropriate logging method based on the severity of the message.

</blockquote>

</details>

---

21. Describe the Servers in ASP.NET Core.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

ASP.NET Core supports multiple server options to host and run your web applications.

**Kestrel Server**: Kestrel is the default and recommended server for ASP.NET Core. It's a cross-platform, lightweight, and fast server that can handle thousands of connections concurrently.
**HTTP.sys Server**: HTTP.sys is a Windows-only server that is optimized for handling requests on Windows operating systems.
**IIS Server**: You can also host your ASP.NET Core application on IIS by using the ASP.NET Core Module. 
**Nginx Server**: Nginx is a popular open-source reverse proxy server that can be used to host ASP.NET Core applications. 

</blockquote>

</details>

---

22. How do you do Validation in Asp.Net core?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In ASP.NET Core, there are several ways to perform validation, including client-side validation, server-side validation, and model binding validation. Here are some approaches for performing validation in ASP.NET Core:

**Client-side validation**: Client-side validation is performed in the user's web browser using JavaScript. ASP.NET Core includes support for client-side validation through the use of jQuery Validation, which is a popular client-side validation library. By using the jquery.validate.unobtrusive.js script, ASP.NET Core can automatically generate client-side validation code based on server-side validation attributes. This approach can provide immediate feedback to the user without requiring a round-trip to the server.

**Server-side validation**: Server-side validation is performed on the server, after the data has been submitted by the user. In ASP.NET Core, server-side validation can be performed using the built-in validation attributes, such as `[Required]`, `[StringLength]`, and `[RegularExpression]`. These attributes can be added to model properties to enforce validation rules. To perform server-side validation, the ModelState dictionary can be used to store validation errors and display them to the user.

**Model binding validation**: Model binding validation is performed during the model binding process, which is responsible for mapping the HTTP request data to a model object.

</blockquote>

</details>

---




