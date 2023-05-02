1. Angular data binding.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Data binding in angular is a way of connect data between component and view. So that changes made in one are automatically reflected in the other. There are four types of data binding in Angular such as interpolation, property binding, event binding, and two-way binding.

</blockquote>

</details>

---

2. what is ngModel.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `ngModel` is an Angular directive that provides two-way data binding. It is used to bind the value of an HTML form element to a variable in the component. With `ngModel` any changes made to the input value will be reflected in the component's variable, and changes to the variable will be reflected in the input field.

For example,

```HTML
<input [(ngModel)]="username" name="username" type="text">
```

In the above example, the input field is binded with the username variable present inside the component.

</blockquote>

</details>

---


3. observables vs promises

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An observable and a promise both are used to handle asynchronous operations, but they have differences.

| Promise | Observable | 
| :---------------: | :---------------: | 
|  Promises represent a single value or an error that will be available in the future. | Observables can represent a stream of multiple values that will be available in the future. |  
|  Promises can only be resolved or rejected once. | Observables can emit values multiple times. | 
|  You can chain multiple promises using `.then()` and `.catch()` methods. | Observables can also be chained using methods like `map()`, `filter()`, and `reduce()` | 
|  Promises are not cancellable once they are initiated. | Observables are cancellable using the `unsubscribe()` method. | 
|  Promises are eager, which means they are executed immediately when they are created. | Observables are lazy, which means they only start executing when someone subscribes to them. | 
|  Promises use the `catch()` method to handle errors | Observables use the error callback function. | 


</blockquote>

</details>

---


4. what is Node and why it's used.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Node.js is a JavaScript runtime environment built on the V8 JavaScript engine that allows developers to run JavaScript code outside of a web browser. It is lightweight and efficient, making it well-suited for building real-time applications that require high concurrency and scalability. Node.js also provides a rich set of libraries and frameworks that simplify the development process.

</blockquote>

</details>

---


5. what are promises

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A Promise is used to handle asynchronous operations. To understand a Promise in a simpler way, we can consider it as a placeholder for future upcoming values or errors. Promises have three states called pending, fulfilled, or rejected. 

When a Promise is in the pending state, it means that the operation is still in progress and we have not yet received the result. When a Promise is fulfilled, it means that the operation has completed successfully, and the result is available. When a Promise is rejected, it means that the operation has failed and has given us an error. Promises use the `then()` and `catch()` methods to handle the results. 

</blockquote>

</details>

---

6. what are callback functions.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A callback function is a function that is passed as an argument to another function. It is commonly used in JavaScript to handle asynchronous operations like making an HTTP request. 

example for a callback function,
```js
function add(a, b, callback) {
  const result = a + b;
  callback(result);
}

add(3, 4, function(sum) {
  console.log('sum :', sum);
});

```

In this example, we created a function called add that takes two numbers and a callback function as arguments. Inside the function, we calculate the sum of a and b, and then call the callback function and pass the result to that function.

</blockquote>

</details>

---

7. What is the declarations in app module?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Angular, the declarations array in the `@NgModule` decorator of the `app.module.ts` file is used to specify the components, directives, and pipes that belong to the current module.

</blockquote>

</details>

---

8. Passing data in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are several ways to pass data between components in Angular, such as using `input/output bindings`, `services`, `RxJS`, `routing parameters`, and `ViewChild`. `Input and output bindings` are used to pass data between components that have a parent-child relationship. `Services` are used to share data between multiple components. `RxJS` can be used to pass data to components in a reactive way. We can also share data using the URL, and to receive data from the URL we can use `routing parameters`. `ViewChild` is used to access the child component's properties and methods from the parent component.

</blockquote>

</details>

---

9. Which decorator is used to declare module in angular

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `@NgModule` decorator is used to define a module. The `@NgModule` decorator takes an object as its argument, which includes several properties that define the module's configuration like `declaration`, `imports`,`providers`, and `exports`.

