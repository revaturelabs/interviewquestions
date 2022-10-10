## Technical
1. In Java 8 how can i filter a collection using the stream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

```Java
    public static void main(String[] args)
    {
        // Creating a list of Integers
        List<Integer> list = Arrays.asList(3, 4, 6, 12, 20);
        // Getting a stream consisting of the
        // elements that are divisible by 5
        // Using Stream filter(Predicate predicate)
        list.stream()
            .filter(num -> num % 5 == 0)
            .forEach(System.out::println);
    }
```
</blockquote>

**Output**<br>
    
    20
    
<details> <summary> <b> Explanation </b> </summary>

<blockquote>
    
- It provides a method `filter()` to filter stream elements on the basis of given predicate. 
- This method take predicate as an argument and returns a stream of consisting of resulted elements.
    
</blockquote>

</details>
    
</details>

---

2. Can we define default method without using default keyword in Java8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
    
<blockquote>

- No, for defining default method inside interface `default` keyword is must and it should prefix method declaration.
- Without prefixing default keyword results in compilation error.
- **Compile-time error**: Abstract methods do not specify a body.
- **Reason**: without default keyword, compiler consider it as abstract method which doesn’t have body.

</blockquote>
    
</details>

---

3. What actual advantage does Java 8 brings ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Code is more concise and readable.
- More reusable,testable and maintable.
- User can write parallel code.
- User can write database like operations.
</blockquote>
</details>

---

4. Tell us about Functional interfaces.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An Interface that contains exactly one abstract method is known as functional interface. It can have any number of default, static methods but can contain only one abstract method. It can also declare methods of object class. Functional Interface is also known as Single Abstract Method Interfaces or SAM Interfaces.
    
</blockquote>
</details>

---


6. How lambda expressions and functional interface are related?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Lambda expressions express instances of functional interfaces (An interface with single abstract method is called functional interface. An example is `java.lang.Runnable`). 
- Lambda expressions implement the only abstract function and therefore implement functional interfaces

</blockquote>
</details>

---

7. What is your understanding about stream pipelining?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It is the process of chaining different operations together. It accomplishes this function by dividing stream operations into two categories, intermediate operation and terminal operations.

</blockquote>
</details>

---

8. Can you create your own functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes, we can create our own functional interface.
- We have to do these two things:
    - Annotate the interface with `@FunctionalInterface`, which is the Java 8 convention for custom functional interfaces.
    - Ensure that the interface has just one abstract method.

</blockquote>
</details>

---

9. What will happen if we define multiple abstract methods inside the Functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Inside Functional Interface we can take only one abstract method, if we take more than one abstract method then compiler raise an error. Interface can declares an abstract method overriding one of the public method from `java.lang.Object`, that still can be considered as functional interface.

</blockquote>
</details>

---

10. Why default methods needed in the interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

 Java 8 has introduced the concept of default methods which allow the interfaces to have methods with implementation without affecting the classes that implement the interface.

</blockquote>
</details>

---

11. What is the behaviour of `findFirst()` method in Java 8  streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Stream `findFirst()` returns an Optional (a container object which may or may not contain a non-null value) describing the first element of this stream, or an empty Optional if the stream is empty.

</blockquote>

<details> <summary> <b> Explanation </b> </summary>
<blockquote>

```Java
    import java.util.stream.Stream;
    public class Main 
    {
        public static void main(String[] args) 
        {
            //sequential stream
            Stream.of("one", "two", "three", "four")
            .findFirst()
            .ifPresent(System.out::println);
            //parallel stream
            Stream.of("one", "two", "three", "four")
            .parallel()
            .findFirst()
            .ifPresent(System.out::println);
        }
    }
```

**Output**

one<br>
one

</blockquote>
</details>
</details>

---

12. What is the behaviour of `findAny()` method in Java 8  streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Stream `findAny()` returns an Optional (a container object which may or may not contain a non-null value) describing some element of the stream, or an empty Optional if the stream is empty.
</blockquote>
</details>

---

13. When to use `findAny()` method in Java 8 streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are instances where you have a stream, but you only want to select a random element; as long as it meets certain conditions and the operation itself takes the shortest time possible.

</blockquote>
</details>

---

14. What do you mean by stream ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Streams are just sequence of data from a source.
- With Java 8, we can do manipulation on data using stream API.
- Example: Youtube
    - If we are watching a video all the content of the video will not be loaded at once. As the time elapses we will get the content.

