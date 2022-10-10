1. Which angular package `HttpClient` service is available?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`@angular/common/http` 

</blockquote>
</details>
  
---
 
2. Why do we need `HttpClient`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The front-end of applications communicate with back-end services to get or send the data over HTTP protocol using either XMLHttpRequest interface or fetch API . This communication is done in Angular with the help of `HttpClient`.

</blockquote>
</details>
  
---
 
3. List some `HttpClient` methods provided by the angular framework.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- `HttpClient.get()` method is used to fetch data from a server. 
- `HttpClient.post()` method is used to send the data to the server.
- `HttpClient.put()` method is used to update the data in th server
- `HttpClient.delete()` method is used to delete the data in the server

All `HttpClient` methods return an **Observable** of something. In general, an observable can return multiple values over time. 
	
</blockquote>
</details>
  
---
 
4. How we can consume RESTful APIs in Angular Projects?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
	
We can consume RESTful APIs in Angular application using HttpClient API.
	
</blockquote>
</details>
  
---
 
5. How to use HttpClient in Angular? _or_ How do you consume REST API in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

HttpClient API service is used to make communication between front-end web apps with backend services. This communication is done over HTTP protocol.

To work with HttpClient service in Angular, you need to import the `HttpClientModule` in `app.module.ts` file. Then inject HttpClient service in constructor method after that you can hit the remote server via HTTP’s POST, GET, PUT and DELETE methods.

Then create a service (`employee.service.ts`) to handle all HTTP requests. We import the `HttpClient` and `HttpHeaders` services to make the HTTP request work. Here, we create CRUD operations using HttpClient methods (GET, POST, PUT, DELETE) 
	
For example:
```ts
import { Injectable } from '@angular/core';
import { HttpClient, HttpHeaders } from '@angular/common/http';
import { Observable } from 'rxjs';
import { Employee } from './Employee';

@Injectable({providedIn: 'root'})
export class EmployeeService {
  // Base url
  baseurl = 'http://localhost:3000/employees/';
  
  constructor(private http: HttpClient) { }
  
  // Http Headers
  httpOptions = {
    headers: new HttpHeaders({
      'Content-Type': 'application/json'
    })
  }
  
  // POST
  CreateEmployee(data): Observable<Employee> {
    return this.http.post<Employee>(this.baseurl , JSON.stringify(data), this.httpOptions);
  }  
  
  // GET
  GetEmployee(id): Observable<Employee> {
    return this.http.get<Employee>(this.baseurl + id)
  }
  
  // PUT
  UpdateEmployee(id, data): Observable<Employee> {
    return this.http.put<Employee>(this.baseurl + id, JSON.stringify(data), this.httpOptions)
  }
  
  // DELETE
  DeleteEmployee(id){
    return this.http.delete<Employee>(this.baseurl + id, this.httpOptions)
    )
  } 
}
```

</blockquote>
</details>
  
---
 
6. What is an observable? How is related with HttpClient?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


Observable in Angular is a feature that provides support for delivering messages between different parts of your single-page application. This feature is frequently used in Angular because it is responsible for handling multiple values, asynchronous programming in Javascript, and also event handling processes.
	
All `HttpClient` methods return an **Observable** of something.
	
</blockquote>
</details>
  
---
 
7. How do you handle errors with HttpClient?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

By using Angular's *HttpClient* along with `catchError` from RxJS, we can easily write a function to handle errors within each service. *HttpClient* will also conveniently parse JSON responses and returns an observable object. 

There are two categories of errors which need to be handled differently:
* Client-side: Network problems and front-end code errors. With *HttpClient*, these errors return *ErrorEvent* instances. 
* Server-side: AJAX errors, user errors, back-end code errors, database errors, file system errors. With *HttpClient*, these errors return HTTP Error Responses.

By verifying if an error is an instance of *ErrorEvent*, we can figure out which type of error we have and handle it accordingly. 

To catch errors, we "pipe" the observable result from `http.get()` (or any *HttpClient* methods) through an RxJS `catchError()` operator. Also, we add the `retry(1)` function to the pipe to retry all requests once before failing.

</blockquote>
</details>
  
---
 
8. Have you heard of Subjects? If so, tell me what is it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

A Subject is a special type of Observable that allows values to be multicasted to many Observers. The subjects are also observers because they can subscribe to another observable and get value from it, which it will multicast to all of its subscribers.

</blockquote>
</details>
  
---
 
9. How subjects differ from observable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Every Subject is an Observable. Given a Subject, you can subscribe to it, providing an Observer, which will start receiving values normally. From the perspective of the Observer, it cannot tell whether the Observable execution is coming from a plain unicast Observable or a Subject.

</blockquote>
</details>
  
---
 
10. What is the difference between a promise and an observable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

11. Every frontend application needs to communicate with the backend microservices to share the data over the HTTP protocol. How this communication established in angular? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Using `HttpClient` Service

</blockquote>
</details>
  
---
 

