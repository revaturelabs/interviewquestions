1. What’s the difference between TDD and BDD? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

| Behavior Driven Development (BDD)                                   | Test Driven Development (TDD)             |
|----------------------------------------------------------------------|-------------------------------------------|
| BDD Scenarios are derived through collaboration between team members | Implemented by developers                 |
| BDD Scenarios are written in Natural Language                        | Written in a programming language         |
| Created and maintained by the entire team                            | Created and maintained by developers      |
| Black-box testing                                                    | White-box testing                         |
| Tests the end-to-end behavior of the application                     | Tests are written for individual function |

</blockquote>
</details>
  
---

2. What is meant by BDD testing?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Behavior Driven Development (BDD) Testing is used to test an application's behaviour from the end user's standpoint. 
  
In BDD, test cases are written in a natural language that even non-programmers can read.
  
</blockquote>
</details>
  
---

3. What is automation testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Automation testing is a software testing strategy in which a tester programmatically runs the tests using a tool or a framework instead of manually going through the test cases and executing them one by one.

</blockquote>
</details>
  
---

4. What is Selenium?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Selenium is an open-source automated testing framework for validating web applications across multiple browsers and platforms.

</blockquote>
</details>
  
---

5. How Selenium launches web browsers?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Using Selenium WebDriver.

</blockquote>
</details>
  
---

6. Why do you need Selenium Automation Testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Let's consider a scenario: Checking whether the web app’s signup page (www.example.com/signup) validates input strings and registers a user successfully.

Assume that the signup page has these input fields—username, email address, and password. 

As a manual tester, we need to follow these steps:

1. Enter the URL in the address bar (www.example.com/signup)
2. Enter an invalid string in each input field (email, username, and password)
3. Check whether the input strings were validated against corresponding regexes and any pre-existing values in the database
4. Enter _valid_ strings in each input field; click Sign Up
5. Check whether _Welcome, {username}_ page showed up
6. Check whether the system database created a new userID for _{username}_
7. Mark the test _passed_ if it did, _failed_ if the signup feature broke anywhere during the test.

Depending on the number of manual testers (and the thoroughness of test cases), it may take anywhere between hours to weeks to be sure that the web app is fully functional.

Modern developers and product teams don’t have that kind of time to allow for testing, but they can’t set aside exhaustive testing in a hurry to release either. 

Therefore, we go for automation testing with Selenium.

</blockquote>
</details>
  
---

7. List the steps to perform a test through Selenium?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

1. Download browser drivers
2. Create a WebDriver instance.
3. Navigate to a webpage.
4. Locate a web element on the webpage via locators in selenium.
5. Perform one or more user actions on the element.
6. Preload the expected output/browser response to the action.
7. Run the test.
8. Record results and compare results them to the expected output.
9. Close the WebDriver

</blockquote>
</details>
  
---

8. How do you navigate to a particular webpage URL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

To navigate to a particular webpage URL, one can use either of the following commands:

- Using the get method: 
	
```java
driver.get("https://www.example.com") ;
```	
	
- Using the navigate method

```java
driver.navigate().to("https://www.example.com/signup");
```
	
</blockquote>
</details>
  
---

9. How can I move to a page in the browser history in selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The forward command navigates the browser forward by one page recorded in the browsing history.

```java
driver.navigate().forward();
```
	
</blockquote>
</details>
  
---

10. How can I go back to the previous page in selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The back command instructs the browser to redirect to the immediate previous webpage.

```java
driver.navigate().back();
```
	
</blockquote>
</details>
  
---

11. How can I reload a page using selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The Refresh command instructs the browser to reload or refresh the current web page.

```java
driver.navigate().refresh();
```

</blockquote>
</details>
  
---

12. What are Locators in Selenium? List the types of locators.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

A locator enables testers to select an HTML DOM element to act on. Some of the different locators are:

|        Method        |                        Syntax                       |                  Description                 |
|:--------------------:|:---------------------------------------------------:|:--------------------------------------------:|
| By ID                | driver.findElement(By.id (<element ID>))            | Locates an element using the ID attribute    |
| By name              | driver.findElement(By.name (<element name>))        | Locates an element using the Name attribute  |
| By class name        | driver.findElement(By.className (<element class>))  | Locates an element using the Class attribute |
| By tag name          | driver.findElement(By.tagName (<htmltagname>))      | Locates an element using the HTML tag        |
| By link text         | driver.findElement(By.linkText (<linktext>))        | Locates a link using link text               |
| By partial link text | driver.findElement(By.partialLinkText (<linktext>)) | Locates a link using the link's partial text |
| By CSS               | driver.findElement(By.cssSelector (<css selector>)) | Locates an element using the CSS selector    |
| By XPath             | driver.findElement(By.xpath (<xpath>))              | Locates an element using XPath query         |