</blockquote>
</details>

---

15. Can you tell me difference between Collection API and Stream API?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Collection API is used for storing data in different kinds of data structures.
- Stream API is used for computation of data on a large set of objects.
- With Collection API we can store a finite number of elements in a data structure.
- With Stream API, we can handle streams of data that can contain infinite number of elements.
- Collection API constructs objects in an eager manner.
- Stream API creates objects in a lazy manner.
- Multiple consumption: Most of the Collection APIs support iteration and consumption of elements multiple times.
- With Stream API we can consume or iterate elements only once.

</blockquote>
</details>

---

16. Do you know what are the various forms of writing lambda expressions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
We can declare a lambda expression by-
    
- () -> expression
- (parameters) -> expression
- (parameters) -> { multiple statements}

</blockquote>
</details>

---

17. What do you understand by `@Functional Interface` annotation in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- `@Functional interface `- used to force the compiler to check whether the given interface has single-abstract method or not.
- If not, compiler will throw error `"Unexpected @FunctionalInterface annotation"`

</blockquote>
</details>

---

18. How do you create a custom annotation in Java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

```Java
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
@Retention(RetentionPolicy.RUNTIME)
@interface TestAnnotationForClass {
   String author();
   String date();
   int currentRevision() default 1;
   String lastModified() default "Not applicable";
   String lastModifiedBy() default "Not applicable";
}

//Now, we’ll use TestAnnotationForClass annotation for Test class.

   @TestAnnotationForClass (
   author = "Editorial Team",
   date = "9/18/2020",
   currentRevision = 6,
   lastModified = "9/18/2020",
   lastModifiedBy = "Editorial Team"
    )
    public class Test {
        public static void main(String[] args) {
        Test t = new Test();
        //print annotations of class Test
        System.out.println(t.getClass().getAnnotations()[0]);
        }
    }
```

</blockquote>

<details> <summary> <b> Explanation </b> </summary>
<blockquote>

In this example, we have used RetentionPolicy.RUNTIME because we want to demonstrate and read annotation at runtime. RetentionPolicy.RUNTIME indicates that annotations are to be recorded in the class file by the compiler and retained by the virtual machine at run time, so they may be read reflectively.

**Output**

@TestAnnotationForClass(currentRevision=6, lastModified=9/18/2020, lastModifiedBy=Editorial Team, author=Editorial Team, date=9/18/2020)

</blockquote>
</details>
</details>

---

19. How to avoid  `NullPointer exception ` in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Java 8 provides concept of Optionals
- Optionals can be used to avoid `NullPointer Exception`

Example:

    ```Java
    String value=null;<br>
    Optional <String> value=Optional.empty();
    ```
</blockquote>
</details>

---

20. What are the different types of functional interfaces in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Consumer
- Predicate
- Function 
- Supplier

</blockquote>
</details>

---

21. How would you convert object of type Iterable to Stream ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Lets have an example:
```Java
import java.util.*;
import java.util.stream.*;
class Main{
    // Function to get the Stream
    public static <T> Stream<T>
    getStreamFromIterable(Iterable<T> iterable)
    {
        // Convert the Iterable to Spliterator
        Spliterator<T>
            spliterator = iterable.spliterator();
        // Get a Sequential Stream from spliterator
        return StreamSupport.stream(spliterator, false);
    }
    public static void main(String[] args)
    {
        // Get the Iterator
        Iterable<Integer>
            iterable = Arrays.asList(10,20,30,40,50);
        // Get the Stream from the Iterable
        Stream<Integer>
            stream = getStreamFromIterable(iterable);
        // Print the elements of stream
        stream.forEach(s -> System.out.println(s));
    }
}
// Output:
// 10
// 20
// 30
// 40
// 50
```


</blockquote>
</details>

---

22.  How to overcome, multiple inheritance problem in Java 8 ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
    
we can do that by overriding the default method in the implementation class. Altogether provide new implementation or invoke either one of the `default()` method using `super` keyword
For example, `\<interfaceName\>.super.\<defaultMethodName\>`

</blockquote>
</details>

---

23. What happens, if a class implements two interfaces having exactly same method with same signature (consider one as default and another abstract) ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Compilation fails with error saying conflicting method.
- **Compile-time error**: The default method `displayDefaultMethod()` inherited from DemoInterfaceA conflicts with another method inherited from DemoInterfaceB
- To overcome this error, override this conflicting method and provide new implementation or invoke default method’s implementation using `super` keyword

