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

4. Difference between ArrayList and Hashmap 

<details> <summary>Show Answer</summary>
 
<blockquote>

ArrayList and HashMap are two different data structures in Java that serve different purposes. 

**Here are some of the key differences between them:**

**1. Data type:** ArrayList is used to store a collection of elements of a single data type, while HashMap is used to store key-value pairs where both the key and value can be of different data types.

**2. Indexing:** ArrayList elements are indexed and can be accessed using the index number, while HashMap elements are accessed using the key.

**3. Ordering:** ArrayList elements are ordered based on the index, while HashMap elements are not ordered.

**4. Duplicates:** ArrayList can contain duplicate elements, while HashMap cannot have duplicate keys. However, values in HashMap can be duplicated.

**5. Search time:** ArrayList uses index-based search, which is faster than HashMap's hash-based search. However, HashMap provides constant time search for a given key, regardless of the size of the map.

**6. Memory usage:** ArrayList requires less memory overhead than HashMap because it only stores elements, while HashMap stores key-value pairs along with the hash table.

In summary, ArrayList is used to store a collection of elements of a single data type in a specific order, while HashMap is used to store key-value pairs in an unordered manner for fast retrieval of values using keys.

</blockquote>

</details>

5. what is Complexity and bigO notations of different sort methods and Arrays.sort


<details> <summary>Show Answer</summary>
 
<blockquote>

| Sorting Algorithm | Time Complexity | Best Case  | Worst Case | Space Complexity | Stable |
| ----------------- | --------------- | ---------- | ---------- | ---------------- | ------ |
| Bubble Sort       | O(n^2)          | O(n)       | O(n^2)     | O(1)             | Yes    |
| Selection Sort    | O(n^2)          | O(n^2)     | O(n^2)     | O(1)             | No     |
| Insertion Sort    | O(n^2)          | O(n)       | O(n^2)     | O(1)             | Yes    |
| Quick Sort        | O(n log n)      | O(n log n) | O(n^2)     | O(log n)         | No     |
| Merge Sort        | O(n log n)      | O(n log n) | O(n log n) | O(n)             | Yes    |
| Heap Sort         | O(n log n)      | O(n log n) | O(n log n) | O(1)             | No     |
| Arrays.sort()     | O(n log n)      | O(n)       | O(n log n) | O(log n)         | Yes    |

<b><i>Note:</b>

- "Stable" refers to whether the algorithm maintains the relative order of equal elements in the sorted array.
- "Space complexity" refers to the amount of additional memory required by the algorithm, apart from the input array itself.</i>


</blockquote>

</details>

6. Create a queue with two stacks.

<details> <summary>Show Answer</summary>
 
<blockquote>

To create a queue using two stacks, we need to maintain two stacks:

1. A "push" stack to enqueue elements.
2. A "pop" stack to dequeue elements.
The approach is as follows:

- To enqueue an element, simply push it onto the "push" stack.
- To dequeue an element, if the "pop" stack is not empty, pop the top element from it and return it. Otherwise, pop all the elements from the "push" stack and push them onto the "pop" stack. Then pop the top element from the "pop" stack and return it.

```java
import java.util.Stack;

public class QueueWithTwoStacks<T> {
    private Stack<T> pushStack = new Stack<>();
    private Stack<T> popStack = new Stack<>();

    public void enqueue(T element) {
        pushStack.push(element);
    }

    public T dequeue() {
        if (popStack.isEmpty()) {
            while (!pushStack.isEmpty()) {
                popStack.push(pushStack.pop());
            }
        }
        return popStack.pop();
    }

    public boolean isEmpty() {
        return pushStack.isEmpty() && popStack.isEmpty();
    }

    public int size() {
        return pushStack.size() + popStack.size();
    }
}

```


</blockquote>

</details>

7. find non repeating characters in a string and convert them to capitals.

<details><summary>Show Answer</summary>

<blockquote>



</blockquote>

</details>

---


8. The challenge was, given an array of numbers, to write a method that moves all 0's to the end of the array. So, if I had an array of numbers [1, 0, 3, 4, 0, 5], the method would return [1, 3, 4, 5, 0, 0]. She asked me to share my screen while completing the challenge. She then asked what test cases I would use to test the method.

<details><summary>Show Answer</summary>

<blockquote>



</blockquote>

</details>

---




