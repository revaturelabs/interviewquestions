1. What is the `Set` Interface and list out the classes that implements it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

 > Set Interface is used to store unique elements of the same type.
 > Classes that implements `Set` interface.
 > 1. `HashSet`
 > 2. `LinkedHashSet`
 > 3. `TreeSet`


</details>

---

2. List out basic operations of the `Set` Interface.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

> Set Inherits all the methods of Collection Interface and other than that there are no special methods for Set Interface.
> `add(element)`, `addAll()`, `remove()`, `clear()`, `contains()`, `retainAll()`, `removeAll()`. 

</details>

---

3. What is `HashSet`? Explain the internal working of `HashSet`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

<blockquote>

 - `HashSet` stores, elements without retaining the order of elements.
 - Internally `HashSet` works as a `HashTable`.
 - `HashTable`: A class that has key and values, it coverts the keys into hashcode and stores them as the idexes of an array.
</blockquote>


</details>

---
4. What is `LinkedHashSet`? Explain the internal working of `LinkedHashSet`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

<blockquote>

- `LinkedHashSet` stores, unique elements by retaining the order of elements.
- Internally ` LinkedHashSet ` is a `HashTable` and `LinkedList`.
 - `HashTable`: A class that has key and values, it coverts the keys into hashcode and stores them as the idexes of an array.
 - `LinkedList`: Linked list is a class which stores data in the form of node( data+ addresss of consecutive element) and its a part of List Interface. 


</blockquote>


</details>

---

5. What is `TreeSet`? Explain the internal working of `TreeSet`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

<blockquote>

- `TreeSet` stores, unique elements by retaining the order of elements.
- Internally ` TreeSet ` implements red-black tree.
- Red-Black tree: Red Black tree is a self balancing tree that uses recoloring and rotation to balance itself.


</blockquote>


</details>

---

6. What is the time complexity of <code>add()</code> method for a `HashSet`?

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

> HashSet Stores elements without maintaining the order, so the time complexity is constant.

</details>
</details>

---

7. What is the time complexity of <code>remove(element)</code> method for a `HashSet`?

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

> HashSet Stores elements in the form of hashcode so the elements can be directly retrieved and deleted, so the time complexity is constant.

</details>
</details>

---

8. What is the time complexity of <code>conatins()</code> method for a `HashSet`?

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

> HashSet Stores elements in the form of hashcode so the elements can be searched directly, so the time complexity is constant.

</details>
</details>

---

9.  What is `EnumSet`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

<blockquote>
Java `EnumSet` class is the special `Set` implementation for enum types. It inherits `AbstractSet` class and implements the `Set` interface.

Features

- It contains enum values that belong to the same enum.
- Null values are not allowed and "NullPointException" is thrown if it's violated.
- It is not Synchronized
 
 Enum:
 
 ``` java
 public enum Seasons{
        Summer,Winter,Spring,Autum;
    }
 
 ```
 
 `EnumSet`:
  
 ``` java
  EnumSet<Seasons> s = EnumSet.allOf(Seasons.class);
 
 ```


</blockquote>
</details>

---

10. What is `hashCode()`?
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

- `hashCode()` method generates the hashCode of two objects, if two objects are equal then the hash Code generated for two objects is the same, while the inverse may or may not be true.

</details>

---

11. What happens if `hashCode()` method is not overridden?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

<blockquote>

- If `hashCode()` method is not overridden then the default implementation of the Object class is implemented.

- The default implementation of the Object class generates different hash codes for different objects, even if they are equal according to the `equals()` method.
- `hashSet`, `hashMap` and `hashTable` use hash code to store the elements and if `hashCode()` method is not overriden it migt cause some issues.

</blockquote>


</details>

---

12. What are the differences between `HashSet` and `TreeSet`.
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

| HashSet                                                                                              | TreeSet                                                                       |
| ---------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| HashSet maintains constant time complexity (O(1)) for insertion, retrieval and searching of elements | TreeSet maintains O(log n) for insertion, retrieval and searching of elements |
| HashSet doesn’t maintain an ordered collection of elements.                                          | TreeSet maintains sorted order of elements.                                   |

</details>

13. What is the output of the following program?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



