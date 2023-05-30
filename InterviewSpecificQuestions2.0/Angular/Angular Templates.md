1. What is a template in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

A template is just like regular HTML that renders a view, or user interface, in the browser.

When you generate an Angular application with the Angular CLI, the `app.component.html` file is the default template containing placeholder HTML.

</blockquote>
</details>
  
---
 
 2. What is the difference between `templateUrl` and `template` in the `@Component` decorator?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- `templateUrl` - You can define the template in a separate HTML file and link to it in the component metadata using the `@Component` decorator's `templateUrl` property.
	
- `template` - You can define it inline using the template property 
</blockquote>
</details>
  
---
 	
	
3. What is the difference between `styleUrls` and `styles` in the `@Component` decorator?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
- You can use the `styles` property to keep the CSS code in line to style your component's HTML template.
```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styles:[`
        .green { color:#003300 !important; }
        .bold { font-weight:bold; }
        `]
})
```
- You can use the `styleUrls` property Keep the CSS code separately in your file to style your component's HTML template.
	
```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```
- **NOTE:** Both the `styles` and `styleUrls` properties are arrays.

</blockquote>
</details>
  
---
 4. Can we have HTML content attached to the component without having a `.html` file? If so, how?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Yes, by using an inline template.
	
Inline Template  - It is defined by placing the HTML code in backticks _`_ and is linked to the component metadata using the `template` property of `the @Component` decorator.
```ts
@Component({
  selector: 'app-root',
  templateUrl: `<h1> Hello World </h1>`,
  styleUrls: ['./app.component.css']
})
````

</blockquote>
</details>
  
---
	
5. Can we have CSS styles attached to the component without having a `.css` file? If so, how?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Yes, by using inline CSS. 

You can use the `styles` property to keep the CSS code inline to style your component's HTML template.
```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styles:[`
        .green { color:#003300 !important; }
        .bold { font-weight:bold; }
        `]
})
```
	
</blockquote>
</details>
  
---
	
6.  Can we have a multiline template? If so, how?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
Yes, by using backticks _`_
	
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `<h1> Hello World </h1>
  <h2> Hello World  </h2>
  ` ,
  styleUrls: ['./app.component.css']
})
export class AppComponent{
  title = 'angularDemoProject';
}
```
	
</blockquote>
</details>
  
---

7. What are views in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Views are almost like their own virtual DOM.  Together, the component and its template describe a view.

</blockquote>
</details>
  
---
	
8. How view is different from a template?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

A template is an HTML snippet that tells Angular how to render the component in an angular application.

The template is immediately associated with a component that defines that component’s view.

</blockquote>
</details>
  
---

9. What are ways to define templates?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

There are two ways of defining a template in an angular component.
1. Inline Template
2. External Template
	
Inline Template  - It is defined by placing the HTML code in backticks _`_ and is linked to the component metadata using the `template` property of `the @Component` decorator.
```ts
@Component({
  selector: 'app-root',
  templateUrl: `<h1> Hello World </h1>`,
  styleUrls: ['./app.component.css']
})
````
External Template - It is defined in a separate HTML file and is linked to the component metadata using the `@Component` decorator’s `templateUrl` property 
	
```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```

</blockquote>
</details>
  
---
 
10. What would you choose between the inline and external template files?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Choose based on the explanation below	

</blockquote>
<details>
<summary><b>Explanation</b></summary>
<blockquote>

Normally we use inline templates for small portion of code and external template files for bigger views. By default, the Angular CLI generates components with a template file. But you can override that with using `ng g c hero -it` command.
	
</blockquote>
</details>
</details>
  
---
