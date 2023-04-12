1. How to implement Angular testing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>
   Angular testing is implemented using Karma and Jasmine.
   
  - The `ng test` command is used to run the tests.
  - Karma checks for `component_name.spec.ts` file to run the tests.
  - Jasmine has inbuilt funtions like `describe()` and `it()` to write tests.
  
  </blockquote>
</details>

---

2. What is Angular restricted routing?
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Angular restricted routing is used to implemenent Autentication and Role based authorization in an application.

 To implement Angular restricted routing, one can use the Angular Router's canActivate guard to check if a user has the necessary permissions to access a particular route. If the user is not authorized, the guard can redirect them to a different route or display an error message.

  </blockquote>
</details>

---

3. Why do we use the Routing Module in Angular?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Routing module is used to navigate between different components in an Angular application.

  </blockquote>
</details>

---

4. What is the advantages of a SPA application?

<details><summary><b>Show Answer</b></summary>

SPA (Single Page Application) is a web application that dynamically rewrites a single web page with new data from the server.

### The advantages of using SPA's are:

- **Quick loading time**: Unlike MPA (Multi-page application) HTML page is loaded only once in SPA.
- **fluid user experience**: SPA's provide an experience like a desktop or mobile app.
- **Ease in building feature-rich apps**: Adding new features to a web application is easy in SPA.
- **Less bandwidth use**: SPA's load page only once. So, they consume less bandwidth.

 <blockquote>

  </blockquote>
</details>

---

5. How would you test an Angular component?

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 To test an Angular component, you need have a `component_name.spec.ts` file, write tests for the component's logic and template by using the functions like `describe()` and `it()`, run the tests using `ng test` command, and debug any issues that arise.

  </blockquote>
</details>

---

6. Can you extend Angular components (like Java classes)?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Every Angular component has a TypeScript class, which can be extended by other TypeScript classes. So, all the functionalities of a componenet mentioned in the class can be inherited by extending the class.

  </blockquote>
</details>

---

7. Tell me about Typescript and Angular and what you liked/disliked about it?

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 **TypeScript:** TypeScript is a powerful and flexible language that combines the best features of JavaScript with additional features that improve code quality and developer productivity like Optional static typing, Object-oriented programming, Better tooling and editor support, Code readability etc.

 **Angular:** Angular is a framework built on TypeScript.

 Few advantages of Angular are:

 1. Developing Large scale dynamic applications

   - Reusable components make it easier to build and manage complex architecture and dynamic elements.

2. Developing PWAs and SPAs

   - Progressive Web Applications (PWA): A website that is similar to a mobile app is called PWA. The goal of PWA is to blur the gap between native apps and the mobile web.

   - Single Page Application (SPA): A single page application is a web app which is built with multiple components, unlike normal web pages, SPA's are loaded only once and they improve the user experience by avoiding multiple web pages and waiting time to load the webpages.

3. Developing cross-platform applications

   - Angular web apps are compatible with both desktop and mobile.

4. You have a massive project with massive team

   - Many developers can work on the same Angular project without any maintenance and error debugging issues.

  </blockquote>
</details>

---

8. How do you connect your angular application with the backend?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

 The Angular application communicates with the backend using HttpClient Module. The HTTP methods like post, get, delete and patch are used to send a HTTP request to the backend and get the response. Normally these methods are written in a Service which can be injected in any Angular component.

  </blockquote>
</details>

---

9. How you show data in your view in angular?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

The ways to show data in a view are:

**One way binding**

1. Text Interpolations: Text interpolation is a one-way transfer of data from a TypeScript file in a model to an HTML template.
2. Property Binding: The properties of HTML elements in the template can be dynamically modified by transferring data from TypeScript. it is used to set a specific element property.
3. Event Binding: Listens for an element change event. Mostly event binding is used to listen to user actions.

**Two way binding**

Conventionally two-way binding is achieved by combining property binding/text interpolation and event binding, but in Angular, this is achieved by "[()]". Two-way binding is used to listen for events and update values.

**Directives**

Angular comes with built-in directives that allow you to add additional functionality to your HTML elements. Structural directices, attribute directives and component directives are the different types of built-in directives.

  </blockquote>
</details>


10. How many data bindings does angular have? and explain.

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 In Angular there are two types of data binding

**One way binding**

1. Text Interpolations: Text interpolation is a one-way transfer of data from a TypeScript file in a model to an HTML template.
2. Property Binding: The properties of HTML elements in the template can be dynamically modified by transferring data from TypeScript. it is used to set a specific element property.
3. Event Binding: Listens for an element change event. Mostly event binding is used to listen to user actions.

**Two way binding**

Conventionally two-way binding is achieved by combining property binding/text interpolation and event binding, but in Angular, this is achieved by "[()]". Two-way binding is used to listen for events and update values.

  </blockquote>
</details>

---

11. What is a component in angular?

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Components are building blocks of Angular applications. `@Component`, is the component decorator which marks the class as an Angular component and provides metadata about how the component works during the runtime.

A component consists of:
1. An HTML template.
2. A CSS selector.
3. Optional CSS Styles applied to the template
4. A TypeScript class that defines the behaviour of the component.

  </blockquote>
</details>

---

12. How does data pass between two components?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

There are multiple ways to pass data betweeen two components in Angular. 

**1. Parent and Child components:**

Angular uses `@Input` and `@Output` decorators to flow data between components. If we have to pass data into a component we use the `@Input` decorator, and if we have to emit the event or data from a component we use the `@Output` decorator with the `EventEmitter` API.

**2. Services:**

