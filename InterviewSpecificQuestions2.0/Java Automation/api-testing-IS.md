1. Why is `API Testing` important?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- API Testing is important for ensuring that the API which we built performs as expected when faced with a wide variety of expected and unexpected requests.

</blockquote>
</details>
  
---

2. What aspects can be covered under `API Testing`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

API testing can be done on the below aspects:
- `Functional Testing`: Checks API's functionality, takes payload in the form of JSON or XML and provides the response code and response body. 
- `Load Testing`:  Checks the performance under the specific load and determines how much traffic the API can handle before being overloaded. 
- `Security Testing`: Checks vulnerabilities like authentication and sensitive data is encrypted over HTTP and includes penetration testing validating authentication.

</blockquote>
</details>
  
---

3. What are the benefits of Automated API Testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are many benefits to automating API testing, including:
- **Improved accuracy**: Automated tests improves precision over manual testing.
- **Reduced cost**: Comparatively less expensive to run than manual tests.
- **Increased coverage**: Can cover a larger area of functionality than manual tests.
- **Faster feedback**: Quicker results than manual tests.
- **Easier maintenance**: Easier to maintain and update than manual tests.
- **Reduced human error**: Produce fewer errors than manual tests run by DevOps.

</blockquote>

</details>

---

4. What is the `Postman Collection`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- `Postman Collection` is a tidy way to group our API requests together so you can save, reuse, and share them with others.
  
  
</blockquote>
</details>
  
---

5. What is `Testing Collection` in Postman?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Testing Collection in Postman is used for testing the behaviour of our API. 
- We can communicate with other team members about how API functions or demonstrate the API’s behaviour under various circumstances.

</blockquote>
</details>
  
---
  
6. What is `Documentation Collection` in Postman??

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Documentation Collection in Postman is used for documentation or showing others how to consume the API.
- Documentation should cover why the APIs used are important, and the how and why to use each endpoint, with examples.
     
</blockquote>

</details>

---

7. What is `Newman` API testing?
   
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `Newman` is a command-line Collection Runner for Postman. 
- We can run and test a Postman Collection directly from the command line. 
- It's built with extensibility in mind and easily integrates with CI servers and build systems.
- Newman resides in the npm registry and on GitHub.

</blockquote>

</details>
  
---

8. How Postman collections are passed to Newman for API testing?
   
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Newman expects or consumes the JSON version of the collection as input.
- It can be obtained by simply exporting the collection in JSON collection format from the postman or the URL of the Postman collection which is nothing but the same JSON that’s obtained by the collection export.

```
newman run {{collectionJsonPath}}
      OR
newman run {{collectionUrl}}
```

</blockquote>

</details>
  
---

9. Is it possible to generate HTML report using Newman?
   
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- There are few custom node modules available for generating Newman test execution reports. 
- First, we need to install the `newman-HTML-reporter` module.

```
npm install -g newman-reporter-html
```
- Once the node module is installed, it can be used along with the Newman run command as follows:

```
newman run Postman_Newman_Collection.json -e enVariable.json -r html
```
- The '-r' flag, indicates the newman-reporter-html module to be used with the Newman collection run.

</blockquote>

</details>
  
---

10. What is `SoapUI`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- `SoapUI` is a tool for testing Web Services; these can be the SOAP Web Services as well as RESTful Web Services or HTTP-based services. 
- `SoapUI` is an Open Source and completely free tool with a commercial companion called `ReadyAPI` that has extra functionality for companies with mission-critical Web Services.

</blockquote>
</details>
  
---

11. What can we use SoapUI for?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- SoapUI can be used for complete RESTful API and SOAP Web Service testing.
- We can do Functional Testing, Performance Testing, Interoperability Testing & Regression Testing etc using SoapUI. 
- Using SoapUI we can-
  - simulate Web Services. 
  - record tests and use them Later. 
  - create code stubs from the WSDL. 
  - create REST specifications (WADL)from recorded communication.
  - Just right-click a functional test and run it as a load test.
  
</blockquote>
</details>
  
---

12. What protocols are supported by SoapUI?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- SoapUI has the most comprehensive support for various protocols as shown below:
  ![SoapUI protocols](https://user-images.githubusercontent.com/110081175/200236666-56cd75e8-7256-4ed6-8f67-c34b4437bd0a.PNG)
  
</blockquote>
</details>
  
---

13. What is the difference between SoapUI and Selenium?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

|SoapUI                               |Selenium                           |
|-------------------------------------|-----------------------------------|
| SoapUI is NOT used for User Interface Testing. It is only used for WebAPI or WebService Testing | Selenium is used for User Interface Testing. |
| Capability to test the data sent and received between the web browser and a web server. Can test protocols/technologies such as REST, and SOAP. | Selenium cannot test protocols, but it can test the UI behaviour.|
| SoapUI is able to perform functional, load and Security Testing of the above-mentioned technologies. | Selenium can perform only Functional Testing. Performance Testing to some extent because we can track execution time with regards to the performance but cannot test multi-user and multi-tenancy. Selenium certainly cannot be used for security testing. |
|SoapUI is PROTOCOL Dependent and NOT browser dependent. | Selenium depends on the browser’s capabilities. |
</blockquote>
</details>