</blockquote>
</details>

---


25. What is the purpose of `joining()` method introduced in Java 8 ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `joining()` method of the Collectors class in Java 8 returns a Collector that concatenates the input elements into a String.
    
``` java
    public class Example {
        public static void main(String[] args) {
            List<Character> list = Arrays.asList('D', 'e', 'm', 'o');
            String str = list.stream().map(String::valueOf).collect(Collectors.joining());
            System.out.println("Concatenated = "+str);
        }
    }
```

**Output**

Concatenated = Demo

</blockquote>
</details>

---

26. What is the use of the `String::ValueOf` expression in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`String::ValueOf` is a simple static method referencing the `valueOf` method, belonging to the class 
`String`.

</blockquote>
</details>

---

27. What do you mean by method reference in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It refer to methods of functional interfaces. It can be considered as a short-code version of using a lambda expression.

The following is the expression for a method reference:

    `Class::methodname`

</blockquote>
</details>

---

28. What is the easiest way to print the current date and time using the new APIs in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `now` method, which is a part of `LocalDate`, can be used to get the current date as shown below:

    ```Java
    LocalDate currentDate = LocalDate.now();
    System.out.println(currentDate);
    ```

Similarly, it can also be used to get the current time:

    ```Java
    LocalTime currentTime = LocalTime.now();
    System.out.println(currentTime);
    ```

</blockquote>
</details>

---

29. Differentiate between intermediate and terminal operations in Java 8.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Intermediate Operation**

- Used for the transition to a new state.	
- Lazy execution of code, i.e., code is not executed as soon as it is encountered Not lazy.

**Terminal Operation**

- Used to end the process under execution.
- Code is immediately executed upon encounter.

</blockquote>
</details>

---
30. Can the following piece of code compile successfully?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<blockquote>

```Java
@FunctionalInterface
public interface Function2<T, U, V> {
public V apply(T t, U u);
default void count() {
    // increment counter
}
}
```

</blockquote>

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, the code can compile and execute without any errors. It uses functional interface specifications when the single abstract method is being defined.

</blockquote>
</details>

---

31. What is the code to sort strings using the Java 8 lambda expression?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The below piece of code sorts strings using the lambda expression:

//Sorting using Java 8 lambda expression

```Java
private void sortUsingJava8(List<String> names) {

Collections.sort(names, (s1, s2) -> s1.compareTo(s2));

}
```

</blockquote>
</details>

---

32. Is it possible to call a static method of any interface in a class using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, it is possible to call a static method in a class by making use of the name as shown below:

```Java
    interface Student {
        static void Present() {
        System.out.println("Student is there!");
        }
    }

    class Associates implements Student {
        public void print() {
            Student.Present();
        }
    }
```

</blockquote>
</details>

---

33. Do you know how the `random` keyword in Java 8 works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `random` keyword, as the name suggests, is used to generate random values for computations and operations in Java 8.

The following piece of code is used to print out 20 random numbers using the forEach loop:

```java

Random random = new Random();
random.ints().limit(20).forEach(System.out::println);

```
</blockquote>
</details>

---

34. Explain about collectors in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Collectors are mainly used to combine the final result after the processing of elements in a stream. They are used to return lists or strings.

</blockquote>
</details>

---

35. What is the easiest way to print the sum of all of the numbers present in a list using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java 8, the following code is used to print the sum of all of the numbers that are present in a list:

```Java
    List<Integer> numbers = Arrays.asList(5, 4, 10, 12, 87, 33, 75);
    IntSummaryStatistics stats = integers.stream().mapToInt((x) −> x).summaryStatistics();
    System.out.println("Sum of all numbers : " + stats.getSum());
```

</blockquote>
</details>

---

36. When is an ideal situation to use the Stream API in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Stream API in Java 8 can be effectively used if the Java project calls for the following operations:

    - Perform database operations
    - Execute operations lazily
    - Write functional-style programming
    - Perform parallel processing
    - Use pipeline operations
    - Use internal iteration

</blockquote>
</details>

---

37. Can you tell me about supplier in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A supplier is a simple functional interface in Java 8 that does not take in any argument. It is used as an assignment target when making use of lambda expressions.

</blockquote>
</details>

---

