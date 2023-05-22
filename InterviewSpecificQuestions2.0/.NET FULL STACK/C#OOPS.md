## Technical

1. What is meant by object-oriented programming?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Object-oriented programming (OOP) is an approach to programming where software is primarily designed by using objects (essentially data) that interact with each other. 

- When different pieces of data are put together, they come to form the software. OOP is an alternative to functional or procedural programming and it’s also the approach used by C#.

</blockquote>

</details>

---

2. What is a Class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, a class is a user-defined blueprint from which objects are created. It brings various types of data together to form a single unit. 

</blockquote>

</details>

---

3. What is an Object in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

An object is a real-world entity and in C# it’s a single instance of a class. For example, if you had a class of ‘birds’ then ‘pigeons’, ‘peacocks’, and ‘crows’ would all be objects.

</blockquote>

</details>

---

4. Can you define a Method in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, a method is a code block that contains a series of statements used to perform specific operations. Methods must be declared within a class or a structure. They help save time by reusing code. 

</blockquote>

</details>

---

5. What is meant by Structures in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A C# structure is a value type, and the instances or objects of a structure are created in the stack. 
- A structure in C# is simply a composite data type consisting of several elements of other types. 
- The structure in C# can contain fields, methods, constants, constructors, properties, indexers, operators, and even other structure types. 

</blockquote>

</details>

---

6. Why is class an abstract data type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A Class is an Abstract Data Type because it specifies what data members and member functions (methods) contain in it (class), but it does not provide information on how those are implemented. That makes Class Abstract and Class is User Defined Data Type. So, it’s an Abstract Data Type

</blockquote>

</details>

---

7. What is the difference between the `string` keyword and the `System.String` class? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Actually, there is no difference. The `string` keyword is an alias for the `System.String` class. Therefore `System.String` and `string` keywords both are the same, and we can use whichever naming convention we prefer. The String class provides many methods for safely creating, manipulating, and comparing strings.

</blockquote>

</details>

---

8. Can you define Constructors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A constructor is a member function with the same name as its class. The constructor is automatically invoked when an object is created. While the class is being initialized, it constructs all the values of data members.

</blockquote>

</details>

---

9.  What is a destructor in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Destructor is used to clean up the memory and free the resources. But in C#, this is done by the garbage collector on its own. `System.GC.Collect()` is called internally for cleaning up. But sometimes it may be necessary to implement destructors manually.

For Example:

```C#
~Car()
{
    Console.writeline(“….”);
}
```

</blockquote>

</details>

---

10. What are the fundamental OOP concepts?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The four fundamental concepts of Object-Oriented Programming are:

**Encapsulation**: Here, the internal representation of an object is hidden from the view outside the object’s definition. Only the required information can be accessed whereas the rest of the data implementation is hidden.
**Abstraction**: It is a process of identifying the critical behaviour and data of an object and eliminating the irrelevant details.
**Inheritance**: It is the ability to create new classes from another class. It is done by accessing, modifying and extending the behaviour of objects in the parent class.
**Polymorphism**: The name means, one name, many forms. It is achieved by having multiple methods with the same name but different implementations.

</blockquote>

</details>

---

11. What is the difference between a struct and a class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Classes are reference types and structs are value types
- Structures do not support inheritance.
- Structures cannot have a default constructor.
- When we create a struct object using the new operator, it gets created and the appropriate constructor is called. Unlike classes, structs can be instantiated without using the New operator.
- Structures do not support inheritance.
- Structures cannot have a default constructor.

</blockquote>

</details>

---

12.  What are the different types of classes in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Static Class
- Sealed Class
- Partial Class
- Abstract Class

</blockquote>

</details>

---

13. What do you understand by static class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Static Classes are created using a `static` keyword, if any class is marked as static it means we can't create an object of that class and the compiler will guarantee that instances (object) of this class cannot be created., just why because static classes are loaded automatically by the .NET Framework common language runtime (CLR).

