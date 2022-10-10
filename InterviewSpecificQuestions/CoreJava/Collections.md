## Technical

1. What does the Collections framework in Java contain?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).

</blockquote>
</details>

---

2. Can you tell the main interfaces, and what are the differences between them?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Set, List and Map are three important interfaces of the Java collection framework.
- A List can be used when the insertion order of elements needs to be maintained.
- We can use a set if we need to maintain a collection that contains no duplicates.
- And Map when data is key-value pairs and need fast retrieval of value based on some key.

</blockquote>
</details>

---

3. Why is Map not inherited from the Collection interface, despite the fact that it is a component of the Java collection framework? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Because they are of an incompatible type. List, Set and Queue are a collection of similar kind of objects but just values where a Map is a collection of key and value pairs.

</blockquote>
</details>

---

4. How do you remove an entry from a collection? And subsequently, what is the difference between the `remove()` method of a collection and the `remove()` method of an iterator? Which one will you use while removing elements during iteration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Collection interface defines `remove(Object obj)` method to remove objects from `Collection.List` interface adds another method `remove(int index)`, which is used to remove objects at a specific index.
- You can use any of these methods to remove an entry from Collection, while not iterating. 
- Things change when you iterate. Suppose you are traversing a List and removing only certain elements based on logic, then you need to use Iterator's `remove()` method. 
-This method removes the current element from Iterator's perspective. If you use Collection's or List's `remove()` method during iteration then your code will throw `ConcurrentModificationException`. 
- That's why it's advised to use the iterator `remove()` method to remove objects from Collection.

</blockquote>
</details>

---

5. How does HashSet use Hashing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HashSet extends `AbstractSet` and implements the Set interface. It creates a collection that uses a hash table for storage. A hash table stores information by using a mechanism called hashing. In hashing, the informational content of a key is used to determine a unique value, called its hash code.

</blockquote>
</details>

---

6. How is HashSet implemented in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

When we create an object of HashSet, it internally creates an instance of HashMap with default initial capacity 16. HashSet uses a constructor `HashSet(int capacity)` that represents how many elements can be stored in the HashSet. The capacity may increase automatically when more elements to be store.

</blockquote>
</details>

---

7. Which one do you prefer in Java between Array and Array Lists for storing objects and why?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Though ArrayList is also backed up by array, it offers some usability advantage over array in Java.Array is fixed length data structure, once created you can not change it's length. On the other hand,ArrayList is dynamic, it automatically allocate a new array and copies content of old array, when it resize.Another reason of using ArrayList over Array is support of Generics.

</blockquote>
</details>

---

8. How does LinkedList is implemented in Java, is it a Singly or Doubly linked list?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Java LinkedList:
    - It is an implementation of the List and Deque interfaces. Internally, it is an implemented using Doubly Linked List Data Structure. It supports duplicate elements. 
    - It stores or maintains it's elements in Insertion order. 

</blockquote>
</details>

---

9. Does Collection and Collections are same in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, Collection is a top level interface of Java collection framework where as Collections is an utility class. Below table shows the difference between them.

- Collection:	
    - Collection is a root level interface of the Java Collection Framework. 
    - Most of the classes in Java Collection Framework inherit from this interface.	
    - List, Set and Queue are main sub interfaces of this interface.	

- Collections:
    - Collections is an utility class in java.util package. 
    - It consists of only static methods which are used to operate on objects of type Collection.
    -  `Collections.max()`, `Collections.min()`, `Collections.sort()` are some methods of Collections class.

</blockquote>
</details>

---

10. What classes should i prefer to use a key in HashMap in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We should prefer String, Integer, Long, Double, Float, Short and any other wrapper class. Reason behind using them as a key is that they override `equals()` and `hashCode()` method, we need not to write any explicit code for overriding `equals()` and `hashCode()` method in java.

</blockquote>
</details>

---

11.  Suppose there is an Student class. We add Student class objects to the ArrayList. Mention the steps that need to be taken if I want to sort the objects in ArrayList using the studentId attribute present in Student class. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Implement the Comparable interface for the Employee class and now to compare the objects by studentId we will override the `std1.compareTo(std2)` .
- We will now call Collections class `sort()` method and pass the list as an argument, that is,
`Collections.sort(stdList)`

</blockquote>
</details>

---

