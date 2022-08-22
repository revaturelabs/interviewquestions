1. In SPA, after the initial page load, does the server send any more HTML to you?
2. Does refreshing a whole page needed in SPA?
3. I have to create component `User` as a parent. Then, I want to 2 child components for `User` component. Let's say 2 child components are `User-Login` and `User-Register`. What are the steps I needed to do?
4.  Below is the code in `user.component.ts`. If I want to insert user component to the `index.html` file.
```ts
import { Component } from '@angular/core';
@Component ({
  selector: 'user'
  templateUrl: './user.component.html' ,
  styleUrls: ['./user.component.css']
export class UserComponent {
} 
```
5. Can we have html content attached to the component without having `.html` file. If so, how?
6. Can we have css styles attached to the component without having `.css` file. If so, how?
7. Can we have multiline template? If so, how?
8. If I decorate a typescript class with `@NgModule`, what does it mean?
9. Complete the missing metadata in `@Component` decorator with following criteria.
    -  This component should be identified by `user`
    -  Template of this component, should say "Hello User!!"
    -  Template should have atleast one heading tag
    -  Also, text inside that heading tag, should be in red color
```ts
import { Component } from '@angular/core';
@Component ({
  // add here
export class UserComponent {
} 
```
10. Design the angular app with the following criteria
    - Get the `name` and `age` from the user
    - If entered `age`is greater than 60, print their `name` then say "is a senior citizen"
    - Else, their `name` then say "is not a senior citizen"
11. Design the angular app with the following criteria
    - Get a character/letter from the user
    - If entered character is vowel(s), print the a word starting with vowel
        - For example, if user entered `a`, you can print `apple`
    - Else, print "It is not vowel"
12. Consider there is a variable `name = "Angular"` in `app.component.ts`, how can I print this value in template.
13. Design the angular app with the following criteria
    - Template should have button named `Click Me`
    - When user clicked on the button, you should greet the user with a message "Welcome to my angular app"
14.  Design the angular app
    - Get the `name` from the user
    - Print the `name` with a message " Hi `name`!! Welcome to my angular app"
15.  Every frontend application needs to communicate with the backend microservices to share the data over the HTTP protocol. How this communication established in angular?
16.  Design the angular application to print current date in this format "MM/dd/yy".
17. Design the angular application with following criteria
    - Get the `name` as an input
    - Print the `name` in the reverse (Use Pipe)
18. Suggest a way to share some data with all the components in my angular application
19. Can we inject a service to a component instead of root module?
20. What happens if I decorate class with `@Pipe`
21. Detail the use of below code:
```ts
interface PipeTransform {
  transform(value: any, ...args: any[]): any
}
```
22. How can I access data stored in the service in a component?
23. Can we create our own pipe in angular? If so, how? If so, why?
24. What happens if I decorate class with `@Pipe`
25. Detail the use of below code:
```ts
interface PipeTransform {
  transform(value: any, ...args: any[]): any
}
```
26. Design an angular application with following criteria.
    - `/login` need to the login page or template
    - `/register` need to the register page or template
27. How do to create an angular, when I need to navigate between components?
