## Technical

1. What is C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
C# is a general-purpose, high-level multi-paradigm programming language. C# encompasses static typing, strong typing, lexically scoped, imperative, declarative, functional, generic, object-oriented (class-based), and component-oriented programming disciplines.

</blockquote>

</details>

---

2. What are nullable types in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- C# provides special data types, the nullable types, to which you can assign a normal range of values as well as null values.

- For example, we can store any value from -2,147,483,648 to 2,147,483,647 or null in a `Nullable<Int32>` variable. Similarly, we can assign true, false, or null in a `Nullable<bool>` variable.

</blockquote>

</details>

---

3. What are variables?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Variables are named memory locations (memory cells) which are used to store the program’s input and its computational results during program execution. As the name suggests, the value of a variable may change during the program execution.

</blockquote>

</details>

---

4. What are dynamic type variables in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

We can store any type of value in the dynamic data type variable. Type checking for these types of variables takes place at run-time.

</blockquote>
</details>

---

5. What are reserved words?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Reserved words or keywords are words, which have predefined meanings. They have predefined uses and cannot be used or redefined for any other purpose in a programming language.

**Examples**
 - IF
 - ELSE
 - THEN

</blockquote>

</details>

---

6. What are Loops?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The loop is a structure which can repeat a set of statements up to a fixed number of times or until a certain criterion is satisfied. Name different types of loops.

</blockquote>

</details>

---

7.  What are constants?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A constant is a quantity whose value cannot be changed. Unlike a variable, the value stored in a constant can’t be modified during program execution.

Numeric constants consist of integers, single precision, or double-precision numbers. Integer constants represent values that are counted and do not have a fractional part, e.g., +56, -678.

A string constant is a sequence of alphanumeric characters enclosed in double quotation marks. The maximum length of a string constant is 255 characters. For example, 'New York`.

</blockquote>

</details>

---

8.  Define Operators.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Operators are symbols which are used to perform certain operations on data. These include arithmetic, relational, logical, and assignment operators.

</blockquote>

</details>

---

9.  What is an Array?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

An array is a data structure that stores a fixed number of literal values (elements) of the same data type. Array elements are stored contiguously in the memory.

In C#, an array can be of three types: single-dimensional, multidimensional, and jagged array. 

</blockquote>

</details>

---

10. What is the syntax to declare a namespace in .NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

In .NET, the namespace keyword is used to declare a namespace in the code. The syntax for declaring a namespace in C# is:

`namespace UserNameSpace;`

</blockquote>

</details>

---

11. What does a break statement do in the switch statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- The switch statement is a selection control statement that is used to handle multiple choices and transfer control to the case statements within its body. 

- The following code snippet shows an example of the use of the switch statement in C#:

```C#
switch(choice) {
     case 1: 
     console.WriteLine(First); 
     break; 
     
     case 2: 
     console.WriteLine(Second); 
     break; 
     
     default: 
     console.WriteLine(Wrong choice); 
     break; 
     }
```
In switch statements, the break statement is used at the end of a case statement. The break statement is mandatory in C# and it avoids the fall-through of one case statement to another.

</blockquote>

</details>

---

12. Can you briefly explain the characteristics of value-type variables that are supported in the C# programming language?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The variables that are based on value types directly contain values. The characteristics of value-type variables that are supported in C# programming language are as follows:

- All value-type variables derive implicitly from the `System.ValueTypeclass`.
- We cannot derive any new type from a value type.
- Value types have an implicit default constructor that initializes the default value of that type.
- The value type consists of two main categories:
  - Structs - Summarizes small groups of related variables.
  - Enumerations - Consists of a set of named constants.

</blockquote>

</details>

---

13. What is a parameter?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A parameter is a special kind of variable, which is used in a function to provide a piece of information or input to a caller function. These inputs are called arguments. In C#, the different types of parameters are as follows:
- Value type 
- Reference type 
- Output type 
- Optional parameter 

</blockquote>

</details>

---

14. Can you briefly explain the characteristics of reference-type variables that are supported in the C# programming language?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The variables are based on reference types of store references to the actual data. The keywords that are used to declare reference types are:
- **Class** - Refers to the primary building block for the programs, which is used to encapsulate variables and methods into a single unit.
- **Interface** - Contains only the signatures of methods, properties, events, or indexers.
- **Delegate** - Refers to a reference type that is used to encapsulate a named or anonymous method.

</blockquote>

</details>

---

15. What are the different types of literals in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The different types of literals in C# are:

- **Boolean literals** - Refers to the True and False literals that map to the true and false states, respectively.
- **Integer literals** - Refers to literals that are used to write values of types int, uint, long, and ulong.
- **Real literals** - Refers to literals that are used to write values of types of float, double, and decimal.
- **Character literals** - Represents a single character that usually consists of a character in quotes, such as 'a'.
- **String literals** - Refers to string literals, which can be of two types in C#:
  -  A regular string literal consists of zero or more characters enclosed in double quotes, such as hello.
  - A verbatim string literal consists of the @ character followed by a double-quote character, such as @hello.
- **The Null literal** - Represents the null-type.

</blockquote>

</details>

---

16. What is the difference between “continue” and “break” statements in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Using the `break` statement, we can jump out of a loop whereas by using the `continue` statement, we can jump over one iteration and then resume our loop execution.

</blockquote>

</details>

---

17. What’s the difference between the `System.Array.CopyTo()` and `System.Array.Clone()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The difference is - `System.Array.CopyTo()` requires a destination array to exist before and it must be capable to hold all the elements in the source array from the index that is specified to copy from the source array. On the other hand, `System.Array.Clone()` method does not require the destination array to exist as it creates a new one from scratch.

</blockquote>

</details>

---

18. What is the difference between `ToString()` and `Convert.ToString()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`ToString()` does not handle null values but `Convert.ToString()` will handle null values

</blockquote>

</details>

---

19.  What is the Difference between `int.Parse()` and `Convert.ToInt32()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`int.Parse()`  will convert only string to int.  `Convert.ToInt32()` is used to convert any datatype to an int type.

</blockquote>

</details>

---

20. What is the difference between `typeOf()` and `sizeOf()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- `TypeOf()` is used to get the Base Datatype name.

- `SizeOf()` is used to get the size of the Datatype.

</blockquote>

</details>

---

21. What is widening and narrowing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Widening is used to convert smaller datatype to longer datatype

**`Ex:int to long`**

The narrowing is used to convert longer datatypes to smaller Datatype

**`Ex:long to int`**

**Note::** Working with Narrowing is an unsafe type of programming.

</blockquote>

</details>

---

22. How to declare an array in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- To declare an array, define the variable type with square brackets:
`datatype[] arr_name;`

**For example:**
`string[] cars;`
- We have now declared a variable that holds an array of strings.

- To insert values to it, we can use an array literal - place the values in a comma-separated list, inside curly braces:

- `string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};`

</blockquote>

</details>

---

23. What are the different types of control statements in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

There are generally considered to be three main types of control statements, each serving different purposes. These include:

**Selection statements**, which enable us to branch to different sections of code.
**Iteration statements**, which enable us to loop through connections or perform the same series of operations repeatedly until a specified condition is met.
**Jump statements**, which enable control of flow to be shifted to another section of code.

</blockquote>

</details>

---

24. Can u differentiate String and StringBuilder in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A string object is immutable, meaning that it cannot be changed after it’s created. Any operation that tries to modify the string object will simply create a new string object. On the other hand, a string builder object is mutable and can be modified.

</blockquote>

</details>

---

25. What are Jagged Arrays?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The Array which comprises elements of a typed array is called a Jagged Array. The elements in Jagged Arrays can be of various dimensions and sizes.

</blockquote>

</details>

---

26.  What is the difference between `out` and `ref` parameters?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

When an argument is passed as a `ref`, it must be initialized before it can be passed to the method. An `out` parameter, on the other hand, need not be initialized before passing to a method.

</blockquote>

</details>

---

27. What is meant by garbage collection in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, garbage collection is the process of managing memory in an application. The garbage collector automatically disposes of memory that is no longer used to make memory available for new allocations.

</blockquote>

</details>
    
---

28. What is Stream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
A stream is a sequence of bytes travelling from a source to a destination over a communication path. There are two main streams: the input stream and the output stream. The input stream is used for reading data from the file (read operation) and the output stream is used for writing into the file (write operation). There are two types of streams used:

- **Input stream**: This stream is used to read data from a file, which is known as a read operation.
- **Output stream**: This stream is used to write data into a file, which is known as a write operation.

</blockquote>

</details>

---

29. Can you brief us on the `System.IO` namespace in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, the `System.IO` namespace contains the required classes which are used to handle the input and output streams and provide information about file and directory structure. The parent class of file processing is Stream. Stream is an abstract class, which is used as the parent of the classes that implement the necessary operations.

**Note**: The FileIno, DirectoryInfo, and DriveInfo classes have instance methods. File, Directory, and Path classes have static methods.

</blockquote>

</details>

---

30. What is FileStream Class in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The FileStream class in C# provides a stream for file operations. It can be used to perform both synchronous and asynchronous read and write operations. With the help of FileStream class, we can easily read and write data into files.

- To use FileStream class in C#, first of all, we need to include the System.IO namespace and then we need to create an instance of the FileStream object to create a new file or open an existing file.

</blockquote>

</details>

---