To declare a module using `@NgModule`, you need to create a new TypeScript class, decorate it with `@NgModule`, and then configure the module by setting its properties in the decorator's argument.

for example,
```ts
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  exports: [
   AppComponent
  ]
})
export class AppModule { }

```


</blockquote>

</details>

---

10. What are some features you used in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The feature which I used in angular are Components, Directives, Services, Dependency injection, Routing, Forms, Pipes, and Observables. The components of angular help the developer to encapsulat each feature in seperate component.  

</blockquote>

</details>

---

11. Create a class component which has an element in it with onClick attribute and a function that is called when that element is clicked.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>


```Ts

import { Component } from '@angular/core';

@Component({
  selector: 'app-home',
  template: 
    `<div>
      <button (click)="handleClick()">Click me!</button>
    </div>`,
  styleUrls: ['./home.component.css']
})
export class HomeComponent {

  handleClick(){
    console.log('Button clicked!');
  }

}

```

In above example, we have created a home component. which contains a button element and when the button is clicked hadleClick() method gets executed.

</blockquote>

</details>

---

12. What is Angular? What is an SPA?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular is a JavaScript framework developed by Google for building web applications. Single Page Application (SPA) is a type of web application that loads a single page and dynamically updates its content without requiring a page refresh. SPAs enhance user experience by providing a smooth and responsive experience to the users. Angular helps developers create SPAs by providing a powerful templating engine, two-way data binding, dependency injection, and a robust router for handling navigation.

</blockquote>

</details>

---

13. What are components in angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Components are the main building block of a web application in Angular. They are self-contained blocks of code that include the HTML template, TypeScript class, and CSS styles to define the view and behavior of a specific part of the application. We use the `@Component` decorator to define a component. Components are reusable and can be composed together to create a complex UI.

</blockquote>

</details>

---

14. How do you get data in Angular to your application using another application’s API?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To get data from another application's API in Angular, you can use the `HttpClient` module to make HTTP requests to the API endpoints. First, import the `HttpClientModule` into your module, then inject the `HttpClient` service into your component or service where you want to make the API request. Next, use the `HttpClient` service's `get()` method to make a `GET` request to the API endpoint and retrieve the data.

</blockquote>

</details>

---

15. What is an observable in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An `Observable` is a stream of data that can be used to handle asynchronous operations. Using observable we can pass the data between different components of angular. `Observables` are similar to `Promises`, but unlike `Promises` that only return a single value, `Observables` can return multiple values over time. Also, Observables are cancelable, which means we can unsubscribe from an Observable if we no longer need to receive updates.

</blockquote>

</details>

---


16. What are some commands in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Angular we have commands like, 

- `ng new <project-name>` : Creates new angular application.
- `ng generate component <component-name>` : Creates a new component with the specified name.
- `ng serve`: Builds and serves the application locally.
- `ng build`: Builds the application for production.
- `ng update`: Updates the application's dependencies to the latest versions.
- `ng deploy`: Deploys the application to a remote server.

</blockquote>

</details>

---


17. How do you do two-way data binding?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To achieve two-way data binding in Angular you can use the `[(ngModel)]` directive. This binds a component property to an input field and synchronizes data in both directions. To use `[(ngModel)]`, create a property in the component class to store the data, bind it to an input field using [(ngModel)]. Any changes made to the input field will be automatically reflected in the property.

</blockquote>

</details>

---


18. What are pipe transform interfaces and have you ever used them? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `PipeTransform` interface is a built-in Angular interface that you can use to create custom pipes. To create a custom pipe first, you have to create a class that will implement the `PipeTransform` interface. In this class, we will create a transform method which defines the functionality of that pipe. You can use the custom pipe by applying it to an expression with the `|` symbol followed by the pipe name. 

</blockquote>

</details>

---


