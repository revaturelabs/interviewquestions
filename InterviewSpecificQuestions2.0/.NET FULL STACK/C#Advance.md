## Technical

1.  What is Reflection in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Reflection is the process of describing the metadata of types, methods, and fields in a code. The namespace System. 
- Reflection enables us to obtain data about the loaded assemblies, and the elements within them like classes, methods, and value types.
	
</blockquote> 

</details>

---

2. What is the difference between dispose and finalize methods in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`dispose()` must be explicitly invoked by the user and the `finalize()` is called by the garbage collector when the object is destroyed.

</blockquote>

</details>

---

3. What are Tuples?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Tuples are data structures that hold object properties and contain a sequence of elements of different data types. They were introduced as a `Tuple<T>` class in .NET Framework to avoid the need of creating separate types to hold object properties.

</blockquote>

</details>

---

4. Why do we use Async and Await in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Processes belonging to asynchronous programming run independently of the main or other processes. In C#, using Async and Await keywords for creating asynchronous methods.

</blockquote>

</details>

---

5. Explain different states of a Thread in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A thread in C# can have any of the following states:

Aborted – The thread is dead but has not stopped
Running – The thread is executing
Stopped – The thread has stopped the execution
Suspended – The thread has been suspended
Unstarted – The thread is created but has not started execution yet
WaitSleepJoin – The thread calls sleep, calls wait on another object, and calls join on some other thread

</blockquote>

</details>

---

6. What do you understand by regular expressions in C#? Can you write a program that searches a string using regular expressions?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A regular expression is a template for matching a set of inputs. It can consist of constructs, character literals, and operators. Regex is used for string parsing, as well as replacing the character string. 

The following code searches a string “C#” against the set of inputs from the languages array using Regex:

```C#

static void Main(strong[] args)
{
string[] languages = {“C#”, “Python”, “Java”};
foreach(string s in languages)
{
if(System.Text.RegularExpressions.Regex.IsMatch(s,“C#”))
{
Console.WriteLine(“Match found”);
}
}
}

```

</blockquote>

</details>

---

7. What are Indexers in C#?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

C# introduces a new concept known as Indexers which are used for treating an object as an array. The indexers are usually known as smart arrays in C#. They are not an essential part of object-oriented programming.

Defining an indexer allows us to create classes that act as virtual arrays. Instances of that class can be accessed using the [] array access operator.

</blockquote>

</details>

---

8. What is Serialization?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Serialization converts a code to its binary format using a process. After it is converted to bytes, it can be easily stored and written to a disk. Serializations are useful so that the original form of the code isn’t lost and can be retrieved later.

</blockquote>

</details>

---

9. Can you explain about delegates?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- A Delegate is a variable that holds the reference to a method. Hence it is a function pointer or reference type. All Delegates are derived from System.Delegate namespace. Both Delegate and the method that it refers to can have the same signature.

- **Declaring a delegate**: `public delegate void AddNumbers(int n);`
After the declaration of a delegate, the object must be created by the delegate using the new keyword.

  - `AddNumbers an1 = new AddNumbers(number);

- The delegate provides a kind of encapsulation to the reference method, which will internally get called when a delegate is called.

```C#

public delegate int myDel(int number);
public class Program
{
    public int AddNumbers(int a)
    {
        int Sum = a + 10;
        return Sum;
    }
    public void Start()
    {
        myDel DelegateExample = AddNumbers;
    }
}

```

</blockquote>

</details>

---

10. What are Events?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Events are user actions that generate notifications to the application to which it must respond. The user actions can be mouse movements, keypress and so on.

- Programmatically, a class that raises an event is called a publisher and a class which responds/receives the event is called a subscriber. The event should have at least one subscriber else that event is never raised.

- Delegates are used to declare Events.

``` C#
Public delegate void PrintNumbers();
Event PrintNumbers myEvent;
```

</blockquote>

</details>

---

11. What do Multicast Delegates mean?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A Delegate that points to more than one method is called a Multicast Delegate. Multicasting is achieved by using the + and += operator.

</blockquote>

</details>

---

12. How to use Delegates with Events?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Delegates are used to raise events and handle them. Always a delegate needs to be declared first and then the Events are declared.

</blockquote>

</details>

---

13. Can you state the difference between direct cast and ctype?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The difference between direct cast and ctype is that direct cast is used for the conversion of the type of an object that requires a run time which is like the specified type in the direct cast. Whereas ctype is used for converting the conversion which is defined for the expression and the type.

</blockquote>

</details>

---

14. What is LINQ in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

LINQ stands for Language Integrated Query. LINQ has the great power of querying any source of data. The data source could be collections of objects, databases, or XML files. We can easily retrieve data from any object that implements the `IEnumerable<T>` interface.

</blockquote>

</details>

---

15. Can you explain the “using” statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The keyword “using” is used to define the scope of the resources used in that using statement block. All the resources used inside the using code block get disposed of once the code block completes execution.

```C#

