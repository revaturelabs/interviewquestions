## Technical

1.What is Node.js?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- Node.js is a web application framework built on Google Chrome's JavaScript Engine (V8 Engine).

Node.js comes with a runtime environment on which a JavaScript-based script can be interpreted and executed (It is analogous to JVM to JAVA byte code).This runtime allows to execution of a JavaScript code on any machine outside a browser.Because of this runtime of Node.js, JavaScript is now can be executed on the server as well.
	
</blockquote  markdown="1"> 

</details markdown="1">

---

2.Name a few popular apps developed with Node.JS.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
Many leading businesses have used Node.JS to develop quality apps.Some of the most popular ones include Netflix, Uber, LinkedIn, PayPal, and eBay.We can go for Node JS download and create reliable apps for mobile and desktop.

</blockquote  markdown="1">

</details markdown="1">

---

3.Why is Node preferred for real-time applications?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Node meets the low-latency requirements of real-time applications.It is ideal for handling countless client requests and suitable for instant messaging apps and online gaming.Node also allows the reuse of library code packages to save time and effort.Additionally, data syncing between the server and end-user happens quickly when we use Node.JS.

</blockquote  markdown="1">

</details markdown="1">

---

4.Why will you choose Node over other popular frameworks?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg) 

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Developers prefer Node for its simplicity.We can also take advantage of a short response time due to event-based models and non-blocking I/O.Node even supports concurrent processing and eliminates the need to use thread management.Additionally, developers can enjoy a reliable performance as Node is built on Google Chrome V8 Engine.

</blockquote  markdown="1">

</details markdown="1">

---

5.Why is Node not suitable for the development of apps with monolith architecture?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Node.JS relies on single-thread programming to execute functions.Monolith apps generally come with multiple functionalities, and a single-thread approach can delay services.Additionally, a single thread makes use of a single processor core and doesn’t fully utilize server capabilities.As a result, Node is not suitable for monolith apps that have a high load.

</blockquote  markdown="1">

</details markdown="1">

---

6.Why is Node.js Single-threaded?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Node.js is single threaded for async processing.By doing async processing on a single thread under typical web loads, more performance and scalability can be achieved instead of the typical thread-based implementation.

</blockquote  markdown="1">

</details markdown="1">

---

7.If Node.js is single-threaded, then how does it handle concurrency?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- The Multi-Threaded Request/Response Stateless Model is not followed by the Node JS Platform, and it adheres to the Single-Threaded Event Loop Model.
- The Node JS Processing paradigm is heavily influenced by the JavaScript Event-based model and the JavaScript callback system.Hence, Node.js can easily manage more concurrent client requests.The event loop is the processing model's beating heart in Node.js.

</blockquote  markdown="1">

</details markdown="1">

---

8.What are the two types of API functions in Node.js? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

The two types of API functions in Node.js are: 
- Asynchronous, non-blocking functions
- Synchronous, blocking functions

</blockquote  markdown="1">

</details markdown="1">

---

9.What do you mean by Asynchronous API?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- All APIs of the Node.js library is asynchronous that is non-blocking.It essentially means a Node.The js-based server never waits for an API to return data.
- The server moves to the next API after calling it and a notification mechanism of Events of Node.js helps the server to get a response from the previous API call.

</blockquote  markdown="1">

</details markdown="1">

---

10.What is NPM?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- NPM stands for Node Package Manager, responsible for managing all the packages and modules for Node.js.

- Node Package Manager provides two main functionalities:

  - Provides online repositories for node.js packages/modules, which are searchable on search.nodejs.org
  - Provides command-line utility to install Node.js packages and manages Node.js versions and dependencies.

</blockquote  markdown="1">

</details markdown="1">

---

11.What is the control flow function?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

It is a generic piece of code which runs in between several asynchronous function calls and is known as a control flow function.

</blockquote  markdown="1">

</details markdown="1">

---

12.What is the global installation of dependencies?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Globally installed packages/dependencies are stored in /npm directory.Such dependencies can be used in CLI (Command Line Interface) function of any node.js but cannot be imported using require() in the Node application directly.To install a Node project globally use `-g flag`.

</blockquote  markdown="1">

</details markdown="1">

---

13.What do you understand by event-driven programming in Node.js?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- Event-driven programming uses various events (mouse click, keypress, messages from other programs) to initiate/trigger a function in the program.
- Callback functions are already registered with events and when an event is executed, the corresponding callback function is called.
- Therefore, the flow of the program is decided by these events and hence the name.

