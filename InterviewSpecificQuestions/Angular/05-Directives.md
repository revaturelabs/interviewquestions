1. What are directives?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
Directives add behaviour to an existing DOM element or an existing component instance.
  </blockquote>
</details>
  
---

2. What are the differences between Component and Directive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

In a short note, A component(`@Component`) is a directive-with-a-template. Some of the major differences are mentioned in a tabular form:

| Component                                                             | Directive                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------|
| To register a component we use @Component meta-data annotation        | To register directives we use @Directive meta-data annotation |
| Components are typically used to create UI widgets                    | Directive is used to add behavior to an existing DOM element  |
| Component is used to break up the application into smaller components | Directive is use to design re-usable components               |
| Only one component can be present per DOM element                     | Many directives can be used per DOM element                   |
</blockquote>
</details>
  
---

3. What are the different types of directives in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
    
 - **Component Directives** - Component directives alter the details of how the component should be processed, instantiated, and used at runtime.
- **Structural Directives** -  Structural directives are used for adding, removing, or manipulating DOM elements.
- **Attribute Directives** - Attribute directives are used to change the look and behavior of the DOM elements.
    
<i>Custom Directive: Custom directive can also be created if any of the above directives does not solve our purpose for the requirement</i>

</blockquote> 
</details>
	
--- 
    
4. Explain about Structural Directives in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
 <blockquote>
    
- Structural directives are used for adding, removing, or manipulating DOM elements
- Structural directives start with an asterisk (*) followed by a directive name. 
- There are three built-in structural directives - `ngIf`, `ngFor` and `ngSwitch`.
- The `ngFor` directive is used to repeat a part of the HTML template once per each item from an iterable list.
- `ngIf` directive allows us to add or remove DOM Elements based upon the Boolean expression. We can also have an else block associated with an ngIf directive.

```html
<div *ngIf=" a > b ; else elseBlock1">
	    {{ a }} is greater than {{ b }}
</div>
<ng-template #elseBlock1>
	    {{ b }} is greater than {{ a }}
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
  
5. Explain about Attribute Directives in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

6. Design the angular app with the following criteria
    - Get the `name` and `age` from the user
    - If entered `age`is greater than 60, print their `name` then say "is a senior citizen"
    - Else, their `name` then say "is not a senior citizen"

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

**Steps:**
1. Create an angular project by running `ng new angularDemo2` command in the angular CLI
2. In `app.component.html` file, create a form to get the `name` and `age` from the user
```html
Name: <input type="text" [(ngModel)]="name" /> <br> 
Age: <input type="text" [(ngModel)]="age" />
```
3. In `app.component.ts` file, create a `name` and `age` variables.
```ts
import { Component } from '@angular/core';
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'angularDemo2';

  name !: string;
  age !: number;
}	
```
4. Since we are using the `ngModel`directive, we have to import `FormsModule` in `app.module.ts` file.
```java
 imports: [
    BrowserModule,
    FormsModule
 ]
```
5. To check entered age and print the sentence according to it. We need to use `ngIf` directive. In `app.component.html` file,
```ts
<div *ngIf=" age > 60; else elseBlock1">
    {{name}} is a senior citizen
</div>
<ng-template #elseBlock1>
    {{name}} is not a senior citizen
</ng-template>	
```
6. Launch the application by running `ng serve -o` command.
7. Now, able to see the excepted output.
![image](https://user-images.githubusercontent.com/70228962/186344357-656f9e28-3cfa-4dc0-9873-dbd62dcd14d8.png) 

![image](https://user-images.githubusercontent.com/70228962/186344483-f0368ed8-f0e2-46ec-8b3e-42e4cc6eb2c1.png)

</blockquote>
</details>

---

7. Design angular application with the following criteria
	-  Get a number from the user. 
	-  Print its a even number or odd number

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
1. Create an angular project by running `ng new angularDemo2` command in the angular CLI
2. In `app.component.html` file, create a form to get the `name` and `age` from the user
```html
Enter a number: <input type="text" [(ngModel)]="num" />
```
3. In `app.component.ts` file, create a `name` and `age` variables.
```ts
import { Component } from '@angular/core';
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'angularDemo2';
	
  num !: number;
}	
```
4. Since we are using the `ngModel`directive, we have to import `FormsModule` in `app.module.ts` file.
```java
 imports: [
    BrowserModule,
    FormsModule
 ]