</blockquote>
</details>
  
---

13. Consider the following form and tell me how we can locate the input elements.
```html
<form id="loginForm">
	<input name="name" type="text" value="Name" />
	<input name="email" type="text" value="Email" />
</form>
```

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Using the `driver.findElement(By.name (<element name>))` method, we can locate the `name` and `email` form elements.
	
```java
email_input = driver.findElement(By.name("email"))
name_input = driver.findElement(By.name("name"))
``` 	

</blockquote>
</details>
  
---

14. Consider the following form and tell me how we can locate the input elements.
```html
<form id="loginForm">
	<input name="name" type="text" value="First Name" />
	<input name="name" type="text" value="Last Name" />
</form>
```

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

If we can locate by name, we are able to only locate the first name, not the last name. Also, we can't locate the first name and last name by ID or class. So, we can locate these elements through its XML path.  
	
We will use the `driver.findElement(By.xpath (<xpath>))` method to locate an appropriate element in the document. 
	
The following code first searches for a form with the ID login form and then selects the form’s first and second input elements as the first and last names.

```java
first_name = driver.findElement(By.xpath ("//form[@id='loginForm']/input[1]"))
last_name = driver.findElement(By.xpath ("//form[@id='loginForm']/input[2]"))
```

</blockquote>
</details>
  
---

15. How can I get all the elements in the HTML DOM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The `findElementsBy()` method helps in finding multiple elements in the DOM structure.

For example, to find all input elements of a form with ID loginForm, we use: 
	
```java
List<WebElement> inputs = driver.findElementsBy(By.id("loginForm"));
```
	
</blockquote>
</details>
  
---

16. What is HTML Source?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

HTML Source refers to the HTML code underlying a certain web element on a web page.

</blockquote>
</details>
  
---

17. What is a Web Element?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Anything that appears on a web page is a web element. Also, web elements mean the tags within the web page’s HTML code.
- Web element refers to text boxes, checkboxes, buttons, or any other fields that display or require data from the user. Such elements usually have unique identifiers, such as ID, name, or unique classes. 

</blockquote>
</details>
  
---

18. `FindElement()` vs `FindElements()`

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

| Find Element                                                                                      | Find Elements                                                                    |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Returns the first most web element if there are multiple web elements found with the same locator | Returns a list of web elements                                                   |
| Throws exception NoSuchElementException if there are no elements matching the locator strategy    | Returns an empty list if there are no web elements matching the locator strategy |
| Find element by XPath will only find one web element                                              | It will find a collection of elements that match the locator strategy.          |
| Not Applicable                                                                                    | Each Web element is indexed with a number starting from 0 just like an array     |
| Example: driver.findElement(By.id("no"))                                                          | Example: List elements = driver.findElements(By.name("name"));                   |

</blockquote>
</details>
  
---
	
19. What is XPath in Selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

XPath, also known as XML Path, is used to locate any element in a web page using its tag name, ID, CSS class, and so on.
	
The basic format of XPath in Selenium is explained below.
```
XPath = //tagname[@Attribute='Value']
```
	
Here,

- `//`: denotes the current node
- `tagname`: denotes the tagname of the current node
- `@`: is the Select attribute
- `Attribute`: denotes the attribute of the node
- `Value`: denotes the value of the chosen attribute

</blockquote>
</details>
  
---
	
20. What are the types of XPath in Selenium?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

There are two types of XPath in Selenium.

1. **Absolute XPath** 
	- It starts with a single slash `/`
	- Provides the entire path starting from the root node
	- Example: `/html//div/div/div/div[1]/div/a/img`
2. **Relative XPath** 
	- It starts with a double slash `//`
	- Here XPath expression starts from the middle of the DOM structure denoting the current node.
	- Example: `//img[@alt='LambdaTest']`

</blockquote>
</details>
  
---	
	
