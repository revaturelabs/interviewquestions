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

4. What is a component in angular?
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
Components are the basic building blocks in the Angular application. Components contain the data & UI logic that defines the view and behavior of the web application.
    
![image](https://user-images.githubusercontent.com/103101208/185570645-2ab168d8-9c3d-4447-a403-703222cf7814.png)

  </blockquote>

</details>

--- 
	
5.	Angular Components Lifecycle or Lifecycle Hooks or LifeCycle Methods
  
<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Angular creates a component; renders it; creates and renders its children; checks it when it’s data-bound properties change; and destroys it before removing it from the DOM. These events are called "Lifecycle Hooks".
- Lifecycle Hooks:
  ![image](https://user-images.githubusercontent.com/103101208/185570891-363fb6d0-3bcd-454e-b2da-68362092fe64.png)
- `constructor()` - The constructor of the component class gets executed first, before the execution of any other lifecycle hook events. If we need to inject any dependencies into the component, then the constructor is the best place to do so.
- `ngOnChanges()` - Called whenever the input properties of the component change. It returns a SimpleChanges object which holds any current and previous property values.
- `ngOnInit()` - Called once to initialize the component and set the input properties. It initializes the component after Angular first displays the data-bound properties.
- `ngDoCheck()` - Called during all change-detection runs that Angular can't detect on its own. Also called immediately after the ngOnChanges() method.
- `ngAfterContentInit()` - Invoked once after Angular performs any content projection into the component’s view.
- `ngAfterContentChecked()` - Invoked after each time Angular checks for content projected into the component. It's called after `ngAfterContentInit()` and every subsequent `ngDoCheck()`
- `ngAfterViewInit()` - Invoked after Angular initializes the component's views and its child views.
- `ngAfterViewChecked()` - Invoked after each time Angular checks for the content projected into the component. It called after `ngAfterViewInit()` and every subsequent `ngAfterContentChecked()`
- `ngOnDestroy()` - Invoked before Angular destroys the directive or component.
	
![image](https://user-images.githubusercontent.com/103101208/185571059-270e2558-e7f9-48e9-8023-3cb594a8d780.png)



</blockquote>  

</details>
	
--- 

6.	What are some advantages of Angular?
  
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
  
7.	What are the different types of directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
 - Component Directives - Component directives alter the details of how the component should be processed, instantiated, and used at runtime.
- Structural Directives Structural directives are used for adding, removing, or manipulating DOM elements.
- Attribute Directives - Attribute directives are used to change the look and behavior of the DOM elements.
    
<i>Custom Directive: Custom directive can also be created if any of the above directives does not solve our purpose for the requirement
    </i>

</blockquote> 

</details>
	
--- 
  
  
8. Structural Directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
 - Structural directives are used for adding, removing, or manipulating DOM elements
- Structural directives start with an asterisk (*) followed by a directive name. 
- There are three built-in structural directives - `ngIf`, `ngFor` and `ngSwitch`.
- The `ngFor` directive is used to repeat a part of the HTML template once per each item from an iterable list.
- `ngIf` directive allows us to add or remove DOM Elements based upon the Boolean expression. We can also have an else block associated with an ngIf directive.

```html
  
<div *ngIf="age > 55; else elseBlock1">
	    {{name}} is a senior citizen
</div>
<ng-template #elseBlock1>
	    {{name}} is not a senior citizen
</ng-template>
    
```
- `ngSwitch` directive lets you hide/show HTML elements depending on an expression. `NgSwitchCase` displays its element when its value matches the switch value. `NgSwitchDefault` displays its element when no sibling `NgSwitchCase` matches the switch value.
    
```html
<!-- user to enter any vowels(a, e, i o, u), print any word starting with vowels -->
<input type="text" [(ngModel)]="str" />
<div [ngSwitch]="str">
	    <div *ngSwitchCase="'a'">Entered a!! Word: Apple</div>
	    <div *ngSwitchCase="'e'"> Entered e!! Word: Egg</div>
	    <div *ngSwitchCase="'i'"> Entered i!! Word: Ice cream</div>
	    <div *ngSwitchCase="'o'"> Entered o!! Word: Orange</div>
	    <div *ngSwitchCase="'u'"> Entered u!! Word: Umberalla</div>
	    <div *ngSwitchDefault> You Entered Constant </div>
</div>


    
```
    
   
</blockquote> 

</details>
	
--- 
  
9. Attribute Directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Attribute directives are used to change the look and behavior of the DOM elements.
- Attribute directives are enclosed with the [] square brackets
- There are two built-in attribute directives - `ngClass` and `ngStyle`
- The `ngClass` directive is used for adding or removing the CSS classes on an HTML element. It allows us to apply CSS classes dynamically based on expression evaluation.
    
```html
    
<h3 [ngClass]="'red'"> Need your attention</h3>
<div [ngClass]="['red','size20']"> Red Background, Text with Size 20px </div>
<div [ngClass]="{'red':false,'size20':true}">Text with Size 20px</div>

```
- The `ngStyle` directive allows us to dynamically change the style of HTML element based on the expression.
    
```html
Enter the username: <input type='text' [(ngModel)]='name'>
<div [ngStyle]="{'background-color':username === 'Admin' ? 'green' : 'red' }"></div>

```

</blockquote> 

</details>
	
--- 
  
10.	Decorators in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Decorators are design patterns or functions that define how Angular features work. 
- Angular supports four types of decorators:
    - Class decorators
    - Property decorators
    - Method decorators
    - Parameter decorators

</blockquote> 

</details>
	
--- 
  
11.	Class Decorators in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- A class decorator tells Angular if a particular class is a component or a module.
- There are various class decorators in Angular, and among them, `@Component` and `@NgModule` are widely used.
    

</blockquote> 

</details>
	
--- 
  
12. `@Component` Decorator.

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

In `app.component.ts` file, we export the `AppComponent` class, and we decorate it with the `@Component` decorator, imported from the `@angular/core package`, which takes a few metadata, such as: `selector`, `templateUrl` and `styleUrls`.

![image](https://user-images.githubusercontent.com/103101208/185589415-67f2a93c-98cd-44e9-b427-17d082620a8a.png)

- `selector` – just name given for the component. In the `index.html` file, `<app-root>` tag corresponds to component’s selector. By doing so, Angular will inject the corresponding template of the component. 

![image](https://user-images.githubusercontent.com/103101208/185589556-9a942bf6-14a7-42c4-9bf1-ed567efcd25c.png)

- `templateUrl` - points to an HTML file that defines what you see on your application. 
- `styleUrls` - points to set of CSS file that defines styles or design for application


</blockquote>
</details>
	
--- 

13. `@NgModule` Decorator

<details>
<summary> <b>Show Answer</b></summary>

<blockquote>

`@NgModule` takes the below metadata to launch the application:
- `declarations` — contains a list of components, directives, and pipes, which belong to this module.
- `imports` — contains a list of modules, which are used by the component templates in this module reference.  For example, we import `BrowserModule` to have browser-specific services such as DOM rendering, sanitization, and location.
- `providers` — the list of service providers that the application needs.
- `bootstrap` — contains the root component of the application

![image](https://user-images.githubusercontent.com/103101208/185590158-9478baf7-8277-471f-88c0-bd3940a0f27b.png)




</blockquote>
</details>
	
--- 

14.	How to consume API using Angular?



<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
- We are required to import and setup `HttpClient` service in Angular project to consume REST APIs.
- To work with `HttpClient` service in Angular, you need to import the `HttpClientModule` in app.module.ts file. 
- Then inject `HttpClient` service in constructor method after that you can hit the remote server via HTTP’s POST, GET, PUT and DELETE methods.



</blockquote>


</details>
	
--- 

15.	How do you do routing?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- First, we need to run `ng new routing-app –routing` command to create an angular application with routing module
- Make sure `AppRoutingModule` is in the `imports` of `@NgModule` in the `app.module.ts` file
- Add routes in the `routing.module.ts` file 

```js
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { LoginComponent } from './Components/UserComponents/login/login.component';
import { RegisterComponent } from './Components/UserComponents/register/register.component';
const routes: Routes = [
  {path : 'login', component: LoginComponent },
  {path : 'register', component: RegisterComponent}
]; 
@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
1})
export class AppRoutingModule { }




```
- In your `app.component.html` file, we add our routes to the application

```html
<h1> Routing Demo </h1>
<nav>
   <li><a routerLink="/login">Login</a></li>
   <li><a routerLink="/register">register</a></li>
</nav>
<router-outlet></router-outlet>


```

Here,
- `routerLink` - is an attribute to an anchor tag which sets the route for the component.
- `<router-outlet>` - works as a placeholder to load the different components dynamically based on the activated component.



</blockquote>

</details>
	
--- 

16. How do you handle dependency injection in angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- In Angular, dependencies are typically services.
- The `@Injectable()` decorator marks a class as a service class that can be injected.
- The `@Injectable()` decorator has a `providedIn` property where we specify the provider of the decorated service class.
- By default, providedIn property has values ‘root’, that means services is injected to the AppModule.

![image](https://user-images.githubusercontent.com/103101208/185592186-04786f62-80f8-476b-b41d-358da5943a58.png)

- Here we are injecting to UserService to the `AppModule`, so all the components able to use this service.


</blockquote>

</details>
	
--- 

17. What are the ways of databinding in angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- Databinding is a technique used to bind the data from an HTML template to a component class (.ts file) or from a component class (.ts file) to an HTML template.
- They are 1 way databinding and 2-way databinding

![image](https://user-images.githubusercontent.com/103101208/185592479-3570b8c1-3fc1-4d06-8328-9c266186a2d3.png)
	
![image](https://user-images.githubusercontent.com/103101208/185592494-637eb0ae-7610-40e8-874d-bd179e2ab16f.png)




</blockquote>

</details>
	
--- 

18. Property Binding 

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
- From Component Class to the HTML Template
- Bind values to the attributes of HTML elements.
- Uses [], square brackets in the html file
- Create a variable in the class, and the bind that value to an attribute for HTML tag

![image](https://user-images.githubusercontent.com/103101208/185592858-66cc92f3-feca-436e-87cf-766c692a8a8c.png)



</blockquote>
</details>
	
--- 

19. Event Binding

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- From HTML template to the component class
- Bind DOM events such as keystrokes, button clicks, mouse overs, touches, etc. to a function in the component.
- Uses (), parentheses in the html file
- Here, we were calling the `OnClick()` function, when the ‘Click Here’ button is clicked.

![image](https://user-images.githubusercontent.com/103101208/185593164-aa23c1a2-497c-4906-8b32-15af3231d0a6.png)


</blockquote>

</details>
	
--- 

20. String Interpolation

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- From the component class to the HTML template
- Uses {{}}, double curly braces in the html

![image](https://user-images.githubusercontent.com/103101208/185593247-f546704d-d3ed-4a80-8ff3-01289401fe00.png)


</blockquote>

</details>
	
--- 


21. What is two-way databinding in angular
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- Two-way data binding is achieved by combining property binding and event binding together.
- Mostly used in forms.
- The Angular uses the `ngModel` directive to achieve two-way binding on HTML `<form>` elements.
- To use the `ngModel` directive, we need to import the `FormsModule` package into our Angular module.
- Here, we enclose `ngModel` directive within [()]

![image](https://user-images.githubusercontent.com/103101208/185593434-3e70965a-c750-4bbd-aa3b-b3fea6fccba7.png)




</blockquote>

</details>
	
--- 

22. Difference between Angular JS and Angular 4 +

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

23. Difference between Angular 2 and Angular 4

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

24. How would you protect routes?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- Routing guards used to protect the routes.
- Routing guards used to check whether the user should grant or remove access to certain parts of the navigation.
- There are 4 different interfaces act as routing guards:

  * `CanActivate `- decides if the route can be activated.
	
  * `CanActivateChild`- decides if children of a route can be activated.
	
  * `CanLoad`- decides if a route can be loaded.
	
  * `CanDeactivate`- decides if the user can leave a route.



</blockquote>

</details>
	
--- 

25. How would you pass data from a parent to a child component or a child to a parent component?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- @Input decorator used to pass the data from a parent to a child component
- @Output decorator used to pass the data from a child to a parent component
	
![image](https://user-images.githubusercontent.com/103101208/185594174-ec042de2-81dd-425b-bc8e-8c26ae214f1b.png)

- Consider we have `AppComponent` as Parent. Let’s create a child component using `ng g c child` command. We’ll pass the data from `AppComponent` to `ChildComponent` and vice versa.
- In `child.component.ts`, we create a change property and decorate with the `@Output()` and bound a new instance of `EventEmitter` to it.
- Also, we have a method - `increment()` which updates the value of the count property based on the event (clicking on the increment count button) and emits the event changes to its parent component (`AppComponent`).
- Here, the change property calls the `emit()` method that emits the count value which can be received by event object `$event`.

```js
import { Component, EventEmitter, Input, Output } from '@angular/core';
@Component({
  selector: 'app-child',
  template: `
    <p> Click this button to increment the count:
     <button (click)='increment()'>increment count</button> </p>
`
})
export class ChildComponent  {
	 
  @Input()
  count: number = 0;	 
  @Output()
  change: EventEmitter<number> = new EventEmitter<number>();
  increment() {
    this.count++;
    this.change.emit(this.count);
    console.log("incrementing count in the child component....." + this.count + " --- passing to AppComponent");
 }
}



```
- In `app.component.ts`, we use event binding to get the count property value from the `ChildComponent` to the `AppComponent`

```js

import { Component } from '@angular/core';
	 
@Component({
  selector: 'app-root',
  template: `
  <h3> Event Emitter Example </h3>
  <p> At AppComponent, count = {{ count }} </p>
  <app-child [count]='count' (change)= 'countChange($event)'></app-child>
  })
  export class AppComponent {
    count = 9;
    countChange(event: number) {
    this.count = event;
  }
}

	 
```

![image](https://user-images.githubusercontent.com/103101208/185595719-d657e42b-362d-4131-8378-072ec2d2ca79.png)



</blockquote>

</details>
	
--- 

26. What are some common Angular CLI commands?

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

27. How components communicate with each other in Angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- By passing data between from a child to a parent or a parent to a child component, we can use `@Input` and `@Output`.
- By passing data through a service using observables



</blockquote>

</details>

--- 
	
28. What are Services in angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- Services are used to organize and share business logic, models, data, or functions with different components of an Angular application.

```js

import { HttpClient, HttpHeaders } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Observable } from 'rxjs';
import { user } from './user';
 
@Injectable({
  providedIn: 'root'
})
export class UserserviceService {
  baseurl = 'http://localhost:3000/users';
  constructor(private http: HttpClient) { }
 
  GetAllUsers() :Observable<user[]>{
    return this.http.get<user[]>(this.baseurl);
  }}



```

</blockquote>

</details>

--- 

29. What are Pipes in angular?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- A pipe takes in data as input and transforms it to the desired output.
- In app.component.html, we have built in pipes and custom pipes.
- **Some of the built-in pipes are:**
   * **Date pipe** - Used for formatting dates.
   * **Decimal pipe** - Used for formatting numbers
   * **Currency pipe** - Used for formatting currencies
   * **Lowercase pipe** - Used for converting strings into lowercase.
   * **Uppercase pipe** - Used for converting strings into uppercase.
	
```html
	
<h2>Built-in Pipes</h2>
<li>{{"Pipes"}} </li>
<li>{{"Pipes" | uppercase}}</li>
<li>{{"Pipes" | lowercase}} </li>
<li>{{dob}}</li>
<li>{{dob | date}}</li>
<li>{{dob | date |uppercase }}</li>
<li>{{17.81922 | number }}</li>
<li>{{17.819227546354 | number: '3.4-6' }}</li>
<li>{{17.81922 | number : '2.0-0'}}</li>
<li>{{365778 | currency}}</li>
<li>{{365778 | currency: 'INR'}}</li>
<h2>Custom Pipes</h2>
<li>{{"Pipes" |firstChar}}</li>
<li>{{"Angular" |firstChar}}</li>
<li>{{"great" |firstChar}}</li>

```

- We can create custom pipes using the `ng g pipe <pipe-name>` command in the terminal with the Angular CLI.
- **For example**, we create a custom pipe to count words by running the `ng g pipe` firstChar command in the terminal. The CLI creates 2 files - `firstChar.pipe.spec.ts` and `firstChar.pipe.ts` under `src/app` folder and updates `the app.module.ts` file.
- In `firstChar.pipe.ts`,

```ts
	
import { Pipe, PipeTransform } from '@angular/core';
 
@Pipe({
  name: 'firstChar'
})
export class FirstCharPipe implements PipeTransform {
  transform(value: string): string {
    return value[0];
  }}


```

- Output:

![image](https://user-images.githubusercontent.com/103101208/185601696-16d193f7-3912-4acb-b237-117173331d03.png)





</blockquote>

</details>
	
--- 
	
30. What is the difference between a promise and an observable?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
	
- A Promise emits a single value while Observable can emit multiple values. 
- So, while handling a HTTP request, a Promise can manage a single response for the same request, but if there are multiple responses to the same request, then we have to use an Observable.
	
```ts
const promise = new Promise((data) =>{ 
    data(1);
    data(2);
    data(3);    }).then(element => console.log('Promise '+ element));
// Logs:
// Promise 1
 
const observable = new Observable((data) => {
    data.next(1);
    data.next(2);
    data.next(3);   }).subscribe(element => console.log('Observable ' + element));
 
// Logs:
//Observable 1
//Observable 2
//Observable 3
	
```

	
	
</blockquote>

</details>
	




  
