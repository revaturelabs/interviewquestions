1. What is Angular?
2. What is SPA?
3. How SPA is different from tradtional web application?
4. List some of the features of Angular application.
5. Angular Framework written using  ____________
6. What is use of npm?
7. What is use of Node.js ?
8. Can we run the javascript file using Node.js?
9. What are the main components in the npm?
10. How do you check Node.js installed successfully in your system?
11. Why do we need Node.js for Angular?
12. What kind of information we can find in `package.json` file?
13. What is the difference between `dependencies` and `devDependencies` in the `package.json` file?
14. What happens if I run `npm install` in the terminal
16. What happens if I run `npm uninstall` in the terminal
17. What is the difference between `npm update` and `npm update -g` command
18. What happens if I run `npm init` in the terminal
19. Can I run angular application using `npm start` command
20. `npm build` used to ____________
21. Node.js is  ______________ built on ____________
22. How can I convert `.ts` file to `.js` file?
23. All npm packages are in ___________
24. What is difference between AngularJS and Angular?
25. How JavaScript is different from TypeScript
26. TypeScript using ________ typing and JavaScript using ______ typing
27. What is the latest version of Angular?
28. Does Angular support mobiles?
29. Does refreshing a whole pade needed in SPA?
30. List some advantages and disadvantages in SPA?
31. List some of the SPA framework
32. List some of the SPA
33. In SPA, after the initial page load, does the server send any more HTML to you?
34. Why do we need Webpack?
35. What is Webpack?
36. What is dependency graph? How is it related to Webpack?
37. What does Angular CLI do?
38. How do you install Angular CLI?
39. How do you create any angular application?
40. Angular by default will serve application on port ________
41. How do you serve the angular application?
42. What is the difference between `ng serve -o` and `ng serve`
43. What is the difference between `npm start` and `ng serve`
44. How do you find which version of angular installed in our system? How do you updated to latest version?
45. Match the commands with its appropriate details

![image](https://user-images.githubusercontent.com/70228962/184809083-a973816f-8468-4a0a-be4e-8ff7bec30861.png)

46. What kind of files we can find on `e2e` folder and `node_modules` folder?
47. What are files we can find under `src` folder?
48. What is the difference between `angular.json` and `package.json` file?
49. What is the difference between `package.json` and `package-lock.json` files?
50. In Angular app, where I can define or specify the target browser?
51. What is a component?
52. In which file, I can find `@Component` and `@NgModule` decorator?
53. What are the metadata does `@Component` decorator>
54. How do you create a component?
55. What are the files created or updated when we create a component?
56. How many files are generated when we create a component?
57. I have to create component `User` as a parent. Then, I want to 2 child components for `User` component. Let's say 2 child components are `User-Login` and `User-Register`. What are the steps I needed to do?
58. Below is the code in `user.component.ts`. If I want to insert user component to the `index.html` file.
```ts
import { Component } from '@angular/core';
@Component ({
  selector: 'user'
  templateUrl: './user.component.html' ,
  styleUrls: ['./user.component.css']
export class UserComponent {
} 
```
60. Can we have `html` content attached to the component without having `.html` file. If so, how?
61. Can we have `css` styles attached to the component without having `.css` file. If so, how?
62. What is the difference between `templateUrl` and `template` in `@Component` decorator?
63. What is the difference between `styleUrls` and `styles` in `@Component` decorator?
64. Complete the missing metadata in `@Component` decorator with following criteria.
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
65. In the case of a Multi-line template, you need to use ______________ to enclose the template string.
66. What is Lifecycle Hooks? List them.
67. Which lifecycle hook executed first?
68. Which lifecycle hook used to inject any dependencies into the component?
69. Tell the order in wich lifecycle hooks get exceuted?
70. Which lifecycle called only one?
71. Which angular module has hook interfaces?
72. What is module in angular?
73. What is the root module of every application?
74. If I decorate a typescript class with `@NgModule`, what does it mean?
75. What are metadata in `@NgModule` decorator
76. What is meant by bootstrapping?
77. How angular application bootstrapped? _or_ List the steps in bootstrapping the angular. _or_ How agular lauches the application
78. Which file loaded in the browser after launced the application?
79. What is a directive in angular?
80. What are different types of directives in angular?
81. Can we able to create our own directive? If so, how? If not, why?
82. Which directive alter layout by adding, removing, and replacing elements in DOM?
83. Explain about structural directive
84. How can I print the list of users in the include?
85. Design the angular app with the following criteria
    - Get the `name` and `age` from the user
    - If entered `age`is greater than 60, print their `name` then say "is a senior citizen"
    - Else, their `name` then say "is not a senior citizen"
86. Design the angular app with the following criteria
    - Get a character/letter from the user
    - If entered character is vowel(s), print the a word starting with vowel
        - For example, if user entered `a`, you can print `apple`
    - Else, print "It is not vowel"
87. Explain about attribute directive
88. What is the difference between structural and attribute directive
89. What is the use of `<ng-template>`
90. What is databinding in angular?
91. List the types of databinding in angular?
92. What is the difference between 1 way and 2 way databinding?
93. What is the difference between property and event binding?
94. How do you achieve two way data binding in angular?
95. Consider there is a variable `name = "Angular"` in `app.component.ts`, how can I print this value in template.
96. What is meant by String Interpolation?
97. Explain about event binding.
98. Explain about property binding.
99. Design the angular app with the following criteria
    - Template should have button named `Click Me`
    - When user clicked on the button, you should greet the user with a message "Welcome to my angular app"
100. Design the angular app
    - Get the `name` from the user
    - Print the `name` with a message " Hi `name`!! Welcome to my angular app"
101. What is the purpose `ngModel` directive
102. The `ngModel` directive from the Angular ________, set up the two way data binding on form elements.
103. What is use of `BrowserModule`?
104. In which file, I need to mention I'm going to use `FormsModule`
105. What are ways to pass data from component class to the View?
106. What are ways to pass data from the view to the component class?
107. Every frontend application needs to communicate with the backend microservices to share the data over the HTTP protocol. How this communication established in angular?
108. The `HttpClient` service is available in the ___________ package in the angular framework
109. Why do we need `HttpClient`?
110. List some `HttpClient` methods provided by the angular framework
111. What is benefits of `HttpClient` in Angular
112. How to use `HttpClient` in Angular?
113. What is an observable? How is related with `HttpClient`?
114. How do you handle errors with `HttpClient`?
115. What is Subject?
116. What is the difference between Subjects and Observables?
117. What is Pipe?
118. How we can create a custom pipe in angular?
119. List some of the built-in pipe.
120. What is service?
121. What is the difference between using reactive and template-driven forms? How would you setup each?
122. How does dependency injection work in Angular?
123. How do we inject a service to the root module?
124. How do you generate service using Angular CLI?
125. Which mechanism mechanism in Angular provides a way to navigate from one view to another view in the application.
126. What is use of `RoutingModule` in Angular?
