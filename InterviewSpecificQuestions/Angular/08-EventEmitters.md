1. In Angular, how can you interact between Parent and Child components?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
  
 When passing data from Parent to Child component, you can use the `@Input` decorator in the Child component. When passing data from Child to Parent component, you can use the `@Output` decorator in the Child component.
  
</blockquote>
</details>
	
--- 
2. How would you pass data from a parent to a child component or a child to a parent component?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>

- `@Input` decorator used to pass the data from a parent to a child component
- `@Output` decorator used to pass the data from a child to a parent component
	
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
  
 