```
5. To check entered number is odd and even and print it. We will use `ngSwitch` directive. In `app.component.html` file,
```ts
Enter a number: <input type="text" [(ngModel)]="num">

<div ngSwitch="{{num%2}}">
    <div *ngSwitchCase="'0'">{{num}} is even.</div>
    <div *ngSwitchCase="'1'">{{num}} is odd</div>
    <div *ngSwitchDefault>Nothing Found</div>
</div>
```
6. Launch the application by running `ng serve -o` command.
7. Now, able to see the excepted output.

![image](https://user-images.githubusercontent.com/70228962/186347155-19484af6-e1f9-4818-bb4d-ba6d47864fb2.png)

![image](https://user-images.githubusercontent.com/70228962/186347246-414044f8-21bf-4021-a3c4-b2dba0540442.png)

</blockquote>
</details>
  
---

8. How do you create a custom directive in Angular?
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Steps to creating custom directive in angular:
	
1. To create an angular application, run `ng new myapp` command.
2. Then, we can create directive by running `ng g d myHighlight` command. Angular CLI creates two files `my-highlight.directive.spec.ts` and `my-highlight.directive.ts` and updates `app.module.ts`
3. In `my-highlight.directive.ts`, we will create an instance of `ElementRef` and just highlighting the background color as yellow.
```ts
import { Directive, ElementRef} from '@angular/core';

@Directive({selector: '[myHighlight]'})
export class MyHighlightDirective {
  constructor( private el: ElementRef) {
    el.nativeElement.style.backgroundColor = 'yellow';
   }
}
```
4. Now this directive extends HTML element behavior with a yellow background as below
```html
<p myHighlight> Hi, there!!</p>	
```
5. Launch the angular application by running `ng serve -o` command.  The expected output will be,
	
![image](https://user-images.githubusercontent.com/70228962/186374096-514930ba-f29c-424e-bcf8-11318b5c0734.png)

</blockquote>
</details>
  
---

9. What's Angular `ElementRef`?
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
Angular `ElementRef`is simply a class that wraps native DOM elements in the browser and allows you to work with the DOM by providing the `nativeElement` object which exposes all the methods and properties of the native elements.

</blockquote>
</details>
  
---

10. How do you choose an element from a component template?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
To directly access items in the view, use the `@ViewChild` directive. Consider an input item with a reference.
```html
<input #example>
```
	
and construct a view child directive that is accessed in the `ngAfterViewInit` lifecycle hook
```ts		
@ViewChild('example') input;

ngAfterViewInit() {
  console.log(this.input.nativeElement.value);
}
```	
	
</blockquote>
</details>
  
---

11. What is `ng-template` in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`ng-template` is an Angular element that is used for rendering HTML in a template. However, it is not rendered directly on DOM. If you include an ng-template tag to a template, the tag and the content inside it will be replaced by comment upon render.

</blockquote>
</details>
  
---
 
12. Create a `myHighlight` attribute directive to set an element’s background color when you hovers over that element.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
1. To create an angular application, run `ng new myapp` command.
2. Then, we can create directive by running `ng g d myHighlight` command. Angular CLI creates two files `my-highlight.directive.spec.ts` and `my-highlight.directive.ts` and updates `app.module.ts`
3. In `my-highlight.directive.ts`, we will create an instance of `ElementRef` and highlighting based on the mouseover and mouseleave.
```ts
import { Directive, ElementRef, HostListener } from '@angular/core';

@Directive({
  selector: '[myHighlight]'
})
export class MyHighlightDirective {

  constructor(private el : ElementRef) {}

  @HostListener('mouseover') onMouseOver() {
    this.changeBackgroundColor('blue');
  }

  @HostListener('mouseleave') onMouseLeave() {
    this.changeBackgroundColor('white');
  }

  private changeBackgroundColor(color: string) {
    this.el.nativeElement.style.backgroundColor = color;
  }

}
```
4. Adding `myHighlight` directive to the HTML elements, will change color based on mouseover and mouse leave
```html
<p myHighlight> Hi, there!!</p>	
```	
5. Launch the angular application by running `ng serve -o` command. Then, we'll able to see the excepted output

![image](https://user-images.githubusercontent.com/70228962/186696341-de34b3a7-9c4a-4102-8d9d-16d6984d4746.png)
	
</blockquote>
</details>
  
---
 
