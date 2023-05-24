## Technical

1. What is JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit helps to test individual pieces of code, or “units,” to ensure that they are functioning properly. By identifying and isolating units that are not working correctly, JUnit makes it easier to find and fix errors in code. In addition, JUnit can be used to automate the execution of unit tests, which can save time and effort.

</blockquote>
</details>

---

2. What are the important features of JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Important features of JUnit are:**
- It is an open-source framework.
- Provides Annotation to identify the test methods.
- Provides Assertions for testing expected results.
- Provides Test runners for running tests.
- JUnit tests can be run automatically and they check their results and provide immediate feedback.
- JUnit tests can be organized into test suites containing test cases and even other test suites.
- JUnit shows test progress in a bar that is green if the test is going fine and it turns red when a test fails.

</blockquote>
</details>

---

3.  What is testing and unit testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Testing is the process of checking whether the application fulfills the requirements and achieves the desired functionalities. Unit testing refers to assessing an individual functionality or a unit of the application.  

</blockquote>
</details>

---

4. What Is A JUnit Test Case?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A JUnit test case is a test case written using the JUnit testing framework. JUnit is a popular Java testing framework that allows developers to write and run tests for their Java code. A JUnit test case is typically made up of several individual tests, each of which tests a specific aspect of the code being tested. 

</blockquote>
</details>

---

5. Define automated testing in the context of JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Automated testing in JUnit is that type of testing where one has the option to take support from tools. These automation tools would display accurate results which are suitable for the process of Java application development.

</blockquote>
</details>

---

6. What is Unit Testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Unit testing is a software testing technique in which individual units or components of a software application are tested in isolation from the rest of the system. The purpose of unit testing is to verify that each unit of the software application performs as expected and meets its design requirements.

In unit testing, the code is tested in small, isolated parts to ensure that each part is functioning correctly. Unit tests are usually automated and run frequently during the development cycle to catch defects early and ensure that the software application meets its quality goals.

</blockquote>
</details>

---


7. What is the purpose of using Junit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit is extensively used by developers to carry out unit testing in Java. Moreover, it is also being used to speed up the application based on Java. It is important to note that by taking into account the source code, the application can efficiently be sped up. 

</blockquote>
</details>

---

8. When are JUnit test cases written in the Developmental Cycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit test cases are typically written during the development cycle of a software project. They are created in parallel with the development of the codebase to verify the correctness of the implementation and ensure that the software meets the specified requirements. Test-driven development (TDD) is a popular approach where test cases are written before the actual code implementation, driving the development process.

</blockquote>
</details>

---

9. What is an assertion in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An assertion in JUnit is a statement that checks whether a specific condition is true during a test. It is used to verify the expected behavior of the code under test. JUnit provides various assertion methods, such as assertEquals, assertTrue, assertFalse, etc., to perform different types of checks.

</blockquote>
</details>

---

10. What are the tools with the help of which JUnit can be easily integrated?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are mainly three types of tools that play a pivotal role in the integration of JUnit. We can use either of them to facilitate the process. They are as follows:

- Maven (One of the Build Tools)
- IDE (e.g. Eclipse, STS, IntelliJ)
- Gradle (One of the Build Tools)

</blockquote>
</details>

---

11. Is it necessary to write a test case for every logic in the application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- In JUnit, it is unnecessary to write a test case for every logic but only for those that can be reasonably broken. 
- A unit test case would comprise a collection of input data and expected output. The org.JUnit package contains several classes and interfaces to help you in unit testing, such as Assert, Test, Before, After, etc. 

</blockquote>
</details>

---

12. How do you write a JUnit test case?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We have to

  - Annotate our test method with the @Test annotation.
  - Write our test method.
  - Run our test case.

</blockquote>
</details>

---

13. How do you run a JUnit test case?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Assuming already we have a JUnit test case written, we can run it by opening it in our IDE and selecting the `run` option. If we are using Eclipse, for example, right-click on the file and select `Run As > JUnit Test`. This will launch the test and run it using the JUnit framework.

</blockquote>
</details>

---

14. How can you group related test cases in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit provides the @Nested annotation, which allows you to define nested test classes within a parent test class. This can be useful for grouping related test cases and providing better organization and readability to the test suite.

</blockquote>
</details>

---

15. What is a Test Suite?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Test suite means bundling a few unit test cases and running them together. In JUnit, both `@RunWith` and `@Suite` annotations are used to run the suite test.

</blockquote>
</details>

---

16. How do you test the `protected` and `private` methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In the `protected` method, the test class and target class are declared in the same package. However, in the `private` method, there is no direct way of testing. Either we have to change your method to `protected` or do the testing manually. 

</blockquote>
</details>

---

17. What are JUnit classes? List some of Junit’s classes.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit classes are those classes that are used in writing and testing JUnit programs. Some of the important JUnit classes are mentioned below –

`Assert` – A set of assert methods.
`TestCase` − A test case that defines the fixture to run multiple tests.
`TestResult` − It contains methods that collect the results after a test case is executed.
`TestSuite` − It is an aggregate of JUnit tests.

</blockquote>
</details>

---

18.  What is JUnit Test Fixture?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The fixture is a fixed state of a set of objects used as a baseline for running tests. The purpose of a test fixture is to ensure that there is a well-known and fixed environment in which tests are run so that results are repeatable. It includes the following methods −

`setUp()` method which runs before every test invocation.
`tearDown()` method which runs after every test method.

