1. What is Map Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- `Map` is an object that stores key and value pairs.
- `Map` doesn't store duplicate values and one key can have at most one value

</blockquote>

</details>

---

2. What is the difference between HashMap and Hashtable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>

<summary><b>Show Answer</b></summary>
 
<blockquote>

HashMap and Hashtable both are used to store data in key and value form. Both are using hashing technique to store unique keys.

|Sl.No|HashMap                |Hashtable                                         |
|-----|-----------------------|--------------------------------------------------|
| 01. |HashMap is **non synchronized**. It is not-thread safe and can't be shared between many threads without proper synchronization code.|Hashtable is **synchronized**. It is thread-safe and can be shared with many threads.|
| 02. |HashMap allows one null key and multiple null values.|Hashtable doesn't allow any null key or value.|
| 03. |HashMap is a new class introduced in JDK 1.2.|Hashtable is a legacy class.|
| 04. |HashMap is fast.       |Hashtable is slow.|
| 05. |HashMap is traversed by Iterator.    |Hashtable is traversed by Enumerator and Iterator.|
| 06. |HashMap<K, V> hm = new HashMap<K, V>() |Hashtable<K, V> ht = new Hashtable<K, V>()|
    
 </blockquote>

</details>

---
3. What is the difference between `HashMap` and `TreeMap`?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>

<summary><b>Show Answer</b></summary>

<blockquote>
    
The `HashMap` and `TreeMap` both are classes of the Java Collections framework. Java Map implementation usually acts as a bucketed hash table. When buckets get too large, they get transformed into nodes of TreeNodes, each structured similarly to those in java.util.TreeMap.

|HashMap                           |TreeMap                           |
|----------------------------------|----------------------------------|
| `HashMap` is a hashtable-based implementation of Map interface.|`TreeMap` is a Tree structure-based implementation of `Map` interface.|
|`HashMap` implements `Map`, Cloneable, and Serializable interface.|`TreeMap` implements NavigableMap, Cloneable, and Serializable interface.|
|`HashMap` allows a single null key and multiple null values.|`TreeMap` does not allow null keys but can have multiple null values.|
|`HashMap` allows heterogeneous elements because it does not perform sorting on keys.|`TreeMap` allows homogeneous values as a key because of sorting.|
|`HashMap` is faster than TreeMap because it provides constant-time performance that is O(1) for the basic operations like `get()` and `put()`.|`TreeMap` is slow in comparison to `HashMap` because it provides the performance of O(log(n)) for most operations like `add()`, `remove()` and `contains()`.|
|The `HashMap` class uses the `HashTable`.    |`TreeMap` internally uses a Red-Black tree, which is a self-balancing Binary Search Tree.|
|It uses the `equals()` method of the Object class to compare keys. The `equals()` method of the Map class overrides it.|It uses the `compareTo()` method to compare keys.|
|`HashMap` class contains only basic functions like `get()`, `put()`, `KeySet()`, etc. .|`TreeMap class` is rich in functionality, because it contains functions like: `tailMap()`, `firstKey()`, `lastKey()`, `pollFirstEntry()`,`pollLastEntry()`.|
|Order of elements  HashMap does not maintain any order.|The elements are sorted in natural order (ascending).|
|The HashMap should be used when we do not require key-value pair in sorted order.| The TreeMap should be used when we require key-value pair in sorted (ascending) order.|

   </blockquote>
</details>

---
4. What happens when you try to add a key-value pair to an existing key in `HashMap`?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
 
<blockquote>

- When you try to add a key-value pair to `HashMap` and the key already exists, it overrides the value.

``` java
import java.util.*;

public class ExistingKey {
    public static void main(String[] args) {
        HashMap<String,Integer> hm = new HashMap<>();
        hm.put("Java",1.5);
        System.out.println(hm.get("Java"));
        hm.put("Java",1.8);
        System.out.println(hm.get("Java"));
        
    }
}


```
- the output of the program is :
- 1.5
- 1.8 
- The value for Java is overridden from 1.5 to 1.8.



</details>
    
---
5. How to avoid overriding the existing value of a key by adding the key-value pair to the `HashMap`?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

<blockquote>
        
``` java
import java.util.*;
public class ExistingKey {
    public static void main(String[] args) {
        HashMap<String,Integer> hm = new HashMap<>();
        hm.put("Java",1.5);
        System.out.println(hm.get("Java"));
        hm.putIfAbsent("Java",1.8);
        System.out.println(hm.get("Java"));
    }
}



```

- The output of the program is :
- 1.5
- 1.5
        
</blockquote>
        
<details>
<summary><b>Explanation</b></summary>
    
> The value for Java is not overridden because `putIfAbsent()` adds key and value, only if it doesn't exist previously.

</details>
    </details>
    
  ---

