1. How do you make a service available for a component?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
Let's consider, we have to make `UserService` available for a `UserComponent` in our angular application.
  
In the `user.component.ts` file, add the `UserService` in the `providers` property of `@Component` decorator
```ts
import { Component, OnInit } from '@angular/core';
import { UserService } from '../user.service';

@Component({
  selector: 'app-user',
  templateUrl: './user.component.html',
  styleUrls: ['./user.component.css'],
  providers : [UserService]
})
export class UserComponent implements OnInit  {

  constructor(private  user : UserService) {  }
  ngOnInit(): void {
    console.log("Form User Component")
    this.user.display()
  }
}
```
  
</blockquote>
</details>
  
---

2. How do you make a service available at application level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Let's consider, we want to make `UserService` available for all the components. 

In the `user.service.ts` file, by default, AngularCLI sets the providedIn to `root` registers the service at the module level. So that is available for all compoenents.
  
```ts
import { Injectable } from '@angular/core';

@Injectable({ providedIn: 'root' })
export class UserService {
}
```
  
</blockquote>
</details>

---

3.  How do you make service available at the NgModule level? _or_ How do you make service available for all components in a NgModule?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
 
At the NgModule level, using the `providers` field of the `@NgModule` decorator. In this scenario, the `UserService` is available to a**ll components, directives and pipes** declared in this NgModule.
  
For example:
```ts
@NgModule({
  declarations: [UserListComponent]
  providers: [UserService]
})
class UserListModule {}
``` 
  
When you register a provider with a specific NgModule, the same instance of a service is available to all components in that NgModule.
  
</blockquote>
</details>

---

4. How do you inject a dependency in angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
The most common way to inject a dependency is to declare it in a **class constructor**. When Angular creates a new instance of a component, directive, or pipe class, it determines which services or other dependencies that class needs by looking at the constructor parameter types.
  
```ts
@Component({ … })
class HeroListComponent {
  constructor(private service: HeroService) {}
}
```

</blockquote>
</details>
  
---
