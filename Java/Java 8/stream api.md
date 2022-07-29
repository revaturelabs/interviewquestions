 1: Which package should be imported to use Stream API in Java 8?

 <details><summary> Show Answer</summary>

 java.util.stream - which includes all the classes and interfaces used for functional - type operations. 

 </details>

 2 : Why we need to import java.util.stream even after importing java.util.* in the code to use stream API?

  <details><summary> Show Answer</summary>

  - java.util.* will import all the direct classes and interfaces but not sub classess/ sub packages.
  - stream class resides in the sub package java.util.stream package so it will not be included in java.util.*.

  </details>

  3: Explain about Stream API.

  <details><summary> Show Answer</summary>

  - Stream API is a collection of objects which can be processed to get a desired result.
  - Example: If we want to filter the movies released in 2022 from the movie database.

  </details>

  4: How many operations are performed in stream API to get the result?

  <details><summary> Show Answer</summary>

- two operations -Intermediate and terminal operations.
- Intermediate - will process the stream to get the result (like filter, map).
- Termainal - it is the end of the stream to return the result.

</details>


5:List some intermediate operations in Stream API.

<details><summary> Show Answer</summary>

- Filter- select elements based on the condition passed
- Map - by applying the given function in the stream
- Sorted - used to sort the stream

</details>

6: List some terminal operations in Stream API.

<details><summary> Show Answer</summary>

- Collect- returns the result of intermediate operations.
- forEach- used to iterate through the elements of stream
- reduce - to reduce the elements of stream to one value

</details>

7: Does the value of elements in stream will be changed when you process it?

<details><summary> Show Answer</summary>

No, because stream API process the elements as per pipelined operations without changing the values.

</details>

8: Explain about pipeline operations.

<details><summary> Show Answer</summary>

- Stream API will take the stream of elements as source, performs pipeline of operations and returns the  result 
-  A pipeline of operations consists of source, zero or more intermediate operations(filter,sort,map) and a terminal operation.

</details>

9: List the ways of creating stream in java8.

<details><summary> Show Answer</summary>

- By creating Stream.of() method 
- Stream from a Collection using stream() & parallelStream() methods
- Stream from an Array using Arrays.stream()
- Stream using Stream.builder()
- By an Empty Stream using Stream.empty()
- Creating an infinite Stream using Stream.generate() method and Stream.iterate() method
- Creating Stream of a File

</details>

10: When should we use filter operation in streams?

<details><summary> Show Answer</summary>

- When we need to process and return a stream from another stream that satisfies a given condition we use filters in intermediate operations.
- Exmaple: Return the movie list relaesed in 2022 from the movie database.

</details>

11: Differentiate between map() and flatMap().

<details><summary> Show Answer</summary>

- map()- will work on the streams and transform the single input value into single output.
- flatMap()- will work on the streams and transform the single input value into mulitple outputs by flattening it.

</details>

12: When do we need sorted intermediate operation to be performed?

<details><summary> Show Answer</summary>

- sorted can be used when we need to return the stream of elements in sorted order like sorting arrays.
- Example: return the student database sorted with their department id's.

</details>

13: what is the use of count() terminal operations in stream API?

<details><summary> Show Answer</summary>

- when we need the result of the stream to be in finite numbers.
- Example : return the numnber of employees working in particular department.

</details>

14: Why do you use forEach() terminal operation?

<details><summary> Show Answer</summary>

- When we need to iterate the elements in stream.
- This is the only one operation that returns void.
- can call directly on collections or stream.

</details>

15: What is the use of collect() terminal operation?


<details><summary> Show Answer</summary>

- When we need to convert the source stream into collections by using intermediate operations. 
- Ressult stream may be of list, set , map etc.

</details>

16: Predict the output for the following operation.
``` java
Stream<String> s = Stream.of("java", "SQL", "python",  "JDBC");
 s.filter(x -> x.startsWith("S")).forEach(System.out::print); 
 ```
 <details><summary> Show Answer</summary>

 - returns SQL
 - Here we are using filter to return the result of element starting with "S".

 </details>

 17: Predict the output of the following intermediate opeartion.
 ``` java
 Stream<String> s = Stream.of("appple", "orange", "apple", "banana", "banana");
 s.distinct().forEach(System.out::print); 
 ```

<details><summary> Show Answer</summary>

- returns orange
- distinct()- will return a stream from the source stream removing the duplicate elements.
 </details>

 18: Can we add or delete elements from streams?

 <details><summary> Show Answer</summary>

 - No, we cannot add/ delete elements in stream
 - we can only perform the operations on the stream
 - Stream does not store the data as well.

 </details>

 19: Predict the output of the following code.

``` java
import java.util.stream.*;  
public class JavaStreamExample {  
    public static void main(String[] args){  
        Stream.iterate(1, element->element+1)  
        .filter(element->element%2==0)  
        .limit(4)  
        .forEach(System.out::println);  
    }  
} 
```

 <details><summary> Show Answer</summary>
   2<br>
   4<br>
   6<br>
   8<br>
   - iterate () used to iterate through the elements in the stream.
   - filter() used to apply the condition on the stream 
   - forEach() used to return the result from the stream after iteration.
</details>

20: Explain about Lazy Invocation.

<details><summary> Show Answer</summary>

- Intermediate operations are lazy because it will be invoked if only its required for the execution of terminal operation.
- But it is optimized and it can process large number of data with high performance.

</details>

