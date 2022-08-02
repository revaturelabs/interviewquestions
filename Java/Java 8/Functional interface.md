## Technical
1: What is the use of `@FunctionalInterface` annotation?

<details>
	<summary><b> Show Answer</b></summary>
	If an interface annotated with <code>@FunctionalInterface</code>, java complier ensures that interface has only one abstract method.
</details>

---

 2:  Is `@FunctionalInterface` annotation mandatory for every interface with a single abstract method?
 <details>
	<summary><b>Show Answer</b></summary>
	No.
	<details><summary><b>Explanation</b></summary>
	Not necessarily because the compiler will consider it as a functional interface when it has only one abstract method. 
	</details>
</details>

---

3: Is it possible to have default and static methods in the functional interface?

 <details><summary><b> Show Answer</b></summary>
 	Yes
	<details><summary><b>Explanation</b></summary>
	 We can have any number of default and static methods but can contain only one abstract method. 
 </details>
</details>

---

4: How many default methods can we have in the functional interface?

 <details><summary><b>Show Answer</b></summary>
 	A functional interface can have any number of default methods with only one abstract method.
</details>
 
 ---

5: Is Functional Interface related to the Lambda Expression?

 <details><summary><b>Show Answer</b></summary>
	Yes
	<details><summary><b>Explanation</b></summary>
		The functional interface has been introduced in Java 8 to support the lambda expression, lambda expression is the instance of a functional interface.
	</details>
</details>
 
 ---

6: Write a code to print "HelloWorld" using lambda expression and functional interface?

<details>
<summary><b>Show Answer</b></summary>
	
```java
@FunctionalInterface
interface Greetings {
	void greet();
}

public class test {
	public static void main(String[] args) {
		Greetings g = () -> System.out.println("HelloWorld");
		g.greet(); // Output: HelloWorld

	}
} 
```
<details> <summary><b>Explanation</b></summary>
<li>Create a functional interface, <code>Greeting</code> with <code>greet</code> as one abstract method</li>
		<li>In main method, provide <code>greet</code> method definition using lambda expression </li>
			<li>Print <b>HelloWorld</b> by calling <code>g.greet()</code></li>
	</details>
</details>

---

7: List some java built-in examples for functional interfaces.

<details><summary><b>Show Answer</b></summary>

- Runnable     
- Callable       
- Comparable
</details>

---

8: What is the  primary condition to convert Anonymous class to lambda expression? 

<details><summary><b>Show Answer</b></summary>

- The Anonymous classes should have only one abstarct method so that it can be converted into lambda expression.
- Functional interface is implemented using lambda expression. which is also called as SAM(Single Abstract Method)
</details>

---

9: Does lambda expression execute on its own? Explain.

<details><summary><b>Show Answer</b></summary>
	
No.
	
</details>

<details><summary><b>Explanation</b></summary>
	
It is used to implement a method defined by a functional interface.

</details>

---

10: List the main kinds of Functional Interfaces in Java 8.

<details><summary><b>Show Answer</b></summary>

- Consumer - which takes only one argument
- Predicate - which takes one argument and returns the result as a boolean value
- Supplier - which does not take any arguments and returns a single result.
- Function - which receives an argument and returns the result based on the processing

</details>

---

11: When does a functional interface can extend another interface?

<details><summary><b>Show Answer</b></summary>

- A functional interface can extend the interface only when there are no abstract methods in it.
- If it has an abstract method then it will be an invalid functional interface.

</details>

---

12: What is SAM?

<details><summary><b>Show Answer</b></summary>
 
- SAM means Single Abstract Method.
- Which is also called functional interfaces, having only one abstract method and multiple default methods.
</details>

---

13: Does the functional interface allows static methods?

<details><summary><b>Show Answer</b></summary>
JDK 8 allows static methods in the interface, before this only
one abstract method is allowed in functional interface </details>

---

14: Is this a functional interface code snippet?

``` java

public interface Runnable {
    public abstract void run();
}
```
<details><summary><b>Show Answer</b></summary>
	
Yes

</details>
	
<details><summary><b>Explanation</b></summary>
	