</blockquote>
</details>

---

19. How do you install JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The first step is to download JUnit 5, the latest version of JUnit ( it would be a file named JUnit.zip). We would be required to unzip the distribution file to a directory, `%JUnit_HOME%`. Then, we would add JUnit to the classpath. 

Next, we would test the installation. This would involve running sample tests (located not in the JUnit.jar file, but in the installation directory) distributed with JUnit. Lastly, we would confirm that all the tests pass with an “OK” message. If they don’t, we would go back and verify whether JUnit.jar is in the classpath.  

</blockquote>
</details>

---

20. Name some JUnit extensions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following are some of the JUnit extensions

  - Cactus: Cactus is a simple test framework for unit testing server-side java code (Servlets, EJBs, Tag Libs, Filters).
  - JWebUnit: JWebUnit is a Java-based testing framework for web applications.
  - XMLUnit: XMLUnit provides you with the tools to verify the XML you emit is the one you want to create.
  - MockObject: In a unit test, mock objects can simulate the behavior of complex, real (non-mock) objects and are therefore useful when a real object is impractical or impossible to incorporate into a unit test.

</blockquote>
</details>

---

21. What are the methods in fixtures?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- `setup`
- `tearDown`

</blockquote>
</details>

---

22. What is `@Test` and where it’s used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`@Test` annotation is used to mark a method as a test method, the result of which is then compared with the expected output to check whether the test is successful or not.

</blockquote>
</details>

---

23. Why JUnit only reports the first failure in a single attempt?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Reporting multiple failures in a single test is generally a sign that the test does too much and it is too big a unit test. JUnit is designed to work best with several small tests. It executes each test within a separate instance of the test class. It reports failure on each test.

</blockquote>
</details>

---

24. What is a JUnit parameterized test?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The parameterized test is a new feature introduced in JUnit 4. It provides the facility to execute the same test case again and again with different values.

</blockquote>
</details>

---

25. What are Annotations and how are they are useful in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Annotations are like meta-tags that you can add to your code and apply  to methods or in class. The annotation in JUnit gives us information about test methods, which methods are going to run before & after test methods, which methods run before & after all the methods, and which methods or classes will be ignored during execution.

</blockquote>
</details>

---

26. In Java, `Assert` is a keyword. Won't this conflict with JUnit's `Assert()` Method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit 3.7 deprecated `assert()` and replaced it with `assertTrue()`, which works the same way. JUnit 4 is compatible with the assert keyword. If you run with the -ea JVM switch, assertions that fail will be reported by JUnit.

</blockquote>
</details>

---

27. Why not just use `System.out.println()` for testing the output of a code instead of using Junit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Debugging the code using `System.out.println()` will lead to manual scanning of the whole output every time the program is run to ensure the code is doing the expected operations. Moreover, in the long run, it takes lesser time to code JUnit methods and tests them on class files.

</blockquote>
</details>

---

28. How will you run JUnit 5 test?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- We can run a JUnit 5 test case using JUnit's console launcher. The executable for this jar can be downloaded from Maven Central, under the `junit-platform-console-standalone` directory.
- Also, we'll need a directory that will contain all our compiled classes:
`$ mkdir target`

</blockquote>
</details>

---

29. What is the purpose of `org.JUnit.jupiter.api.Assertions` class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

This class provides a set of assertion methods useful for writing tests. Only failed assertions are recorded.

</blockquote>
</details>

---

30. What is the purpose of `org.JUnit.testresult` Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A TestResult collects the results of executing a test case. It is an instance of the Collecting parameter pattern. The test framework distinguishes between failures and errors. A failure is anticipated and checked for with assertions. Errors are unanticipated problems like an `ArrayIndexOutOfBoundsException`.

</blockquote>
</details>

---

31. What is the purpose of `org.JUnit.testsuite` Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A TestSuite is a composite of tests. It runs a collection of test cases.

</blockquote>
</details>

---

32.  What is the purpose of `@BeforeEach` Annotation In JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Several tests need similar objects created before they can run. Annotating a public void method with `@BeforeEach` causes that method to be run before each Test method.

</blockquote>
</details>

---

33.  What is the purpose of `@AfterAll` annotation in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If you allocate external resources in a Before method you need to release them after the test runs. Annotating a public void method with `@AfterAll` causes that method to be run after the Test method.
```Java
@AfterAll
    public static void runsAfterEverything(){
        System.out.println("Finished Running a Test Class");
    }

```
</blockquote>
</details>

---

34. What is the purpose of `@BeforeAll` annotation in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Annotating a public static void method with `@BeforeAll` causes it to be run once before any of the test methods in the class.
```Java
 @BeforeAll
    public static void runsBeforeEverything(){
        System.out.println("Running a Test Class");
    }
```

</blockquote>
</details>

---

35. What is the purpose of `assertTrue()` and `assertFalse()` in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `assertTrue()` asserts that the supplied condition is true or the boolean condition supplied by BooleanSupplier is true.
Similarly, `assertFalse()` asserts that supplied condition is false.

</blockquote>
</details>

---

36. What is the `@Disabled` annotation and how is this useful?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>


To disable a test in JUnit 5, you will need to use the `@Disabled` annotation. It is equivalent to JUnit 4’s `@Ignored` annotation.