19. How do you use ngfor in Angular? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`ngFor` is a structural directive in Angular that is used to render a list of items in the template based on an array or an iterable object. The `ngFor` can be used as `*ngFor="let item of items"`, where items is an array that contains the items to be rendered, and the item is a variable that represents the current item in the iteration.

</blockquote>

</details>

---


20. what are Angular lifecycle hooks

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular lifecycle hooks are methods that are called at specific stages in the life cycle of an Angular component, such as when it is created, updated, or destroyed. It includes methods like `ngOnInit()`, `ngOnChanges()`, `ngAfterViewInit()`, and `ngOnDestroy()`. 

</blockquote>

</details>

---


21. What are Angular directives and what do they do?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular directive is a type of Angular component that allows you to add custom behavior or attributes to an DOM element. There are three types of directives structural, attribute and custom. Structural directives add or remove elements, attribute directives modify the attributes of an element, and custom directives are used to create custom functionality. Directives are used to build dynamic and interactive web applications.


</blockquote>

</details>

---


22. How to connect an Angular Project to a Spring Boot Project?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To connect an Angular project to a Spring Boot project, you can use RESTful APIs. The Angular project can send HTTP requests to the Spring Boot project, which will handle these requests and return the required data. You can create the RESTful APIs in the Spring Boot project using Spring Web MVC, and then call these APIs from the Angular project using the `HttpClient` module.

</blockquote>

</details>

---


23. Would I do an API call that filters entirely through the backend or get all the information in the frontend, filter it, and return the rest of the data back into the database? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

This depends on the use case and requirements of your application. If you have a large amount of data or the data contains sensitive information filtering the data in the backend will be a good option. If you want to enhance the user experience then filtering the data in the front end can be considered as it will reduce the calls to the backend and improves the response time of the application.

</blockquote>

</details>

---

24. What is the syntax in Angular for creating and submitting a form in HTML?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`ngForm` directive is used to create form element in angular and bind it to a template variable.

For example,

```html
<form #myForm="ngForm" (ngSubmit)="onSubmit(myForm)">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" ngModel required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" ngModel required>

  <button type="submit">Submit</button>
</form>

```
In above example the `ngModel` directive is also used for two-way data binding, which allows you to bind the input value to a variable in the component.

</blockquote>

</details>

---

25. How do you start a server in angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To start an server in angular you can use `ng serve` command.

</blockquote>

</details>

---

26. What is dependency injection in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dependency Injection (DI) in Angular is a feature that allows you to inject dependencies into a component, service or other class. The dependencies that your component or service needs are added in the constructor of the component, and Angular will automatically provide those dependencies when the component or service is instantiated. 

</blockquote>

</details>

---

27. Do you know states and props in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular does not have any states and props. These feature are related to React.

</blockquote>

</details>

---

28. Do you know lazy loading (Angular)?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Angular, lazy loading is a technique where instead of loading all the components and modules of an application at once during its initial loading, we load the modules based on their requirement. It is achieved by configuring the application's routing module to load the components or modules asynchronously when needed using the `loadChildren` property. This approach helps to reduce the initial load time of an application and improve performance. 

</blockquote>

</details>

---

29. Route guards in angular.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Route guards are used to prevent unauthorized access to certain routes in an Angular. It checks if the user is allowed to access a particular route or not. There are different type of route guard in Angular such as `CanActivate`, `CanActivateChild`, `CanDeactivate`, `Resolve`, and `CanLoad`.

</blockquote>

</details>

---

30. List some decorators in Angular.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Decorators are used to modify the behavior of a class or its members.  Some examples of decorators are `@Component`, `@Directive`, `@Injectable`, `@Input`, `@Output`, `@ViewChild`, and `@HostBinding`, etc.

</blockquote>

</details>

---

31. Difference between AngularJS and Angular

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