``` java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        HashSet<Integer> hs= new HashSet<>();
        hs.add(1);
        hs.add(3);
        hs.add(2);
        hs.add(-1);

        TreeSet<Integer> ts = new TreeSet<>(hs);
        LinkedHashSet<Integer> lhs = new LinkedHashSet<>(ts);

        System.out.println(hs);
        System.out.println(ts);
        System.out.println(lhs);



    }
}



```

A. <br>
   any random order<br>
   [-1,1,2,3]<br>
   [1,3,2,-1]

B. <br>
   [-1,1,2,3]<br>
   any random order<br>
   [1,3,2,-1]

C. <br>
   [-1,1,2,3]<br>
   any random order<br>
   [-1,1,2,3]

D. <br>
    any random order<br>
   [-1,1,2,3]<br>
   [-1,1,2,3]


<details>

<summary><b>Show Answer</b></summary>

>D

<details>
<summary><b>Explanation</b></summary>

<blockquote>

- `HashSet` doesn't maintain insertion order, so elements will be printed in random order.
- `TreeSet ` maintains sorted order, so the elements will be in sorted order.
- `LinkedHashSet` maintains the insertion order, but the elements of `TreeSet` are added to `LinkedHashSet`, so sorted order is printed.


</blockquote>
</details>

</details>

## Problem Solving

1. Consider there are two hash sets a and b with some elements in each, How to get the intersection of a and b?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>
<blockquote>

- `a.retainAll(b)`, transforms a into the intersection of a and b.
</blockquote>


</details>

---

2. Consider there are two hash sets a and b with some elements in each, How to get the union of a and b?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>
<blockquote>

- `a.addAll(b)`, transforms a into the union of a and b.
</blockquote>


</details>

---

3. Consider there are two hash sets a and b with some elements in each, How to check if a is a subset of b?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>
<blockquote>

- `b.containsAll(a)` returns true, if b contains all the elements of a, i.e. a is a subset of b, returns false otherwise.
</blockquote>


</details>

---

4. Consider there are two hash sets a and b with some elements in each, How to get the separate the unique elements present in a but not b?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>
<blockquote>

- `a.removeAll(b)`, transforms an into the set difference of a and b. only elements in a that are not in b are stored in a.
</blockquote>


</details>
 
 ---

5. Write a program to get the union, intersection and difference of two sets without altering the existing sets.
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

``` java

import java.util.HashSet;

public class SetOperations {
    public static void main(String[] args) {
        HashSet<Integer> a = new HashSet<>();
        HashSet<Integer> b = new HashSet<>();
        
        a.add(1);
        a.add(2);
        a.add(3);
        a.add(4);
        b.add(3);
        b.add(4);
        b.add(5);
        b.add(6);

        HashSet<Integer> union = new HashSet<>(a);
        union.addAll(b);
        HashSet<Integer> intersection = new HashSet<>(a);
        intersection.retainAll(b);
        HashSet<Integer> difference = new HashSet<>(a);
        difference.removeAll(b);

    }
}


```

- a new set is created for union, intersection and difference and all the elements of a are added to them, all the operations are performed on union, difference and intersection. So, a and b remain unchanged.

</details>



## Real-Time Application

1. Local elections are planned to occur one month from now, and there is a list with all the names of people who live in the city but some names are repeated. so prepare a unique list of people who are eligible to vote from the existing list. 
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)



<details>

<summary><b>Show Answer</b></summary>

<blockquote>

``` java
HashSet<String> voterList = new HashSet<>(names);
```
- names holds the details of all people who live in the city and the names might be repeated and voterList holds the unique list of Citizens.
</blockquote>

</details>

##  Error detection

1. Which of the following is true for the code snippet mentioned below?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



``` java
HashSet<Integer> a = new HashSet<>();
a.add(2);
a.get(0);
a.set(0,1);
a.isEmpty();

```
A. `a.get(0)` returns 2 and `a.set(0,1)` overrides 2 to 1;

B. `a.get(0)` returns 2 and `a.set(0,1)` throws an exception.

C. `a.get(0)` throws exception and `a.set(0,1)` overrides 2 to 1;

D. both `a.get(0)` and `a.set(0,1)` throw exceptions.

<details>
<summary><b>Show Answer</b></summary>

> D

<details>
<summary><b>Explanation</b></summary>

- `HashSet` stores elements in a random order without positional access, so get and set methods are not applicable for `HashSet`.

</details>


</details>