12. What is the sorting algorithm used in `Collections.sort()`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`Collections.sort()` uses Merge sort algorithm to sort the objects.

</blockquote>
</details>

---

13. What will happen if we put two values ​​with the same key in Map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If we try to insert two values for the same key, the second value will be stored, while the first one will be dropped.

</blockquote>
</details>

---

14. How to create a Thread-Safe `ConcurrentHashSet` in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

JDK 8 has the newly added `keySet()` (the default) and `newKeySet()` methods to create a ConcurrentHashSet in Java that is supported by `ConcurrentHashMap`

</blockquote>
</details>

---

15. Can an ArrayList contain mutiple references to the same object in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The ArrayList in java does not provide the checks for duplicate references to the same object. Therefore, we can insert the same object or reference to a single object as many times as we want.

</blockquote>
</details>

---

16. If the frequent operation is retrieval which collection is used and if the frequent operation is insertion or deletion which one is used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If the frequent operation is retrieval the ArrayList for the othercase LinkedList.

</blockquote>
</details>

---

17. How iterator and enumerator differs while iterating the elements in the collection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Enumeration is twice as fast as Iterator and uses less memory. Iterator is thread-safe because does not allow other threads to modify the collection when iterating.
- Enumeration can only be used for read-only collections. It also has no `remove()` method ;
- Enumeration:  `hasMoreElement()` ,  `nextElement ()`
- Iterator:  `hasNext()` ,  `next()` ,  `remove()`

</blockquote>
</details>

---


18. Can we use null element in TreeSet? Give reason?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, TreeSet does not allows to store any null keys. Any attempt to add null throws `runtimeException (NullPointerException)`.
- TreeSet internally compares elements for sorting elements by natural order (comparator may be used for sorting, if defined at creation time) and null is not comparable, Any attempt to compare null with other object will throw `NullPointerException`.

</blockquote>
</details>

---

19. What will be the output of the given snippet?

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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
	
**Output**

a infinite times

</blockquote>

<blockquote>

<details> <summary> <b> Explanation </b> </summary>

ArrayList provides listIterator for traversing in forward and backward direction, so program will compile and run infinitely.

</details>

</details>

---

20.If we want to use a custom object as a key in Collection classes like Map or Set, how can we achieve that?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- If you are using any custom object in Map as key, you need to override `equals()` and `hashCode()` method, 
and make sure they follow their contract. On the other hand if you are storing a custom object in Sorted Collection 
- e.g. SortedSet or SortedMap, you also need to make sure that your `equals()` method is consistent to `compareTo()` method, otherwise that collection will not follow there contacts e.g. Set may allow duplicates.

</blockquote>
</details>

---


21. Do you know what is BlockingQueue? Give a practical example of BlockingQueue?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- BlockingQueue is a java Queue that support operations that wait for the queue to become non-empty when retrieving and removing an element, and wait for space to become available in the queue when adding an element.
- Producer-consumer problem is a best example of BlockingQueue.

</blockquote>
</details>

---

22.  What is the difference between fail-safe and fail-fast properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Fail-fast Iterators throw `ConcurrentModificationException` when one thread is iterating over collection object and other thread structurally modify Collection either by adding, removing, or modifying objects on the underlying collection. 
- They are called fail-fast because they try to immediately throw Exception when they encounter failure. - On the other hand, fail-safe Iterators works on copy of collection instead of the original collection

</blockquote>
</details>

---

23. Which Collection type do you suggest me If I want a sorted collection of objects with no duplicates?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TreeSet is the best suitable for such scenarios where you want a collection of objects with no duplicates and also sorted based on a particular data field.

</blockquote>
</details>

---

24. Why is it recommended not to use the Vector class in our code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Vector class is preferred over ArrayList class when you are developing a multi threaded application. 
But, precautions need to be taken because vector may reduce the performance of your application as it is 
thread safe and only one thread is allowed to have object lock at any moment of time and remaining threads have to wait until a thread releases the object lock. So, it is always recommended that if you don’t need thread safe environment, it is better to use ArrayList class than the Vector class.And also Vector class is often considered as obsolete or “Due for Deprecation” by many experienced Java developers. They always recommend and advise not to use Vector class in your code. They prefer using ArrayList over Vector class.

</blockquote>
</details>

---

