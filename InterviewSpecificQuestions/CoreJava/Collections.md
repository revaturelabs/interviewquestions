## Technical

1. What does the Collections framework in Java contain?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).

</blockquote>
</details>

---

2. Can you tell the main interfaces, and what are the differences between them?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Set, List and Map are three important interfaces of the Java collection framework.
- A List can be used when the insertion order of elements needs to be maintained.
- We can use a set if we need to maintain a collection that contains no duplicates.
- And Map when data is key-value pairs and need fast retrieval of value based on some key.

</blockquote>
</details>

---

3. Why is Map not inherited from the Collection interface, even though it is a component of the Java collection framework? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Because they are of an incompatible type. List, Set, and Queue are a collection of similar kind of objects but just values whereas a  Map is a collection of key and value pairs.

</blockquote>
</details>

---

4. How do you remove an entry from a collection? And subsequently, what is the difference between the `remove()` method of a collection and the `remove()` method of an iterator? Which one will you use while removing elements during iteration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Collection interface defines `remove(Object obj)` method to remove objects from `Collection.List` interface and adds another method `remove(int index)`, which is used to remove objects at a specific index.
- You can use any of these methods to remove an entry from Collection, while not iterating. 
- Things change when you iterate. Suppose you are traversing a List and removing only certain elements based on logic, then you need to use Iterator's `remove()` method. 
-This method removes the current element from Iterator's perspective. If you use Collection's or List's `remove()` method during iteration then your code will throw `ConcurrentModificationException`. 
- That's why it's advised to use the iterator `remove()` method to remove objects from Collection.

</blockquote>
</details>

---

5. How does HashSet use Hashing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HashSet extends `AbstractSet` and implements the Set interface. It creates a collection that uses a hash table for storage. A hash table stores information by using a mechanism called hashing. In hashing, the informational content of a key is used to determine a unique value, called its hash code.

</blockquote>
</details>

---

6. How is HashSet implemented in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

When we create an object of HashSet, it internally creates an instance of HashMap with default initial capacity 16. HashSet uses a constructor `HashSet(int capacity)` that represents how many elements can be stored in the HashSet. The capacity may increase automatically when more elements are to be stored

</blockquote>
</details>

---

7. Which one do you prefer in Java between Array and Array Lists for storing objects and why?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Though ArrayList is also backed up by array, it offers some usability advantage over array in Java.Array is fixed length data structure, once created you can not change it's length. On the other hand,ArrayList is dynamic, it automatically allocate a new array and copies content of old array, when it resize.Another reason of using ArrayList over Array is support of Generics.

</blockquote>
</details>

---

8. How does LinkedList is implemented in Java, is it a Singly or Doubly linked list?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Java LinkedList:
    - It is an implementation of the List and Deque interfaces. Internally, it is implemented using Doubly Linked List Data Structure. It supports duplicate elements. 
    - It stores or maintains elements in Insertion order. 

</blockquote>
</details>

---

9. Does Collection and Collections are same in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, Collection is a top-level interface of the Java collection framework whereas Collections is a utility class. The below table shows the difference between them.

- Collection:	
    - Collection is a root-level interface of the Java Collection Framework. 
    - Most of the classes in the Java Collection Framework inherit from this interface.	
    - List, Set, and Queue are main sub-interfaces of this interface.	

- Collections:
    - Collections is a utility class in java.util package. 
    - It consists of only static methods which are used to operate on objects of type Collection.
    -  `Collections.max()`, `Collections.min()`, `Collections.sort()` are some methods of Collections class.

</blockquote>
</details>

---

10. What classes should i prefer to use a key in HashMap in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We should prefer String, Integer, Long, Double, Float, Short and any other wrapper class. Reason behind using them as a key is that they override `equals()` and `hashCode()` method, we need not to write any explicit code for overriding `equals()` and `hashCode()` method in java.

</blockquote>
</details>

---

11.  Suppose there is a Student class. We add Student class objects to the ArrayList. Mention the steps that need to be taken if I want to sort the objects in ArrayList using the studentId attribute present in the Student class. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Implement the Comparable interface for the Employee class and now to compare the objects by studentId we will override the `std1.compareTo(std2)` .
- We will now call Collections class `sort()` method and pass the list as an argument, that is,
`Collections.sort(stdList)`

</blockquote>
</details>

---