</blockquote  markdown="1">

</details markdown="1">

---

14.What are the modules in Node.js?


![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Modules are like JavaScript libraries that can be used in a Node.js application to include a set of functions.To include a module in a Node.js application, use the `require()` function with the parentheses containing the module's name.

</blockquote  markdown="1">

</details markdown="1">

---

15.What is the purpose of the module .Exports?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

In Node.js, a module encapsulates all related codes into a single unit of code that can be parsed by moving all relevant functions into a single file.We may export a module with the module and export the function, which lets it be imported into another file with a needed keyword.

</blockquote  markdown="1">

</details markdown="1">

---

16.What is the Express.js package?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

Express is a flexible Node.js web application framework that provides a wide set of features to develop both web and mobile applications.

</blockquote  markdown="1">

</details markdown="1">

---

17.How do you create a simple Express.js application?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- The request object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on.
- The response object represents the HTTP response that an Express app sends when it receives an HTTP request.

</blockquote  markdown="1">

</details markdown="1">

---

18. What are streams in Node.js?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- Streams are objects that enable you to read data or write data continuously.
- There are four types of streams:
  - Readable – Used for reading operations.
  - Writable − Used for writing operations.
  - Duplex − Can be used for both reading and writing operations.
  - Transform − A type of duplex stream where the output is computed based on input.

</blockquote  markdown="1">

</details markdown="1">

---

19.How do you install, update, and delete a dependency?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- To install: `npm install express`.
- To update:  `npm update`.
- To delete:  `npm uninstall express`.

</blockquote  markdown="1">

</details markdown="1">

---

20.What is the package.Json file?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

- The package.json file is the heart of the Node.js system.It is the manifest file of any Node.js project and contains the metadata of the project.

- The metadata information in the package.json file can be categorized into below categories: 
1.**Identifying metadata properties**: It basically consists of the properties to identify the module/project such as the name of the project, current version of the module, license, author of the project, description of the project etc.
2.**Functional metadata properties**: As the name suggests, it consists of the functional values/properties of the project/module such as the entry/starting point of the module, dependencies in the project, scripts being used, repository links of Node project etc.

</blockquote  markdown="1">

</details markdown="1">

---

21.How to create a package.json file in Node.js?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1">

A package.json file can be created in two ways: 
1.**Using npm init** : Running this command, the system expects the user to fill in the vital information required as discussed above.It provides users with default values which are editable by the user.

**Syntax**: 

```Node.js
npm init
```
2.**Writing directly to file** : One can directly write into a file with all the required information and can include it in the Node project.


**Example**: A demo package.json file with the required information.
 
```js
{
  "name": "GeeksForGeeks",
  "version": "1.0.0",
  "description": "GeeksForGeeks",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node start.js",
  },
  "engines": {
    "node": ">=7.6.0",
    "npm": ">=4.1.2"
  },
  "author": "GeeksForGeeks",
  "license": "ISC",
  "dependencies": {
    "body-parser": "^1.17.1",
    "express": "^4.15.2",
    "express-validator": "^3.1.2",
    "mongoose": "^4.8.7",
    "nodemon": "^1.14.12",
  },
  "devDependencies": {},
  "repository": {
    "type": "git",
    "url": "https://github.com/gfg/gfg.git" //sample git repo url
  },
  "bugs": {
    "url": "https://github.com/gfg/gfg/issues"
  },
  "homepage": "https://github.com/gfg/gfg#readme"
}
```

</blockquote  markdown="1">

</details markdown="1">

---

22.How would you use a URL module in Node.js?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 

The URL module in Node.js provides various utilities for URL resolution and parsing.It is a built-in module that helps split up the web address into a readable format.

```js
const url = require('url');
  
const newUrl = new URL(
    'https://revature.org/p/a/t/h?query=string#hash');
  
// url array in JSON Format
console.log(newUrl);
  
const myUR = url.parse(
    'https://revature.org/:3000/p/a/t/h?query=string#hash');
console.log(myUR);
console.log(URL === require('url').URL);
  
const myURL1 = new URL(
    { toString: () => 'https://revature.org/' });
  
console.log(myURL1.href)

```

</blockquote  markdown="1">

</details markdown="1">

---