21. What is Cucumber?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Cucumber is a behaviour-driven development (BDD) testing tool. 
- It allows testers to create test cases for evaluating program behaviour. 
- It's primarily used to develop acceptance tests for web apps based on their features' behaviour.
- It provides a method for writing tests that anyone, regardless of technical knowledge, can comprehend. 

</blockquote>
</details>
  
---

22. What language is used by the Cucumber tool?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- The Cucumber tool uses the Gherkin language, a simple English representation of the application behaviour. 
- The Gherkin language uses several keywords to describe the behaviour of applications such as Feature, Scenario, Scenario Outline, Given, When, Then, etc.

</blockquote>
</details>
  
---

23. What is a Feature file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Features files contain a high-level description of the Test Scenario in simple language.
- It consists of the components like Feature, Scenario, Scenario outline, Given, When, Then

</blockquote>
</details>
  
---


24. What do you mean by feature in Cucumber?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

A project's feature can be described as a stand-alone unit or functionality. 

Example: For an e-commerce website, we can have the following features: -

- User registers and signs up on the website
- User tries to log in to their account using their credentials
- Users add a product to their cart
- User clicks on checkout now
- User pays for their items
- User logs out from the website


</blockquote>
</details>
  
---


25. What do you mean by Scenario in Cucumber?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The scenario is a fundamental Gherkin structure. Every feature can have one or more scenarios, each of which has one or more steps. 

For example,
 
**Scenario − Verify My Orders Functionality**

_Explanation_: When a user clicks on the My Orders option, he/ she should be taken to the My Orders page

</blockquote>
</details>
  
---



26. What do you mean by Scenario Outline?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Consider the situation when we need to run a test scenario multiple time.
- Assume we need to ensure that the login feature is functional for all types of subscribers. 
- This necessitates repeating the login functionality scenario. 
- Copying and pasting the identical instructions to just re-run the code does not appear to be a good approach. 

Scenario Outline is used when the same scenario needs to be executed for multiple sets of data, however, the test steps remain the same. Also, a Scenario outline is a way of parameterization of scenarios.

```
Scenario Outline: A user wants to update the status of any potentially completed todos
		Given the user has <complete> completed todos and <incomplete> incomplete todos in their list of todos
		When the user hits the CHECK TODOS button
		Then <complete> of the todos will be marked as complete on the page
		And there should be a total of <total> todos listed on the page
		
		Examples:
			| complete | incomplete | total   |
			| 3        | 6          | 9       |
			| 10       | 1          | 11      |  
			| 4        | 19         | 23      |
```

</blockquote>
</details>
  
---


27. What are the two files required to execute a Cucumber test scenario?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Feature file
- Step Definition file

</blockquote>
</details>
  
---


28. What is the purpose of the Step Definition file in Cucumber?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- While feature files are written in an easily understandable language like, Gherkin, Step Definition files are written in programming languages such as Java, .Net, Ruby, etc
- It essentially acts as a translator between the test scenario steps provided in the feature file and the automation code.
- Each step of the feature file can be mapped to a corresponding method on the Step Definition file.
- Cucumber searches the step definition file and executes the relevant functions that are assigned to that step when it runs a step described in the feature file.

</blockquote>
</details>
  
---


29.  Give an example of a feature file using the Cucumber framework.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Feature: Login to the application under test.
Scenario: Login to the application.

- Open the Chrome browser and launch the application.
- When the user enters the username into the UserName field.
- And the User enters the password into the Password field.
- When the user clicks on the Login button.
- Then validate if the user login is successful.

</blockquote>
</details>
  
---


30. List some common BDD keywords. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Scenario: a representation of a concrete example of the behaviour of the system that is in development or under test.
- Step: scenarios are composed of steps. There are three types of steps: given, when, and then:
	- Given: specifies a precondition to an event that will or should or occur during a scenario.
	- When: specifies the occurrence of the event itself.
	- Then: specifies the expected outcome of the event that has occurred.
- Background: used when all the scenarios within a feature share at least one precondition. The preconditions defined using the background keyword apply to all scenarios within a feature.
- Scenario Outline: used to create a data-driven driven scenario that is run several times around different sets of data.
- Examples: used to define data sets for scenario outlines.
- And/But: used to replace given, when, or then. If, for instance, there are multiple preconditions for a scenario, a developer may choose to use and our but for every precondition following the first precondition. 

For example:

```
Given first precondition
And second precondition
And third precondition
When event occurs
And another event occurs
Then expected outcome
```