12. What is the sorting algorithm used in `Collections.sort()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`Collections.sort()` uses the Merge sort algorithm to sort the objects.

</blockquote>
</details>

---

13. What will happen if we put two values with the same key in Map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If we try to insert two values for the same key, the second value will be stored, while the first one will be dropped.

</blockquote>
</details>

---

14. Can an ArrayList contain multiple references to the same object in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The ArrayList in java does not provide checks for duplicate references to the same object. Therefore, we can insert the same object or reference to a single object as many times as we want.

</blockquote>
</details>

---

15. If the frequent operation is retrieval which collection is used and if the frequent operation is insertion or deletion which one is used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If the frequent operation is retrieval the ArrayList for the othercase LinkedList.

</blockquote>
</details>

---

16. How iterator and enumerator differ while iterating the elements in the collection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Enumeration is twice as fast as Iterator and uses less memory. The iterator is thread-safe because does not allow other threads to modify the collection when iterating.
- Enumeration can only be used for read-only collections. It also has no `remove()` method ;
- Enumeration:  `hasMoreElement()` ,  `nextElement ()`
- Iterator:  `hasNext()` ,  `next()` ,  `remove()`

</blockquote>
</details>

---


17. Can we use a null element in TreeSet? Give reason?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, TreeSet does not allows to store any null keys. Any attempt to add null throws `runtimeException (NullPointerException)`.
- TreeSet internally compares elements for sorting elements by natural order (comparator may be used for sorting, if defined at creation time) and null is not comparable, Any attempt to compare null with other object will throw `NullPointerException`.

</blockquote>
</details>

---

18. What will be the output of the given snippet?

<blockquote>

```Java

    List<String> arrayList = new ArrayList<String>();
    arrayList.add("a");
    arrayList.add("b");
 
    ListIterator<String> listIterator = arrayList.listIterator();
    while (listIterator.hasNext()) {
        System.out.println(listIterator.next());
        listIterator.previous();
    }
```
</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
	
**Output**

infinite times

</blockquote>

<blockquote>

<details> <summary> <b> Explanation </b> </summary>

ArrayList provides a listIterator for traversing in forward and backward directions, so the  program will compile and run infinitely.

</details>

</details>

---

19. If we want to use a custom object as a key in Collection classes like Map or Set, how can we achieve that?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- If you are using any custom object in Map as a key, you need to override `equals()` and `hashCode()` method, 
and make sure they follow their contract. On the other hand, if you are storing a custom object in the  Sorted Collection 
- e.g. SortedSet or SortedMap, you also need to make sure that your `equals()` method is consistent to `compareTo()` method, otherwise that collection will not follow their contacts e.g. Set may allow duplicates.

</blockquote>
</details>

---

20. Do you know what is BlockingQueue? Give a practical example of BlockingQueue?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- BlockingQueue is a java Queue that support operations that wait for the queue to become non-empty when retrieving and removing an element, and wait for space to become available in the queue when adding an element.
- Producer-consumer problem is a best example of BlockingQueue.

</blockquote>
</details>

---

21.  What is the difference between fail-safe and fail-fast properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Fail-fast Iterators throw `ConcurrentModificationException` when one thread is iterating over the collection object and another thread structurally modifies the Collection either by adding, removing, or modifying objects on the underlying collection. 
- They are called fail-fast because they try to immediately throw Exceptions when they encounter failure. - On the other hand, fail-safe Iterators works on a copy of the collection instead of the original collection

</blockquote>
</details>

---

22. Which Collection type do you suggest to me If I want a sorted collection of objects with no duplicates?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TreeSet is the best suitable for such scenarios where you want a collection of objects with no duplicates and also sorted based on a particular data field.

</blockquote>
</details>

---

23. Why is it recommended not to use the Vector class in our code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Vector class is preferred over ArrayList class when you are developing a multi-threaded application. 
But, precautions need to be taken because vector may reduce the performance of your application as it is 
Thread-safe and only one thread is allowed to have an object lock at any moment of time and the remaining threads have to wait until a thread releases the object lock. So, it is always recommended that if you don’t need thread safe environment, it is better the to use ArrayList class than the Vector class.And also Vector class is often considered as obsolete or “Due for Deprecation” by many experienced Java developers. They always recommend and advise not to the use Vector class in your code. They prefer using ArrayList over Vector class.

</blockquote>
</details>

---

24. How to sort ArrayList in descending order?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can use `reverseorder()` like `Collections.sort(arraylist, Collections.reverseOrder())`;  

</blockquote>
</details>

---

25. Predict the output?

<blockquote>

```Java

    PriorityQueue<Integer> queue = new PriorityQueue<>();
    queue.add(25);
    queue.add(15);
    queue.add(23);
    queue.add(5);
    queue.add(12);
    queue.add(2);
 
    while (queue.isEmpty() == false)
        System.out.printf("%d ", queue.remove());
 
    System.out.println("\n");