6. List out the different methods to iterate over a `Map`.
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Collection view methods are used to view a `Map` as a Collection.
- They are the only means to iterate over a `Map`.
- `keySet`:  the set of keys in the `Map`.
- `values`: the Collection of values obtained from the `Map`.
- `entrySet`: the set of key-value pairs from a `Map`. 

</blockquote>
</details>

---
    
## Problem Solving

7. Create a map in which each key has multiple values.
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

<blockquote>
    
``` java

public class MultiMap {
    public static void main(String[] args) {
        Map<String, List<String >> Multimap = new HashMap<>();
        ArrayList<String> al = new ArrayList<>();
        al.add("Sheldon Cooper");
        al.add("Leslie Winkle");
        al.add("Barry Kripkie");
        Multimap.put("Theoretical Physists",al );
    }
}


```
</blockquote>
    
<details>
<summary><b>Explanation</b></summary>
<blockquote>

- A Map is created with keys as Strings and Values as `ArrayList<String>`.
- An `ArrayList` can store String objects.
- Since each key will be referenced to a single `ArrayList`, no conditions are violated.
</blockquote>
</details>

</details>

 ---

8. How to convert a `Map` of random order into a sorted  `Map`.
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

<blockquote>
    
``` java

public class OrderedMap {
    public static void main(String[] args) {
        HashMap<Integer,String> hm = new HashMap<>();
        hm.put(1,"Stephen Hawkins");
        hm.put(2,"Albert Einsten");
        hm.put(3,"Michel Faraday");
        hm.put(4,"Issac Newton");
        TreeMap<Integer,String > tm = new TreeMap<>(hm);
    }
}


```
    
</blockquote>
<details>
<summary><b>Explanation</b></summary>

<blockquote>

- `HashMap` stores keys and values in random order, whereas `TreeMap` stores all the elements in sorted order.
- By creating a `TreeMap` and adding all the values of `HashMap` to `TreeMap` a sorted `Map` is created.

</blockquote>
</details>


</details>
    
  ---

9. Write a program to order the `HashMap`based on the value?
    
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)


<details>
<summary><b>Show Answer</b></summary>

   <blockquote>
       
``` java
public class ValueOrder {
    public static void main(String[] args) {
        HashMap<Integer,String> hm = new HashMap<>();
        hm.put(1,"Stephen Hawkins");
        hm.put(2,"Albert Einsten");
        hm.put(3,"Michel Faraday");
        hm.put(4,"Issac Newton");
        hm.entrySet().stream().sorted(Map.Entry.comparingByValue()).forEach(System.out::println);
    }
}



```

</blockquote>

<details>

<summary><b>Explanation</b></summary>

<blockquote>

- A HashMap is created and the elements are sorted by value using aggregate functions.


</blockquote>


</details>
</details>
    
---

10. Given a Sentence, print the frequency of each word in the list using a `HashMap`.
    
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details>

<summary><b>Show Answer</b></summary>

 <blockquote>
     
``` java
import java.util.*;
public class DistinctWords {
    public static void main(String[] args) {
        String sentence= "The world is full of obvious things, which nobody by any chance ever observes, I repeat nobody";
        String[] s = sentence.split(" ");
        HashMap<String,Integer> hm = new HashMap<>();
        for(String w: s)
        {
            Integer frequency = hm.get(w);
            if(frequency==null)
            {
                hm.put(w,1);
            }
            else {
                hm.put(w, frequency + 1);
            }
        }
        System.out.println(hm.size()+ " Distinct Words");
        System.out.println(hm);
    }
}


```
</blockquote>

<details>
<summary><b>Explanation</b></summary>
<blockquote>

- A `String` array of the given string is created, if the words are new then a new key-value pair with word and frequency is added to the map and if the word already exists, then the frequency is increased by 1.

</blockquote>
</details>
</details>
    
---

11. Write a program to check if a `Map` is a sub-map of another `Map`.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


<details>

<summary><b>Show Answer</b></summary>

<blockquote>
    
``` java
import java.util.*;
public class SubMap {
    public static void main(String[] args) {
        HashMap<String,Integer> Map1 = new HashMap<>();
        Map1.put("Jupiter",1);
        Map1.put("Saturn",2);
        Map1.put("Venus",3);
        HashMap<String,Integer> Map2 = new HashMap<>();
        Map2.put("Jupiter",1);
        Map2.put("Saturn",2);
        System.out.println(Map1.entrySet().containsAll(Map2.entrySet()));
    }
}


```

 </blockquote>
    
<details>
<summary><b>Explanation</b></summary>
<blockquote>

- `entrySet()` gets all the key and value pairs to form the `Map` and `containsAll(Collection)` returns true if Map1 contains all the key-value pairs of Map2.

</blockquote>
</details>


</details>
    
---

12. Write a program to get the common keys of two Maps.
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)



<details>
<summary><b>Show Answer</b></summary>

<blockquote>
        