A service is a singleton object that can be injected into multiple components. Components can then use the service to retrieve or update data, and the service can keep track of the state of the data.

**3. RxJS**

RxJS is a reactive programming library that can be used in Angular to pass data between components. RxJS provides observable and subscriber patterns that can be used to asynchronously pass data between components.

  </blockquote>
</details>

---

13. What is a service in angular?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

**Service** : A TypeScript class to share data or functionality throughout the application.

Uses of service:

- Code reuse
- Cross-component communication


  </blockquote>
</details>

---

14. Describe how angular work.
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Angular is a framework built on TypeScript. Angular includes:

- A component-based framework to create single-page applications and scalable applications.
- A collection of well-defined libraries that include many features like routing, and client-server management etc.
- Tools to develop, build, test and deploy a front-end application.

  </blockquote>
</details>

---

15. How does the angular framework connect to the database? 

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Angular application is not directly connected to the database. The Angular application sends HTTP requests to the Backend application which is connected to the database. The backend will perform the necessary operations and provides the response to the Angular applcation.

  </blockquote>
</details>

---

16. The difference between angular and reactjs.

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Angular and React are both popular front-end development frameworks used to build dynamic and interactive web applications. 

The differences between Angular and react:

1. **Language:** Angular is written in TypeScript, a superset of JavaScript that adds static type checking and other features, while React is written in plain JavaScript.

2. **Architecture:** Angular follows a component-based architecture where everything is a component, including services and directives, while React uses a more functional approach where components are defined as functions.

3.  **Data binding:** Angular uses two-way data binding, where changes in the model are automatically reflected in the view and vice versa, while React uses one-way data binding, where data flows from parent components to child components.

4. **Template system:** Angular uses an HTML-based template system with special syntax and directives for dynamic rendering, while React uses a JSX syntax that allows developers to write HTML-like code directly in their JavaScript.

5. **State management:** Angular comes with built-in state management tools like RxJS and ngRx, while React relies on third-party libraries like Redux or the newer Context API for state management.

  </blockquote>
</details>

---

17. What are the benefits of angular over react and vice versa.


<details><summary><b>Show Answer</b></summary>

 <blockquote>

### Benefits of Angular :

- **Comprehensive framework:** Angular is a complete framework that comes with everything you need to build a web application, including routing, state management, and testing tools. This means that developers don't need to spend time choosing and integrating different libraries, making it a good choice for large and complex projects.

- **Strong typing:** Angular is written in TypeScript, a superset of JavaScript that adds static typing and other features to the language. This makes it easier to catch errors at compile time and maintain large codebases.

- **Dependency injection:** Angular's built-in dependency injection system makes it easy to manage dependencies between components and services.

- **Performance:** Angular's change detection mechanism is highly optimized, So it's suitable for large and complex applications.

### Benefits of React:

**Virtual DOM:** React uses a virtual DOM, which is a lightweight representation of the actual DOM. This allows React to efficiently update only the parts of the DOM that have changed, leading to better performance.

**Flexibility:** React is a lightweight library that can be used with other libraries and frameworks. This makes it a good choice for smaller projects and for integrating with existing codebases.

**JSX:** React's use of JSX, a syntax extension that allows you to write HTML-like code in JavaScript, makes it easier to write and read complex UI components.


  </blockquote>
</details>

18. What is the difference between typescript and javascript?
  

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Few differnces between TypeScript and JavaScript are:

 1. TypeScript is a statically typed language that is a superset of JavaScript. Where as JavaScript is dynamically typed.
 2. TypeScript has type annotations, which help catch errors at compile-time rather than at runtime, making it easier to catch bugs and improve the overall quality of code. 
 3. TypeScript also supports object-oriented programming features such as classes and interfaces. JavaScript is not class based object oriented programming language.



  </blockquote>
</details>

---

19.  What are the parts of a Component in Angular?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Components are building blocks of Angular applications.

The parts of the component are:
1. An HTML template.
2. A CSS selector.
3. Optional CSS Styles applied to the template
4. A TypeScript class that defines the behaviour of the component.

  </blockquote>
</details>

19. How to create angular components dynamically?


<details><summary><b>Show Answer</b></summary>

 <blockquote>

 
Loading components during runtime is called Dynamic component loading.

Procedure to load components dynamically

1. Creating and Anchor Directive: 

Before adding components, It is necessary to define an anchor point to tell Angular where to insert components.

2. Loading Components:

Using `<ng-template>` and the Anchor directive selector, you can inform Angular where to dynamically load components.

3. Resolving components:

Using an array of components or by conditions or user actions the components can be loaded dynamically.

  </blockquote>
</details>
 
 ---

20. What are decorators in angular give an example.

<details><summary><b>Show Answer</b></summary>

 <blockquote>
Decorators are a way to annotate and modify classes, properties, and methods. They are used to add metadata and provide additional functionality to classes or class members.
 
There are four types of decorators in Angular:

1. Class Decorators: The class decorator as name imples is used to provide metadata about classes. `@Component` and `@NgModel` are examples of class decorators.
2. Property Decorators: Property decorators are used to decorate the specific properties within the classes. `@Input` and `@Output` are examples for property decorators.
3. Method Decorators: Method Decorator is applied for specific methods within your class with functionality. `@HostListener` is an example for method decorator.
4. Parameter Decorators: Paramater decorators are used for paramaters present in a constructor of a class. `@Inject` is an example for paramater decorator.

  </blockquote>
</details>

21. 

<details><summary><b>Show Answer</b></summary>

 <blockquote>



  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
  
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  </blockquote>
</details>
