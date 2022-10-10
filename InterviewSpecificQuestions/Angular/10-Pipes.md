1. What are Pipes in angular? Explain with example. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Pipes provide a way to transform values in an Angular template. Pipes are used with a Pipe (`|`) character, and take integers, strings, arrays, and date as input and returns a desired formatted output which can be displayed in the browser.
    
For example, a Date object shows the date in this format: `Sat Aug 03 2019 19:48:11 GMT+0530 (India Standard Time)` which is not easy for the normal users to understand. It’s better to have the date in this format `Saturday, 03 Aug 2019 07:50 PM`. This can be achieved using pipes.

</blockquote>
</details>
  
---
 
2. How you can transform any strings, currency amounts, dates, and other data for display?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Using Pipes, we can transform any strings, currency amounts, dates, and other data for display.

</blockquote>
</details>
  
---
 
3. What happens if I decorate class with `@Pipe` decorator?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

If we want to create a custom pipe in angular, we need to annotate the class with `@Pipe` decorator.

`@Pipe` decorator has a name property, which used to specify the name of the pipe. 
  
</blockquote>
</details>
  
---
 
4. What do you get from the below code?
```ts
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({
  name: 'filter'
})
export class FilterPipe implements PipeTransform {
  transform(array: string[], startWith: string): any {
    let temp: string[] = [];
    temp = array.filter(a => a.startsWith(startWith));
    return temp;
  }
}
```
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
    
- `FilterPipe` is a custom pipe.
- We take array of strings (`array`) and another string (`startWith`) as an input.
- Using `filter` method, we only filter string that starts with value in `startsWith` and returning it.
    
</blockquote>
</details>
  
---
 

5. Can we create our own pipe in angular? If so, how?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
 Yes, we can our own pipe in angular. 
  
**For example:** we create a custom pipe to get first character in a given string, by running the `ng g pipe firstChar` command in the terminal. The CLI creates 2 files - `first-char.pipe.spec.ts` and `first-char.pipe.ts` under _src/app_ folder and updates the `app.module.ts` file.

In `first-char.pipe.ts` file, we write the logic for returning first character in a given string.
  
```ts
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({   name: 'firstChar' })
export class FirstCharPipe implements PipeTransform {

  transform(value: string): string{
    return value[0];
  }
}  
```
And, we can use it any template file. For example,  in `app.component.ts` file,
  
```ts
{{ "Hello World" | firstChar}}  
```

</blockquote>
</details>
  
---
 
6. Design the angular application to print current date in this format "MM/dd/yy".

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

We can use date pipe to date in this format "MM/dd/yy". Also, we can get the current date using `Date.now()`.

![image](https://user-images.githubusercontent.com/70228962/186723294-69118376-7c4a-48e5-966f-c8cd0ba50954.png)

**NOTE:**  Output will be like  _08/25/22_
    
</blockquote>
</details>
  
---
 
7. Design the angular application to get a sentence form user and print the count of words in the given sentence.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

1. Create an angular application by running `ng new myapp` command 
2. Create an custom pipe to count words by running the `ng g pipe wordcount` command
3. In `wordcount.pipe.ts` file, write the logic for word count
```ts
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({   name: 'wordcount' })
export class WordcountPipe implements PipeTransform {
  transform(value : string): unknown {
    return value.trim().split(' ').length;
  }
}
```
4. In `app.component.html`, get the sentence and use the `wordcount` pipe. Also, we have to import `FormsModule` in the `app.module.ts` and create `sentence` variable of type `string` like `sentence !: string` in the `app.component.ts`.
    
```ts
<p>Enter a sentence: <input type="text" [(ngModel)]="sentence"> <br/></p>

{{ sentence | wordcount}}
```
5. Output will be
    
![image](https://user-images.githubusercontent.com/70228962/186726853-a751b72f-faf3-4a00-ad1a-5b43176b0ae5.png)

</blockquote>
</details>
  
---
 
8. Design the angular application to print the list of groceries items followed by its price in rupees

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

For example, below are the groceries items and its cost.
```ts
    items = [
    { name : "Pasta" ,  cost: 32 },
    { name : "Rice" ,  cost: 50 },
    { name : "Milk" ,  cost: 30 },
    { name : "Egg" ,  cost: 5}
  ]
```
    
 To print the list of groceries items followed by its price in rupees, we just need to use `ngFor` directive and `currency` pipe
 
```html
 <div *ngFor="let item of items">
    <li> {{item.name}} - {{ item.cost | currency:'INR'}}</li>
</div>
 ```

Output will be like
   
![image](https://user-images.githubusercontent.com/70228962/186734281-ebe35c70-f152-402b-9e36-8b3a48f9ff90.png)


</blockquote>
</details>
  
---
 
9. How can slice the strings?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

 For example,
 ```html
<p>{{ "abcdefghijk" | slice:3:7}}  </p>
<!-- output: 'defg' -->
```

We have slice pipe in angular to slice the strings. Here, a number is given per character to our input string to understand start and end index. Index starts from 0.
    
```
 0   1   2   3   4   5   6   7   8   9   10 
 |   |   |   |   |   |   |   |   |   |   |    
 a   b   c   d   e   f   g   h   i   j   k
 ```
In our example we have following indexes. 
    
start = 3
    
end = 7
    
Slice pipe will return substring starting from index 3 i.e character d and will include all characters before index 7 i.e up to g. The character at end index will not be included in the output substring.

</blockquote>
</details>
  
---
 
10. List some of the built in pipes in angular. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Some of the built-in pipes are:

- **Date pipe**: Used for formatting dates.
- **Decimal pipe**: Used for formatting numbers
- **Currency pipe**: Used for formatting currencies
- **Lowercase pipe**: Used for converting strings into lowercase.
- **Uppercase pipe**: Used for converting strings into uppercase.
    
**For example:**
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
```
    
 Output:
 
![image](https://user-images.githubusercontent.com/70228962/186727762-9ca23c43-6cb0-4026-a00d-c443324950ee.png)  
    
</blockquote>
</details>
  
---

11. Design the angular application to print user's brithday in this format "MAY 19, 1997".
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

1. Create an angular application by running `ng new myapp` command 
2. In `app.component.html`, get the user's brithdate. Also, import `FormsModule` in the `app.module.ts` and create `brithdate` variable of type `number` like `birthday !: number;` in the `app.component.ts`.
 ```html
 <p>Enter your birthday: <input type="date" [(ngModel)]="birthday"> <br/></p>

<p>Date Of birth : {{ birthday | date | uppercase}} </p>
<!-- OUTPUT Date Of birth : MAY 19, 1997 -->  
 ```
   
 Here we're chaining pipes, chaining the `date` pipe and `uppercase` pipe. If, we just have only date pipe `{{ birthday | date }}` the output will be like `Aug 3, 2022`. Since the excepted output has Month is in uppercase, there is need to transform month to the uppercase. so will chain the uppercase pipe after the date pipe. 

</blockquote>
</details>
  
---

12. What is use of `PipeTransform` in angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`PipeTransform` is an interface that is implemented by pipes in order to perform a transformation. Angular invokes the `transform` method with the value of a binding as the first argument, and any parameters as the second argument in list form.
    
```ts
interface PipeTransform {
  transform(value: any, ...args: any[]): any
}
```
</blockquote>
</details>
  
---
