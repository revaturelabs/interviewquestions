## Technical
1. What is the use of `@FunctionalInterface` annotation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
<blockquote>
	
If an interface annotated with <code>@FunctionalInterface</code>, Java complier ensures that interface has only one abstract method.
	
</blockquote>
	
</details>

---

 2.  Is `@FunctionalInterface` annotation mandatory for every interface with a single abstract method?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
 <details><summary><b>Show Answer</b></summary>
<blockquote>
  No
</blockquote>
<details><summary><b>Explanation</b></summary>
<blockquote>	
	Not necessarily because the compiler will consider it as a functional interface when it has only one abstract method. 
</blockquote>			
</details>
</details>

---

3. Is it possible to have default and static methods in the functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 <details><summary><b> Show Answer</b></summary>
	<blockquote>
 	Yes
		</blockquote>
<details><summary><b>Explanation</b></summary>
<blockquote>
We can have any number of default and static methods but can contain only one abstract method.
</blockquote>
 </details>
</details>

---

4. How many default methods can we have in the functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 <details><summary><b>Show Answer</b></summary>
	<blockquote>
 	A functional interface can have any number of default methods with only one abstract method.
		</blockquote>
</details>
	

 
 ---

5. Is Functional Interface related to the Lambda Expression?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 <details><summary><b>Show Answer</b></summary>
	<	blockquote>
	Yes
	</blockquote>
	<details><summary><b>Explanation</b></summary>
<blockquote>
		The functional interface has been introduced in Java 8 to support the lambda expression, lambda expression is the instance of a functional interface.
</blockquote>
	</details>
</details>
 
 ---

6. Write a code to print "HelloWorld" using lambda expression and functional interface?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

	
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
<details> <summary><b>Explanation</b></summary>
	
<blockquote>
<li>Create a functional interface, <code>Greeting</code> with <code>greet</code> as one abstract method</li>
		<li>In main method, provide <code>greet</code> method definition using lambda expression </li>
			<li>Print <b>HelloWorld</b> by calling <code>g.greet()</code></li>
</blockquote>
	</details>
</details>

---

7. List some java built-in examples for functional interfaces.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	
<blockquote>

- `Runnable` - Used in Multithreading , which has `run()` method    
- `Callable` - Used to wrap a text and pass to a thread , which has `call()` method
- `Comparable` - Used to compare between the objects in the class, which has `compareTo()` method
	
</blockquote>
	
</details>

---

8. What is the  primary condition to convert Anonymous class to lambda expression? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- The Anonymous classes should have only one abstract method so that it can be converted into lambda expression.
- Functional interface is implemented using lambda expression. which is also called as SAM(Single Abstract Method)
	
</blockquote>
</details>

---

9. Does lambda expression execute on its own? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	<blockquote>
	
No
</blockquote>
<details><summary><b>Explanation</b></summary>
	
<blockquote>
	
It is used to implement a method defined by a functional interface.
	
</blockquote>

</details>
	
	
</details>

---

10. List the main kinds of Functional Interfaces in Java 8.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


<details><summary><b>Show Answer</b></summary>

<blockquote>

- `Consumer` - which takes only one argument
- `Predicate` - which takes one argument and returns the result as a boolean value
- `Supplier` - which does not take any arguments and returns a single result.
- `Function` - which receives an argument and returns the result based on the processing
	
</blockquote>

</details>

---

11. When does a functional interface can extend another interface?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


<details><summary><b>Show Answer</b></summary>
<blockquote>

- A functional interface can extend the interface only when there are no abstract methods in it.
- If it has an abstract method then it will be an invalid functional interface.
</blockquote>

</details>

---

12. What is SAM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
 
<blockquote>
	
- SAM means Single Abstract Method.
- Which is also called functional interfaces, having only one abstract method and multiple default methods.
	
</blockquote>
	
</details>

---

13. Does the functional interface allows static methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	
<blockquote>
	
JDK 8 allows static methods in the interface, before this only
one abstract method is allowed in functional interface 

</blockquote>
	
</details>

---

14. Is this a functional interface code snippet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java

public interface Circle {
    public abstract void draw();
}
```
<details><summary><b>Show Answer</b></summary>
<blockquote>	
Yes

</blockquote>	
<details><summary><b>Explanation</b></summary>
	
<blockquote>
	
This is a functional interface, since there is only one abstract method
	
</blockquote>
	
</details>
	

</details>

---

15. Write the syntax for the consumer functional interface?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>
	
<blockquote>

``` java
Consumer<Integer> consumer = (value) -> System.out.println(value);	
```
</blockquote>

	
<details><summary><b>Explanation</b></summary>

<blockquote>
	
Which accepts only one argument and has no return value. 
	
</blockquote>

</details>

</details>
	
---

16. Write the syntax of the Predicate Functional Interface.
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
<details><summary><b>Show Answer</b></summary>
	
<blockquote>

``` java
public interface Predicate<T> {
    boolean test(T t);
}
```
</blockquote>
	
	
<details><summary><b>Explanation</b></summary>
<blockquote>
	
	A function that accepts an argument and returns a boolean value as an answer

</blockquote>

</details>
	

</details>

---

17. Write the Syntax of Supplier Functional Interface.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
<details><summary><b>Show Answer</b></summary>
	
<blockquote>

``` java
@FunctionalInterface
public interface Supplier<T>{
    //returns the specific result 
    T get();
}
```
	
</blockquote>

<details><summary><b>Explanation</b></summary>
<blockquote>

Which does not take any input or argument and yet returns a single output. 
</blockquote>

</details>
	
</details>
	

---
	
18. Is there any limit for static and default methods in the functional interface?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

- No
	
	
<details><summary><b>Explanation</b></summary>
<blockquote>
	
We can add any number of static and default methods in the functional interface in java 8.
</blockquote>

</details>

</details>
	
---

## Error Detection
	
 19. redict the error of the following code snippet.
	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
``` java  

@FunctionalInterface
interface Arithmetic {  
    void addition(String msg);  
    void subtraction();
}
	
```
	
<details><summary><b>Show Answer</b></summary>
<blockquote>
	
It will throw a compile time error that Arithmetic is not a functional interface, since it has 2 abstract methods.
</blockquote>
	
</details>

---
	
## Problem-Solving
	
20. Write lambda expression for the method sum.
	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
	
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
<blockquote>

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

<details><summary><b>Explanation</b></summary>
	
<blockquote>


A lambda expression is a short block of code that takes in parameters and returns a value. Which is similar to methods, but they do not need a name(Function name) and they can be implemented right in the body of a method.
	
</blockquote>

	
</details>

</details>
	
---
	
21. Convert the follwing Anonymous class code into Lambda expresssion.
 

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
<blockquote>


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

	
<details><summary><b>Explanation</b></summary>
<blockquote>

	
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

<details><summary><b>Show Answer</b></summary>
<blockquote>
	
- It will throw a compile time error
- When a functional interface extends another interface it should not contain any abstract methods.
	
</blockquote>


</details>
	
---





