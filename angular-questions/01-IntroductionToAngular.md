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

  

</blockquote>
</details>
  
 ---
  
6. In SPA, after the initial page load, does the server send any more HTML to you?
<details>
<summary><b>Show Answer</b></summary>
<blockquote>


</blockquote>
</details>
  
 ---
  
8. Does refreshing a whole page needed in SPA?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>


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
	
10. What do you choose between Traditional Web Apps and Single Page Apps
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
Choose based on the explanation given
</blockquote> 
<details>
<summary><b>Explanation</b></summary>
Use traditional web applications when:
- Your application's client-side requirements are simple or even read-only.
- Your application needs to function in browsers without JavaScript support.

Use a SPA when:

- Your application must expose a rich user interface with many features.
- Your team is familiar with JavaScript, TypeScript, or Blazor WebAssembly development.
- Your application must already expose an API for other (internal or public) clients.

Additionally, SPA frameworks require greater architectural and security expertise.

</blockquote> 
</details>
</details>

---

	
	
