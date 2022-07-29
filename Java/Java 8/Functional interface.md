## Technical
1: How do we implement the interface with lambda expression?

<details><summary> Show Answer</summary>
A functional interface(An interface with a single abstract method)
</details>



 2:  Is @Functional Interface annotation mandatory for every interface with a single abstract method?
 <details><summary> Show Answer</summary>
No, not necessarily because the compiler will consider it as a functional interface when it has only one abstract method. </details>

3: Is it possible to have default and static methods in the functional interface?
 <details><summary> Show Answer</summary>
 Yes, we can have any number of default and static methods but can contain only one abstract method. 
 </details>

4: How many default methods can we have in the functional interface?
 <details><summary> Show Answer</summary>
 a functional interface can have Multiple default methods with only one abstract method. </details>

5: Exaplain about Lambda Expression?
 <details><summary> Show Answer</summary>
 The functional interface has been introduced in Java 8 to support the lambda expression, lambda expression is the instance of a functional interface.</details>

6: Write a single–line lambda expression having void return type?
<details><summary> Show Answer</summary>
Answer: () -> System.out.println("Welcome");</details>

7: List some java built-in examples for functional interfaces.
<details><summary> Show Answer</summary>

-Runnable     
-Callable       
-Comparable
</details>

8: What is the use of @Functional Interface annotation?
<details><summary> Show Answer</summary>

It forces the Java compiler to indicate that the interface is a functional interface, so it should not allow having more than one abstract method. 
</details>

9: Does lambda expression execute on its own? Explain.
<details><summary> Show Answer</summary>
No, it is used to implement a method defined by a functional interface.

</details>

10: List the main kinds of Functional Interfaces in Java 8.
<details><summary> Show Answer</summary>

- Consumer - which takes only one argument
- Predicate - which takes one argument and returns the result as a boolean value
- Supplier - which does not take any arguments and returns a single result.
- Function - which receives an argument and returns the result based on the processing

</details>

11: When does a functional interface can extend another interface?
<details><summary> Show Answer</summary>

- A functional interface can extend the interface only when there are no abstract methods in it.
- If it has an abstract method then it will be an invalid functional interface.

</details>

12: What is SAM?
<details>
<summary> Show Answer</summary>
 
- Single Abstract Method interfaces
- Which is also called functional interfaces, having only one abstract method and multiple default methods.
</details>

13: Does the functional interface allows static methods?
<details>
 <summary> Show Answer</summary>
JDK 8 allows static methods in the interface, before this only
one abstract method is allowed in functional interface </details>

14: Is this a functional interface code snippet?
``` java
@FunctionalInterface
public interface Runnable {
 public abstract void run();
}
```
<details><summary> Show Answer </summary>
Yes, this is a functional interface, since there is only one
abstract method
</details>

15: Write the syntax for the consumer functional interface?

<details><summary> Show Answer </summary>

``` java

Consumer<Integer> consumer = (value) -> System.out.println
(value);
```

-  which accepts only one argument and has no return value. 

</details>

16: Write the syntax of the Predicate Functional Interface.

<details><summary> Show Answer </summary>

``` java
public interface Predicate<T> {

    boolean test(T t);

}
```
- a function that accepts an argument and returns a boolean value as an answer

</details>


17: Write the Syntax of Supplier Functional Interface?


<details><summary> Show Answer </summary>

``` java
@FunctionalInterface
public interface Supplier<T>{
 returns the specific result 
T.get();

}
```

- which does not take any input or argument and yet returns a single output. 

</details>


18: Is there any limit for static and default methods in the functional interface?

<details><summary> Show Answer </summary>

- No, we can add any number of static and default methods in the functional interface in java 8.

</details>


# Error Detection
 19:Predict the error of the following code snippet.
 
``` java  
@FunctionalInterface  
interface Arithmetic {  
    void addition(String msg);  
    void subtraction();
} 
```
 <details><summary> Show Answer</summary>
It will throw a compile time error that Revature is not a functional interface, since it has 2 abstract methods.</details>


# Problem-Solving
20: Convert the following code into a lambda expression.
``` java
import java.util.Scanner;  
public class Addition 
{  
public static void main(String args[])  
{  
int x, y, sum;  
Scanner sc = new Scanner(System.in);  
System.out.print("Enter the first number: ");  
x = sc.nextInt();  
System.out.print("Enter the second number: ");  
y = sc.nextInt();  
sum = sum(x, y);  
System.out.println("The sum of two numbers x and y is: " + sum);  
}  
//method that calculates the sum  
public static int Sum(int a, int b)  
{  
int sum = a + b;  
return sum;  
}  
}  
```

<details><summary> Show Answer</summary>
Explanation: A lambda expression is a short block of code that takes in parameters and returns a value. Which is similar to methods, but they do not need a name(Function name) and they can be implemented right in the body of a method.

``` java

public class Main
{  
public static void main(String args[])  
{  
Sum sum = (a,b) -> a+b;
System.out.print(sum.add(2,3));  
}  
}  
interface Sum{
    int add(int a, int b);
}
```

</details>



21: Convert the follwing Anonymous class code into Lambda expresssion.
 

 ``` java

 public class Anonymousclass  {

    public static void main(String[] args) {

        Thread thread = new Thread(){
            public void run(){
                System.out.println("Understanding what is an anonymous class");
            }
        };
        thread.start();
    }
}
```
<details><summary> Show Answer</summary>


``` java

public class AnonymousClassExample {

    public static void main(String[] args) {

        Runnable runnable = () -> {
            System.out.println("Understanding functional interfaces");
        };
        runnable.run();
    }
}
```

 - Functional interface can be instantiated using lambda expression instead of AnonymousClass. 
 - It can reduce the lines of code. 
 </details>

 

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

<details>
<summary> Show Answer</summary>

- It will throw a compile time error

- When a functional interface extends another interface it should not contain any abstract methods.

</details>






