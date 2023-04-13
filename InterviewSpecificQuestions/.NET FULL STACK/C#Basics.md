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

A nullable value type `T?` represents all values of its underlying value type T and an additional null value. For example, you can assign any of the following three values to a `bool? variable: true, false, or null`. An underlying value type T cannot be a nullable value type itself.

Any nullable value type is an instance of the generic `System.Nullable<T>` structure. You can refer to a nullable value type with an underlying type T in any of the following interchangeable forms: `Nullable<T> or T?`.

```C#

double? pi = 3.14;
char? letter = 'a';

int m2 = 10;
int? m = m2;

bool? flag = null;

// An array of a nullable value type:
int?[] arr = new int?[10];

```
The default value of a nullable value type represents null, that is, it's an instance whose `Nullable<T>`.HasValue property returns false.

</blockquote>

</details>

---

3. What are variables?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Variables represent storage locations. Every variable has a type that determines what values can be stored in the variable. C# is a type-safe language, and the C# compiler guarantees that values stored in variables are always of the appropriate type. The value of a variable can be changed through assignment or through use of the ++ and -- operators.

C# defines seven categories of variables: static variables, instance variables, array elements, value parameters, reference parameters, output parameters, and local variables. The subclauses that follow describe each of these categories.

```C#

class A
{
    public static int x;
    int y;

    void F(int[] v, int a, ref int b, out int c)
    {
        int i = 1;
        c = a + b++;
    }
}

```

In the above example x is a static variable, y is an instance variable, v[0] is an array element, a is a value parameter, b is a reference parameter, c is an output parameter, and i is a local variable.

</blockquote>

</details>

---

4. What are dynamic type variables in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The dynamic type is a static type, but an object of type dynamic bypasses static type checking. In most cases, it functions like it has type object. The compiler assumes a dynamic element supports any operation.

For example, if instance method exampleMethod1 in the following code has only one parameter, the compiler recognizes that the first call to the method, ec.exampleMethod1(10, 4), isn't valid because it contains two arguments. The call causes a compiler error. The compiler doesn't check the second call to the method, dynamic_ec.exampleMethod1(10, 4), because the type of dynamic_ec is dynamic. Therefore, no compiler error is reported. However, the error doesn't escape notice indefinitely. It appears at run time and causes a run-time exception.

```C#

static void Main(string[] args)
{
    ExampleClass ec = new ExampleClass();
    // The following call to exampleMethod1 causes a compiler error
    // if exampleMethod1 has only one parameter. Uncomment the line
    // to see the error.
    //ec.exampleMethod1(10, 4);

    dynamic dynamic_ec = new ExampleClass();
    // The following line is not identified as an error by the
    // compiler, but it causes a run-time exception.
    dynamic_ec.exampleMethod1(10, 4);

    // The following calls also do not cause compiler errors, whether
    // appropriate methods exist or not.
    dynamic_ec.someMethod("some argument", 7, null);
    dynamic_ec.nonexistentMethod();
}

class ExampleClass
{
    public ExampleClass() { }
    public ExampleClass(int v) { }

    public void exampleMethod1(int i) { }

    public void exampleMethod2(string str) { }
}

```

</blockquote>
</details>

---

5. What are reserved words?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Keywords are predefined, reserved identifiers that have special meanings to the compiler. They can't be used as identifiers in your program unless they include @ as a prefix. For example, `@if` is a valid identifier, but if isn't because if is a keyword.

A contextual keyword is used to provide a specific meaning in the code, but it isn't a reserved word in C#. Some contextual keywords, such as partial and where, have special meanings in two or more contexts.

</blockquote>

</details>

---

6. What are Loops?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The iteration statements repeatedly execute a statement or a block of statements. The for statement: executes its body while a specified Boolean expression evaluates to true. The foreach statement: enumerates the elements of a collection and executes its body for each element of the collection. The do statement: conditionally executes its body one or more times. The while statement: conditionally executes its body zero or more times.

At any point within the body of an iteration statement, you can break out of the loop using the break statement. You can step to the next iteration in the loop using the continue statement.