**Characteristics of a static class are** :

- Static classes are sealed and therefore cannot be inherited.
- Contains only static members and static constructors.
- Static variables are stored in the heap memory.
- You can access the members of a static class by using the class name itself. 
- Static class can be public.

</blockquote>

</details>

---

14. Do you know about sealed classes? If so, keep it brief. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A sealed class is a class that does not allow inheritance. Some object model designs need to allow the creation of new instances but not inheritance, if this is the case, the class should be declared as sealed. To create a sealed class in C#, the class declaration should be done as:

**Characteristics of sealed classes are**:

- We can create an instance of the sealed class in c#.
- We cannot inherit the sealed class.

</blockquote>

</details>

---

15. Can u explain a bit about partial class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The `partial` keyword indicates that other parts of the class, struct, or interface can be defined in the namespace. All the parts must use the `partial` keyword.

When we work on a large project and write the code in a single .cs file. It is possible to include more than one type in a single class file, but a single type's code cannot be split into sections into multiple separate files. That's why, Microsoft decided to overcome the above issue, with the introduction of something called partial types.

**Characteristics of partial class**

- Each part of a partial class should be in the same assembly or DLL.
- A partial class is only possible in the same namespace and same assembly.
- The partial class must be prefixed with the partial keyword.
- We can apply inheritance on partial class.

</blockquote>

</details>

---

16. What is an abstract class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- An Abstract class is a class which is denoted by an abstract keyword and can be used only as a Base class. This class should always be inherited. An instance of the class itself cannot be created. If we do not want any program to create an object of a class, then such classes can be made abstract.

- Any method in the abstract class does not have implementations in the same class. But they must be implemented in the child’s class.

For Example:

```C#
abstract class AB1
{
    Public void Add();
}
Class childClass : AB1
{
    childClass cs = new childClass ();
    int Sum = cs.Add();
}
```

- All the methods in an abstract class are implicitly virtual methods. Hence, the virtual keyword should not be used with any methods in the abstract class.

</blockquote>

</details>

---

17. What is the difference between the Virtual method and the Abstract method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A Virtual method must always have a default implementation. An Abstract method does not have an implementation. An override keyword is not necessary here, though it can be used.

</blockquote>

</details>

---

18. Can u tell the difference between the Equality Operator (==) and Equals() Method in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Both the `==` Operator and the `Equals()` method are used to compare two value-type data items or reference-type data items. The Equality Operator `(==)` is the comparison operator and the `Equals()` method compares the contents of a string. The `==` Operator compares the reference identity while the `Equals()` method compares only contents.

</blockquote>

</details>

---

19. What’s the difference between the `Is` and `As` operators in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**`is` operator**: In C# language, we use the **“is”** operator to check the object type. If two objects are of the same type, it returns true, else it returns false.

**`as` operator**: The **“as”** operator behaves in a similar way as the **“is”** operator. The only difference is it returns the object if both are compatible with that type. Else it returns a null.

</blockquote>

</details>

---

20.  What is the difference between fields and properties in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A field is a member of a class or an object of any type that represents a location for storing a value, whereas a property is a class member that provides a mechanism to read, write, and compute the value of a private field.

</blockquote>

</details>

---

21.  What are circular references in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, circular references occur when two or more interdependent resources refer to each other, either directly or indirectly, resulting in a closed loop or lock condition. This situation makes the resource unusable.

</blockquote>

</details>

---

22. How is Operator Overloading achieved in C#? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, most of the built-in operators are available and can be overloaded or redefined using the operator keyword. The example below explains the syntax used to implement the addition operator(+) for a user-defined class.

```C#
public static Rectangle operator + (Rectangle b, Rectangle c) {
     Rectangle rectangle = new Rectangle(); 
     rectangle.length = b.length + c.length; 
     rectangle.breadth = b.breadth + c.breadth; 
     rectangle.height = b.height + c.height; 
     return rectangle; 
     } 
```

</blockquote>