``` java

import java.util.*;
public class CommonKeys {
    public static void main(String[] args) {
        HashMap<String,Integer> Map1 = new HashMap<>();
        Map1.put("Jupiter",1);
        Map1.put("Saturn",2);
        Map1.put("Venus",3);
        HashMap<String,Integer> Map2 = new HashMap<>();
        Map2.put("Jupiter",1);
        Map2.put("Saturn",2);
        HashMap<String ,Integer> CommonKeys = new HashMap<>(Map1);
        CommonKeys.entrySet().retainAll(Map2.entrySet());
        System.out.println(CommonKeys.keySet());
    }
}



``` 
    
</blockquote>
    
<details>
<summary><b>Explanation</b></summary>

> - A new `HashMap` CommonKeys is created to avoid changing the existing HashMaps and `retainAll()` methods to give the intersection of two Maps. 


</details>

</details>
    
 ---

13. Consider that a company stores the details of the employee as a key-value pair of employee names and managers, and writes a program to get only the details of non-managers.
    
    
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

<blockquote>
    
``` java
import java.util.*;
public class Employee {
    public static void main(String[] args) {
        HashMap<String,String> Employees = new HashMap<>();
        Employees.put("Dwight", "Michel");
        Employees.put("Jim","Michel");
        Employees.put("Michel","Jan");
        HashSet<String> NonManagers = new HashSet<>(Employees.keySet());
        NonManagers.removeAll(Employees.values());
        System.out.println(NonManagers);
    }
}



```
</blockquote>
    
<details>
<summary><b>Explanation</b></summary>
 
<blockquote>

- Employees contain employee name as key and manager name as value
- A `HashSet` is created with all the employee names
- From the hash set all the manager names are removed by get the manager names from `Employee.values()`.
- `removeAll()` method deletes all the values from the list that are present in a specific collection.



</blockquote>
 
</details>
</details>
    
    
---

14. Write a program to print all the keys of a `Map`.
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

<blockquote>
 
``` java
import java.util.*;
public class Employee {
    public static void main(String[] args) {
        HashMap<String,String> Employees = new HashMap<>();
        Employees.put("Dwight", "Michel");
        Employees.put("Jim","Michel");
        Employees.put("Michel","Jan");
        for( String s: Employees.keySet()){
            System.out.println(s);
        }
    }
}

```
    
</blockquote>

<details>
<summary><b>Explanation</b></summary>
 
<blockquote>

- `keySet()` returns all the keys of a `Map`. 
</blockquote>
 
</details>
</details>
    
---

15. Write a program to print all the values of a `Map`.
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

<blockquote>
    
``` java
import java.util.*;
public class Employee {
    public static void main(String[] args) {
        HashMap<String,String> Employees = new HashMap<>();
        Employees.put("Dwight", "Michel");
        Employees.put("Jim","Michel");
        Employees.put("Michel","Jan");
        for( String s: Employees.values()){
            System.out.println(s);
        }
    }
}

```
    
</blockquote>
 
<details>
<summary><b>Explanation</b></summary>
 
<blockquote>

- `values(?)` returns all the values of a `Map`. 
 
</blockquote>
 
</details>
</details>
    
 ---

16. Write a program to print all the key-value pairs of a `Map`.
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>

 <blockquote>
     
``` java
import java.util.*;
public class Employee {
    public static void main(String[] args) {
        HashMap<String,String> Employees = new HashMap<>();
        Employees.put("Dwight", "Michel");
        Employees.put("Jim","Michel");
        Employees.put("Michel","Jan");
        for( Map.Entry<String,String> emp : Employees.entrySet()){
            System.out.println(emp.getKey()+": "+emp.getValue());
        }
    }
}

```
     
</blockquote>

<details>
<summary><b>Explanation</b></summary>
 
<blockquote>

- `entrySet()` returns all the key and value pairs of a `Map` and `get key` and `getValue` are used to get keys and values individually from an `entrySet`. 
 
</blockquote>
 
</details>
</details>



## Scenario Based

17. Consider that a country stores its citizen's data in a form of Aadhar number and age, a deadly virus outbreak led to a global shutdown and the country wants to vaccinate the older people first as they get easily infected by the virus. Which of the following best represents the scenario?
    
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

A. `TreeMap` with Aadhar number as key and age as value but ordered by value in descending order.<br>
B. `HashMap` with Aadhar number key and age as value .<br>
C. `TreeMap` with age as key and Aadhar number as value but ordered by key.<br>
B. `HashMap` with age as key and Aadhar number as value.<br>

<details>
<summary><b>Show Answer</b></summary>

> A
    
<details>
<summary><b>Explanation</b></summary>

> `TreeMap` orders elements in a certain order and many people can be of the same age but everyone has a unique Aadhar number and by ordering them in descending order the people with high age will come first in the list.

</details>

</details>





