## Technical


1. What is List Interface?

<details>

<summary><b>Show Answer</b></summary>

> - A list is an ordered collection of elements. 
> - Duplicate elements are allowed in the list. 
``` java 
List <E> l ;
```

> the above code represents List declaration, where E is an element ( type parameter).

</details>

---

2. List out basic List operations.

<details>

<summary><b>Show Answer</b></summary>
 <blockquote>

Along with the operations inherited from the collection interface, the list has the following operations
1. Positional Access: accessing an element by its index.
   
- Insertion: `add` and `addAll` methods are used to insert elements into the collection.
- Update: to update an existing element `set` is used.
- deletion: `remove` is used to delete elements.


2. Search: used to search the specific element and get the index of the element
indexOf and lastIndexOf are Search methods.

3. Iteration: used to iterate over a list as it is a sequential data structure.
listIterator is an Iteration method.

4. Range-view: is used to get the subList of the list of a specific range.
subList method is a range-view method.


 </blockquote>
</details>

 ---
3. what are the different classes that come under the list interface?

<details>

<summary><b>Show Answer</b></summary>

> The following are the classes that implement List Interface.
> 1. `ArrayList`
> 2. `LinkedList`
> 3. `Vector`
> 4. `Stack`

</details>

---

4. What is Array List and explain the internal working of an ArrayList?

<details>

<summary><b>Show Answer</b></summary>

> ArrayList is a dynamic array and it implements the list interface.

> internal working of ArrayList:

> 1. Initially, an array of capacity 10 is created
> 2. when elements beyond the capacity i.e. 10 are added to the ArrayList a new array of size 

  $ n + n/2 + 1$

> where n is the capacity of the array

> 3. All the elements in the old array are copied to the new array and the old array is dumped.


</details>

---

5. What is LinkedList and explain the internal working of LinkedList?

<details>

<summary><b>Show Answer</b></summary>

> - LinkedList is used to store the elements in a sequential manner.
> - Linked list implements both list and deque interface.
> - Internally Linked list is a double-linked list with nodes that store the address of the previous element and the next element.

</details>

---


6. How to add a single element at the end of the list?

<details>

<summary><b>Show Answer</b></summary>

> 1. <code>add(element)</code> method is used to add single element at the end of the list.

``` java

List <Integer> al = new ArrayList<>();
al.add(1);

```

> - In the above code an array list "al" is created and it stores Integer elements and element 1 is added to the ArrayList.


</details>

---

7. How to add bulk elements to the list?

<details>

<summary><b>Show Answer</b></summary>

> 1. addAll method is used to add bulk elements to the list.

``` java

List <Integer> al1 = new ArrayList<>();

al1.add(1);
al1.add(2);

List <Integer> al2 = new ArrayList<>();

al2.addAll(al1);
al2.addAll(0,al2);

```

>- In the above code an array list "al1" and "al2" are created and some elements are added to al1, all the elements in al1 are added to al2 using addAll().
>-  <code>addAll(collection)</code> adds elements at the end of the list and <code>addAll(int index, collection)</code> adds elements from a specific position.


</details>

---

8. How to retrieve an element from a specific position in a list?

<details>

<summary><b>Show Answer</b></summary>

> 1. <code>get(int index)</code> method is used to get a  single element from the list.

</details>

---

9. What is a vector and how does a vector work internally?

<details>

<summary><b>Show Answer</b></summary>

> - Vector is internally a dynamic array with an initial capacity and capacity increment.
> - Vector is similar to ArrayList, the main difference is that the vector is synchronized.
> - Vector is a legacy class so it has some methods which are not part of the collection framework.

</details>

---


10. What is Stack and what are the different stack operations?

<details>
<summary><b>Show Answer</b></summary>

> -  Stack follows the Last in First out principle
>-  Stack extends Vector and it has five additional operations, which are:

> 1. push(element): adds elements to the top of the stack and returns the element.
> 2. pop(): deletes the top element of the stack and returns that element, throws EmptyStackException if the stack is empty.
> 3. peek(): returns the topmost element of the stack, and throws EmptyStackException if the stack is empty. 
> 4. empty(): returns a boolean value. returns true if the stack is empty and false if the stack is not empty.
> 5. Search(element): this method returns the distance of the element from the top of the stack, the distance for the top element is 1. is the element is not present it returns -1.

</details>

---


11. When to use ArrayList and LinkedList?

<details>

<summary><b>Show Answer</b></summary>

> - Array list and linked list are two general purpose list classes.
>-  mostly array list is preferred over a linked list because in ArrayList elements can be accessed at a constant time. In a linked list as elements are stored in the form of nodes, it gives linear positional access

> <i><b>Note:</b> 
> - constant access: The time complexity is directly proportional to a constant value and is in no way related to the size of the data structure.
> - linear access: the time complexity is proportional to the size of the data structure.

</i> 