</blockquote>
</details>
  
---


31. Difference between Selenium and Cucumber.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

| Selenium                                                           | Cucumber                                                                                       |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Selenium is a web browser automation tool for web projects         | Cucumber is a behaviour-driven development automation tool that may be used with Selenium.      |
| Automation tool for E2E tests                                      | Automation tool for BDD tests                                                                  |
| Selenium is written in programming languages like Java, .Net, etc. | Cucumber is written both in programming language as well as plain text.                        |
| Requires programming knowledge to understand                       | Easier to read as it is written in both programming language as well as plain readable format. |

</blockquote>
</details>
  
---


32. How we can implement BDD using cucumber?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


The general workflow for implementing BDD using Cucumber is as follows:

1. A developer must first write their feature files in Gherkin. A feature file defines several scenarios and steps to define a system's behaviour level.
2. After the developer has finished drafting the feature file, they should generate their glue code by running the feature file. We'll talk more about glue code in the future, but for now, you need only know that this glue code consists of potential test methods that are associated with a scenario's steps. We say "potential" test methods because the developer may or may not choose to implement those suggested test methods.
3. Once the developer has generated the glue code and written the tests, they should choose a test runner for running the glue code.

</blockquote>
</details>
  
---


33. What Is Glue Code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


- While Gherkin is understandable for everyone on a development team, feature files are not compatible with the programming languages in which applications are written. 
- If, for instance, a developer is writing an application in Java, the compiler can't make sense of Gherkin.
- Because of this incompatibility, Cucumber allows developers to "translate" Gherkin into source code into the appropriate source code based on the BDD keywords used within the feature file. 
- The source code that Cucumber generates is called glue code. 

</blockquote>
</details>
  
---


34. What is the purpose of the Cucumber Options tag?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


The cucumber Options tag is used to provide a link between the feature files and step definition files. 
Each step of the feature file is mapped to a corresponding method on the step definition file.

Below is the syntax of the Cucumber Options tag:

```
@CucumberOptions(features="Features",glue={"StepDefinition"})
```

</blockquote>
</details>
  
---



35. Is glue code enough to run the test?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

No. Glue Code is not quite a test suite. We need to do a couple of more things to get a suite up and running.

We need to create CucumberTestRunner class annotated with @CucumberOptions and @RunWith annotations.

```java
//CucumberTestRunner.class
@CucumberOptions(
	features = "features/TodoComplete.feature",
	glue = "com.revature.gluecode")
@RunWith(Cucumber.class)
public class CucumberTestRunner {
}
```

</blockquote>
</details>
  
---


36. What happens if we try to query for an element, but that element does not exist on the page?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


Selenium will throw a `NoSuchElementException`. There is also a chance that we have a reference to an element that no longer exists.

</blockquote>
</details>
  
---


37. Suggest what we can do when we get `NoSuchElementException`.


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


In NoSuchElementException cases, we would like to wait for the element to appear. There are two ways of approaching this:

- Implicit waits are a global configuration on the WebDriver object and apply every time the DOM is queried. 
- Explicit waits apply individually and adjust the waiting time explicitly and dynamically at regular intervals. 

</blockquote>
</details>
  
---


38. What is the reason to go for the Page Object Model?

	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Imagine you are trying to automate a single-page application. There are multiple views that you need to interact with and many elements to query for. Navigating to pages and repeatedly querying the DOM can result in messy, unorganized code. A simple design pattern to organize your code around is called the Page Object Model.


</blockquote>
</details>
  
---


39. What is a `Page Object Model` in Selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


- Page Object Model, also known as POM, is a design pattern in Selenium that creates an object repository for storing all web elements. 
- It is useful in reducing code duplication and improves test case maintenance. 
- In-Page Object Model, consider each web page of an application as a class file.

</blockquote>
</details>
  
---


40. What is `Page Factory` in Selenium?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


`Page Factory` is a class provided by Selenium WebDriver to support Page Object Design patterns. 
In Page Factory, testers use `@FindBy` annotation. 
The `initElements` method is used to initialize web elements.

`@FindBy:` An annotation used in Page Factory to locate and declare web elements using different locators. Below is an example of declaring an element using @FindBy

```java
@FindBy(id="elementId") WebElement element;
```

initElements(): initElements is a static method in Page Factory class. Using the initElements method, one can initialize all the web elements located by @FindBy annotation.