```C#

int i;
int j = 3;
for (i = 0, Console.WriteLine($"Start: i={i}, j={j}"); i < j; i++, j--, Console.WriteLine($"Step: i={i}, j={j}"))
{
    //...
}
// Output:
// Start: i=0, j=3
// Step: i=1, j=2
// Step: i=2, j=1

```

</blockquote>

</details>

---

7.  What are constants?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Constants are immutable values which are known at compile time and do not change for the life of the program. Constants are declared with the const modifier. Only the C# built-in types (excluding System.Object) may be declared as const. User-defined types, including classes, structs, and arrays, cannot be const. Use the readonly modifier to create a class, struct, or array that is initialized one time at run time (for example in a constructor) and thereafter cannot be changed.

C# does not support const methods, properties, or events.

```C#

class Calendar1
{
    public const int Months = 12;
}

```

In this example, the constant Months is always 12, and it cannot be changed even by the class itself. 

</blockquote>

</details>

---

8.  Define Operators.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

C# provides a number of operators. Many of them are supported by the built-in types and allow you to perform basic operations with values of those types. Those operators include the following groups:

`Arithmetic operators` that perform arithmetic operations with numeric operands.
`Comparison operators` that compare numeric operands.
`Boolean logical operators` that perform logical operations with bool operands.
`Bitwise and shift operators` that perform bitwise or shift operations with operands of the integral types.
`Equality operators` that check if their operands are equal or not.

</blockquote>

</details>

---

9.  What is an Array?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

You can store multiple variables of the same type in an array data structure. You declare an array by specifying the type of its elements. If you want the array to store elements of any type, you can specify object as its type. In the unified type system of C#, all types, predefined and user-defined, reference types and value types, inherit directly or indirectly from Object.

The following example creates single-dimensional, multidimensional, and jagged arrays:

```C#

class TestArraysClass
{
    static void Main()
    {
        // Declare a single-dimensional array of 5 integers.
        int[] array1 = new int[5];

        // Declare and set array element values.
        int[] array2 = new int[] { 1, 3, 5, 7, 9 };

        // Alternative syntax.
        int[] array3 = { 1, 2, 3, 4, 5, 6 };

        // Declare a two dimensional array.
        int[,] multiDimensionalArray1 = new int[2, 3];

        // Declare and set array element values.
        int[,] multiDimensionalArray2 = { { 1, 2, 3 }, { 4, 5, 6 } };

        // Declare a jagged array.
        int[][] jaggedArray = new int[6][];

        // Set the values of the first array in the jagged array structure.
        jaggedArray[0] = new int[4] { 1, 2, 3, 4 };
    }
}

```


</blockquote>

</details>

---

10. What is the syntax to declare a namespace in .NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Namespaces are heavily used in C# programming in two ways. First, .NET uses namespaces to organize its many classes, as follows:

```C#
System.Console.WriteLine("Hello World!");
```

`System` is a namespace and `Console` is a class in that namespace. The `using` keyword can be used so that the complete name isn't required, as in the following example:

```C#
using System;
```
```C#
Console.WriteLine("Hello World!");
```
Second, declaring your own namespaces can help you control the scope of class and method names in larger programming projects. Use the namespace keyword to declare a namespace, as in the following example:

```C#
namespace SampleNamespace
{
    class SampleClass
    {
        public void SampleMethod()
        {
            System.Console.WriteLine(
                "SampleMethod inside SampleNamespace");
        }
    }
}
```
The name of the namespace must be a valid C# identifier name.

</blockquote>

</details>

---

11. What does a break statement do in the switch statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

```C#

switch ( expression )
{
    // declarations
    // . . .
    case constant_expression:
        // statements executed if the expression equals the
        // value of this constant_expression
        break;
    default:
        // statements executed if expression does not equal
        // any case constant_expression
}

```

You can use the break statement to end processing of a particular labeled statement within the switch statement. It branches to the end of the switch statement. Without break, the program continues to the next labeled statement, executing the statements until a break or the end of the statement is reached. This continuation may be desirable in some situations.

</blockquote>

</details>

---