```

</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Output**
	
2 5 12 15 23 25

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

Priority queue always outputs the minimum element from the queue when the `remove()` method is called, no matter what the sequence of input is.

</blockquote>
</details>
</details>
	
---

26. Can you pass `List(String)` to a method which accepts `List(Object)`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- List(Object) can store any thing including String, Integer etc, but List(String) can only store Strings.
- List(Object) objectList;
- List(String) stringList;
- objectList = stringList; **compilation error**

</blockquote>
</details>

---

27. If the compiler erases all type parameters at compile time, why should you use generics?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The reason to use generics is, the Java compiler enforces tighter type checks on generic code at compile time.
- Generics support programming types as parameters.
- Generics enable us to implement generic algorithms

</blockquote>
</details>

---

28. Why is String a popular Hashmap key in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Since String is immutable, its hashcode is cached at the time of creation and it doesn’t need to be calculated again. This makes it a great candidate for keys in a Map and its processing is fast than other HashMap key objects. Therefore,String is mostly used Object as HashMap keys.

</blockquote>
</details>

---

29. How will you create a Readonly List, Set, and Map in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can use `Collections.unModifiableList()` method to create a read-only List,`Collections.unmodifiableSe()`for creating a read-only Set like a read-only HashSet and similarly creating a read-only Map in Java.

</blockquote>
</details>

---

30. When to use Queues and stack? What is the possible use case?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Stack and Queue work on the principle of First in Last Out and First in First out. The best use case of Queue is in the messaging services, where we implement the messaging container, which allows one message to get input and another message to get output from the queue.
- The queue has the ability to also act as a buffer to store the elements for a temporary time.
- Whereas Stack’s best use is to perform prefix, postfix, and infix operations in the Tree.

</blockquote>
</details>

---

30. What is a collision problem ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The collision problem is, whenever the hash function returns the same index position for a different key, then a collision occurs. The collision detection technique is also called collision detection.

</blockquote>
</details>

---

31. Can I add a null element to HashSet and TreeSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- We can’t add any null element in TreeSet as it uses NavigableMap for element storage. But we can add just one to HashSet.
- SortedMap doesn’t allow null keys and NavigableMap is its subset.
- That’s why we can’t add a null element to TreeSet, it will come up with the `NullPointerException`
 every time you try to do that.

</blockquote>
</details>

---

32. How will you remove the duplicates from the Array List?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are two ways to remove duplicates from the ArrayList.

- **Using HashSet**: By using HashSet we can remove the duplicate element from the ArrayList, but it will not then preserve the insertion order.
- **Using LinkedHashSet**: We can also maintain the insertion order by using LinkedHashSet instead of HashSet.

</blockquote>
</details>

---

33. Can you use iterateor interface over map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, Map does not implement Iterable interface, only Collection ( thus , list and set ) do , so the Collection implements iterable \<E\> , make the set and the list iteratble.
- The Map can't be iterable only the key part can be iterable 

</blockquote>
</details>

---

34. Predict the output?
<blockquote>

```Java

    public class HashMapTest {
        public static void main(String args[]) {
                Map<Integer, String> hashMap = new HashMap<Integer, String>();
                hashMap.put(11, "a");
                hashMap.put(null, "c");
                hashMap.put(null, null);
 
                System.out.println(hashMap.size());
                System.out.println(hashMap);
            }
        }
```
</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**OUTPUT**
    
2<br>
{null=null, 11=a} 

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

HashMap does not maintains insertion order of keys, and allows one null key and many null values.

</blockquote>
</details>
</details>

---

35.  Predict the output?
<blockquote>

```Java
    public class HashSetTest {
        public static void main(String args[]) {
 
            Set hashSet = new HashSet();
            hashSet.add("1");
            hashSet.add(1);
            hashSet.add(null);
            hashSet.add("null");
            System.out.println(hashSet);
 
        }
    }
```

</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**OUTPUT**
 
[null, 1, 1, null]

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

HashSet does not store duplicates but “1” is a String, while 1 is Integer & null is nothing, while “null” is a String . Also HashSet does not maintain insertion order and allows null.

</blockquote>
</details>
</details>

---

36. Predict the output?
<blockquote>

```Java
    public class LinkedHashSetTest {
        public static void main(String args[]) {
 
            Set s = new LinkedHashSet();
            s.add("1");
            s.add(1);
            s.add(3);
            s.add(2);
            System.out.println(s);
 
        }
    }
```
</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**OUTPUT**
 
[1, 1, 3, 2]

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

LinkedHashSet maintains insertion order and does not allow duplicates.

</blockquote>
</details>
</details>

---

37. Predict the output?
<blockquote>

```Java
    public class MyClass {
        public static void main(String args[]) {
            Map<String, String> identityHashMap = new IdentityHashMap<String, String>();
            identityHashMap.put(new String("a"), "audi");
            identityHashMap.put(new String("a"), "ferrari");
            System.out.println(identityHashMap);
        }
    }