`@Disabled` annotation can be applied over the test class (disables all test methods in that class) or individual test methods as well.
```Java
@Disabled
@Test
void testCalcTwo()
{
	System.out.println("======TEST TWO EXECUTED=======");
	Assertions.assertEquals( 6 , Calculator.add(2, 4));
}
```

</blockquote>
</details>

---

37. Explain the execution procedure of the JUnit test API methods with Junit Annotations?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following is how the JUnit execution procedure works −

- The method annotated with `@BeforeAll` is executed once at the start of the class.
- The method annotated with `@BeforeEach` executes before Testcase 1 begins.
- The method Testcase1 annotated with @Test is the testcase in the class.
- The method annotated with `@AfterEach` runs after Testcase 1 completes execution.
- The method annotated with `@BeforeEach` executes before Testcase 2 begins.
- The method Testcase2 annotated with `@Test` is the testcase in the class.
- The method annotated with `@AfterEach` runs after Testcase 2 completes execution.
- The method annotated with `@AfterAll` is executed once at the end of the class after both testcase 1 and 2 are executed.

</blockquote>
</details>

---

38. What is the purpose of `org.JUnit.JUnitcore` Class?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The test cases are executed using JUnitCore class. JUnitCore is a facade for running tests. It supports running JUnit 4 tests, JUnit 3.8.x tests, and mixtures.

</blockquote>
</details>

---

39. How to simulate a timeout situation In JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit provides a handy option for Timeout. If a test case takes more time than the specified number of milliseconds then JUnit will automatically mark it as failed. The timeout parameter is used along the with `@Test` annotation.

</blockquote>
</details>

---

40. How can you use JUnit to test that the code throws desired exception?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit provides an option for tracing the Exception handling of code. You can test if a code throws the desired exception or not. The expected parameter is used along with `@Test` annotation as follows − `@Test(expected)`

</blockquote>
</details>

---

41.  How to create parameterized tests?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following are the steps to create parameterized tests in JUnit5:
- Declare `@ParameterizedTest` to the test.
- Declare at least one source (for example – `@ValueSource`) that will provide the arguments for each invocation of the test.
- Consume the arguments in the test method. 
- JUnit 5 parameterized test maven dependency : We need `JUnit-jupiter-params` maven dependencies to support parameterized tests.

```Java
public class Junit5_Parameterized_Test {
  
  // This test will run sequentially 5 times with 1 argument each time
    @ParameterizedTest
    @ValueSource(ints = {8,4,2,6,10})
    void test_int_arrays(int arg) {
      System.out.println("arg => "+arg);
        assertTrue(arg % 2 == 0);
    }   
}
```
**Output**

arg => 8<br>
arg => 4<br>
arg => 2<br>
arg => 6<br>
arg => 10<br>


</blockquote>
</details>

---

42. How to compile a JUnit Test Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Compiling a JUnit test class is like compiling any other Java class. The only thing we need to watch out for is that the JUnit JAR file must be included in the classpath.

</blockquote>
</details>

---

43. What happens if a JUnit test method is declared as "private"?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If a JUnit test method is declared as "private", it compiles successfully. But the execution will fail. This is because JUnit requires that all test methods must be declared as "public".

</blockquote>
</details>

---

44. Can you use a `main()` method for Unit testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes we can test using `main()` method. One obvious advantage seems to be that we can whitebox test the class. That is, we can test the internals of it (private methods for example). We can't do the unit testsit-tests. But primarily the test framework tests the interface and the behavior from the user's perspective.

</blockquote>
</details>

---

45. Do you need to write a Test Class for every class that needs to be tested?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

No. We need not write an independent test class for every class that needs to be tested. If there is a small group of tests sharing a common test fixture, you may move those tests to a new test class.

</blockquote>
</details>

---

46. Can we change the return type of the JUnit test method from void to some other type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Ideally, we should not do that. All the JUnit test methods have a void return type. If we change the return type then the test method would not be considered a test method and would be ignored during the execution of tests.

</blockquote>
</details>

---

47. When you should run the JUnit test, Is there any particular time interval between each run?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

No there is no time constraint. A JUnit test needs to run whenever there is a change in the source code. This ensures that the new change passes through all the tests.

</blockquote>
</details>

---

48. What is the annotation we have in JUnit 5 as a replacement for @Rule in JUnit 4?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- `@ExtendWith`	is replacement for `@Rule`.
- `@Rule` is extended from the class TestRule that helps apply certain rules on the test cases.
  - For Example: creating a temporary folder before test case execution and deleting the folder post-execution can be set through a Rule.
- `@Rule` is available only in JUnit 4 which can be used in JUnit 5 Vintage, however, `@ExtendWith` provides a closer feature for JUnit 5

</blockquote>
</details>

---

49. What does the `@TestFactory` annotation do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- This annotation is supported by JUnit 5 only and helps the creation of dynamic or runtime tests.
- It returns a stream of data as collection and cannot use lifecycle callback annotations

</blockquote>
</details>

---

50. Mention different methods of exception handling in JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are different methods of exception handling in JUnit

- Try catch idiom
- With the JUnit rule
- With `@Test` annotation
- With catch exception library
- With customs annotation

</blockquote>
</details>

---

51. Explain who should use JUnit – a developer or a tester? Why do you use JUnit to test your code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>


JUnit is more often used by developers to implement unit tests in JAVA.  It is designed for unit testing that is more of a coding process and not a testing process. However, many testers and QA engineers use JUnit for unit testing.

JUnit is used because:

