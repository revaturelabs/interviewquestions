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

</details>

11: Differentiate between map() and flatMap().

<details><summary> Show Answer</summary>

- map()- will work on the streams and transform the single input value into single output.
- flatMap()- will work on the streams and transform the single input value into mulitple outputs by flattening it.

</details>

12: 