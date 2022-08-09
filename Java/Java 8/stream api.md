 ## Technical 
 
 1: Which package should be imported to use Stream API in Java 8?

 <details><summary><b> Show Answer</b></summary>

 We should import java.util.stream, which includes all the classes and interfaces used for functional-type operations. 

 </details>

 ---
 
 2: Why do we need to import java.util.stream even after importing java.util.* in the code to use stream API?

   <details><summary><b> Show Answer</b></summary>

  - java.util.* will import all the direct classes and interfaces but not sub-classes/sub-packages.
  - stream class resides in the sub package java.util.stream package so it will not be included in java.util.*.

  </details>

  ---
    
  3: Explain Stream API.
    
 <details><summary><b> Show Answer</b></summary>

 - Stream API is a collection of objects which can be processed to get the desired result. 
 - A stream is a sequence of objects that supports various methods which can be pipelined to produce the desired result.
   The features of Java stream are –
   - A stream is not a data structure instead it takes input from the Collections, Arrays or I/O channels.
   - Streams don’t change the original data structure, they only provide the result as per the pipelined methods.
   - Each intermediate operation is lazily executed and returns a stream as a result, hence various intermediate operations can be pipelined.   
     Terminal operations mark the end of the stream and return the result.
 
 **Example:**  If we want to filter the movies released in 2022 from the movie database.

  </details>

  ---
  
  4: How many operations are performed in stream API to get the result?

  <details><summary><b> Show Answer</b></summary>

- Two operations - Intermediate and terminal operations.
- Intermediate - will process the stream to get the result (like a filter, or map).
- Terminal - it is the end of the stream to return the result.

</details>

---
   
5:List some intermediate operations in Stream API.

 <details><summary><b> Show Answer</b></summary>
 These are some intermediate operations used in Stream API.
 
 ![image](https://user-images.githubusercontent.com/92523245/183340700-36890903-b56e-4875-b2c5-5f3b0e9e812b.png)

</details>

  ---
  
6: List some terminal operations in Stream API.

 <details><summary><b> Show Answer</b></summary>
 
 These are some terminal operations used in Stream API.

![image](https://user-images.githubusercontent.com/92523245/183340851-0d37a284-efa2-4743-b2e1-ae56137139f0.png)

</details>
  
  ---

7: Will the values of elements in the stream change when you process it?

 <details><summary><b> Show Answer</b></summary>

No.
  
 <details><summary><b> Explanation </b></summary>
  
Because stream API processes the elements as per pipelined operations without changing the values.

</details>
  
</details>
  
 ---

8: Explain pipeline operations.

 <details><summary><b> Show Answer</b></summary>

- Stream API will take the stream of elements as the source, performs a pipeline of operations, and returns the  result 
- A pipeline of operations consists of a source, zero or more intermediate operations(filter, sort, map), and a terminal operation.

</details>
  
 ---

9: List the ways of creating a stream in java8.

 <details><summary><b> Show Answer</b></summary>

- By creating Stream.of() method 
- Stream from a Collection using stream() & parallelStream() methods
- Stream from an Array using Arrays.stream()
- Stream using Stream.builder()
- By an Empty Stream using Stream.empty()
- Creating an infinite Stream using Stream.generate() method and Stream.iterate() method
- Creating Stream of a File

</details>

 ---
  
10: When should we use filter operation in streams?

 <details><summary><b> Show Answer</b></summary>

- When we need to process and return a stream from another stream that satisfies a given condition we use filters in intermediate operations.
- Example: Return the movie list released in 2022 from the movie database.

</details>
  
 ---

11: Differentiate between map() and flatMap().

 <details><summary><b> Show Answer</b></summary>

- map() - will work on the streams and transform the single input value into a single output.
- flatMap() - will work on the streams and transform the single input value into multiple outputs by flattening it.
- The primary difference between map() vs flatMap() is the return type of both methods.
-  map() is used for transformation only, but flatMap() is used for both transformation and flattening.

   ` flatMap() = map() + Flattening `

</details>

  ---
  
12: When do we need a sorted intermediate operation to be performed?

 <details><summary><b> Show Answer</b></summary>

- sorted can be used when we need to return the stream of elements in sorted order like sorting arrays.
- Example: return the student database sorted with their department ids.

</details>
  
---

13: What is the use of count() terminal operations in stream API?

 <details><summary><b> Show Answer</b></summary>
 
- The count() method returns the count of elements in a stream
- when we need the result of the stream to be finite numbers.
- Example: return the number of employees working in a particular department.

</details>
  
---

14: What are the uses of forEach() terminal operation?

 <details><summary><b> Show Answer</b></summary>

- When we need to iterate the elements in the stream.
- This is the only operation that returns void.
- It can directly call on collections or stream.

</details>

 ---
  
15: What is the use of collect() terminal operation?

 <details><summary><b> Show Answer</b></summary>

- When we need to convert the source stream into collections by using intermediate operations. 
- Result stream may be of the list, set, map, etc.

</details>
 
 ---

 16: Can we add or delete elements from streams?

  <details><summary><b> Show Answer</b></summary>

 No
  
   <details><summary><b> Explanation </b></summary>
    
    
 - we cannot add/ delete elements in the stream
 - we can only perform the operations on the stream
 - Stream does not store the data as well.

 </details>
    
   </details>
    
 ---
 
 17: Explain about Lazy Invocation.

 <details><summary><b> Show Answer</b></summary>

- Intermediate operations are lazy because they will be invoked if only required for the execution of terminal operations.
- But it is optimized and it can process large numbers of data with high performance.

</details>

  ---

## Problem Solving

18: Predict the output for the following operation.
 ``` java
 
Stream<String> s = Stream.of("java", "SQL", "python",  "JDBC");
 s.filter(x -> x.startsWith("S")).forEach(System.out::print);
  
 ```
  <details><summary><b> Show Answer</b></summary>

  returns SQL
   
  <details><summary><b> Explanation </b></summary>
   
 - Here we are using the filter to return the result of the element starting with "S".

 </details>
   
   </details>
   
  ---

 19: Predict the output of the following intermediate operation.
 ``` java

Stream<String> s = Stream.of("apple", "orange", "apple", "banana", "banana");
s.distinct().forEach(System.out::print);
   
 ```
 <details><summary><b> Show Answer</b></summary>

   returns appleorangebanana
  
 <details><summary><b> Explanation </b></summary>
  
- distinct()- will return a stream from the source stream removing the duplicate elements.
  
 </details>
  
   </details>
  
  ---


 20: Predict the output of the following code.

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
 <details><summary><b> Show Answer</b></summary>
  
   2<br>
   4<br>
   6<br>
   8<br>
  
  <details><summary><b> Explanation </b></summary>
   
   - iterate () is used to iterate through the elements in the stream.
   - filter() used to apply the condition on the stream 
   - forEach() is used to return the result from the stream after iteration.
 
</details>
   
</details>
   
---