- It tests early and does automate testing.
- JUnit tests can be compiled with the build so that at the unit level, regression testing can be done.
- It allows test code re-usage.
- JUnit tests behave as a document for the unit tests when there is a transfer.

</blockquote>
</details>

---

52. What `assert()` does in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`assert()` is used to compare actual and expected results in JUnit. It has various implementations like `assertEquals()`,`assertArrayEquals()`,`assertFalse()`, `assertNotNull()`, etc.

</blockquote>
</details>

---

53. Differentiate TDD and BDD?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The key difference is the scope. TDD is a development practice while BDD is a team methodology. In TDD, the developers write the tests while in BDD the automated specifications are created by users or testers (with developers wiring them to the code under test.) 

</blockquote>
</details>

---

54. Why do we need Unit testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Unit tests help to fix bugs early in the development cycle and save costs.
- It helps the developers to understand the testing code base and enables them to make changes quickly.
- Good unit tests serve as project documentation.
- Unit tests help with code reuse. Migrate both your code and your tests to your new project. Tweak the code until the tests run again.

</blockquote>
</details>

---

55. What is the purpose of Assumptions in JUnit5? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Assumptions provide static methods to support conditional test execution based on assumptions. A failed assumption results in a test being aborted.

Assumptions are typically used whenever it does not make sense to continue the execution of a given test method. In the test report, these tests will be marked as passed.

The assumptions class has three methods with many overloaded forms:

`assumeFalse()`: validates the given assumption to be false.
`assumeTrue()`: validates the given assumption to be true.
`assumingThat()`: executes the supplied Executable, but only if the supplied assumption is valid.
```Java
@Test
void testOnDev()
{
    System.setProperty("ENV", "DEV");
    Assumptions.assumeTrue("DEV".equals(System.getProperty("ENV")));
    //remainder of the test will proceed
}

@Test
void testOnProd()
{
    System.setProperty("ENV", "PROD");
    Assumptions.assumeTrue("DEV".equals(System.getProperty("ENV")));
    //remainder of the test will be aborted
}
```

</blockquote>
</details>

---

56. Can we have Non-Public test methods in JUnit 5?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- JUnit 5 test classes and test methods are not required to be public. We can now make them package-protected.
- JUnit internally uses reflection to find test classes and test methods. Reflection can discover them even if they have limited visibility, so there is no need for them to be public.

</blockquote>
</details>

---

57. What is the purpose of the `@RepeatedTest` annotation in JUnit 5?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JUnit Jupiter provides the ability to repeat a test a specified number of times by annotating a method with `@RepeatedTest` and specifying the total number of repetitions desired. 

Below is the example of `@RepeatedTest` in JUnit5.
```Java
@RepeatedTest(3)
void repeatedTestWithRepetitionInfo1(RepetitionInfo repetitionInfo) {
    assertEquals(3, repetitionInfo.getTotalRepetitions());
}
```

</blockquote>
</details>

---


58. What is Mocking?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Mocking is a technique used in unit testing to simulate the behavior of external dependencies, such as databases or web services, by creating fake objects that mimic their behavior. This allows developers to test their code in isolation, without actually interacting with the real external dependencies. Mocking frameworks, such as Mockito and EasyMock, provide a set of tools and APIs to easily create and manage these fake objects, making the process of writing unit tests faster and more efficient.

</blockquote>

</details>

---

59. What is Mockito and integration testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Mockito is a popular open-source Java mocking framework that allows you to easily create mock objects for testing purposes. It provides methods to create mock objects, stubbing methods of mock objects, and verify method invocations on mock objects.

Integration testing, on the other hand, is a type of testing that involves testing the behavior of multiple modules of an application when they are integrated together. Integration testing is done to ensure that different modules of an application work correctly when integrated and to identify issues with the interactions between the modules. It is generally performed after unit testing and before system testing.

</blockquote>

</details>

---

60. Can Mockito be used for UI testing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Mockito is not typically used for UI testing. Mockito is primarily used for unit testing to mock dependencies and ensure that individual units of code function correctly in isolation.

UI testing, on the other hand, involves testing the entire application or a significant portion of it to ensure that the various parts of the application are working together correctly. For UI testing, tools like Selenium and Appium are typically used to simulate user interactions with the application and validate the behavior of the application in response to those interactions.

</blockquote>

</details>

---

61. What is the purpose of mocking an object or class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The purpose of mocking an object or class is to create a fake or substitute object that mimics the behavior of the original object, but allows for controlled and predictable behavior in tests. This is particularly useful when the real object is difficult or impossible to create or maintain in a test environment, or when the real object has side effects that may interfere with the test. By using a mock object, a developer can isolate the code being tested and focus on the specific functionality they are testing, without worrying about the behavior of other parts of the system. This helps in achieving more reliable and faster unit tests.

</blockquote>

</details>

---

62. How would you mock a class in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To mock a class in Java, you can use a mocking framework like Mockito. Here's an example of how to mock a class in Java using Mockito:

Assume you have a class MyClass that you want to mock. Here's how you can do it:

```Java

// Create a mock object of MyClass
MyClass myClassMock = Mockito.mock(MyClass.class);

// Define the behavior of the mock object
Mockito.when(myClassMock.someMethod()).thenReturn(someValue);

// Use the mock object in your test
// ...
```

In the above example, MyClass is mocked using the Mockito.mock() method. The behavior of the mock object is then defined using the Mockito.when() method. The someMethod() method of the mock object is then defined to return someValue. Finally, the mock object is used in the test.