```
</blockquote>

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**OUTPUT**
 
{a=audi, a=ferrari}

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

- IdentityHashMap when comparing keys (and values) performs reference-equality in place of object-equality. 
- In an IdentityHashMap, two keys k1 and k2 are equal if and only if (k1==k2). (In normal Map implementations (like HashMap) two keys k1 and k2 are considered equal if and only if (k1==null ? 
k2==null : k1.equals(k2)).) 
- new String("a") & new String("a") are different by reference.

</blockquote>
</details>
</details>

---

38. Which methods do you need to override to use any object as a key in HashMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To use any object as a key in HashMap, it needs to implement `equals()` and `hashCode()` methods.


</blockquote>
</details>

---


39. What is and when to use `Collections.emptySet()` . What is the advantage of having emptySet in Collections class ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`Collections.emptySet()` returns the empty immutable Set ,not containing null.

</blockquote>
</details>

---

40. Why do we call `emptySet()` method, as we can also create an empty Set using a constructor ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Advantages of using `emptySet()` method over creating an object using a constructor are :

1. Immutable: You should prefer to use immutable collections against mutable collections wherever possible. It becomes handy as multiple threads accessing the same instance of an object will see the same values.

2. Concise:  You do not need to manually type out the generic type of the collection - normally it is inferred from the context of the method call.


3. Efficient: As `emptySet()` method doesn’t create new objects, so they just reuse the existing empty and immutable object . Although, practically, this trick is not that handy, and rarely improves the performance

</blockquote>
</details>

---

41.  What copy technique internally used by HashSet `clone()` method ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- There are two copy techniques in every object oriented programming language , 
deep copy and shallow copy.
- To create a clone or copy of the Set object, HashSet  internally uses shallow copy 
in `clone()` method , the elements themselves are not cloned . 
- In other words , a shallow copy is made by copying the reference of the object.

</blockquote>
</details>

---

42. What is a good way to sort the Collection objects in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A good way to sort Java collection objects is using Comparable and Comparator interfaces. A developer can use `Collections.sort()`, the elements are sorted based on the order mention in `compareTo()`.
- When a developer uses Collections, `sort (Comparator)`, it sorts the objects depend on `compare()` of the Comparator interface.

</blockquote>
</details>

---

43. What are Generics in Java ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java Generics is a set of related methods or a set of similar types. Generics allow types Integer, String, or even user-defined types to be passed as a parameter to classes, methods, or interfaces. Generics are mostly used by classes like HashSet or HashMap.

</blockquote>
</details>

---

44. What is Collection API ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Collection API is a set of classes and interfaces that support operation on collections of objects. These classes and interfaces are more flexible, more powerful, and more regular than the vectors, arrays, and hashtables if effectively replaces. Example of classes: HashSet, HashMap, ArrayList, LinkedList, TreeSet and TreeMap. Example of interfaces: Collection, Set, List and Map.

</blockquote>
</details>

---

45. What is the difference between hashMap and hashSet in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**HashSet:-**

- HashSet class implements the Set interface
- In HashSet, we store objects (elements or values) e.g. If we have a HashSet of string elements then it could depict a set of HashSet elements: {“Hello”, “Hi”, “Bye”, “Run”}
- HashSet does not allow duplicate elements that mean you cannot store duplicate values in HashSet.
- HashSet permits to have a single null value.
- HashSet is not synchronized which means they are not suitable for thread-safe operations until unless synchronized explicitly.

**HashMap:-**

- HashMap class implements the Map interface
- HashMap is used for storing key & value pairs. In short, it maintains the mapping of key & value (The  HashMap class is roughly equivalent to Hashtable, except that it is unsynchronized and permits nulls).  
- This is how you could represent HashMap elements if it has integer key and value of String type: e.g. {1->”Hello”, 2->”Hi”, 3->”Bye”, 4->”Run”}
- HashMap does not allow duplicate keys however it allows having duplicate values.
- HashMap permits single null key and any number of null values.
- HashMap is not synchronized which means they are not suitable for thread-safe operations until unless synchronized explicitly.

</blockquote>
</details>

---

46. What is the difference between HashSet and TreeSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- HashSet gives better performance (faster) than TreeSet for the operations like add, remove, contains, size etc. HashSet offers constant time cost while TreeSet offers log(n) time cost for such operations.

- HashSet does not maintain any order of elements while TreeSet elements are sorted in ascending order by default.

</blockquote>
</details>

---

47. What is difference between ArrayList and LinkedList?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ArrayList and LinkedList both implements List interface and maintains insertion order. Both are non-synchronized classes.

|Sl.No |ArrayList               |LinkedList                                                                 |
|------|------------------------|--------------------------------------------------------------------------|
|  01. |ArrayList internally uses a dynamic array to store the elements.|LinkedList internally uses a doubly linked list to store the elements.|
| 02. |Manipulation with ArrayList is slow because it internally uses an array. If any element is removed from the array, all the bits are shifted in memory.	|Manipulation with LinkedList is faster than ArrayList because it uses a doubly linked list, so no bit shifting is required in memory.|
| 03. |An ArrayList class can act as a list only because it implements List only.|	LinkedList class can act as a list and queue both because it implements List and Deque interfaces.|
| 04. | ArrayList is better for storing and accessing data.|LinkedList is better for manipulating data.|

</blockquote>
</details>

---

48. What is difference between HashMap and Hashtable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HashMap and Hashtable both are used to store data in key and value form. Both are using hashing technique to store unique keys.

|Sl.No|HashMap	              |Hashtable                                         |
|-----|-----------------------|--------------------------------------------------|
| 01. |HashMap is **non synchronized**. It is not-thread safe and can't be shared between many threads without proper synchronization code.|Hashtable is **synchronized**. It is thread-safe and can be shared with many threads.|
| 02. |HashMap allows one null key and multiple null values.|Hashtable doesn't allow any null key or value.|
| 03. |HashMap is a new class introduced in JDK 1.2.|Hashtable is a legacy class.|
| 04. |HashMap is fast.       |Hashtable is slow.|
| 05. |We can make the HashMap as synchronized by calling this code Map m = Collections.synchronizedMap(hashMap);|Hashtable is internally synchronized and can't be unsynchronized.|
| 06. |HashMap is traversed by Iterator.	|Hashtable is traversed by Enumerator and Iterator.|
| 07. |Iterator in HashMap is fail-fast.	|Enumerator in Hashtable is not fail-fast.         |
| 08. |HashMap inherits AbstractMap class.	|Hashtable inherits Dictionary class.              |

</blockquote>
</details>

---

49. What is Comparable and Comparator Interface in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Comparable and Comparator both are interfaces and can be used to sort collection elements.

|Comparable	                |Comparator                                                                                |
|---------------------------|------------------------------------------------------------------------------------------|
|1) Comparable provides a single sorting sequence. In other words, we can sort the collection on the basis of a single element such as id, name, and price. |The Comparator provides multiple sorting sequences. In other words, we can sort the collection on the basis of multiple elements such as id, name, and price etc.|
|2) Comparable affects the original class, i.e., the actual class is modified.|Comparator doesn't affect the original class, i.e., the actual class is not modified.|
|3) Comparable provides compareTo() method to sort elements. | Comparator provides compare() method to sort elements.
|4) Comparable is present in java.lang package.|A Comparator is present in the java.util package.|
5) We can sort the list elements of Comparable type by Collections.sort(List) method.|We can sort the list elements of Comparator type by Collections.sort(List, Comparator) method.|

</blockquote>
</details>

---

50. Can you differentiate Vector and ArrayList?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, Vector and ArrayList are both data structures used to store and manage collections of objects in Java, but they have some differences.

*Thread Safety*: Vector is thread-safe, while ArrayList is not. This means that multiple threads can access a Vector object without causing any issues, while accessing an ArrayList from multiple threads at the same time can lead to unexpected behavior.

*Synchronization*: Vector is internally synchronized, which means that each method of Vector acquires a lock on the object before executing, while ArrayList is not synchronized. This can cause some performance overhead with Vector, especially in multi-threaded environments.

*Performance*: Since Vector is synchronized, it has additional overhead that can affect its performance. ArrayList is not synchronized, so it can perform better in scenarios where synchronization is not necessary.

*Capacity*: Both Vector and ArrayList can grow dynamically, but they differ in how they handle capacity. Vector doubles its size when it reaches its capacity, while ArrayList increases its capacity by 50% of its current capacity.

*Iterator*: Vector's iterator is designed to be fail-safe, while ArrayList's iterator is not. This means that if the underlying collection is modified while iterating through a Vector, it will not throw a `ConcurrentModificationException`, while ArrayList's iterator may throw this exception.

</blockquote>

</details>

---

51. Do you know any thread safe collections?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java provides several thread-safe collections that can be used in multi-threaded applications where multiple threads can access the same collection concurrently. Stack, Vector, Hashtable these are some of the examples of thread safe collections.

</blockquote>

</details>

---

52. Do you know about any concurrent collections?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, Java provides several concurrent collections that are designed to be thread-safe and can be used in multi-threaded environments without any issues.

ConcurrentHashMap, CopyOnWriteArrayList, ConcurrentLinkedQueue, BlockingQueue, and ConcurrentSkipListMap these are some of the examples of concurrent collections.

</blockquote>

</details>

---

53. How do you make an arraylist synchronized?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, you can make an ArrayList synchronized by using the Collections.synchronizedList() method. This method returns a synchronized (thread-safe) list backed by the specified list. Here's an example of how to create a synchronized ArrayList:

```Java
List<String> list = new ArrayList<>();
List<String> syncList = Collections.synchronizedList(list);
```

</blockquote>

</details>

---

54. What is a set?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A Set in java is an unordered collection which do no allow duplicate values to be stored in it. We can implement the Set interface using HashSet, LinkedHashSet, TreeSet. The LinkedHashSet maintains the order of elements in which they were inserted and in TreeSet the elements are stored in sorted manner. To perform operations on set we can use methods like `add()`, `remove()`, `contains()`,and `size()`.

</blockquote>

</details>

---

55. Can you differentiate ArrayList and HashMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, ArrayList and HashMap are different data structures in Java with different characteristics and use cases.

**Internal data structure**:
`ArrayList`: It is internally implemented using an array, which stores a contiguous block of elements.
`HashMap`: It is internally implemented using an array of linked lists, called buckets. Each bucket stores a key-value pair.

**Order of elements**:
`ArrayList`: It maintains the insertion order of elements. The position of an element is determined by the index at which it was inserted.
`HashMap`: It does not maintain the order of elements. The order in which the key-value pairs are stored is not guaranteed.

**Accessing elements**:
`ArrayList`: Elements can be accessed by their index using the get() method. The time complexity for accessing an element is O(1).
`HashMap`: Elements are accessed using their key using the get() method. The time complexity for accessing an element is O(1) on average, but can be O(n) in the worst case when there are many collisions in the bucket.

**Duplicates**:

`ArrayList`: It allows duplicate elements to be stored.
`HashMap`: It allows duplicate values, but not duplicate keys.

**Use cases**:

`ArrayList`: It is useful when you need to store and retrieve elements based on their index, and when the order of elements is important.
`HashMap`: It is useful when you need to store and retrieve key-value pairs, and when the order of elements is not important.

</blockquote>

</details>

---

56. What is the difference between HashMap and TreeMap in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The main difference between HashMap and TreeMap in Java is the way they store and order their elements:

HashMap is implemented using a hash table and is unordered.
TreeMap is implemented using a red-black tree and is ordered based on the natural order of its keys, or based on a custom comparator if provided.

Other differences between HashMap and TreeMap include:

`Performance`: HashMap generally has better performance for most operations due to its constant-time (O(1)) complexity for most operations. TreeMap has a logarithmic-time (O(log n)) complexity for many operations due to its use of a balanced tree.
`Null values`: HashMap allows null keys and values, while TreeMap does not allow null keys but allows null values.
`Memory usage`: HashMap uses less memory than TreeMap for storing the same number of elements.
`Iteration order`: HashMap does not guarantee any specific order for its elements, while TreeMap guarantees a sorted order based on the keys.

</blockquote>

</details>

---

57. What is Concurrent HashMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ConcurrentHashMap is a thread-safe implementation of the Map interface provided by Java's standard library. It allows multiple threads to access and modify the map concurrently without the need for external synchronization.

ConcurrentHashMap achieves thread-safety by dividing the map into several segments, each of which can be locked independently for read and write operations. This allows multiple threads to access different segments of the map simultaneously without blocking each other.

</blockquote>

</details>

---

58. Name any two items in the collections API and when would you use them?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

*ArrayList* - It is an implementation of the List interface and is used to store a dynamic list of objects of a specific type. It allows elements to be added or removed from the list, and provides methods to access elements by index or search for elements in the list. It is useful when you need a dynamic and resizable list of elements, and when you need fast access to elements by index.

*HashMap* - It is an implementation of the Map interface and is used to store key-value pairs. It allows keys to be mapped to values, and provides methods to add, remove, and retrieve elements based on their keys. It is useful when you need to map keys to values and perform operations on the values based on their keys. It provides fast access to elements based on their keys and is commonly used to implement caches and lookup tables.

</blockquote>

</details>

---

59. What is the difference between List and Map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A List is used to store a collection of elements in a specific order that can be accessed by their index position, while a Map is used to store a collection of key-value pairs where each key maps to a specific value.

</blockquote>

</details>

---

60. What is the difference between List and Set?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In short, a List is an ordered collection that can contain duplicate elements, while a Set is an unordered collection that cannot contain duplicate elements. In other words, elements in a List are accessed by their index position, and elements in a Set are accessed via their value.

</blockquote>

</details>

---

61. What is the difference between Array and LinkedList ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An array is a collection of elements stored in contiguous memory locations, where elements can be accessed using their index, while a linked list is a collection of elements (called nodes) where each node points to the next node using a reference, and elements are accessed sequentially by following the node references. The main difference is that arrays have a fixed size, while linked lists can grow or shrink dynamically. Also, insertion and deletion operations can be faster in a linked list because it requires only changing a few references, whereas in an array, these operations may require moving many elements to maintain order.

</blockquote>

</details>

---

62. What is HashTable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HashTable is a data structure that maps keys to their associated values using a hash function. It provides constant-time performance for basic operations such as get and put, making it a popular choice for implementing associative arrays, caches, and databases. In a HashTable, keys are hashed to an index in an array, and the associated value is stored at that index. In case of collisions, where two keys hash to the same index, the HashTable uses a collision resolution technique to store and retrieve the values correctly.

</blockquote>

</details>

---

63. How does a HashMap Work?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HashMap works by using a hash function to map keys to an index in an array, where the associated value is stored. When a key-value pair is inserted, the hash function is applied to the key to determine the index in the array where the value should be stored. If another key maps to the same index, a collision occurs. To handle collisions, the HashMap uses a linked list or a balanced tree data structure to store multiple key-value pairs at the same index. When a value is retrieved, the hash function is applied to the key to determine the index in the array, and the list or tree at that index is searched for the key.

</blockquote>

</details>

---

64. How would you get a sorted Hashmap?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, a HashMap is an unordered collection, so there is no inherent sorting order. However, you can get a sorted view of a HashMap by converting it to a TreeMap.

A TreeMap is a sorted collection that maintains its entries in a sorted order based on the natural ordering of its keys or a custom ordering specified by a Comparator. You can create a TreeMap from a HashMap by passing the HashMap to the TreeMap constructor. For example:

```Java
HashMap<Integer, String> hashMap = new HashMap<>();
// add entries to the hashMap

