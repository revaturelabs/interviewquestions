## Technical
1. What is the use of `@FunctionalInterface` annotation?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>
	
<blockquote markdown="1">
	
If an interface is annotated with <code>@FunctionalInterface</code>, Java complier ensures that interface has only one abstract method.
	
</blockquote>
	
</details>

---

 2.  Is `@FunctionalInterface` annotation mandatory for every interface with a single abstract method?
 
 ![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
 
 <details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">
  No
</blockquote>
<details markdown="1"><summary><b>Explanation</b></summary>
<blockquote markdown="1">	
	Not necessarily because the compiler will consider it as a functional interface when it has only one abstract method. 
</blockquote>			
</details>
</details>

---

3. Is it possible to have default and static methods in the functional interface?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

 <details markdown="1"><summary><b> Show Answer</b></summary>
	<blockquote markdown="1">
 	Yes
		</blockquote>
<details markdown="1"><summary><b>Explanation</b></summary>
<blockquote markdown="1">
We can have any number of default and static methods but can contain only one abstract method.
</blockquote>
 </details>
</details>

---

4. How many default methods can we have in the functional interface?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

 <details markdown="1"><summary><b>Show Answer</b></summary>
	<blockquote markdown="1">
 	A functional interface can have any number of default methods with only one abstract method.
		</blockquote>
</details>
	

 
 ---

5. Is Functional Interface related to the Lambda Expression?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

 <details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">	
Yes
</blockquote>
	
<details markdown="1"><summary><b>Explanation</b></summary>
<blockquote markdown="1">
		The functional interface has been introduced in Java 8 to support the lambda expression. Lambda expression is the instance of a functional interface.
</blockquote>
	</details>
</details>
 
 ---

6. Write a code to print "HelloWorld" using lambda expression and functional interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

<blockquote markdown="1">

	
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
	
</blockquote>
<details markdown="1"> <summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
<li>Create a functional interface, <code>Greeting</code> with <code>greet</code> as one abstract method</li>
		<li>In main method, provide <code>greet</code> method definition using lambda expression </li>
			<li>Print <b>HelloWorld</b> by calling <code>g.greet()</code></li>
</blockquote>
	</details>
</details>

---

7. List some java built-in examples for functional interfaces.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">

- `Runnable` - Used in Multithreading , which has `run()` method    
- `Callable` - Used to wrap a text and pass to a thread , which has `call()` method
- `Comparable` - Used to compare between the objects in the class, which has `compareTo()` method
	
</blockquote>
	
</details>

---

8. What is the  primary condition to convert Anonymous class to lambda expression? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>

<blockquote markdown="1">

- The Anonymous classes should have only one abstract method so that it can be converted into lambda expression.
- Functional interface is implemented using lambda expression which is also called as SAM(Single Abstract Method)
	
</blockquote>
</details>

---

9. Does lambda expression execute on its own? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
	<blockquote markdown="1">
	
No
</blockquote>
<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
	
It is used to implement a method defined by a functional interface.
	
</blockquote>

</details>
	
	
</details>

---

10. List the main kinds of Functional Interfaces in Java 8.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)


<details markdown="1"><summary><b>Show Answer</b></summary>

<blockquote markdown="1">

- `Consumer` - which takes only one argument.
- `Predicate` - which takes one argument and returns the result as a boolean value.
- `Supplier` - which does not take any arguments and returns a single result.
- `Function` - which receives an argument and returns the result based on the processing.
	
</blockquote>

</details>

---

11. When does a functional interface extend another interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)


<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">

- A functional interface can extend the interface only when there are no abstract methods in it.
- If it has an abstract method then it will be an invalid functional interface.
</blockquote>

</details>

---

12. What is SAM?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
 
<blockquote markdown="1">
	
- SAM means Single Abstract Method.
- Which is also called functional interfaces, having only one abstract method and multiple default methods.
	
</blockquote>
	
</details>

---

13. Does the functional interface allow static methods?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">
	
JDK 8 allows static methods in the interface, prior to this, only one abstract method is allowed in functional interface.

</blockquote>
	
</details>

---

14. Is Circle interface a functional interface code snippet?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

``` java

public interface Circle {
    public abstract void draw();
}
```
<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">	
Yes

</blockquote>	
<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
	
This is a functional interface, since there is only one abstract method.
	
</blockquote>
	
</details>
	

</details>

---

15. Write the syntax for the consumer functional interface?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">

``` java
Consumer<Integer> consumer = (value) -> System.out.println(value);	
```
</blockquote>

	
<details markdown="1"><summary><b>Explanation</b></summary>

<blockquote markdown="1">
	
Which accepts only one argument and has no return value. 
	
</blockquote>

</details>

</details>
	
---

16. Write the syntax of the Predicate Functional Interface.
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
	
<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">

``` java
public interface Predicate<T> {
    boolean test(T t);
}
```
</blockquote>
	
	
<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
	
A function that accepts an argument and returns a boolean value as an answer.

</blockquote>

</details>
	

</details>

---

17. Write the Syntax of Supplier Functional Interface.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
	
<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">

``` java
@FunctionalInterface
public interface Supplier<T>{
    //returns the specific result 
    T get();
}
```
	
</blockquote>

<details markdown="1"><summary><b>Explanation</b></summary>
<blockquote markdown="1">

Which does not take any input or argument and yet returns a single output. 
</blockquote>

</details>
	
</details>
	

---
	
18. Is there any limit for static and default methods in the functional interface?
	
![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">
	
No
	
</blockquote>
	
<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
	
We can add any number of static and default methods in the functional interface in java 8.
	
</blockquote>

</details>

</details>
	
---

## Error Detection
	
 19. Predict the output of the following code snippet.
	

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
 
``` java  

@FunctionalInterface
interface Arithmetic {  
    void addition(String msg);  
    void subtraction();
}
	
```
	
<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">
	It will throw a compile time error
</blockquote>	
<details markdown="1"><summary><b>Explanation</b></summary>	
<blockquote markdown="1">	
 The Arithmetic interface is not a functional interface, since it has 2 abstract methods.
</blockquote>
	</details>
</details>

---
	
## Problem-Solving
	
20. Below code gets two numbers from the user and prints the sum of it. Here we are using `sum` method to calculate the sum of two number. Achieve the same goal using lambda expression. 

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
	
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

<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">

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
</blockquote>

<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">


A lambda expression is a short block of code that takes in parameters and returns a value which is similar to methods, but they do not need a name(Function name) and they can be implemented right in the body of a method.
	
</blockquote>

	
</details>

</details>
	
---
	
21. Convert the following Anonymous class code into Lambda expresssion.
 

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
<details markdown="1"><summary><b>Show Answer</b></summary>
<blockquote markdown="1">


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
</blockquote>

	
<details markdown="1"><summary><b>Explanation</b></summary>
<blockquote markdown="1">

	
 - Functional interface can be instantiated using lambda expression instead of AnonymousClass. 
 - It can reduce the lines of code. 
	
</blockquote>

	
 </details>

</details>

 ---

22. Predict the output for the following code snippet.
	
``` java
	
interface Single{  
    void say(String msg);   // abstract method  
}  
@FunctionalInterface  
interface Double extends Single{  
    void doIt();  
}
```

<details markdown="1"><summary><b>Show Answer</b></summary>
	
<blockquote markdown="1">
	
It will throw a compile time error
	
</blockquote>	
	

<details markdown="1"><summary><b>Explanation</b></summary>
	
<blockquote markdown="1">
	
 When a functional interface extends another interface, it should not contain any abstract methods.
	
</blockquote>

</details>
</details>
	
---