</blockquote>

</details>

---
 
63. What is TDD?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TDD stands for Test-Driven Development. It is a software development approach in which tests are written before the actual code is written. The process usually involves the following steps:

- Write a test for a specific piece of functionality.
- Run the test and verify that it fails.
- Write the code that implements the functionality.
- Run the test again and verify that it passes.
- Refactor the code if necessary and repeat the process.

</blockquote>

</details>

---

64. What is Red-green testing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Red-green testing is a term used in Test-driven development (TDD) to describe the two stages of writing and running automated tests.

The first stage, the "red" stage, involves writing a failing test. This test is written before any code has been written to meet the requirements of the test. The purpose of the failing test is to ensure that the code that is written later on will meet the requirements of the test.

The second stage, the "green" stage, involves writing code that will pass the failing test. The goal is to make the test pass by writing the minimum amount of code necessary. Once the code has passed the test, it can be refactored or improved upon without fear of introducing bugs, since the test provides a safety net for catching any regressions.

The term "red-green" refers to the color of the test status indicators in the testing framework. When a test fails, it turns red. When a test passes, it turns green. The red-green testing cycle is repeated over and over as new features are added or existing features are changed, with the goal of continuously improving the codebase while maintaining a high level of test coverage.

</blockquote>

</details>

---

65. Why is TDD useful?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TDD (Test Driven Development) is useful because it helps developers to write clean, reliable, and maintainable code. By writing automated tests before the actual code, developers can better understand the requirements, improve the design, catch and fix issues early, and ensure that their code is always working as intended. This leads to higher code quality, faster development cycles, and increased confidence in the codebase.

</blockquote>

</details>

---

66. What are the considerations and best practices for Unit testing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Here are some considerations and best practices for unit testing:

`Test one thing at a time`: Each unit test should focus on testing one specific behavior or function of the code. This ensures that the test is easy to write, easy to understand, and provides clear feedback on whether the code is working as expected.

`Use a consistent naming convention`: Use a consistent naming convention for your test cases that accurately reflects what the test is testing. This makes it easier to understand what each test case is testing and helps to organize your tests.

`Write tests before writing code`: One of the key benefits of unit testing is that it helps to catch bugs early in the development process. To take full advantage of this, write your unit tests before you write your code. This approach is known as test-driven development (TDD).

`Use automated testing frameworks`: There are many automated testing frameworks available for different programming languages and platforms. These frameworks make it easy to run and manage your tests, and they can also provide useful features such as test coverage reports.

`Test all code paths`: Make sure to test all possible code paths, including both positive and negative scenarios. This ensures that your code is working as expected in all possible scenarios.

`Keep your tests independent`: Each test should be independent of other tests and should not rely on external resources such as databases or network connections. This makes it easier to debug failing tests and ensures that each test is testing only one specific behavior.

`Keep your tests fast`: Unit tests should be fast and efficient. Slow tests can slow down your development process and reduce the effectiveness of your testing strategy.

`Test for edge cases`: Make sure to test edge cases and corner cases, such as input values at the boundaries of acceptable ranges. This can help uncover bugs that may not be apparent in normal usage scenarios.

`Continuously refactor your tests`: As your code evolves, make sure to refactor your tests to keep them up to date with the changes. This ensures that your tests remain accurate and effective over time.

</blockquote>

</details>

---

67.  How would you test a method in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To test a method in JUnit, you can follow these steps:

`Create a test class`: Create a new class in your test package and annotate it with `@RunWith(JUnit4.class)`.

`Create a test method`: Create a new method in your test class and annotate it with `@Test`. This method will be used to test your target method.

`Prepare the test data`: Prepare the input data for your target method and any necessary dependencies.

`Invoke the target method`: Call the target method with the input data prepared in the previous step.

`Verify the result`: Verify that the result returned by the target method is correct. You can use various assertion methods provided by JUnit, such as `assertEquals()` or `assertThat()`, to compare the actual result with the expected result.

`Handle exceptions`: If the target method throws any exceptions, you can use the @Test annotation's expected attribute to specify the expected exception type. You can also use the `@Rule` annotation to specify a rule that handles exceptions.

</blockquote>

</details>

---

68. How do you use the ExternalResource rule to fetch data from a database for a test?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can use JUnit's `@Rule` annotation with the ExternalResource rule. This rule allows you to specify a method that will be executed before and after each test method in the class, and you can use this method to perform setup and teardown operations, including fetching data.

Here's how you can use the ExternalResource rule to fetch data from a database for a test:

```Java

public class MyTest {
    @Rule
    public ExternalResource resource = new ExternalResource() {
        private Connection conn;

        // Set up the resource
        @Override
        protected void before() throws Throwable {
            conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydb", "user", "password");
        }

        // Tear down the resource
        @Override
        protected void after() {
            try {
                if (conn != null) {
                    conn.close();
                }
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }

        // Fetch data from the resource
        public ResultSet fetchSomeData() throws SQLException {
            Statement stmt = conn.createStatement();
            ResultSet rs = stmt.executeQuery("SELECT * FROM mytable WHERE someCondition = true");
            return rs;
        }
    };

    @Test
    public void testSomethingWithLiveData() throws SQLException {
        ResultSet rs = resource.fetchSomeData();
        // Use the fetched data in your test
        // ...
    }
}

```

</blockquote>

</details>

---

69. Differentiate e2e and Unit testing ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

