1. Design an angular application with following criteria.
    - `/login` need to the login page or template
    - `/register` need to the register page or template
 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
    
1. Run the `ng new routing-app --routing ` command to generate a basic Angular app with an app routing module, where we can configure our routes.
2. To use the Angular router, an app needs to have at least two components so that it can navigate from one to the other. Run these command `ng g c login` and `ng g c register` to generate 2 components - *LoginComponent* and RegisterComponent*.
3. In the app routing module, the CLI creates a Routes array used to define our routes. There we can path `/login`  and  `/register`
```typescript
const routes: Routes = [
  { path: 'login', component: LoginComponent },
  { path: 'register', component: RegisterComponent },
];
```

</blockquote>
</details>
  
---
 
2. How do to create an angular project, when I need to navigate between components?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
    
Run the `ng new routing-app --routing ` command to generate a basic Angular app with an app routing module, where we can configure our routes.

</blockquote>
</details>
  
---
 
3. Why do we need router guards?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

To prevent unauthorized access to certain parts of our navigation, we use route guards in Angular.

</blockquote>
</details>
  
---
 
4. What is the purpose `routerLink` attributes and `<routeroutlet>`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

* `<router-outlet>` - works as a placeholder to load the different components dynamically based on the activated component.

*  *routerLink* - is an attribute to an anchor tag which sets the route for the component.


</blockquote>
</details>
  
---
 
5. Where you define the routes in the Angular application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

In `app.routing.ts` file, you can add the paths and components under `routes` array.
```ts
 const routes: Routes = [
  { path: 'first-component', component: FirstComponent },
  { path: 'second-component', component: SecondComponent },
];
```        

</blockquote>
</details>
  
---
 
6. List some of the interfaces used in routing guards?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

* `CanActivate` - decides if the route can be activated.
* `CanActivateChild`- decides if children of a route can be activated.
* `CanLoad`- decides if a route can be loaded. 
* `CanDeactivate`- decides if the user can leave a route. 


</blockquote>
</details>
  
---
 
7. How do you create routing guard?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Run the `ng g guard <guard-name>` command in your terminal to generate a guard service. When we run the `ng g guard admin` command, the CLI creates a service class that implements any one of the guard interface.

*admin.guard.ts:*
```typescript
import { Injectable } from '@angular/core';
import { CanActivate, ActivatedRouteSnapshot, RouterStateSnapshot } from '@angular/router';
import { Observable } from 'rxjs';

import { AuthService } from './auth/auth.service';

@Injectable({
  providedIn: 'root'
})
export class AdminGuard implements CanActivate {

  constructor(private authService: AuthService){}

  canActivate(
    next: ActivatedRouteSnapshot,
    state: RouterStateSnapshot): Observable<boolean> | Promise<boolean> | boolean {
      return this.authService.isLoggedIn;
  }
}
```
* Adminguard is a class that implements the *CanActivate* interface and overrides the `canActivate()` method. The canActivate() method uses the following parameters:
    * `next: ActivatedRouteSnapshot` - Contains the information about a route associated with a component loaded in an outlet at a particular moment in time. 
    * `state: RouterStateSnapshot` - Contains the information about router state at a particular moment in time. 

* In this example, the `canActivate()` method to only allow access if the user is logged in. 
Here imported the *AuthService* to get the value of `isLoggedIn` property which holds `true` if the user logged in else `false`.

* We apply the guard to the routes, by imposing `canActivate` property of the path object. 
*admin-routing.module.ts* 
```typescript
const routes: Routes = [
    {
        path: 'admin',
        component: ProjectComponent,
        children: [
            {
                path: 'list',
                component: EmployeeListComponent,
                canActivate: [AdminGuard]
            },            
            {
                path: 'create',
                component: EmployeeListComponent,
                canActivate: [AdminGuard]
            }
        ]
    }
```
* Here, we can access the *EmployeeListComponent* and *EmployeeListComponent* only if we had logged in.



</blockquote>
</details>
  
---

8. Which mechanism in Angular provides a way to navigate from one view to another view in the application.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The Router mechanism in Angular provides a way to navigate from one view to another view in the application.

</blockquote>
</details>
  
---

9. What is use of `RoutingModule` in Angular?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Angular provides a `RouterModule` that has the necessary service providers and directives for navigating through application views. The router defines navigation of views on a single page and interprets URL links to determine which views to create or destroy, and which components to load or unload.
    
</blockquote>
</details>
  
---
