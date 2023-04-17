## Technical

1.  What is `extern` modifier in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
The `extern` modifier is used to declare a method that is implemented externally. A common use of the `extern` modifier is with the `DllImport` attribute when you are using Interop services to call into unmanaged code. In this case, the method must also be declared as `static`, as shown in the following example:

```C#
[DllImport("avifil32.dll")]
private static extern void AVIFileInit();
```

The `extern` keyword can also define an external assembly alias, which makes it possible to reference different versions of the same component from within a single assembly. 
	
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

The `async` keyword turns a method into an async method, which allows you to use the `await` keyword in its body. When the `await` keyword is applied, it suspends the calling method and yields control back to its caller until the awaited task is complete. `await` can only be used inside an `async` method.

```C#

public class HelloWorld
{
    public static void Main(string[] args)
    {
        Method1_2();
        int k=Method3();
        Console.WriteLine(k);
        Console.Read();
    }
    static async void Method1_2()
    {
        Console.WriteLine("Test");
        var i=await Task.Run(()=>
        {
            return Method1();
        })
        Console.WriteLine(i);
        int j=Method2(i);
        Console.WriteLine(j);
    }
    public static int Method1()
    {
        Thread.sleep(500);
        return 10;
    }
    public static int Method2(int i)
    {
        return 20 *i;
    }
    public static int Method3()
    {
        return 30;
    }
}

// Output Test 30 10 200

```

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

Indexers allow instances of a class or struct to be indexed just like arrays. The indexed value can be set or retrieved without explicitly specifying a type or instance member. Indexers resemble properties except that their accessors take parameters.

The following example defines a generic class with simple get and set accessor methods to assign and retrieve values. The Program class creates an instance of this class for storing strings.

```C#
using System;

class SampleCollection<T>
{
   // Declare an array to store the data elements.
   private T[] arr = new T[100];

   // Define the indexer to allow client code to use [] notation.
   public T this[int i]
   {
      get { return arr[i]; }
      set { arr[i] = value; }
   }
}

class Program
{
   static void Main()
   {
      var stringCollection = new SampleCollection<string>();
      stringCollection[0] = "Hello, World";
      Console.WriteLine(stringCollection[0]);
   }
}
// The example displays the following output:
//       Hello, World.

```

</blockquote>

</details>

---

8. What is Serialization? When to use it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Serialization is a process of converting object to its BINARY FORMAT (BYTES) Once it is converted to bytes, it can be easily stored and written to a disk or any such storage devices.

It is mostly used in Web API to convert class objects into JSON string like this.

```C#

private void JSONSerialize()
{
    Employee empObj=new Employee();
    empObj.ID=1;
    empObj.Name="Revature";
    empObj.Address="India";

    string jsonData=JSONConvert.SerializeObject(empObj);
    Response.Write(jsonData);
}

```

</blockquote>

</details>

---

9. Can you explain about delegates?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`IEnumerable` interface is used when we want to iterate among our collection classes using a FOREACH loop. For example, in below code there is a List of Employees then you are adding new Employees in the list here. Then you are running a foreach loop to print the employee id and names one by one. Now how this loop is working. This is enabled by the `IEnumerable` only because internally List is using `IEnumerable`

```C#

class Program
{
    static void Main(string[] args)
    {
        var employees=new List<Employee>(){
            new Employee(){Id=1,Name="DotNet"},
            new Employee(){Id=2,Name="Training"}
        };
        foreach(var employee in employees)
        {
            Console.WriteLine(employee.Id+", "+employee.Name);
        }
        Console.ReadLine();
    }
}

public class Employee
{
    public int Id{get;set;}
    public string Name{get;set;}
}
```
If you got the definition of List then you will see the below code where List is inherited from `IEnumerable` interface.

```C#

namespace system.Collections.Generic
{
    public class List<T>:ICollection<T>,IEnumerable<T>,IEnumerable,IList<T>
    {
        ...public List();
        ...public List(IEnumerable<T> collection);
        ...public List(int capacity);
    }
}
```
And if you see the definition of `IEnumerable`, then you will see the below definition where it states that it supports iteration of non-generic collection.

```C#

namespace System.Collections
{
    public interface IEnumerable
    {
        IEnumerator GetEnumerator();
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

13. Explain Multithreading?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Multithreading in C# is a process in which multiple threads work simultaneously.It is a way to achieve Multitasking. It saves time because multiple tasks are being executed at a time. To create multithreaded application in C#, we need to use `SYSTEM.THREDING` namespace.

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
17. What are Anonymous Delegates in C#?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Anonymous Delegates, you can create a delegate, but there is no need to declare the method associated with it.

See in the below code, there is not Add method or any other method. But the logic of adding is written inline using `delegate` keyword.

```C#

public delegate void Calculator(int x,int y);
class Program
{
    static void Main(string[] args)
    {
        Calculator calAdd=delegate(int a,int b)
        {
            Console.WriteLine(a+b);
        };
        calAdd(20,30);
        Console.ReadLine();
    }
}

```
</blockquote>

</details>

---

18. What is ENUM keyword used for?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

An enum is a special "class" that represents a group of constants.

```C#

enum Level
{
    Low,
    Medium,
    High
}

class Program
{
    static void Main(string[] args)
    {
       Level myVar=Level.Medium;
       Console.WriteLine(myVar);
       Console.ReadLine(); 
    }
}
```

```C#
enum Weekdays
{
    Sunday,
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday
}
```

</blockquote>

</details>

---

19. What is Covariance in C#?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Covariance enables you to pass a derived type where a base type is expected.

`Small sml = new Bigger();`

</blockquote>

</details>

---

20. What is Parsing? How to parse a DATE TIME string?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Parsing converts a string into another data type.

**For Example:**

```C#
string text = “500”;
int num = int.Parse(text);
```

500 is an integer. So, the Parse method converts the string 500 into its own base type, i.e int.

Follow the same method to convert a DateTime string.

```C#

string dateTime = “Jan 1, 2018”;
DateTime parsedValue = DateTime.Parse(dateTime);

```

</blockquote>

</details>

---

21. Can we have multiple threads in one APPDomain?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

One or more threads run in an AppDomain. An AppDomain is a runtime representation of a logical process within a physical process. Each AppDomain is started with a single thread, but can create additional threads from any of its threads.

</blockquote>

</details>

---

22. What is THREAD.SLEEP() in threading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Thread's execution can be paused by calling the `Thread.Sleep` method. This method takes an integer value that determines how long the thread should sleep. Example

`Thread.CurrentThread.Sleep(2000)`.

</blockquote>

</details>

---

23. Why we need Multi-threading in our project? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Multi-threading is running the multiple threads simultaneously. Some main advantages are:

- You can do multiple tasks simultaneously. For e.g. saving the details of user to a file while at the same time retrieving something from a web service.
- Threads are much lightweight than process. They don't get their own resources. They used the resources allocated to a process.
- Context-switch between threads takes less time than process.

</blockquote>

</details>

---