12. Can you briefly explain the characteristics of value-type variables that are supported in the C# programming language?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A variable of a value type contains an instance of the type. This differs from a variable of a reference type, which contains a reference to an instance of the type. By default, on assignment, passing an argument to a method, and returning a method result, variable values are copied. In the case of value-type variables, the corresponding type instances are copied. The following example demonstrates that behavior:

```C#
using System;

public struct MutablePoint
{
    public int X;
    public int Y;

    public MutablePoint(int x, int y) => (X, Y) = (x, y);

    public override string ToString() => $"({X}, {Y})";
}

public class Program
{
    public static void Main()
    {
        var p1 = new MutablePoint(1, 2);
        var p2 = p1;
        p2.Y = 200;
        Console.WriteLine($"{nameof(p1)} after {nameof(p2)} is modified: {p1}");
        Console.WriteLine($"{nameof(p2)}: {p2}");

        MutateAndDisplay(p2);
        Console.WriteLine($"{nameof(p2)} after passing to a method: {p2}");
    }

    private static void MutateAndDisplay(MutablePoint p)
    {
        p.X = 100;
        Console.WriteLine($"Point mutated in a method: {p}");
    }
}
// Expected output:
// p1 after p2 is modified: (1, 2)
// p2: (1, 200)
// Point mutated in a method: (100, 200)
// p2 after passing to a method: (1, 200)

```
As the preceding example shows, operations on a value-type variable affect only that instance of the value type, stored in the variable.

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

Variables of reference types store references to their data (objects), while variables of value types directly contain their data. With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable. With value types, each variable has its own copy of the data, and it's not possible for operations on one variable to affect the other (except in the case of `in, ref, and out` parameter variables; see in, ref, and out parameter modifier).

The following keywords are used to declare reference types:
- class
- interface
- delegate
- record

C# also provides the following built-in reference types:
- dynamic
- object
- string

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

16. What is the difference between `continue` and `break` statements in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The break statement terminates the closest enclosing iteration statement (that is, for, foreach, while, or do loop) or switch statement. The break statement transfers control to the statement that follows the terminated statement, if any.

```C#
int[] numbers = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
foreach (int number in numbers)
{
    if (number == 3)
    {
        break;
    }

    Console.Write($"{number} ");
}
Console.WriteLine();
Console.WriteLine("End of the example.");
// Output:
// 0 1 2 
// End of the example.
```

The continue statement starts a new iteration of the closest enclosing iteration statement (that is, for, foreach, while, or do loop), as the following example shows:

```C#

for (int i = 0; i < 5; i++)
{
    Console.Write($"Iteration {i}: ");
    
    if (i < 3)
    {
        Console.WriteLine("skip");
        continue;
    }
    
    Console.WriteLine("done");
}
// Output:
// Iteration 0: skip
// Iteration 1: skip
// Iteration 2: skip
// Iteration 3: done
// Iteration 4: done

```

</blockquote>

</details>

---

17. What’s the difference between the `System.Array.CopyTo()` and `System.Array.Clone()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`Array.CopyTo( )`:

The CopyTo method of the array class copies all the data in the array to an existing array. It performs a shallow copy. It is used to copy a one-dimensional array. It copies the complete content of the array to the new array starting from the index passed in the parameter.

```C#
class Educative
{
    static void Main()
    {
      var arr1 = new[] { "Lodhi", "Educative", "Faheem", "Welcomes","You" };
      var arr2= new string[10];
      arr2[0]="Ed Tech";
      // cloning arr and storing it in new array
      arr1.CopyTo(arr2,1);
      // Printing array using loop
      foreach (var element in arr2)
      {
        System.Console.WriteLine(element);
      }

      }
}
```

- Line 5: We initialize an array arr1 of size 5.
- Lines 6–7: We initialize an array arr2 with a memory allocation of 10 indexes and assign the first index with a string "Ed Tech."
- Line 9: We call the copyto() method of arr1 copying its elements to arr2 starting with index 1.
- Lines 11–14: We print the elements of the array arr2.

`Array.Clone( )`

The Clone() method of the Array class copies all the data in the array and returns a new object. It needs to be typecast to the datatype of the original array. It performs a shallow copy. It can also be used to make copies of multi-dimensional arrays. It copies the complete content of the array stored in the new array.

```C#
class Educative
{
    static void Main()
    {
      
      var arr = new[] { "Lodhi", "Educative", "Faheem", "Welcomes","You" };
      
      // cloning arr and storing it in new array
      var new_arr = (string[])arr.Clone();
  
      // Printing array using loop
      foreach (var element in new_arr)
      {
        System.Console.WriteLine(element);
      }

      }
}
```

</blockquote>

</details>

---

18. What is the difference between `ToString()` and `Convert.ToString()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

 Both methods are used to convert a string. But, yes, there is a difference between both the method and the main difference between both the methods is that `Convert.ToString()` method handles the NULL whereas `.ToString()` method does not handle the NULL and throws a NULL reference exception.

