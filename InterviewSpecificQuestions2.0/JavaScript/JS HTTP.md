## Technical

1. What is HTTP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

HTTP stands for Hypertext Transfer Protocol. It is a protocol that defines how clients (such as web browsers) and servers communicate over the internet.

</blockquote>
</details>

---

2. What are cookies in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is generally a small data that is sent from a website and stored on the user’s machine by a web browser that was used to access the website. Cookies are used to remember information (e.g., user preferences, settings, passwords) for later use and also to record the browsing activity on a website.

</blockquote>
</details>

---

3. How would you create a cookie?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can create a cookie as below:

``` java
document.cookie = "key1 = value1; key2 = value2; expires = date";
```
</blockquote>
</details>

---

4. Which method is used to break the cookie value in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

`split()` method to break the cookie value into keys and values.

</blockquote>
</details>

---

5. Differentiate Local storage and Session storage?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

`Local Storage` – The data is not sent back to the server for every HTTP request , which will reduce the amount of traffic between client and server. 

`Session Storage` – The data stored in local storage has no expiration time, data stored in session storage gets cleared when the page session ends. Which will leave when the browser is closed.

</blockquote>
</details>

---

6. How do you make an HTTP request in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can make an HTTP request in JavaScript using the `XMLHttpRequest` object or the newer `fetch()` function. Both methods allow you to send requests to a server and receive responses.

</blockquote>
</details>

---

7. What is AJAX?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

AJAX (Asynchronous JavaScript and XML) is a technique that allows you to make asynchronous HTTP requests from JavaScript without reloading the entire web page.

</blockquote>
</details>

---

8. How do you make an HTTP GET request in JavaScript using `fetch()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can make an HTTP GET request using the `fetch()` function by providing the URL you want to request as the first parameter. For example: `fetch('https://api.example.com/data')`.

</blockquote>
</details>

---

9. How do you handle the response of an HTTP request in JavaScript using `fetch()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can handle the response of an HTTP request using the `.then()` method and passing a callback function that processes the response data. For example:
```javascript
fetch('https://api.example.com/data')
  .then(function(response) {
    // Handle the response
  });
```
</blockquote>
</details>

---

10. How do you make an HTTP POST request in JavaScript using `fetch()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To make an HTTP POST request using `fetch()`, you need to pass an object as the second parameter with the `method` set to `'POST'` and include the request payload. For example:
```javascript
fetch('https://api.example.com/data', {
  method: 'POST',
  body: JSON.stringify({ name: 'John', age: 25 })
});
```
</blockquote>
</details>

---

11. How do you handle errors in an HTTP request using `fetch()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can handle errors in an HTTP request by adding a `.catch()` block after the `.then()` block to catch any network errors or failed responses. For example:
```javascript
fetch('https://api.example.com/data')
  .then(function(response) {
    // Handle the response
  })
  .catch(function(error) {
    // Handle the error
  });
```
</blockquote>
</details>

---

12. What is JSON?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is often used for data transfer between a client and server.

</blockquote>
</details>

---

13. How do you parse JSON data in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can parse JSON data in JavaScript using the `JSON.parse()` function, which converts a JSON string into a JavaScript object. For example: `var obj = JSON.parse('{"name":"John","age":25}');`

</blockquote>
</details>

---

14. How do you stringify an object to JSON in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can stringify a JavaScript object to JSON using the `JSON.stringify()` function, which converts a JavaScript object into a JSON string. For example: `var jsonString = JSON.stringify({ name: 'John', age: 25 });`

</blockquote>
</details>

---

15. What are the differences between synchronous and asynchronous HTTP requests in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Synchronous HTTP requests block the execution of code until the response is received, while asynchronous HTTP requests allow the code to continue running without waiting for the response. Asynchronous requests are typically preferred as they do not freeze the user interface.

</blockquote>
</details>

---

16. What is the XMLHttpRequest object in JavaScript used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The XMLHttpRequest object is used to send HTTP requests and receive responses asynchronously. It provides methods to handle various aspects of the request, such as setting headers, monitoring progress, and handling responses.

</blockquote>
</details>

---

17. How do you make an HTTP request with the XMLHttpRequest object in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To make an HTTP request with the XMLHttpRequest object, you create an instance of it, set the request method, URL, and any headers or parameters, and then call the `open()` and `send()` methods. You can also define callback functions to handle the response. Here's an example:
```javascript
var xhr = new XMLHttpRequest();
xhr.open('GET', 'https://api.example.com/data', true);
xhr.setRequestHeader('Content-Type', 'application/json');
xhr.onreadystatechange = function() {
  if (xhr.readyState === XMLHttpRequest.DONE && xhr.status === 200) {
    var response = JSON.parse(xhr.responseText);
    // Handle the response
  }
};
xhr.send();
```
</blockquote>
</details>

---

18. What is the Fetch API in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The Fetch API is a modern replacement for XMLHttpRequest that provides a simpler and more powerful way to make HTTP requests. It uses promises and allows for a more flexible handling of requests and responses.

</blockquote>
</details>

---

19. What is CORS (Cross-Origin Resource Sharing)?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

CORS is a mechanism that allows resources (e.g., JavaScript) on a web page to make requests to a different domain than the one the page originated from. It is used to enhance security and prevent unauthorized access to resources.

</blockquote>
</details>

---

20. How do you handle CORS-related issues in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To handle CORS-related issues, you can set appropriate CORS headers on the server-side to allow or restrict access to resources. On the client-side, you may need to use techniques like JSONP, proxy servers, or server-side proxies to overcome CORS restrictions.

</blockquote>
</details>

---