</details>

---

23. What is Encapsulation? How is Encapsulation handled in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Encapsulation reduces coupling between objects and increases maintainable code. It involves enclosing objects within a logical pack by limiting access to implementation details. In C#, encapsulation is achieved through the access specifiers public, private, protected, internal, and protected internal.

</blockquote>

</details>

---

24. What is an Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

An Interface is a class with no implementation. The only thing that it contains is the declaration of methods, properties, and events.

</blockquote>

</details>

---

25. What does the extension method do in c# and why do you need it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Extension methods are special static methods in a static class which enables us to add new methods to built-in types and custom types without creating new derived type. Which provides a user-defined custom functionality just like built-in methods have. For Example, String has ToLower(), ToUpper() methods. In the same way, we can create our own method.

Let's check the following example, we have created Remove() method which removes any given character/string from the original string.

public class Program
{
    public static void Main()
    {
        string sample1 = "This, is a, sample string";

        Console.WriteLine("output string : " + sample1.Remove(","));
    }   
}


public static class SampleExtensions
{
    public static string Remove(this string str1, string InputStr)
    {       
        return str1.Replace(InputStr,"");
    }
}

</blockquote>

</details>

---

26. What is enum in C#? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Enumeration (or enum) is a value data type in C#. It is mainly used to assign the names or string values to integral constants, which make a program easy to read and maintain. For example, the 4 suits in a deck of playing cards may be 4 enumerators named Club, Diamond, Heart, and Spade, belonging to an enumerated type named Suit.

</blockquote>

</details>

---

27. What is Boxing and Unboxing in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**Boxing In C#**

- The process of Converting a Value Type (char, int, etc.) to a Reference Type(object) is called Boxing.
- Boxing is an implicit conversion process in which object type (supertype) is used.
- The Value type is always stored in Stack. The Referenced Type is stored in Heap.

**Unboxing In C#**

- The process of converting the reference type into the value type is known as Unboxing.
- It is an explicit conversion process.

</blockquote>

</details>

---

28. What are properties in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- Properties are special types of methods that provide a flexible mechanism for classes for exposing private fields. Hence these are called accessors.


- There are two types of accessors under properties. These are:

  - The get property accessors.
  - The set property accessors.
- These accessors are used to get, set as well as compute class member values.

**The uses of different C# properties are:**

- Properties have to be either read-only or write-only.
- Every property holds some specific logic while setting values for any particular work.
- Fields in properties are contained within the class private so that they cannot be accessed from another class or outside the class's scope straightforwardly.

</blockquote>

</details>

---

29. What is the difference between late binding and early binding in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- The Early Binding occurs at compile time while the Late Binding occurs at runtime. 
- The major difference between Early and Late Binding is that Early Binding uses the class information to resolve method calling while Late Binding uses the object to resolve method calling.

</blockquote>

</details>

---

30. What is Constructor Overloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Constructor Overloading allows us to call a different constructor based on the input parameters we’ve provided when creating a new instance of the class. For each accepted parameter scenario, we must define the constructor to be used. We can have as many constructor overloads as you wish.

We’ve added another constructor function that accepts a single-string input in the example below. If an input is provided, it will set the name variable to that of the input value.

```C#
class Sample
{
    public string name;
    public DateTime created_date;
    public List<string> topics;
    public string description;
    public bool draft;

    public Sample()
    {
        //This is the initial constructor method and will be used if no parameter is passed
        this.name = "Draft"; 
        this.created_date = DateTime.Now;
        this.topics = new List<string>();
        this.description = "Description";
        this.draft =  true; 
    }

    public S_Class(string name)
    {
        //This is the second constructor method and will be used if you pass a single string parameter
        //Instead of the name variable being set to "Tutorial Draft", it will be set to the value of the input parameter
        this.name = name;
        this.created_date = DateTime.Now;
        this.topics = new List<string>();
        this.description = "Description";
        this.draft =  true;
    }
}

```

