## Technical

1. What is  Queue Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - Queue stores elements before processing and normally queue follows the First in First out principle.
> Consider that there are two states "Ready for processing"(RFP) and " On Hold " (OH), the head is in the "RFP" state and all the elements behind the head are in the "OH" state. so elements in the queue are in pre processing state.
> - Queue Interface is used to implement a queue in java.
  
![Queue Interface](https://user-images.githubusercontent.com/103101208/184882415-4ff432b0-e6ae-4e92-a5f2-ba15675458b6.jpg)
  


</details>

---

2. List out basic queue operations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> Along with operations in collections queue has some special operations like

> 1. `offer(element)`: used to add elements to the queue.
> 2. `poll()`: used to get the head element of the queue.
> 3. `element()`: returns head element of the queue.


</details>

---

3. What is `offer(element)` and how is it different from `add(element)`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - `offer(element)` is used to insert elements into queue
> - `offer(element)` returns a boolean value, true if the element is added to the queue and false if otherwise.
> - `add(element)` is also used to insert elements but add returns the element and creates an exception if elements cant be added to the collections.
> - `offer(element)` is prefered over `add(element)` to avoid exceptions in the program. 


</details>

---

4. What is `poll()` and how is different from `remove()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - `poll()` is used to get head element from the queue.
> - `poll()` returns a the element, returns null if queue is empty.
> - `remove()` is used to delete elements from the queue.
> - `remove()` returns the element and throws an exception when the queue is empty.
> - `poll()` is prefered over `remove()` to avoid exceptions in the program.


</details>

---

5. What is  `element()` and how is different from `peek()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - `element()` is used to get the head element from the queue, unlike the poll element doesn't remove elements from the queue. returns element or throws an exception if the queue is empty. 
> - `peek()` is used to get the head from the queue.  returns element or returns null if the queue is empty.
> -  `peek()` is prefered over `element()` to avoid excpetions in the program.


</details>

---

6. What is ArrayDeque? Explain the internal working of ArrayDeque.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - ArrayDeque is a double-ended queue and it implements the Deque Interface.
> - Along with queue interface methods array, deque has some special methods to add and retrieve elements from both the front and rear end.

</details>

---

7. List out the operations of `ArrayDeque`.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> 1. `offerFirst(element)` is used to insert elemnts from the head
> 2. `offerLast(element)` similar to `offer(element)`, is used to add elements in the rear end.
> 3. `pollFirst()` is used to get an element from the head.
> 4. `pollLast()` similar to `poll()`, is used to get an element from the rear end.
> 5. `getFirst()` similar to `element()` ,is used to retrive an element from the head.
> 6. `getLast()` is used to retrive  an element from the rear end.
> 7. `peekFirst()` similar to `peek()`, is used to get but not remove the first element from the head.
> 8. `peekLast()` is used to but not remove the elemnt from the rear end.



</details>

---

8. What is `PriorityQueue` and how does it work internally?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

> - `PriorityQueue` is a queue that stores the elements in general order(ascending) or uses a comparator to sort the elements.
> - Internally ` PriorityQueue` is a heap.
> - By default elements are stored in the form of a min heap.



</details>

---

9. What is BlockingQueue?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

<blockquote>

- `BlockingQueue` is similar to queue but it supports some operations like waiting for the queue to be non-empty to retrieve an element and waiting till the space is available to insert the elements.

- `BlockingQueue` doesn't accept null elements.
</blockquote>


</details>

---

10. What is the time complexity of <code>offer(element)</code> method for `ArrayDeque`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> In `ArrayDeque` elements are added at the rear end when `offer(element)` is used so time complexity is O(1).

</details>
</details>

---


11. What is the time complexity of <code>poll()</code> method for `ArrayDeque`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> In `ArrayDeque` elements are retrieved from the front end when `poll()` is used so time complexity is O(1).

</details>
</details>

---

12. What is the time complexity of <code>element()</code> method for `ArrayDeque`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

>  In `ArrayDeque` elements are retrieved but not removed from the front end. When `element()` is used so time complexity is O(1). 

</details>
</details>

---

13. What is the time complexity of <code>offer(element)</code> method for a `PriorityQueue`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> C

<details>
<summary><b>Explanation</b></summary>

> Elements are sorted and stored in the form of a heap in `PriorityQueue`. The time complexity to insert an element using `offer(element)` is O(log n).

</details>
</details>

---


14. What is the time complexity of <code>poll()</code> method for a `PriorityQueue`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> Elements are sorted in `PrirityQueue`, when ` poll()` is used the first element is retrieved.

</details>
</details>

---

15. What is the time complexity of <code>element()</code> method for a `PriorityQueue`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> Elements are sorted in `PrirityQueue`, when ` element()` is used the first element is retrieved but not removed.

</details>
</details>

---
16. What is the Difference between `Queue` and `Deque`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary><b>Show Answer</b></summary>
  
<blockquote>
  
  
  
  
  
  </blockquote>
  
  
</details>



## Problem Solving

17.  What are AA, BB, CC and DD?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
ArrayDeque<Integer> ad = new ArrayDeque<>();
```
a. ad.AA(e): to insert an element at the front end.<br>
b. ad.BB(e): to get an element from the rear end.<br>
c. ad.CC(e): to insert an element at the rear end.<br>
d. ad.DD(e): to get an element from the front end.

<details>

<summary><b>Show Answer</b></summary>

<blockquote>


- AA is `offerFirst()` or `addFirst()`.
- BB is `pollLast()` or `removeLast()`.
- CC is `offer()` or `add()`.
- DD is `poll()` or `remove()`.

</blockquote>

</details>

---

18. Predict the output of the following code snippet.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java

ArrayDeque<Integer> ad = new ArrayDeque<>();
ad.push(4);
System.out.println(ad.pop());

``` 

<details>

<summary><b>Show Answer</b></summary>

> - 4
> - `ArrayDeque` acts like a stack , so `push(element)` and `pop()` can be implemented.

</details>

---

19. Predict the output of the following code snippet. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
ArrayDeque<Integer> ad = new ArrayDeque<>();
ad.offer(1);
System.out.println(ad.poll());

```

<details>

<summary><b>Show Answer</b></summary>

> -  4
> -  `ArrayDeque` acts like a queue , so `offer(element)` and `poll()` can be implemented.

</details>

---

20. Predict the output of the following code snippet. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
ArrayDeque<Integer> ad = new ArrayDeque<>();
ad.add(1);
System.out.println(ad.remove());

```

<details>

<summary><b>Show Answer</b></summary>

> - 1
> - `ArrayDeque` acts like a `List` , so `add(element)` and `remove()` can be implemented.
</details>



## Real-time Application

21. There is a movie premiere and people should walk through the red carpet before they are allowed into the movie theatre. people walk on the carpet based on their importance, The order goes like, Produce, Director, lead Actors, supporting actors and the list continues. Which of the following best represents the following scenario?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. `ArrayDeque` <br>
B. `PriorityQueue` <br>
C. `BlockingQueue` <br>
D. `Queue` 

<details>

<summary><b> Show Answer </b></summary>

> B

<details>

<summary><b> Explanation </b></summary>

<blockquote>

People are allowed into the theatre based on their priority so the list of people can be stored using a PriorityQueue.

</blockquote>


</details>


</details>


















