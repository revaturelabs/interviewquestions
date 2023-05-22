## Technical

1. What is a Collection in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The Collections in C# are a set of predefined classes that are present in the `System.Collections` namespace that provides greater capabilities and functionalities.
- The collections in C# are classes that represent a group of objects. With the help of C# Collections, we can perform different types of operations on objects such as Store, Update, Delete, Retrieve, Search, and Sort objects, etc. 
- All the data structure work can be performed by collections in C#. 

</blockquote>

</details>

---

2. Do you know the types of collections in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are 3 ways to work with collections. The three namespaces are,

- `System.Collections` classes.
- `System.Collections.Generic` classes.
- `System.Collections.Concurrent` classes.

</blockquote>

</details>

---

3. Can you brief on Non-Generic Collection classes in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Non-Generic collection classes in C# are defined under `System.Collections`classes which operate on objects, and hence can handle any type of data, but not in a safe-type manner. The `System.Collections` namespace contains the following classes:

**ArrayList**: It Implements the `System.Collections.IList` interface using an array whose size is dynamically increased as required.

**Stack**: It represents a simple last-in-first-out (LIFO) non-generic collection of objects.

**Queue**: It represents a first-in, first-out collection of objects.

**HashTable**: It represents a collection of key/value pairs that are organized based on the hash code of the key.

**SortedList**:  It represents a collection of key/value pairs that are sorted by the keys and are accessible by key and by index.

</blockquote>

</details>

---

4. Can you elaborate on Generic Collection Classes in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It provides a generic implementation of standard data structures like linked lists, stacks, queues, and dictionaries. These collection classes are type-safe because they are generic means only those items that are type-compatible with the type of the collection can be stored in a generic collection; it eliminates accidental type mismatches. The `System.Collections.Generic` namespace has the following classes:

`List<T>`: It represents a strongly typed list of objects that can be accessed by index. Provides methods to search, sort, and manipulate lists.

`Stack<T>`: It represents a variable size last-in-first-out (LIFO) collection of instances of the same specified type.

`Queue<T>`: It represents a first-in, first-out collection of objects.

`HashSet<T>`: It represents a set of values. It removes duplicate elements from the collection.

`Dictionary<TKey, TValue>`: It represents a collection of keys and values.

`SortedList<TKey, TValue>`: It represents a collection of key/value pairs that are sorted by key based on the associated `System.Collections.Generic.IComparer` implementation.

`SortedSet<T>`: It represents a collection of objects that are maintained in sorted order.

`SortedDictionary<TKey, TValue>`: It represents a collection of key/value pairs that are sorted on the key.

`LinkedList<T>`: It represents a doubly linked list.

</blockquote>

</details>

---

5. Do you know about Concurrent Collection classes in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It provides various threads-safe collection classes that are used in place of the corresponding types in the `System.Collections` and `System.Collections.Generic` namespaces, when multiple threads are accessing the collection simultaneously. The `System.Collections.Concurrent` namespace provides classes for thread-safe operations. Now multiple threads will not create problems for accessing the collection items. The `System.Collections.Concurrent` namespace has the following classes:

`BlockingCollection<T>`: It provides blocking and bounding capabilities for thread-safe collections that implement `System.Collections.Concurrent.IProducerConsumerCollection`.

`ConcurrentBag<T>`: It represents a thread-safe, unordered collection of objects.

`ConcurrentStack<T>`: It represents a thread-safe last-in-first-out (LIFO) collection.

`ConcurrentQueue<T>`: It represents a thread-safe first-in-first-out (FIFO) collection.

`ConcurrentDictionary<TKey, TValue>`: It represents a thread-safe collection of key/value pairs that can be accessed by multiple threads concurrently.

</blockquote>

</details>

---

6. What is the difference between an Array and an Array List in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The ArrayList collection in C# is very much like the Arrays data type. The major difference between them is the **dynamic nature** of the non-generic collection ArrayList. 
- For arrays, we need to define the size i.e. the number of elements that the array can hold at the time of array declaration. But in the case of the ArrayList collection in C#, this does not need to be done beforehand. Elements can be added or removed from the Array List collection at any point in time.

</blockquote>

</details>

---

7. Do we face any problems with Array and ArrayList Collection in C#? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the case of Array and ArrayList in C#, we access the elements from the collection using the index position. The index position of the elements starts from zero (0) to the number of elements – 1. But it is very difficult for us to remember the index position of the element to access the values.

**For example**, let us say we have an employee array that contains the name, address, mobile, dept no, email id, employee id, salary, location, etc. Now if I want to know the email id or dept number of the employee then it is very difficult for me to use the index position.

</blockquote>

</details>

---

8. What is a HashTable in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Hashtable in C# is a Non-Generic Collection that stores the element in the form of “Key-Value Pairs”. The data in the Hashtable are organized based on the hash code of the key. The key can be of any data type. Once we created the Hashtable collection, then we can access the elements by using the keys. The Hashtable class comes under the `System.Collections` namespace.