End-to-end (E2E) testing and unit testing are two different types of testing that serve different purposes in the software development life cycle.

Here are some key differences between E2E and unit testing:

`Scope`: Unit tests focus on testing individual units of code in isolation, while E2E tests focus on testing the entire application from start to finish.

`Speed`: Unit tests are typically faster than E2E tests because they test smaller pieces of code in isolation. E2E tests can be slower because they test the entire application.

`Dependencies`: Unit tests are designed to be independent of other units of code and do not rely on external dependencies. E2E tests, on the other hand, rely on all of the application's dependencies to be available and working properly.

`Coverage`: Unit tests provide better coverage of the codebase because they test individual units of code in isolation. E2E tests, on the other hand, provide better coverage of the user's experience with the application.

`Maintenance`: Unit tests are usually easier to maintain than E2E tests because they test smaller pieces of code that are less likely to change. E2E tests can be more difficult to maintain because they test the entire application, which can be more prone to change.

</blockquote>

</details>

---

70. How can we test a class in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To test a class in JUnit, you can create a test class that contains one or more test methods that test the behavior of the class under different conditions. Here's an example:

```Java

import org.junit.Test;
import static org.junit.Assert.*;

public class MyClassTest {
    @Test
    public void testAdd() {
        MyClass myClass = new MyClass();
        int result = myClass.add(2, 3);
        assertEquals(5, result);
    }
}

```
</blockquote>

</details>

---

71. How to do Unit testing in Spring and in Angular?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Unit testing in Spring**:

- Add the JUnit and Mockito dependencies to your project's build configuration file.
- Create a test class for the class or method you want to test.
- Annotate the test class with `@RunWith(SpringJUnit4ClassRunner.class)` to use Spring's test runner.
- Use `@Autowired` to inject dependencies into your test class.
- Write test methods that test the behavior of your class or method under different conditions.
- Use the Assert class to compare expected results with actual results.
- Run your tests using a test runner like Maven Surefire or Gradle.

**Unit testing in Angular**:

- Create a new test file for the component or service you want to test.
- Import the necessary modules, components, and services to set up the test environment.
- Set up the test environment using the `TestBed` class.
- Use the `compileComponents` method to compile the component and its template.
- Create an instance of the component or service you want to test.
- Write test methods that test the behavior of your component or service under different conditions.
- Use the `expect` function to compare expected results with actual results.
- Run your tests using the `ng test` command or a test runner like Karma.

</blockquote>

</details>

---

72. What is the purpose of using `@Rule` in JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The purpose of using @Rule in JUnit is to apply additional test rules or modify test behavior, allowing you to enhance the capabilities of your tests beyond what is provided by the core framework.

</blockquote>

</details>

---

73. How would you determine the percentage of the code that has been tested by Junit? How would you generate a report for it?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In JUnit, you can use code coverage tools to determine how much of your code has been tested by your JUnit tests. These tools analyze your code and generate a report that shows which lines and branches of code have been executed by your tests.

One popular code coverage tool for Java is `JaCoCo (Java Code Coverage)`. Here are the steps to generate a code coverage report using JaCoCo and Maven:

- Add the `JaCoCo Maven plugin` to your project's build configuration file.
- Configure the plugin to run during the test phase of the build.
- Run your JUnit tests using the test goal of the maven-surefire-plugin.
- Generate a code coverage report using the jacoco:report goal of the JaCoCo Maven plugin.
- View the report in your web browser or in your IDE's coverage tool.

Here's an example configuration for the JaCoCo Maven plugin:

```XML

<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-surefire-plugin</artifactId>
            <version>3.0.0-M5</version>
        </plugin>
        <plugin>
            <groupId>org.jacoco</groupId>
            <artifactId>jacoco-maven-plugin</artifactId>
            <version>0.8.6</version>
            <executions>
                <execution>
                    <id>prepare-agent</id>
                    <goals>
                        <goal>prepare-agent</goal>
                    </goals>
                </execution>
                <execution>
                    <id>report</id>
                    <goals>
                        <goal>report</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

To generate a code coverage report, run the following command:

`mvn clean test jacoco:report`

This will run your JUnit tests and generate a code coverage report in the `target/site/jacoco/index.html` file. You can open this file in your web browser to view the code coverage report. The report will show the percentage of code that was covered by your tests, as well as detailed information about which lines and branches of code were covered.

</blockquote>

</details>

---

74. What does `@AfterClass` do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`@AfterClass` is a JUnit annotation that is used to indicate that a method should be executed after all tests in a test class have been run. This annotation is useful for performing cleanup tasks after all the tests have been executed, such as closing resources or resetting the state of the system.

Here's an example of using `@AfterClass` in JUnit:

```java

import org.junit.AfterClass;
import org.junit.Test;
import static org.junit.Assert.*;

public class MyTest {
    
    @Test
    public void test1() {
        // Test code
    }
    
    @Test
    public void test2() {
        // Test code
    }
    
