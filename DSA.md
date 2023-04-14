1. If I have a list of 100,000 records, what search algorithm would you use to find a specific record?

<details> <summary>Show Answer</summary>
 
<blockquote>

If the list is sorted then binary search is the best option as it provides O(log n) time complexity.

If the records are not sorted then the linear search is used which provides a time complexity of O(n).
  
</blockquote>

</details>

2. How do you create a doubly linked list?

<details> <summary>Show Answer</summary>
 
<blockquote>

- A doubly linked list is a data structure that consists of a sequence of nodes, where each node contains a reference to both the previous and next nodes in the list.

- Java has Collections with Interfaces like List interface and a class `LinkedList` which is a doubley linked list.

Code to create doubly linked list in java:


```java
Java provides a built-in implementation of the linked list data structure in the java.util.LinkedList class. Here is an example of how to use it:

csharp
Copy code
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        LinkedList<String> list = new LinkedList<String>();
        list.add("Alice");
        list.add("Bob");
        list.add("Charlie");
        
        System.out.println(list); // prints [Alice, Bob, Charlie]
        
        list.remove(1); // removes "Bob"
        System.out.println(list); // prints [Alice, Charlie]
        
        System.out.println(list.get(1)); // prints "Charlie"
    }
}
```


  
</blockquote>

</details>

3. What's the difference between an array and arrayList

<details> <summary>Show Answer</summary>
 
<blockquote>

| Feature        | Array                   | ArrayList                                       |
| -------------- | ----------------------- | ----------------------------------------------- |
| Data type      | Can only hold a single  | Can hold any object or primitive data type      |
|                | data type               |                                                 |
| Length         | Fixed length            | Dynamic length, can grow or shrink as needed    |
| Initialization | Must specify length     | Can be initialized without specifying length    |
| Performance    | Faster for small arrays | Slower for large arrays due to resizing         |
|                |                         | and other overhead                              |
| Methods        | Fewer built-in methods  | More built-in methods for manipulating elements |
|                | for manipulating        | such as add(), remove(), get(), etc.            |
| Memory usage   | Less memory overhead    | More memory overhead due to additional objects  |
  
</blockquote>

</details>