The Hashtable computes a hash code for each key. Then it uses that hash code to look up the elements very quickly which increases the performance of the application.

</blockquote>

</details>

---

9. How the HashTable works in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

When we add elements to a hashtable like string, int, or complex types, then it converts the key data which can be a string, integer, numeric, or anything in the world into simple hash integer values so that lookup can be easy. Once the conversion is done, then the data will be added to the hashtable. collection.

**Note**: The performance of the hashtable is less as compared to the ArrayList because of this key conversion (converting the key to an integer hashcode).

</blockquote>

</details>

---

10. Can you differentiate ArrayList and Hashtable in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**Lookup**: ArrayList can be only looked up via the index number which is generated internally. Hashtable can be looked up by a custom-defined key.
**Performance**: ArrayList is faster than hashtable because of extra tasks performed in hashtables i.e., hashing.
**Scenario**: If you want a key lookup use hashtable. If you just want to add and browser through a collection, then use ArrayList.

</blockquote>

</details>

---

11. Can you brief me on the Stack Collection class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- In C#, stacks are used to store a collection of objects in a LIFO (Last in, First out) style, i.e., the element which added last will come out first.
-By using the `Push()` method, we can add elements to a stack.
- The `Pop()` method will remove and return the topmost element from the stack.
- The `Peek()` method will return the last (top-most) inserted element of the stack, and it won’t delete the element from the stack.
- The capacity of a Stack is the number of elements the Stack can hold. As we add elements to a Stack, the capacity of the stack is automatically increased.
- The Stack Collection in C# allows both null and duplicate values.

</blockquote>

</details>

---

12. Can you brief me on the Queue Collection class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- In C#, Queues are used to store a collection of objects in a FIFO (First in, First out) style, i.e., the element which is added first will remove first.
- By using the `Enqueue()` method, we can add elements at the end of the queue.
- The `Dequeue()` method will remove and return the first element from the queue.
- The queue `Peek()` method will always return the first element of the queue, and it won’t delete elements from the queue.

</blockquote>

</details>

---

13. When to Use Non-Generic SortedList Collection in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Non-Generic SortedList Collection is a powerful tool for performing quick manipulation of key-value data in an orderly manner. But there are certain scenarios where this class may not be suitable. For example, by its nature, a SortedList must always be sorted. 
- Therefore, whenever we add a new key-value pair to the list or remove a key-value pair from the SortedList, then it must sort itself to ensure that all elements are in the right order. This becomes more expensive as we increase the number of elements in our SortedList.

**Note:** We should only use SortedList when we want to handle smaller collections that need to be sorted at all times.

</blockquote>

</details>

---

14. What is Generics in C#? Why do we need Generics in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Generics allow us to define classes and methods which are decoupled from the data type otherwise we can also say that the Generics allow us to create classes using angular brackets specifying the data type of its members. At compilation time, these angular brackets are going to be replaced with some specific data types. In C#, the Generics can be applied to:

- Interface
- Abstract class
- Class
- Method
- Static method
- Property
- Event
- Delegates

</blockquote>

</details>

---

15. Can you brief me on Generic Dictionary Collection Class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A dictionary is a collection of key-value pairs.
- The Dictionary Generic Collection class is present in System.Collections.Generic namespace.
- When creating a dictionary, we need to specify the type for the key as well as the type for the value.
- The fastest way to find a value in a dictionary is by using the keys.
- Keys in a dictionary must be unique.

</blockquote>

</details>

---

16. Can you differentiate List and Dictionary in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Both lists and dictionaries belong to Generics collections that are used to store collections of data.
- Both Dictionary `<TKey, TValue>` and List `<T>` are similar both have random access data structures on top of the .NET framework. 
- The Dictionary is based on a hash table which means it uses a hash lookup, which is an efficient algorithm to look up things, on the other hand, a list, has to go and check element by element until it finds the result from the beginning.
- When comparing with the List data structure, the dictionary always has a fixed lookup time.

</blockquote>

</details>

---

17. What is the ForEach loop in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The foreach loop in C# is used to iterate over the elements of a collection. Here, the collection may be an array or a list or a dictionary, etc. As per the name i.e. foreach, it executes the loop body for each element present in the array or collection.

- In C#, the foreach loop iterates collection types such as Array, ArrayList, List, Hashtable, Dictionary, etc. It can be used with any type that implements the `IEnumerable` interface.

**Syntax**:

```C#
foreach(datatype var_name in collection_variable)
{
    //statements
}
```

</blockquote>

</details>

---

18. Can you brief us on BlockingCollection class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`BlockingCollection<T>` is a thread-safe collection class that provides the following features:

- An implementation of the Producer-Consumer pattern.
- Concurrent adding and taking of items from multiple threads.
- Optional maximum capacity.
- Insertion and removal operations block when the collection is empty or full.
- Insertion and removal “try” operations that do not block or that block up to a specified period.
- Encapsulates any collection type that implements `IProducerConsumerCollection<T>`

</blockquote>

</details>

---