25. How to sort ArrayList in descending order?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can use `reverseorder()` like `Collections.sort(arraylist, Collections.reverseOrder())`;  

</blockquote>
</details>

---

26. Predict the output?

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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Output**
	
2 5 12 15 23 25

</blockquote>


<details> <summary> <b> Explanation </b> </summary>
<blockquote>

Priority queue always outputs the minimum element from the queue when `remove()` method is called, no matter what the sequence of input is.

</blockquote>
</details>
</details>
	
---

27. Arrange the following in the ascending order (performance):
HashMap, Hashtable, ConcurrentHashMap, and Collections.SynchronizedMap 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Hashtable  <  Collections.SynchronizedMap  <  ConcurrentHashMap  <  HashMap

</blockquote>
</details>

---

28. Can you pass `List(String)` to a method which accepts `List(Object)`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- List(Object) can store any any thing including String, Integer etc but List(String) can only store Strings.
- List(Object) objectList;
- List(String) stringList;
- objectList = stringList; **compilation error**

</blockquote>
</details>

---

29. If the compiler erases all type parameters at compile time, why should you use generics?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The reason to use generics is,the Java compiler enforces tighter type checks on generic code at compile time.
- Generics support programming types as parameters.
- Generics enable us to implement generic algorithms

</blockquote>
</details>

---

30. Why is String a popular Hashmap key in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Since String is immutable, its hashcode is cached at the time of creation and it doesn’t need to be calculated again. This makes it a great candidate for key in a Map and it’s processing is fast than other HashMap key objects. This is why String is mostly used Object as HashMap keys.

</blockquote>
</details>

---

31. How will you create a Readonly List, Set, Map in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can use `Collections.unModifiableList()` method to create read-only List,`Collections.unmodifiableSe()`for creating read-only Set like read-only HashSet and similarly creating a read-only Map in Java.

</blockquote>
</details>

---

32. When to use Queues and stack? What is the possible use case?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Stack and Queue work on the principal of First in Last Out and First in First out. The best use case of Queue is in the messaging services, where we implement the messaging container, which allows one message to get input and another message get output from the queue.
- The queue has the ability to also act as a buffer to store the elements for the temporary time.
- Whereas Stack best use is to perform prefix, postfix and infix operation in the Tree.

</blockquote>
</details>

---

33. What is the purpose of the initial capacity and load factor parameters of a HashMap? What are
their default values? How is the threshold plays the role to decide the size?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Initial capacity in HashMap plays a vital role in the allocation of memory as we know that HashMap works on the key-value pair, that means the HashMap needed a large amount of memory to maintain the key and value, to overcome these challenges the HashMap works on the principal to allocate the optimum size, whenever the HashMap get instantiated, that is called Initial capacity, which is usually a 16.

Now let’s focus on load factor, so there is a concept of threshold value, which is always a 0.75 size of the total capacity, the significance of this is whenever any new record gets inserted in the HashMap, the HashMap computes the allocated size of the HashMap, then it checks whether this size reaches the threshold value then HashMap increased the size of 75% from the current size to augmented the storage for next incoming record.

</blockquote>
</details>

---

34. What is collision problem ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The collision problem is, whenever the hash function returns the same index position for the different key, then a collision occurs. The collision detection technique is also called collision detection.

</blockquote>
</details>

---

35. Can i add a null element to HashSet and TreeSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- We can’t add any null element in TreeSet as it uses NavigableMap for element storage. But we can add just one to HashSet.
- SortedMap doesn’t allow null keys and NavigableMap is its subset.
- That’s why we can’t add a null element to TreeSet, it will come up with the `NullPointerException`
 every time you try to do that.

</blockquote>
</details>

---

36. How will you remove the duplicates from the ArrayList?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are two ways to remove duplicates from the ArrayList.

- **Using HashSet**: By using HashSet we can remove the duplicate element from the ArrayList, but it will not then preserve the insertion order.
- **Using LinkedHashSet**: We can also maintain the insertion order by using LinkedHashSet instead of HashSet.

</blockquote>
</details>

---

37. Can you use iterateor interface over map?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- No, Map does not implement Iterable interface, only Collection ( thus , list and set ) do , so the Collection implements iterable \<E\> , make the set and the list iteratble.
- The Map can't be iterable only the key part can be iterable 