38. Do you know about predicate in Java 8 ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The Predicate is also a functional interface in Java and it is defined in the java.util.function package.
- It improves the readability and manageability of our code. Also, it helps us in unit testing them separately.
- We can use Predicate anywhere where we need to evaluate a condition on a Collection of objects such that evaluation can result either in true or false.
</blockquote>
</details>

---

39. Can you name the common types of functional interfaces in the standard library?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are many functional interface types in the standard library, and some of them are as follows:

- BiFuction
- BinaryOperator
- Consumer
- Predicate
- Supplier
- UnaryOperator

</blockquote>
</details>

---

40. Can you give examples of intermediate operations in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The examples that are widely used in intermediate operations are:

- `Distinct()`
- `Limit(long n)`
- `Filter(Predicate)`
- `Map(Function)`
- `skip(long n)`

</blockquote>
</details>

---

41. What are the similarities between `map` and `flatMap` stream operations in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Both `map` and `flatMap` operations are a form of intermediate stream operations that take in a function and use the input function for performing various activities in the stream.

</blockquote>
</details>

---

42.How  to find and remove duplicate elements from a list using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Duplicate elements can be listed and removed easily by applying stream operations and performing a collection, later using the `Collections.toSet()` method. This should remove all of the duplicate elements present in the list.

</blockquote>
</details>

---

43. What is the easiest way to convert an array into a stream in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Any array in Java 8 can be converted into a stream easily using the stream class. The creation of a stream using a factory method is as shown below:

```Java
    String[] testarray = {"Hello", "Intellipaat", "learners"};
    Stream numbers = Stream.of(testarray);
    numbers.forEach(System.out::println);
```
</blockquote>
</details>

---

44. What is the use of the `peek()` method in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `peek()` method is a part of the stream class in Java 8, which is used to see actions performed through a stream pipeline. Peeking can be done at every step to print messages about the code being executed onto the console.

Peeking has a wide amount of usage when efficiency is a requirement, when debugging code with the lambda expression, or when performing stream processing.

</blockquote>
</details>

---

45.  What is the meaning of a `Spliterator` in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Spliterator is a newly introduced iterator interface for Java 8. It is very efficient and handles API-related operations seamlessly across the runtime environment.

</blockquote>
</details>

---

46. Explain the different time and date APIs and when you may use them.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Important classes of Date-Time API are:
    - Local: It is used to simplify the date-time API with no complexity of timezone handling.
    - Zonal: It is a specialized date-time API to deal with various timezones.

- Java LocalDate Time Class:
    - It is an immutable date-time object that represents a date-time, with the default format as yyyy-MM-dd-HH-mm-ss.zzz. It is used when time zones are NOT required.

- ZonedDate Time Class in Java:
    - It is an immutable representation of a date-time with a time-zone. Use it when time zones are to be considered. It is used to store all date and time fields.
    
</blockquote>
</details>

---

47. In Java, how do you convert a String to a LocalDate or a LocalDateTime? ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
The Java 8 `LocalDate-Time API` includes a `parse()` method, which can be used to parse a given input string using a specified format.

For example,

```java

LocalDate newDate = LocalDate.parse("2016-08-23");
System.out.println("Parsed date : " + newDate);

```
</blockquote>
</details>

---

48. What is the difference between a predicate and a function ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A predicate takes one argument and returns a boolean value.
- A function takes one argument and returns an object.
- Both are useful for evaluating lambda expressions.

</blockquote>
</details>

---

49. Can a functional interface extend/inherit another interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A functional interface cannot extend another interface with abstract methods as it will void the rule of one abstract method per functional interface. 

Example:

```Java
    interface Parent { 
        public int parentMethod(); 
    } 
    @FunctionalInterface // This cannot be FunctionalInterface 
    interface Child extends Parent { 
        public int childMethod(); 
            // It will also extend the abstract method of the Parent Interface 
            // Hence it will have more than one abstract method 
            // And will give a compiler error 
        }
```
It can extend other interfaces which do not have any abstract method and only have the default, static, another class is overridden, and normal methods.

</blockquote>
</details>

---

50. What are the advantages of using the Optional class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It encapsulates optional values, i.e., null or not-null values, which helps in avoiding null checks, which results in better, readable, and robust code It acts as a wrapper around the object and returns an object instead of a value, which can be used to avoid run-time NullPointerExceptions.

</blockquote>
</details>

---