| ArrayList                                                                            | LinkedList                                                                                                                                                                 |
| ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Used when deletion and insertion operations are minimal.                             | Used when insertion operations and deletion operations are more frequent                                                                                                   |
| ArrayList has a tuning point to set the initial capacity                             | Linked list has no tuning point but has seven operations, clone, addFirst, addLast, reomveFirst, removeLast, getFirst and getLast. It also implements the queue interface. |
| ArrayList is fast and constant time complexity is achieved in most of the operations | LinkedList is comparatively slow and linear time complexity is achieved in most of the cases                                                                               |


</details>

---

12. Which of the following is the non-synchronized version of the vector?

A. ArrayList<br>
B. LinkedList<br>
C. Stack<br>
D. ArrayDeque

<details>

<summary><b>Show Answer</b></summary>

> A

<details>

<summary><b>Explanation</b></summary>

> Array List like vector is a dynamic array and is non-synchronized
> ArrayList is prefered over Vector as it's fast because it is not synchronized.

</details>
</details>

---

13. What is the best case time complexity of <code>add(element)</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> as elements are added to the end of the ArrayList the time complexity is O(1)
> but in the worst case, i.e. when the capacity of ArrayList is exceeded, a new array is created and all the elements are copied to the new Array and the new element is added, here the time complexity is O(n).

</details>
</details>

---

14. What is the complexity of <code>add(index,element)</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> A

<details>
<summary><b>Explanation</b></summary>

> Since the element can be added at any specific index, most of the elements in the list are shifted to insert the new element. on average the time complexity is O(n).

</details>
</details>

---

15. What is the time complexity of <code>get(index)</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> B

<details>
<summary><b>Explanation</b></summary>

> In an array List the elements can be accessed directly by their position, So the time complexity is O(1).

</details>
</details>

---

16. What is the time complexity of <code>remove()</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> A

<details>
<summary><b>Explanation</b></summary>

> to remove an element the entire array is traversed and after finding the element the element is deleted. So the time complexity is O(n).

</details>
</details>

---

17. What is the time complexity of <code>indexOf(element)</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> A

<details>
<summary><b>Explanation</b></summary>

> In the worst-case scenario the element is the last element and the entire ArrayList should be traversed to get the position of the element, So the time complexity is O(n).

</details>
</details>

---

18. What is the time complexity of <code>contains(element)</code> method?

A. O(n)<br>
B. O(1)<br>
C. O(log n)<br>
D. O(n <sup>2</sup>)

<details>
<summary><b>Show Answer</b></summary>

> A

<details>
<summary><b>Explanation</b></summary>

> <code>contains(element)</code> implementation is similar to <code>indexOf(element)</code>. so the time complexity is O(n).

</details>
</details>

---
## Problem Solving

1. <b>Problem Statement:</b>size, list of sorted elements and a key are given as input. write a program to print the indexes of all the occurrences of a key in the list with the time complexity of O(n). 

> <b>Sample Input:</b>
> 7
> 1 2 2 2 3 4 5
> 2

> <b>Sample Output</b>
> 1 2 3

> <b>Explanation</b>
> - line 1 is the size = 7
> - line 2 is the list of elements.
> - line 3 is the key element which is 2.
> - Output is the indices of all the occurrences of 2(key).

<details>

<summary><b>Show Answer</b></summary>

``` java

import java.util.*;
public class Collections {
  public static void main(String[] args) {
    
    Collections c = new Collections();
    Scanner sc = new Scanner(System.in);
    ArrayList<Integer> al = new ArrayList<>();
    int size = sc.nextInt();
    for( int i=0;i<size;i++)
    {
      al.add(sc.nextInt());
    }
    
    int key = sc.nextInt();
    
    c.printOccurance(al, key);
    
  }
  
  void printOccurance(ArrayList<Integer> al, int key)
  {
    int start = al.indexOf(key);
    int last = al.lastIndexOf(key);
    for( int i = start;i<=last;i++) {
      
      System.out.print(i + " ");
    }
      
      
  }
    
}


```

</details>

## Scenario Based

1. Dora is going for an adventure and she needs a backpack to carry all her items (more than one copy of the item may exist) and she might buy some items on the way and store it in her backpack. and she wants to get items immediately from her backpack when she needs them. So the backpack should be resizable and elements can be accessed in constant time. which of the following is the best option?

A. LinkedList <br>
B. ArrayList <br>
C. HashSet<br>
D. None of the Above

<details>

<summary><b>Show Answer</b></summary>

> B

<details>

<summary><b>Explanation</b></summary>

> Array list is a dynamic array, so Dora can store any number of items in the backpack, Array list allows duplicate elements, and elements can be accessed with a time complexity of O(1) using the index, So Dora can get her items from her backpack immediately. 


</details>
</details>

---

1. Indiana Jones is going for a treasure hunt and he needs a backpack to store the valuable items throughout his journey, if he finds out that an item he stored in the backpack is fake he takes it throws it away, and he never takes any item out of his back till the journey ends. which of the following is the best option?

A. LinkedList <br>
B. ArrayList <br>
C. HashSet<br>
D. None of the Above

<details>

<summary><b>Show Answer</b></summary>

> A

<details>

<summary><b>Explanation</b></summary>

> LinkedList varies in size dynamically and insertion and deletion operations in the linked list have constant time. So Indiana Jones can store and remove elements from his backpack easily using a LinkedList.


</details>
</details>









