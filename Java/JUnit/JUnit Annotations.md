## Technical

1. Explain about JUnit Annotations.

<details><summary><b> Show Answer </b></summary>

- Which refers to syntactic meta-data added to the Java source code for better structure and 
  readability. 
- Where Syntactic meta-data refers to the type of data representing the structure of a file with 
  references to bytes, data types, and data structures.

</details>

---

2. List the annotations used in JUnit.

<details><summary><b> Show Answer </b></summary>

- `@Test`	
- `@Before`	
- `@BeforeClass`
- `@After`	
- `@AfterClass`	
- `@Ignores`	
- `@Test(timeout=500)`	
- `@Test(expected=IllegalArgumentException.class)`

</details>

---

3. Which annotation is the replacement for the pacakge org.junit.TestCase.

<details><summary><b> Show Answer </b></summary>

- `@Test` - indicates JUnit about which public void method can be run as a test case.

</details>

---

4. What is the purpose of `@Ignores` annotation in JUnit?

<details><summary><b> Show Answer </b></summary>

- Used to ignore some statements during test execution. 
- <b>Example</b>- Disabling some testcases during test exceution.

</details>

---

5. Differentiate between `@Before` and `@BeforeClass` annotations.

<details><summary><b> Show Answer </b></summary>

- `@Before` is used to execute some statements before each test case, whereas`@BeforeClass` is used to 
   execute some statements before all the test case.

</details>

---

6. When should we use this `@Test(expected=IllegalArgumentException.class)` annotation?

<details><summary><b> Show Answer </b></summary>

- It is to be used when some exceptions occured during the test execution.

</details>

---

7. Which annotation is used to set timeout in JUnit Test cases?

<details><summary><b> Show Answer </b></summary>

- `@Test(timeout=500)`- used if you want to set some timeout during test execution.
- <b>Example</b> : we can use this annotation, when we are working under some projects, and tests need to be completed within some specified time.	

</details>

---
8. How can we do testing for 'private' methods in a class?

<details><summary><b> Show Answer </b></summary>

- We caanot test the private method directly, so manual testing is to be performed, or the method should 
  be changed to "protected" method in the class.

</details>

---

9. What will happen if the return type of JUnit method is string?

<details><summary><b> Show Answer </b></summary>

- The execution will fail because the JUnit test methods are designed to return 'void'. 

</details>

---


## Problem Solving


10. Create test class for the following code.

``` java

package com.example.junit5;
public class Calculator {
    public int addition(int a, int b) {
        return a + b;
    }
}

```
<details><summary><b> Show Answer </b></summary>

``` java

package com.example.junit5;
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;
class CalculatorTest {
    Calculator calculator;
    @BeforeEach                                         
    void setUp() {
        calculator = new Calculator();
    }
    @Test                                               
    @DisplayName("Simple addition should work")   
    void testAddition() {
        assertEquals(9, calculator.addition(4, 5),     
                "Regular addition should work");  
    }
}
```

<details><summary><b> Explanation </b></summary>

>- `@BeforeEach`- used to create an object before the method execution
>- `@Test` - used to add the numbers and using assertEquals to check the result after adding the numbers.

</details>
</details>

---