class Books : IDisposable
    	{
        private string _name { get; set; }
        private decimal _price { get; set; }

        public Books(string name, decimal price)
        {
            _name = name;
            _price = price;
        }

        public void Print()
        {
            Console.WriteLine("Book name is {0} and price is {1}", _name, _price);
        }

        public void Dispose()
        {
            throw new NotImplementedException();
        }
   	}

    	class Students
    	{
        public void DoSomething()
        {
            using (Books myBook = new Books("book name", 12.45))
            {
                myBook.Print();
            }
        }
}

```

</blockquote>

</details>

---

16. In C# private constructor or sealed class, which one would you prefer to prevent a class extension in inheritance and why?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The best choice is to use a sealed class to prevent the class not to be extended/inherited. This is true that a private constructor and sealed class both can prevent the extension of a class, which means, we cannot derive any class from it. However, they have their own purpose and properties.

</blockquote>

</details>

---
	
17.What are C# attributes and its significance?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
	
Attributes are declarative tags on certain entities, eg. Class, method, etc. are called attributes. The attribute’s information can be retrieved at runtime using Reflection.
	
</blockquote>

</details>

---
	
18.What is the difference between the Virtual method and the Abstract method?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Virtual method must always have a default implementation. However, it can be overridden in the derived class, although it is not mandatory. It can be overridden using the override keyword.

An Abstract method does not have an implementation. It resides in the abstract class. It is mandatory that the derived class implements the abstract method. An override keyword is not necessary here though it can be used.
	
</blockquote>

</details>

---
	
19. What are C# I/O classes? What are the commonly used I/O classes?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	

C# has System.IO namespace, consisting of classes that are used to perform various operations on files like creating, deleting, opening, closing, etc.

Some commonly used I/O classes are:

File – Helps in manipulating a file.
StreamWriter – Used for writing characters to a stream.
StreamReader – Used for reading characters to a stream.
StringWriter – Used for reading a string buffer.
StringReader – Used for writing a string buffer.
Path – Used for performing operations related to the path information.
	
</blockquote>

</details>

---	
	
20. What is StreamReader/StreamWriter class?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
StreamReader and StreamWriter are classes of namespace System.IO. They are used when we want to read or write charact90, Reader-based data, respectively.

Some of the members of StreamReader are: Close(), Read(), Readline().

Members of StreamWriter are: Close(), Write(), Writeline().	
	
</blockquote>

</details>

---	

21.Explain Publishers and Subscribers in Events.
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
Publisher is a class responsible for publishing a message of different types of other classes. The message is nothing but Event.

Subscribers capture the message of the type that it is interested in.
	
</blockquote>

</details>

---	
	
22.What are the types of Serialization?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The different types of Serialization are: 

XML serialization – It serializes all the public properties to the XML document. Since the data is in XML format, it can be easily read and manipulated in various formats. The classes reside in System.sml.Serialization.
SOAP – Classes reside in System.Runtime.Serialization. Similar to XML but produces a complete SOAP compliant envelope that can be used by any system that understands SOAP.
Binary Serialization – Allows any code to be converted to its binary form. Can serialize and restore public and non-public properties. It is faster and occupies less space.
	
</blockquote>

</details>

---	
	
23.What do you understand about dependency injection?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
You can de-couple tightly linked classes using the dependency injection. Thus, it reduces the direct dependency of classes upon each other. You can achieve dependency injection via the following: 

Constructor dependency
Property dependency
Method dependency
	
</blockquote>

</details>

---	
	
24. What are the advantages of using partial classes?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
The major advantages of using partial classes are as follows:

They allow multiple developers to work on the same class easily.
The code generators mainly use them to keep different concerns separate.
It allows one developer to define the method while the other developer can implement it.
	
</blockquote>

</details>

---
	
25.What is string interpolation in C#?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
String Interpolation in C# allows to create formatted strings with readable and convenient syntax. You can create an interpolation string containing interpolation expressions using the $ special character. On resolving, the interpolation string replaces the interpolation expression with the string representation of the interpolation item.
	
</blockquote>

</details>

---
	
26.How is Var different from Dynamics in C#?
	
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 	
	
Variables declared with var are implicitly but statically typed. Variables declared with dynamic are dynamically typed. 
	
This means that dynamic declarations are resolved at run-time, and var declarations are resolved at compile-time.
	
</blockquote>

</details>

---