// create a sorted view of the hashMap
TreeMap<Integer, String> sortedMap = new TreeMap<>(hashMap);
```

</blockquote>

</details>

---

65. Is the insertion time slow (or fast) when using a LinkedList? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Insertion time is generally considered to be fast in a linked list as compared to an array, especially when inserting elements at the beginning or end of the list. This is because a linked list stores its elements in separate nodes that are linked to each other through pointers, so adding or removing elements involves simply updating pointers. However, searching for an element in a linked list can be slower than in an array, as it requires traversing the list sequentially until the element is found.

</blockquote>

</details>

---

66. How do Map works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A Map is an interface in Java that stores key-value pairs. It works by associating keys with values and allowing the retrieval of values based on their corresponding keys. When an entry is added to a map, it is stored as a key-value pair, and the key is used to retrieve the corresponding value. In order to retrieve a value from a map, you provide the key associated with that value, and the map returns the value that was associated with that key. Maps can have duplicate values but not duplicate keys, and they can be implemented using various data structures such as hash tables, trees, or linked lists.

</blockquote>

</details>

---

67. What is a Linked List and best used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A linked list is a data structure consisting of a sequence of nodes, where each node contains a value and a reference (or pointer) to the next node in the sequence.

Linked lists are best used when we need to frequently insert or delete elements in the middle of the list, as adding or removing elements in a linked list is faster than in an array or array list.

</blockquote>

</details>

---

68. What is Array List and best used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ArrayList is best used when we need a resizable array that can grow dynamically. We can add or remove elements from the ArrayList easily, and it automatically resizes the array if needed. ArrayList is also faster than LinkedList for random access, but slower for inserting or deleting elements in the middle of the list. Hence, it is best used when we need frequent random access to elements in the list and fewer insertions or deletions.

</blockquote>

</details>

---

69. Why should we use Map over Set/List?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Maps are used over sets/lists when there is a need to store data as key-value pairs, where keys are unique identifiers and values are associated data. Maps provide fast access to values based on their keys, which makes them ideal for applications such as caching, database indexing, and lookups.

</blockquote>

</details>

---

70. What is the time complexity of Map and List?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The time complexity of Map and List operations depends on the specific implementation of the Map or List data structure.

In general, Map operations have a time complexity of O(1) for average case insertion, deletion, and retrieval using a hash table implementation such as HashMap or ConcurrentHashMap. However, some operations like iterating over a Map can have a time complexity of O(n) where n is the number of entries in the Map.

List operations have a time complexity of O(1) for accessing elements by index using an ArrayList, but O(n) for inserting or deleting elements in the middle of the list as all subsequent elements need to be shifted. LinkedList, on the other hand, has O(1) time complexity for insertion or deletion at any position, but O(n) time complexity for accessing elements by index.

</blockquote>

</details>

---

71. When to use TreeMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can consider using TreeMap when you need to maintain a collection of key-value pairs in sorted order based on the keys. This can be helpful for tasks such as range queries, finding the next or previous key in the sorted order, or performing operations such as ceilingEntry, floorEntry, or subMap that are specific to the TreeMap implementation.

</blockquote>

</details>

---

72. How do you define an arraylist?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An ArrayList can be defined in short by specifying the data type it will contain within angled brackets <>, followed by the variable name and the new keyword. For example, to define an ArrayList of integers named myList, you would write:

```java