    @AfterClass
    public static void cleanup() {
        // Cleanup code
    }
}
```
In this example, the `@AfterClass` annotation is used to indicate that the `cleanup()` method should be executed after all tests in the MyTest class have been run. This method can be used to perform any necessary cleanup tasks after the tests have been executed. Note that the `cleanup()` method must be static in order to be executed by JUnit.

</blockquote>

</details>

---

75. Why use Mockito/JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit and Mockito are commonly used testing frameworks in Java. JUnit is used for writing and executing unit tests, while Mockito is used for creating mock objects to isolate the code being tested. Together, they provide a comprehensive suite of tools for developers to ensure their code is working correctly and efficiently.

</blockquote>

</details>

---

76. Spy vs Mock?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Mockito, a mock object is created to replace a real object or system, while a spy object is a real object that is being monitored for certain interactions. In other words, a mock object is a complete replacement of the real object, while a spy object is a wrapper around the real object that allows for additional testing.

</blockquote>

</details>

---

77. Difference between TestNG and JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

TestNG and JUnit are both popular testing frameworks in Java, but they differ in their approach to testing. TestNG provides more advanced features such as test suites, data-driven testing, and parallel testing, while JUnit is more focused on writing and executing unit tests. TestNG also supports more configuration options and provides better reporting capabilities than JUnit.

</blockquote>

</details>

---

78. JUnit annotations and assertion methods.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit provides a variety of annotations and assertion methods to help developers write effective and efficient unit tests. Some commonly used annotations include `@Test`, `@Before`, `@After`, and `@Ignore`, while commonly used assertion methods include `assertEquals()`, `assertNotEquals()`, `assertTrue()`, and `assertFalse()`. These annotations and assertion methods help developers to organize and execute their tests, as well as verify that their code is working correctly.

</blockquote>

</details>

---

79. Explain how you would conduct a JUnit test.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To conduct a JUnit test, you would first write a test class that contains methods with JUnit test annotations (`@Test`). Within each test method, you would create the necessary objects, set up any necessary data, and then call the method being tested. You would then use JUnit assertion methods to verify that the output of the method matches the expected output. You can run the test class using an IDE such as Eclipse or IntelliJ IDEA, or you can run it from the command line using a build tool such as Maven or Gradle.

</blockquote>

</details>

---

80. What is the difference between a unit test and a feature test?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A unit test is a type of test that focuses on a small, isolated piece of code, such as a single method or function. The purpose of a unit test is to ensure that this piece of code is working correctly in isolation. In contrast, a feature test is a type of test that focuses on a larger piece of functionality, such as a user interface or a complete system. The purpose of a feature test is to ensure that the system is working correctly as a whole, and that all the individual pieces are working together as expected.

</blockquote>

</details>

---

81. How to reduce redundancy in tests of JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

To reduce redundancy in JUnit tests, one can follow the following practices:

- Use parameterized tests to avoid duplicating the same test code for different inputs.
- Use test inheritance to share common setup and teardown code between test classes.
- Use test fixture objects to encapsulate setup and teardown logic that is shared across multiple tests.

<blockquote>
</details>

---

82. What is the purpose of the `@BeforeEach` and `@AfterEach` annotations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
The @BeforeEach annotation is used to mark a method that should be executed before each test method in a test class. It is typically used for setup tasks that need to be performed before each individual test. Similarly, the @AfterEach annotation marks a method that is executed after each test method, allowing for cleanup tasks.

<blockquote>
</details>

---

83. How would you verify a function that adds two numbers by using Junit?

<details><summary><b> Show Answer</b></summary>

To verify a function that adds two numbers using unit testing, we would create a test method that calls the function with two known input values and verifies that the result is correct. Here is an example test method using JUnit:

```java
@Test
public void testAddition() {
    int a = 5;
    int b = 7;
    int expectedSum = 12;

    int actualSum = MyClass.add(a, b);

    assertEquals(expectedSum, actualSum);
}
```

In this example, we create two input values `a` and `b`, call the `add()` function with these values, and then compare the expected result `expectedSum` with the actual result `actualSum` using the `assertEquals()` assertion method.

</details>

---

84. How did you provide data to the JUnit tests?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
JUnit tests need input data to test different scenarios. There are several ways to provide data to JUnit tests, including:

1. Hard-coding values in test methods
2. Creating test data as input files and reading them in the test methods
3. Creating test data objects and passing them as method parameters
4. Using data providers or test factories provided by testing frameworks like JUnit or TestNG

The approach taken depends on the specific needs of the test cases and the size and complexity of the test data.

</blockquote>

</details>

---

85. What are you testing for in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
In JUnit, we are testing the behavior of a specific unit of code, such as a method or a class, in isolation from other units. The goal of testing with JUnit is to ensure that the code under test meets the requirements and specifications set out in the design and documentation, and that it functions correctly and robustly in different scenarios and conditions.

Some of the things we might be testing for in JUnit include:

1. Correctness: Does the code produce the expected output or behavior given a specific input or set of inputs?
2. Boundary conditions: Does the code behave correctly when input values are at the limits or extremes of the allowable range?
3. Error handling: Does the code handle unexpected or erroneous input or conditions gracefully and without crashing?
4. Performance: Does the code execute within the expected time or resource constraints?
5. Compatibility: Does the code work correctly with different environments, configurations, or platforms?

</blockquote>

</details>

---

86. How do you test an exception?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Testing exceptions in JUnit is a way to ensure that code under test behaves as expected when it encounters unexpected or erroneous input or conditions. Here's how you can test an exception in JUnit:

1. Use the `@Test` annotation to identify the test method that will throw the exception.
2. Use the `@Test` annotation's `expected` parameter to specify the exception class that is expected to be thrown.
3. Add the code that will trigger the exception in the test method.
4. Run the test and verify that the exception is thrown.

Here's an example of how to test an exception in JUnit:

```java
@Test(expected = ArithmeticException.class)
public void testDivideByZero() {
  int a = 10;
  int b = 0;
  int result = a / b; // this line will trigger the exception
}
```

In this example, we expect an `ArithmeticException` to be thrown when we divide an integer by zero. The `@Test` annotation's `expected` parameter specifies that the test method should pass if the exception is thrown.

</blockquote>

</details>

---

87. How do you override a test designation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
In JUnit, you can override a test method's default name by using the `@DisplayName` annotation. This allows you to provide a more descriptive name for the test method that makes it easier to understand what the test is actually doing.

For example, if you have a test method called `testAddition()` and you want to override its name to `Test Addition of Two Positive Integers`, you can annotate the method with `@DisplayName("Test Addition of Two Positive Integers")`.

This annotation can be placed on the test method itself, or on the test class if you want to apply it to all test methods in the class.
</blockquote>

</details>

---

88. What is a test runner in JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A test runner is responsible for executing test cases and generating reports. JUnit provides different test runners, such as `BlockJUnit4ClassRunner`, `Parameterized`, and `Suite`, to handle different types of tests and test configurations.

</blockquote>
</details>

---

89. How can you organize multiple test classes in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit provides the concept of test suites, which allow you to group multiple test classes together. You can create a test suite class that includes the desired test classes using the `@RunWith` and `@SuiteClasses` annotations.

</blockquote>

</details>

---

90. What is the purpose of the `@Ignore` annotation in JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The @Ignore annotation is used to temporarily disable a test method or an entire test class. Tests marked with this annotation will not be executed during test runs

</blockquote>
</details>

---

91. How can you perform parameterized testing in JUnit?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit supports parameterized testing through the @ParameterizedTest annotation. You can provide different sets of input values as arguments to the test method using @ValueSource, @CsvSource, @MethodSource, or custom argument providers.

</blockquote>
</details>

---

92. What is the purpose of the @RunWith annotation in JUnit?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The @RunWith annotation is used to specify a custom test runner for executing the test cases. It allows you to extend or modify the default behavior of JUnit. For example, you can use @RunWith(MockitoJUnitRunner.class) to enable the integration of Mockito framework for mocking dependencies.

</blockquote>
</details>

---

93. What is the difference between @Before and @BeforeEach in JUnit 5?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JUnit 4, the `@Before` annotation is used to denote a method that runs before each test method, while in JUnit 5, the equivalent annotation is `@BeforeEach`. The purpose of both annotations is the same - to perform setup tasks before each individual test method.

</blockquote>
</details>

---

94. What are JUnit rules, and how do they differ from annotations?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit rules are additional components that can be applied to tests or test classes to modify their behavior. Unlike annotations, rules provide more flexibility and allow you to add custom logic or wrap the test execution in additional functionality. Rules are defined as fields in test classes and are annotated with `@Rule` or `@ClassRule` depending on their scope.

</blockquote>
</details>

---

95. What is the role of JUnit categories, and how can you use them?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit categories allow you to categorize your test methods or classes based on specific criteria. This is useful for selectively running tests based on their categories, such as unit tests, integration tests, or performance tests. You can annotate tests or test classes with category annotations and then configure the test runner to include or exclude specific categories during test execution.

</blockquote>
</details>

---

96. What are dynamic tests in JUnit 5, and how can you create them?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dynamic tests in JUnit 5 allow you to generate and execute tests programmatically at runtime. You can use the DynamicTest class and the DynamicContainer class to create dynamic tests and nest them hierarchically. This is useful when you need to generate tests based on some logic or when the number of tests is determined dynamically.

</blockquote>
</details>

---

97. How can you perform parallel execution of tests in JUnit 5?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JUnit 5 provides built-in support for parallel test execution. You can enable parallel execution at different levels, such as at the test class level or at the test method level, using the `@Execution` and `@Parallelizable` annotations. Parallel execution can significantly speed up the test suite execution time, especially for large test suites.

</blockquote>
</details>

---

98. How can you create custom JUnit extensions in JUnit 5?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JUnit 5, you can create custom extensions by implementing the `TestInstancePostProcessor`, `BeforeEachCallback`, `AfterEachCallback`, `BeforeAllCallback`, or `AfterAllCallback` interfaces. By implementing these interfaces, you can define custom behavior for test setup, teardown, or execution.

</blockquote>
</details>

---

99. What is parameter resolution in JUnit 5, and how does it work?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Parameter resolution in JUnit 5 is a feature that allows you to inject values into test methods or lifecycle methods. JUnit 5 provides various parameter resolvers, such as `TestInfo`, `TestReporter`, or custom resolvers, to access information about the currently executing test or to provide additional context to the tests.

</blockquote>
</details>

---

100. What is test coverage, and how can you measure it with JUnit?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Test coverage refers to the degree to which your tests exercise the codebase. JUnit itself does not provide direct tools for measuring test coverage. However, you can integrate JUnit with code coverage tools like JaCoCo or Cobertura to measure the coverage of your tests and identify areas of code that need more testing.

</blockquote>
</details>

---

101. How can you configure JUnit 5 to run tests in a specific order?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JUnit 5, the default test execution order is randomized to promote test independence. However, you can explicitly specify the test execution order using the `@TestMethodOrder` annotation and specifying the desired order mode, such as `MethodOrderer.OrderAnnotation` or `MethodOrderer.Random`.

</blockquote>
</details>

---