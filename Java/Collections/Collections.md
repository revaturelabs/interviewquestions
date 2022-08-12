 ## Technical
 
 1. What is the collection framework? 

<details>
  <summary><b>Show answer</b></summary>
 
 > Collection is a container or object that combines multiple elements into a single unit. Collections are used to store retrieve and manipulate data.
 > Collection framework is an architecture for collections and every collection framework has Interface, implementation for the interface and the algorithms( searching and sorting etc.)
  
</details>

---

2. What are the benefits of the collection framework? 

<details>
  <summary><b>Show answer</b></summary>
  
> Collection framework contains implementations for all the data structures, so the hectic task of creating and implementing everything is avoided.

> All the classes in the Collection Framework are optimized. So the programmer utilizes the optimized data structure classes.

> There are predefined methods for all Interfaces and the Collection class has some built-in methods like `sort()`, `shuffle()` etc.
  
</details>

---

3. What is Iterable Interface?

<details>
<summary><b>Show Answer</b></summary>

>- All the classes under the collection framework implement an Iterable interface.
> - Any class that implements an Iterable interface can be traversed using for each Construct. 

</details>

---

## Problem Solving


4. Write a program to traverse any collection using for each Construct.


<details>
<summary><b>Show Answer</b></summary>

``` java

import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> al = new ArrayList<>();
        al.add(1);
        al.add(13);
        al.add(2);
        al.add(0);
        for( Integer i: al)
        {
            System.out.println(i);
        }
    }
}

```



<details>
<summary><b>Explanation</b></summary>

<blockquote>

- for each loop uses list iterator internally
- for each loop can be used to only iterate over a loop but not modify the Collection.

</blockquote>


</details>


</details>
 
 ---

5. Write a program to traverse any collection using an iterator.


<details>
<summary><b>Show Answer</b></summary>

``` java

import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> al = new ArrayList<>();
        al.add(1);
        al.add(13);
        al.add(2);
        al.add(0);
        Iterator i = al.iterator();
        while(i.hasNext())
        {
            System.out.println(i.next());
        }
    }
}

```

<details>
<summary><b>Explanation</b></summary>

<blockquote>

- An Iterator is an object that is used to traverse through a collection and to remove elements from the collection based on a condition.
- `hasNext()` returns true if collection has the next element and false if empty. `next()` returns the next elemnent int the iteration.

</blockquote>


</details>


</details>
 
 ---

6. Write a program to traverse any collection using aggregate operations.

<details>
<summary><b>Show Answer</b></summary>

``` java

import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> al = new ArrayList<>();
        al.add(1);
        al.add(13);
        al.add(2);
        al.add(0);
        al.stream().forEach(e-> System.out.println(e));

    }
}

```

<details>
<summary><b>Show Answer</b></summary>

<blockquote>

- `ArrayList` is converted to a stream and `forEach()` method is used to iterate over the `ArrayList`

</blockquote>

</details>
</details>
 
 ---


7. What is the difference between the Comparable and Comparator interface?

<details>
<summary><b>Show Answer</b></summary>

**Comparable**: A comparable object is capable of comparing itself with another object. The class itself must implement the `java.lang.Comparable` interface to be able to compare its instances.

**Comparator**: A comparator object is capable of comparing two different objects. The class is not comparing its instances, but some other classes' instances. This comparator class must implement the `java.util.Comparator` interface.

Comparable and Comparator both are interfaces and can be used to sort collection elements.

| Sl.No|Comparable           |Comparator                                                |
|------|-----------------------|----------------------------------------------------------|
| 01.|Comparable provides a single sorting sequence. In other words, we can sort the collection based on a single element such as id, name, and price.|The Comparator provides multiple sorting sequences. In other words, we can sort the collection based on multiple elements such as id, name, price etc.|
| 02.|Comparable affects the original class, i.e., the actual class is modified.|Comparator doesn't affect the original class, i.e., the actual class is not modified.|
| 03.|Comparable provides compareTo() method to sort elements.| Comparator provides compare() method to sort elements.|
| 04.|Comparable is present in java.lang package.|A Comparator is present in java.util package.|
| 05.|We can sort the list elements of Comparable type by Collections.sort(List) method.|We can sort the list elements of Comparator type by Collections.sort(List, Comparator) method.|
 

</details>
 
 ---

8. What are concurrent collection classes?

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
The concurrent collection APIs of Java provides a range of classes that are specifically designed to deal with concurrent operations. These classes are alternatives to the Java Collection Framework and provide similar functionality except with the additional support of concurrency.

**Java Concurrent Collection Classes**  

* BlockingQueue  
* ArrayBlockingQueue 
* SynchronousQueue 
* PriorityBlockingQueue 
* LinkedBlockingQueue 
* DelayQueue 
* BlockingDeque 
* LinkedBlockingDeque 
* TransferQueue 
* LinkedTransferQueue 
* ConcurrentMap 
* ConcurrentHashMap 
* ConcurrentNavigableMap 
* ConcurrentSkipListMap

</blockquote>

</details>
 
 ---

9. What is the difference between the Enumeration and Iterator interface?

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Enumeration and Iterator are two interfaces in java.util package which is used to traverse over the elements of a Collection object.

**Differences**  

|Iterator |Enumeration         |
|-----------|--------------------|
|hasNext()  |hasMoreElements()   |
|next()     |nextElement()       |
|remove() |(Not Available)     |


| Sl.No |Enumeration               |Iterator                          |
|-------|----------------------------|----------------------------------|
| 01.  |Using Enumeration, you can only traverse the collection. You can’t do any modifications to the collection while traversing it.    |Using an Iterator, you can remove an element of the collection while traversing it.|
| 02.  |Enumeration is introduced in JDK 1.0| Iterator is introduced from JDK 1.2     |
| 03.  |Enumeration is used to traverse the legacy classes like Vector, Stack and HashTable.|Iterator is used to iterate most of the classes in the collection framework like ArrayList, HashSet, HashMap, LinkedList etc.|
| 04.  |Methods : hasMoreElements() and nextElement()|  Methods : hasNext(), next() and remove()|
| 05.  |Enumeration is fail-safe in nature. |Iterator is fail-fast in nature.|
| 06.  |Enumeration is not safe and secured due to its fail-safe nature.|  Iterator is safer and secured than Enumeration.|

</blockquote>
</details>

## Problem Solving

1. What are AA, BB, and CC in the following code that satisfies the following conditions?

- AA: to sort the elements of the list
- BB: to arrange elements in random order.
- CC: to inverse the order of elements.

```  java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> al = new ArrayList<>();
        al.add(1);
        al.add(13);
        al.add(2);
        al.add(0);
        al.stream().forEach(e-> System.out.println(e));
        Collections.AA(al);
        Collections.BB(al);
        Collections.CC(al);

    }
}

```

<details>
<summary><b>Show Answer</b></summary>

<blockquote>

- AA: `sort(Collection)`
- BB: `shuffle(Collection)`
- CC: `reverse(Collection)`

</blockquote>


</details>





