1.	Demonstrate a basic understanding of Angular or What is Angular

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Angular is a typescript-based web application framework used to create & build web apps
- It allows us to create Single Page Application (SPA)
- Gmail, Youtube, PayPal apps are developed using Angular

</blockquote>
</details>

--- 

2. What is meant by SPA?

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>

- It is a single web page, website, or web application that works within a web browser and loads just a single document.
- It does not need page reloading during its usage, and most of its content remains the same while only some of it needs updating.
- **Gmail**, **Facebook**, **Trello**, **Google Maps**, etc., all are Single Page Applications that offer an outstanding user experience in the browser with no page reloading.

</blockquote>
</details>

--- 

3. Angular workflow or How does Angular work or bootstrapping your angular app?

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Flow: `angular.json`-> `main.ts` -> `AppModule` -> `AppModule` -> `index.html`.
- Every Angular app consists of a file named `angular.json` . This file will contain all the configurations of the app. While building the app, the builder looks at this file to find the entry point of the application.

![image](https://user-images.githubusercontent.com/103101208/185569359-55632ef6-971e-47d9-a7bf-96a1de37026e.png)
  
- Inside the build section, the main property of the options object defines the entry point of the application which in this case is `main.ts`.
- `main.ts` is the entry point of the angular application. 
- The `main.ts` file creates a browser environment for the application to run, and, along with this, it also calls a function called bootstrapModule, which bootstraps the application. These two steps are performed in the following order inside the `main.ts` file:
	
![image](https://user-images.githubusercontent.com/103101208/185569651-35a2ba9f-73fc-43c6-8548-0a24daac640b.png)
- In the above line of code, `AppModule` is getting bootstrapped.
- The `AppModule` is declared in the `app.module.ts` file. This module contains declarations of all the components.
- Below is an example of `app.module.ts` file:
	
![image](https://user-images.githubusercontent.com/103101208/185569778-9ff0d34a-b0e2-4701-a1db-21919ebd3ad7.png)
	
- As one can see in the above file, `AppComponent` is getting bootstrapped.
- This component is defined in `app.component.ts` file. This file interacts with the webpage and serves data to it.
- Below is an example of `app.component.ts` file:
  
 ![image](https://user-images.githubusercontent.com/103101208/185569886-8ca076a7-6633-4d61-beb5-0d673014b347.png)

- After this, Angular calls the `index.html` file. This file consequently calls the root component that is `app-root`. 
- This is how the `index.html` file looks:
	
![image](https://user-images.githubusercontent.com/103101208/185569990-6c67e5b0-d9a6-4340-b2f0-dcd9a9f738c5.png)
	
- The HTML template of the root component is displayed inside the `<app-root>` tags.
- This is how every angular application works. Or This is how angular application get bootstrapped

  </blockquote>
</details>
	
--- 
  
4. How SPA is different from tradtional web application?
<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
- In traditional web technology, the client requests for a web page (HTML/JSP) and the server sends the resource (or HTML page), and the client again requests for another page and the server responds with another resource. 
- The problem here is a lot of time is consumed in the requesting/responding or due to a lot of reloading. 
- Whereas, in the SPA technology, we maintain only one page (`index.html`) even though the URL keeps on changing. 

  </blockquote>

</details>
  
 ---
  
5. Have you used Angular in your project. Can you list some of the features of Angular.
  
<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Yes, used Angular.
	
- Angular written using TypeScript
- Angular uses Databinding and Routing
- Angular uses Jasmine testing framework

</blockquote>
</details>
  
 ---
  
6. In SPA, after the initial page load, does the server send any more HTML to you?
<details>
<summary><b>Show Answer</b></summary>
<blockquote>

On a SPA, after the initial page load, no more HTML gets sent over the network. Instead, only data gets requested from the server (or sent to the server).
	
</blockquote>
</details>
  
 ---
  
8. Does refreshing a whole page needed in SPA?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

In a SPA, a page refresh never occurs; instead, all necessary HTML, JavaScript, and CSS code is either retrieved by the browser with a single page load,or the appropriate resources are dynamically loaded and added to the page as necessary, usually in response to user actions.
	
</blockquote>
</details>
  
---
  
9. What are some advantages of Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Effective cross platform development
- Two-way data binding in Angular will help users to exchange data from the component to view and from view to the component.  It will help users to establish communication bi-directionally. 
- The Angular command-line interface (CLI) makes the developer’s job easier because it offers a set of helpful tools for coding. 
- Angular offers powerful DI (dependency injection) instrument and services to resolve various productivity issues and speed up the development process.
- Modularity of angular application makes our code readable and testable

</blockquote> 

</details>
	
--- 
	
10. What do you choose between Traditional Web Apps and Single Page Apps _or_ What do you choose between Multiple Page Apps and Single Page Apps
	
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
Choose based on the explanation given
</blockquote> 
	
<details>
<summary><b>Explanation</b></summary>
<blockquote>	
Use traditional web applications or MPA when:
- Your application's client-side requirements are simple or even read-only.
- Your application needs to function in browsers without JavaScript support.

Use a SPA when:

- Your application must expose a rich user interface with many features.
- Your team is familiar with JavaScript, or TypeScript.
- Your application must already expose an API for other (internal or public) clients.

Both SPA and MPA are not flawless as they obviously have their pros and cons. SPA is the best choice if you care about **speed and code reusability** that can be applied to develop a **mobile app**. However, it has deficiencies in SEO optimization. MPAs win in case you strive to be **ranked higher in Google**, and it is more scalable but much slower than single-page applications.

Choosing the best option, you should always have your business goals and requirements in mind.

</blockquote> 
</details>
</details>

---

11. How SPA different from MPA?
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
A SPA is an app that works inside a browser and does not require page reloading during use.

On the other hand, a MPA (multiple page application) is considered a more traditional approach to app development. The multi-page design pattern requires a page reload every time the content changes. It’s a preferred option for large companies with extensive product portfolios, such as e-commerce businesses.	
	
</blockquote> 
</details>

---

12. Difference between Angular JS and Angular 4 +

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

| **Angular JS**                                                                                     | **Angular 4**                                                                                                                    |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Uses MVC architecture to build the applications.                                                   | Uses component-based UI to build the applications.                                                                               |
| AngularJS is written in JavaScript.                                                                | Angular is compatible with the most recent versions of TypeScript that have powerful type checking and object-oriented features. |
| To bind an image/property or an event with AngularJS, you have to remember the right ng directive. | Angular focuses on “()” for event binding and “\[ \]” for property binding.                                                      |
| AngularJS doesn't support mobiles.                                                                 | Angular support mobiles.                                                                                                         |

</blockquote>

</details>
	
--- 

13. Difference between Angular 2 and Angular 4

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

| **Angular 2**                                                                      | **Angular 4**                                                                                       |
| ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Angular v2.0 uses Typescript, superset of JavaScript, for writing the application. | Angular v4.0 serves to be compatible with the new version of TypeScript 2.1 as well TypeScript 2.2. |
| Code is not Reduced much                                                           | Reduce the size of the generated bundled code up to 60%                                             |

</blockquote>

</details>
	
--- 

14. What are some common Angular CLI commands?
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
- `ng  new MyApp` – used to create an angular application named ‘MyApp’
- `ng new MyApp  --routing`  - used to create an angular application named ‘MyApp’ with the routing module
- `ng g c first` – used to create component named ‘first’
- `ng g p changePipe` – used to create pipe named `changePipe’
- `ng g s user` -  used to create service named ‘user’
- `ng serve` – used to build, run and launch application on HTTP port 4200
- `ng serve -o` -  used to build, run and launch application on HTTP port 4200, -o option automatically opens the browser to [ http://localhost:4200]( http://localhost:4200)
	
</blockquote>
</details>
	
--- 
	
15. What `ng` means?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
- `ng` stands for A**ng**ular
	
</blockquote>
</details>
	
--- 
	
16. List drawbacks and benfits of MPA _or_ List the advantages and disadvantages of MPA

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
Benefits:
- Performs well on the search engine.
- Provides a visual map of the web app to the user.

Drawbacks:
- Comparatively complex development
- Coupled backend and frontend
	
</blockquote>
</details>
	
--- 
	
17. List drawbacks and benfits of SPA _or_ List the advantages and disadvantages of SPA

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
Benefits:
- Single Page Apps are smooth and fast.
- They are easy to develop and deploy.
- SPAs are easier to debug.
- Can be transited to mobile apps by reusing the same backend code.

Drawbacks:
	
- SPAs perform poor on the search engine. But now, with isomorphic rendering/server-side rendering even SPAs can be optimized for search engine too.
- Single page applications provide single sharing link.
- They are less secure compared to traditional multi-page apps because of its cross-site scripting.
	
</blockquote>
</details>
	
--- 

18. What is the latest version of Angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
- Angular 14 (as per August 2022)
</blockquote>
	
<details>
<summary> <b>Reference</b></summary>
<blockquote>

[Angular versioning and releases](https://angular.io/guide/releases)
	
</blockquote>
</details> </details>
	
--- 
	
19. Does Angular support in mobiles?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

 Yes, we can create a mobile application using Angular Framework. 
	
</blockquote>
</details>
	
--- 
	
20. Why do we need Webpack?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- In our web application, we use many javascript files that are added into the HTML pages via `<script>` tags.  For each user request, the browser loads these bunch of script files inside the HTML page. This is inefficient as it reduces the page speed since the browser requests each script file separately.
- This can be solved by **bundling** several files together into one file to be downloaded by the browser in one single request.
- **Module bundlers** are used to bundle a group of JavaScript modules with their dependencies and merge them into a single file in the correct order, which can be executed by the browser.
- **Webpack** is a powerful static module bundler for JavaScript applications that packages all modules in our application into a bundle and serves it to the browser. Webpack builds a dependency graph when it processes the application. 
		
</blockquote>
</details>
	
--- 
	
21. Webpack builds a dependency graph. What does that mean?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- Any time one file depends on another, webpack treats this as a dependency. This allows webpack to take images or web fonts, and also provide them as dependencies for your application.

- When webpack processes your application, it starts from a list of modules defined on the command line or in its configuration file. Starting from these entry points, webpack recursively builds a dependency graph that includes every module your application needs, then bundles all of those modules into a small number of bundles - often, only one - to be loaded by the browser.
		
</blockquote>
</details>
	
--- 

22. 
	