</blockquote>
</details>

---

38. Predict the output?
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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

39.  Predict the output?
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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

40. Predict the output?
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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

41. Predict the output?
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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

42. Which methods you need to override to use any object as a key in HashMap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To use any object as a key in HashMap, it needs to implement `equals()` and `hashCode()` method.


</blockquote>
</details>

---


43. What is and when to use `Collections.emptySet()` . What is the advantage of having emptySet in Collections class ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`Collections.emptySet()` returns the empty immutable Set ,not containing null  .

</blockquote>
</details>

---

44. Why we call `emptySet()` method,as we can also create empty Set  using constructor ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Advantages of using `emptySet()` method over creating object using constructor are :

1. Immutable : You should prefer to use immutable collection against the mutable collections wherever possible . It becomes handy as multiple threads accessing the same instance of object will see the same values.

2. Concise :  You do not need to manually type out the generic type of the collection - normally it is inferred from the context of the method call.


3. Efficient : As `emptySet()` method dont create new objects , so they just reuse the  existing empty and immutable object . Although ,practically,this trick is not that handy , and rarely improves the performance

</blockquote>
</details>

---

45.  What copy technique internally used by HashSet `clone()` method ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- There are two copy techniques in every object oriented programming lanuage , 
deep copy and shallow copy.
- To create a clone or copy of the Set object, HashSet  internally uses shallow copy 
in `clone()` method , the elements themselves are not cloned . 
- In other words , a shallow copy is made by copying the reference of the object.

</blockquote>
</details>

---

46. What is a good way to sort the Collection objects in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A good way to sort Java collection objects is using Comparable and Comparator interfaces. A developer can use `Collections.sort()`, the elements are sorted based on the order mention in `compareTo()`.
- When a developer uses Collections, `sort (Comparator)`, it sorts the objects depend on `compare()` of the Comparator interface.

</blockquote>
</details>

---

47. What are Generics in Java ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Java Generics is a set of related methods or a set of similar types. Generics allow types Integer, String, or even user-defined types to be passed as a parameter to classes, methods, or interfaces. Generics are mostly used by classes like HashSet or HashMap.

</blockquote>
</details>

---

48. What is Collection API ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Collection API is a set of classes and interfaces that support operation on collections of objects. These classes and interfaces are more flexible, more powerful, and more regular than the vectors, arrays, and hashtables if effectively replaces. Example of classes: HashSet, HashMap, ArrayList, LinkedList, TreeSet and TreeMap. Example of interfaces: Collection, Set, List and Map.

</blockquote>
</details>

---

49. What is the difference between hashMap and hashSet in Java ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**HashSet:-**

- HashSet class implements the Set interface
- In HashSet, we store objects(elements or values) e.g. If we have a HashSet of string elements then it could depict a set of HashSet elements: {“Hello”, “Hi”, “Bye”, “Run”}
- HashSet does not allow duplicate elements that mean you can not store duplicate values in HashSet.
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

50. What is the difference between HashSet and TreeSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- HashSet gives better performance (faster) than TreeSet for the operations like add, remove, contains, size etc. HashSet offers constant time cost while TreeSet offers log(n) time cost for such operations.

- HashSet does not maintain any order of elements while TreeSet elements are sorted in ascending order by default.

</blockquote>
</details>

---

51. What is difference between ArrayList and LinkedList?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ArrayList and LinkedList both implements List interface and maintains insertion order. Both are non synchronized classes.

|Sl.No |ArrayList               |LinkedList                                                                 |
|------|------------------------|--------------------------------------------------------------------------|
|  01. |ArrayList internally uses a dynamic array to store the elements.|LinkedList internally uses a doubly linked list to store the elements.|
| 02. |Manipulation with ArrayList is slow because it internally uses an array. If any element is removed from the array, all the bits are shifted in memory.	|Manipulation with LinkedList is faster than ArrayList because it uses a doubly linked list, so no bit shifting is required in memory.|
| 03. |An ArrayList class can act as a list only because it implements List only.|	LinkedList class can act as a list and queue both because it implements List and Deque interfaces.|
| 04. | ArrayList is better for storing and accessing data.|LinkedList is better for manipulating data.|

</blockquote>
</details>

---

52. What is difference between HashMap and Hashtable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

53. What is Comparable and Comparator Interface in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