When you use the `.ToString()` method, this method expects that the value must not be NULL otherwise, it will throw an error.

```C#
using System;

namespace Tutorialsrack
{
    class Program
    {
        /* Difference Between Convert.ToString() and .ToString() Method in C# */
        static void Main(string[] args)
        {

            object obj1 = null;
            string str = null;

            //Convert using Convert.ToString()

            //When Object is Null
            string str1 = Convert.ToString(obj1);
            // Output ==> it will return empty string ""

            //When String is Null
            string str2 = Convert.ToString(str);
            // Output ==> it will return 'null'

            //Hit ENTER to exit the program
            Console.ReadKey();
        }
    }
}
```

```C#
using System;

namespace Tutorialsrack
{
    class Program
    {
        /* Difference Between Convert.ToString() and .ToString() Method in C# */
        static void Main(string[] args)
        {

            object obj1 = null;
            string str = null;

            //Convert using .ToString() Method

            //When Object is Null
            string str1 = obj1.ToString();
            // Ouptut ==> it will throw an Null reference exception

            //When String is Null
            string str2 = str.ToString();
            // Output ==> it will throw an Null reference exception

            //Hit ENTER to exit the program
            Console.ReadKey();
        }
    }
}
```
So, it is a good programming practice to use `Convert.ToString()` method over the `.ToString()` method. 

</blockquote>

</details>

---

19.  What is the difference between `int.Parse()` and `Convert.ToInt32()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The `int.Parse()` method converts a given string representation of a number to its equivalent integer:
```C#
var inputString = " 123 ";
var outputInteger = int.Parse(inputString);
```
We pass the inputString parameter in the `int.Parse()` method. It returns the equivalent integer to the variable outputInteger. The `int.Parse()` method has an overload that can take other parameter types. We can set the specific style and culture-specific format as well.

`Convert.ToInt32()` is also a method that converts a string into its corresponding integer just like the `int.Parse()` method:
```C#
var inputString = " 123 ";
var outputInteger = Convert.ToInt32(inputString);
```
We pass the same string inputString to the `Convert.ToInt32()` method. It sets the desired integer to the variable outputInteger.

</blockquote>

</details>

---

20. What is the difference between `typeOf()` and `sizeOf()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- The C# `typeof` operator (GetType operator in Visual Basic) is used to get a Type object representing String
- The `sizeof()` operator is used to obtain the size of a data type in bytes in bytes. It will not return the size of the variables or instances. Its return type is always int.

**Syntax**:
```C#
int sizeof(type);
```

</blockquote>

</details>

---

21. What is widening and narrowing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Widening conversion occurs when a value of one type is converted to another type that is of equal or greater size. A narrowing conversion occurs when a value of one type is converted to a value of another type that is of a smaller size. 

</blockquote>

</details>

---

22. What is the purppose of `Params` keyword?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

`params` is used as a parameter which can take the VARIABLE NUMBER OF ARGUMENTS. 

```C#
class Program
{
  static void Main(string[] args)
  {
    int y=Add(5,10,15,20);
    Console.WriteLine(y);
    Console.ReadLine();
  }

  public static int Add(params int[] listNumbers)
  {
    int total=0;
    foreach(int i in listNumbers)
    {
      total+=i;
    }
    return total;
  }
}

```

It is useful when programmer don’t have any prior knowledge about the number of parameters to be passed.

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