| AngularJS                                                                | Angular                                                                  |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| It is a JavaScript-based open-source front-end web application framework | It is a TypeScript-based open-source front-end web application framework |
| It is based on the Model-View-Controller (MVC) architecture.             | It is based on the Model-View-ViewModel (MVVM) architecture              |
| AngularJs is slower as compared to Angular.                              | Angular is generally faster as compared to AngularJS                     |
| It is not mobile-friendly                                                | It has excellent mobile support.                                         |
| It uses controllers and $scope for building applications                 | It uses components and services for building applications                |
| AngularJS do not have a CLI tool.                                        | Angular comes with a CLI tool                                            |


</blockquote>

</details>

---

32. How does routing work in the UI layer?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Routing is a mechanism that allows the user to navigate between different components or views. When a user clicks a link or enters a URL into the browser, the Angular router checks the URL against the registered routes and loads the associated component. The router then adds the component to the DOM and replace any existing component that was previously displayed. 

</blockquote>

</details>

---

33. How do you handle an exception in the UI layer? (like, how would you handle an exception in angular?)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To handle exceptions, Angular has a built-in exception handling mechanism which is implemented using the `ErrorHandler` class. You can create a custom error handler by extending the `ErrorHandler` class and overriding its `handleError()` method.

</blockquote>

</details>

---

34. What is TypeScript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

TypeScript is an open-source, object-oriented programming language. It is a strict syntactical superset of JavaScript and adds optional static typing and class-based object-oriented programming concepts to it. TypeScript code is compiled into plain JavaScript code and can be executed in any browser or runtime environment that supports JavaScript. It is used to build web and mobile applications. 

</blockquote>

</details>

---

35. What is the apply() method?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `apply()` method is a built-in method in JavaScript that allows you to call a function with a given `this` value and arguments provided as an array. The main advantage of using the `apply()` method is that it allows you to dynamically set the value of `this` for a function

Syntax for `apply()` method:

```js
function.apply(thisArg, [argsArray])
```

</blockquote>

</details>

---

36. What is bind()?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JavaScript, the `bind()` method is used to create a new function with a specified this value. When `bind()` is called on a function, it creates a new function as the original function, but the `this` keyword inside the function will be bound to the first argument of the `bind()` method.

For example,

```js

const myObj = {
  x: 1,
  getX: function() {
    return this.x;
  }
};

const unboundGetX = myObj.getX;
console.log(unboundGetX()); // Output: undefined

const boundGetX = unboundGetX.bind(myObj);
console.log(boundGetX()); // Output: 1

```

In the above example, when we assign the getX method to a variable unboundGetX and call it, the `this` keyword inside the method is not bound to myObj, so it returns undefined. So, We use bind method to bind `this` keyword to myObj.

</blockquote>

</details>

---

37. How would you create a component in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a component in Angular, you can use the command `ng generate component component-name` or `ng g c component-name`.

</blockquote>

</details>

---

38. How would you create a module?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a module in angular application, inside the `src/app` folder create a typescript file with name `<module-name>.module.ts`. Use the `@NgModule` decorator to define the metadata for the module. The `@NgModule` decorator takes an object as an argument with properties such as `declarations`, `imports`, `exports`, `providers`, and `bootstrap`. Add the `@NgModule` decorator to the top of the module class and export it by using the `export` keyword.

</blockquote>

</details>

---

39. What file do you edit for dependencies?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`package.json` file is used to edit the dependencies for the application. This file contains metadata about the project and the dependencies required by the application.

</blockquote>

</details>

---


40. What is the angular component life cycle?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular component lifecycle refers to a series of stages in the life of an Angular component, starting from its intialization till its destruction.These stages are hooked to methods that are executed by Angular. The most important methods in this lifecycle are `ngOnInit()`, `ngOnChanges()`, `ngDoCheck()`, `ngAfterContentInit()`, `ngAfterContentChecked()`, `ngAfterViewInit()`, `ngAfterViewChecked()`, and `ngOnDestroy()`.

</blockquote>

</details>

---