</blockquote>

</details>

---

31. How does `this` keyword works in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`this` keyword is used to refer to instance members of the current class from within an instance method or a constructor. It removes name ambiguity between method parameters and instance variables if they have the same name. 

Following are some uses of ‘this’ keyword in C#:

- It can be used to invoke any method of the current object.
- It can be used to invoke another constructor from the constructor of the same class.
- It can be used as a parameter for a method call that takes the object of the same class as a parameter.

</blockquote>

</details>

---

32. Can you brief us on C# access modifiers?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

We have four access modifiers in C#:

- **Private** - A private attribute or method can only be accessed from within the class.
- **Public** - When we declare an attribute or method public, it can be accessed from anywhere in the code.
- **Internal** - When a property or method is defined as internal, it can only be accessible from the current assembly point of that class.
- **Protected**- When we declare a method or attribute as protected, then it can only be accessed by members of that class and those who inherit it.

</blockquote>

</details>

---

33. What is method overloading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Method overloading is the process of generating many methods in the same class with the same name but with distinct signatures. The compiler utilizes overload resolution to identify which method to invoke when we compile.

</blockquote>

</details>

---

34. What is an object pool in .NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A container that has objects which are ready to be used is known as an object pool. It helps in tracking the object which is currently in use and the total number of objects present in the pool. This brings down the need for creating and re-creating objects.

</blockquote>

</details>

---

35. Can you brief me on Method Overriding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- It is an approach for defining multiple methods with the same name and with the same signature means the same number, type, and order of parameters.
- Overriding of methods is not possible within the same class it must be performed under the child classes only.
- To override a parent class method under the child classes, first and foremost the child class requires to take permission from its parent.
- This is all about changing the behaviour of a method.
- This is used to implement dynamic polymorphism.
- To implement function overriding, we use the virtual keyword for the base class function and override keyword in the derived class function 

</blockquote>

</details>

---

36.  How do you inherit a class into another class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

In C#, the colon can be used as an inheritance operator. You need to place a colon and follow it with the class name.

</blockquote>

</details>

---

37.  How can we set the class to be inherited, but prevent the method from being overridden?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

To set the class to be inherited, it needs to be declared as public. The method needs to be sealed to prevent any overrides.

</blockquote>

</details>
---

38. How can a class be set to be inherited without overriding the method in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Provided that the method isn’t virtual, it won’t be overridden. However, if the class is inheriting from a base class that contains a virtual member function, you can use the `<sealed>` modifier to avoid further overriding that member function.

</blockquote>

</details>

---

39. Can an interface inherit from another interface in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Yes, an interface can inherit from another interface in C#. It is possible for a class to inherit an interface multiple times, through base classes or interfaces it inherits. In this case, the class can only implement the interface one time if it is declared as part of the new class. If the inherited interface is not declared as part of the new class, its implementation is provided by the base class that declared it. It is possible for a base class to implement interface members using virtual members; in that case, the class inheriting the interface can change the interface behaviour by overriding the virtual members.

</blockquote>

</details>

---

40. What are the differences between method hiding and overriding in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- For hiding the base class method from the derived class, simply declare the derived class method with the new keyword.
Whereas in C#, for overriding the base class method in a derived class, you need to declare the base class method as virtual, and the derived class method as overridden.
- If a method is simply hidden then the implementation to call is based on the compile-time type of the argument "this".
Whereas if a method is overridden then the implementation to be called is based on the run-time type of the argument "this".
- New is reference-type specific and overriding is object-type specific.

</blockquote>

</details>

---
    
41. Can "this" be used within a static method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
    
We can't use `this` in the static method because the keyword `this` returns a reference to the current instance of the class containing it. Static methods (or any static member) do not belong to a particular instance. They exist without creating an instance of the class and call with the name of a class not by instance so we can't use this keyword in the body of static Methods, but in the case of Extension Methods, we can use it as the parameters of the function.

</blockquote>

</details>
    
---
    