If we have to perform two or three string concatenations, or read and compare values then use a String.

If we have to make repeated modifications to a string or concatenate many strings then StringBuilder must be used, as it will increase the performance by not creating a new instance each time, unlike String.



</blockquote>

</details>

---

25. What are Jagged Arrays?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

A jagged array is an array whose elements are arrays, possibly of different sizes. A jagged array is sometimes called an "array of arrays." The following examples show how to declare, initialize, and access jagged arrays.

```C#
class ArrayTest
{
    static void Main()
    {
        // Declare the array of two elements.
        int[][] arr = new int[2][];

        // Initialize the elements.
        arr[0] = new int[5] { 1, 3, 5, 7, 9 };
        arr[1] = new int[4] { 2, 4, 6, 8 };

        // Display the array elements.
        for (int i = 0; i < arr.Length; i++)
        {
            System.Console.Write("Element({0}): ", i);

            for (int j = 0; j < arr[i].Length; j++)
            {
                System.Console.Write("{0}{1}", arr[i][j], j == (arr[i].Length - 1) ? "" : " ");
            }
            System.Console.WriteLine();
        }
        // Keep the console window open in debug mode.
        System.Console.WriteLine("Press any key to exit.");
        System.Console.ReadKey();
    }
}
/* Output:
    Element(0): 1 3 5 7 9
    Element(1): 2 4 6 8
*/
```

</blockquote>

</details>

---

26.  What is the difference between `out` and `ref` parameters?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The `ref` keyword indicates that a variable is a reference, or an alias for another object. It's used in five different contexts:

- In a method signature and in a method call, to pass an argument to a method by reference. For more information, see Passing an argument by reference.
- In a method signature, to return a value to the caller by reference. For more information, see Reference return values.
- In a member body, to indicate that a reference return value is stored locally as a reference that the caller intends to modify. Or to indicate that a local variable accesses another value by reference. For more information, see Ref locals.
- In a struct declaration, to declare a ref struct or a readonly ref struct. 
- In a ref struct declaration, to declare that a field is a reference. 

The `out` keyword causes arguments to be passed by reference. It makes the formal parameter an alias for the argument, which must be a variable. In other words, any operation on the parameter is made on the argument. It is like the ref keyword, except that ref requires that the variable be initialized before it is passed. It is also like the in keyword, except that in does not allow the called method to modify the argument value. To use an `out` parameter, both the method definition and the calling method must explicitly use the out keyword. 


</blockquote>

</details>

---

27. What is meant by garbage collection in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Garbage collection is a memory management technique used in the .NET Framework and many other programming languages. In C#, the garbage collector is responsible for managing memory and automatically freeing up memory that is no longer being used by the application.

The garbage collector works by periodically scanning the application’s memory to determine which objects are still being used and which are no longer needed. Objects that are no longer being used are marked for garbage collection, and their memory is freed up automatically by the garbage collector.

</blockquote>

</details>
    
---

28. What is Stream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
There are two purpose of using keyword in C#:

**USING DIRECTIVE**
` using System.IO;`
**USING STATEMENT**
The using statement ensures that `DISPOSE()` method of the class object is called even if an exception occurs.
This is mostly used while creating database connections.

Below code will make sure that connection.Dispose will be called even if it is not written

```C#
static void Main(string[] args)
{
  using(var connection=new SqlConnection("ConnectionString"));
  {
    var query="UPDATE YourTable SET Property=Value";
    var command=new SqlCommand(query,connection);
    connection.Open();
    command.ExecuteNonQuery();

    //connection.Dispose();
  }
}
```

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

30. What is the difference between `IS` and `AS` operator?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The `IS operator` is USED TO CHECK the type of an object.

```C#
static void Main(string[] args)
{
  int i=5;
  bool check=i is int;
  Console.Write(str1);
  Console.ReadLine();
}
//Output: true
```

`AS operator` is used to PERFORM CONVERSION between compatible 
reference type

```C#
static void Main(string[] args)
{
  object obj="Hello";
  string str1=obj as string;
  Console.Write(str1);
  Console.ReadLine();
}
//Output:Hello
```
</blockquote>

</details>

---