This is a functional interface, since there is only one abstract method
	
</details>

---

15: Write the syntax for the consumer functional interface?

<details><summary><b>Show Answer</b></summary>

``` java

Consumer<Integer> consumer = (value) -> System.out.println(value);
	
```
</details>
	
<details><summary><b>Explanation</b></summary>
	
-  which accepts only one argument and has no return value. 

</details>

---

16: Write the syntax of the Predicate Functional Interface.
	
<details><summary><b>Show Answer</b></summary>

``` java
	
public interface Predicate<T> {
    boolean test(T t);
}
	
```
	
</details>
	
<details><summary><b>Explanation</b></summary>
	
- a function that accepts an argument and returns a boolean value as an answer

</details>

---

17: Write the Syntax of Supplier Functional Interface.

<details><summary><b>Show Answer</b></summary>

``` java
	
@FunctionalInterface
public interface Supplier<T>{
    //returns the specific result 
    T get();
}
```
</details>
	
<details><summary><b>Explanation</b></summary>

- which does not take any input or argument and yet returns a single output. 

</details>

---
	
18: Is there any limit for static and default methods in the functional interface?

<details><summary><b>Show Answer</b></summary>

- No.
	
</details>
	
<details><summary><b>Explanation</b></summary>
	
- We can add any number of static and default methods in the functional interface in java 8.

</details>

---

## Error Detection
	
 19:Predict the error of the following code snippet.
 
``` java  

interface Arithmetic {  
    void addition(String msg);  
    void subtraction();
}
	
```
	
<details><summary><b>Show Answer</b></summary>
	
It will throw a compile time error that Revature is not a functional interface, since it has 2 abstract methods.
	
</details>

---
	
## Problem-Solving
	
20: Convert the following code into a lambda expression.
	
``` java
import java.util.Scanner;  
public class Addition {
    public static void main(String[] args) {
    int x, y, sum;  
        Scanner sc = new Scanner(System.in);  
        System.out.print("Enter the first number: ");  
        x = sc.nextInt();  
        System.out.print("Enter the second number: ");  
        y = sc.nextInt();  
        sum = sum(x, y);  
        System.out.println("The sum of two numbers x and y is: " + sum); 
         
   } 
   public static int Sum(int a, int b)  {  
       int sum = a + b;  
       return sum;  
   }  
}
	
```

<details><summary><b>Show Answer</b></summary>
	

``` java

public class Main{ 
     public static void main(String args[]){ 
         Sum sum = (a,b) -> a+b;
         System.out.print(sum.add(2,3));  
    }  
}  
interface Sum{
    int add(int a, int b);
}
	
```

</details>

<details><summary><b>Explanation</b></summary>

-  A lambda expression is a short block of code that takes in parameters and returns a value. Which is similar to methods, but they do not need a name(Function name) and they can be implemented right in the body of a method.
	
</details>
	
---
	
21: Convert the follwing Anonymous class code into Lambda expresssion.
 

 ``` java

 public class AnonymousClassExample  {
 
    public static void main(String[] args) {
 
        Runnable runnable = new Runnable(){
            public void run(){
                System.out.println("Convertion of Anonymous class into Lamda");
            }
        };
        runnable.run();
    }
}
```
<details><summary><b>Show Answer</b></summary>


``` java

public class AnonymousClassExample {
    public static void main(String[] args) {
        Runnable runnable = () -> {
            System.out.println("Convertion of Anonymous class into Lamda");
        };
        runnable.run();
    }
}
	
```
	
</details>
	
<details><summary><b>Explanation</b></summary>
	
 - Functional interface can be instantiated using lambda expression instead of AnonymousClass. 
 - It can reduce the lines of code. 
	
 </details>

 ---

22: Predict the output for the following code snippet.
	
``` java
	
interface Single{  
    void say(String msg);   // abstract method  
}  
@FunctionalInterface  
interface Double extends Single{  
  
    void doIt();  
}
```

<details><summary><b>Show Answer</b></summary>

- It will throw a compile time error

- When a functional interface extends another interface it should not contain any abstract methods.

</details>
	
---