ArrayList<Integer> myList = new ArrayList<Integer>();

```

</blockquote>

</details>

---

73. What is Hashing ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Hashing is a process of converting a large amount of data into a small, fixed-size value that represents the original data in a unique way. This small value, known as a hash or hash code, is generated using a hashing algorithm that takes the input data and produces a fixed-size output. 

</blockquote>

</details>

---

74. What is stack? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A stack is an abstract data type that represents a collection of elements, where elements can be added and removed only from the top. It follows the Last-In-First-Out (LIFO) principle, which means that the last element added to the stack will be the first one to be removed. Stacks can be implemented using an array or a linked list.

</blockquote>

</details>

---

75. What is hashcode() in Java collection framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In the Java Collections framework, the `hashCode()` method is defined in the Object class and is used to generate a hash code value for an object. The hash code is an integer value that represents the object's state.


</blockquote>

</details>

---

76. Can a HashMap have null or blank values?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, a HashMap can have null values and null keys. In fact, the put method of the HashMap class allows null values to be inserted as key-value pairs. Here's an example:

```Java
HashMap<String, Integer> map = new HashMap<>();
map.put("one", null);
map.put(null, 2);
```

</blockquote>

</details>

---

77. What is the difference between an ArrayList and a List? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, ArrayList is a class that implements the List interface. So, List is an interface while ArrayList is a concrete implementation of the List interface.

The main difference between ArrayList and List is that ArrayList is a resizable array, meaning that its size can be dynamically changed during runtime, while List is just an interface that defines certain operations that a collection of elements should support, such as adding, removing, and accessing elements by index.

</blockquote>

</details>

---

78. What is a Map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>


In Java, a Map is a collection interface that stores a set of key-value pairs, where each key is unique. It provides methods for adding, removing, and retrieving elements based on their keys. The most commonly used classes that implement the Map interface are HashMap, TreeMap, and LinkedHashMap.

</blockquote>

</details>

---

79. What other classes besides ArrayList?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are many other classes besides ArrayList in the Java Collections Framework. Some of the commonly used ones are:

- LinkedList
- HashSet
- TreeSet
- HashMap
- TreeMap
- PriorityQueue
- ConcurrentHashMap
- ArrayDeque
- EnumSet
- LinkedHashMap

</blockquote>

</details>

---

80. Does vector implements interface List ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, Vector implements the List interface in Java.

</blockquote>

</details>

---

81. What is the difference between Map and hashMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Map is a generic interface that represents a mapping between keys and values. It defines the basic operations such as put, get, containsKey, and containsValue for accessing and manipulating the elements of the mapping.

HashMap is a specific implementation of the Map interface in Java. It uses a hash table to store the key-value pairs, allowing for fast access and retrieval of the elements. HashMap is an unordered collection and does not guarantee any particular order of the elements.

</blockquote>

</details>

---

82. How do you initialize an arraylist?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To initialize an ArrayList in Java, you can create an instance of the ArrayList class and use the add() method to add elements to it. Here's an example:

```Java

ArrayList<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
list.add("orange"); 
```
</blockquote>

</details>

---

83. What collection would you use to store an entire JSon Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, you could use a Map collection to store an entire JSON object. The keys of the map would correspond to the property names of the JSON object, and the values of the map would correspond to the values of the properties. You could use a HashMap, TreeMap, or other implementations of the Map interface depending on your specific use case

</blockquote>

</details>

---

84. With an array of numbers, how do you display only the duplicates?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To display only the duplicates in an array of numbers, we can use a combination of loops and conditional statements to compare each element in the array to every other element in the array, and print out the duplicate elements. Here's an example code snippet in Java:

```Java
int[] numbers = {1, 2, 3, 2, 4, 5, 3};
for(int i=0; i<numbers.length; i++) {
   for(int j=i+1; j<numbers.length; j++) {
      if(numbers[i] == numbers[j]) {
         System.out.println(numbers[i]);
         break;
      }
   }
}
```

</blockquote>

</details>

---