</blockquote>
</details>
  
---


41. Difference Between Page Object Model and Page Factory in Selenium.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


| Page Object Model                                              | Page Factory                                                                                    |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Finding web elements using By                                  | Finding web elements using @FindBy                                                              |
| POM does not provide lazy initialization                       | Page Factory does provide lazy initialization                                                   |
| Page Object Model is a design pattern                          | PageFactory is a class that provides the implementation of the Page Object Model design pattern |
| In POM, one needs to initialize every page object individually | In Page Factory, all page objects are initialized by using the initElements() method             |

</blockquote>
</details>
  
---

42. How do you handle alerts using Selenium?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


Selenium provides a wide range of functionalities and methods to handle alerts.

The following methods are useful to handle alerts in selenium:

1. void dismiss(): This method is used when the 'Cancel' button is clicked in the alert box.
```java
driver.switchTo().alert().dismiss();
```
2. void accept(): This method is used to click on the 'OK' button of the alert.
```java
driver.switchTo().alert().accept();
```
3. String getText(): This method is used to capture the alert message.
```java
driver.switchTo().alert().getText();
```
4. void sendKeys(String stringToSend): This method is used to send data to the alert box.
```java
driver.switchTo().alert().sendKeys("Text");
```

</blockquote>
</details>
  
---


43. How I can select a value from the dropdown using Selenium?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>


The following methods help us to select a desired option/value from the dropdown list.

- selectByVisibleText() method is used to select one of the options in a drop-down box or an option among multiple selection boxes.

```java
Select objSelect =new Select(driver.findElement(By.id("search-box")));
objSelect.selectByVisibleText("Automation");
```

- selectByIndex() method is similar to ‘selectByVisibleText’, but the difference here is that the user has to provide the index number for the option rather than the text

```java
Select objSelect = new Select(driver.findElement(By.id("Search-box")));
Select.selectByIndex(4);
```

- selectByValue() method asks for the value of the desired option rather than the option text or an index. 

```java
Select objSelect = new Select(driver.findElement(By.id("Search-box")));
objSelect.selectByValue("Automation Testing");
```

</blockquote>
</details>
  
---


44. How I can get all the options listed in the dropdown?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

getOptions() method gets all the options belonging to the Select tag. It takes no parameter and returns List<WebElements>.

```java
Select objSelect = new Select(driver.findElement(By.id("Search-box")));
List <WebElement> elementCount = oSelect.getOptions();
System.out.println(elementCount.size());
```

</blockquote>
</details>
  
---


45. How we can know whether we can select multiple items from the dropdown?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

isMultiple(): boolean – This method informs whether the Select element supports multiple selection options at the same time or not. This method accepts nothing and returns a Boolean value (true/false).

</blockquote>
</details>
  
---


46. What is used for the Select class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

In Selenium, the Select class provides the implementation of the HTML SELECT tag. A Select tag provides the helper methods with select and deselects options.

</blockquote>
</details>
  
---


47. Differences between Black Box Testing and White Box Testing.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

| Black Box Testing                                                                                                                                      | White Box Testing                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| The Black Box Test is a test that only considers the external behaviour of the system; the internal workings of the software are not considered. | The White Box Test is a method used to test software taking into consideration its internal functioning. |
| It is carried out by testers.                                                                                                                          | It is carried out by software developers.                                                                  |
| This method is used in System Testing or Acceptance Testing.                                                                                           | This method is used in Unit Testing or Integration Testing.                                                |
| No knowledge of implementation is needed.                                                                                                              | Knowledge of implementation is required.                                                                   |

</blockquote>
</details>
  
---

48. What are the Selenium suite components?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- **Selenium Client API** - Support for writing Selenium in various languages.
- **Selenium Remote Control** - Server that allows for running web applications written in those various languages.
- **Selenium Grid** - A server that can test using multiple machines running in parallel.
	- Beneficial for scaling your application across multiple browsers/OSs.
- **Selenium IDE** - Plugin used to set up testing scripts and offer record-and-playback automation functionality.
- **Selenium WebDriver** - A Serverless way to execute your scripts. The heart of Modern Selenium. Starts a browser and controls it.
	- Each type of browser has its own Selenium WebDriver.
		- chromedriver	->	Google Chrome
		- geckodriver	->	Mozilla Firefox
		- edgedriver	->	Microsoft Edge


</blockquote>
</details>

---
	
