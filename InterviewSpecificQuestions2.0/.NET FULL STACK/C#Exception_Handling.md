## Technical

1. What are the different types of errors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

When we write and execute our code in the .NET framework then there is a possibility of two types of error occurrences. They are as follows:

- Compilation Errors
- Runtime Errors

</blockquote> 

</details>

---

2. What is an Exception in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

An Exception is a class in C# which is responsible for the abnormal termination of the program when runtime errors occur while running the program.  So, these errors (runtime) are very dangerous because whenever the runtime errors occur in the programs, the program gets terminated abnormally on the same line where the error gets occurred without executing the next line of code.

**Note**: Most people are saying Runtime Errors are Exceptions which is not true. Exceptions are classes that are responsible for the abnormal termination of the program when runtime errors occur.

</blockquote>

</details>

---

3. Who is Responsible for the Abnormal Termination of the Program whenever Runtime Errors occur?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Objects of Exception classes are responsible for the abnormal termination of the program whenever runtime errors occur. These exception classes are predefined under BCL (Base Class Libraries) where a separate class is provided for every different type of exception like,

- IndexOutOfRangeException
- FormatException
- NullReferenceException 

**Note**: Exception class is the superclass of all Exception classes in C#.

</blockquote>

</details>

---

4. What is Exception Handling in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The process of catching the exception for converting the CLR-given exception message to an end-user understandable message and for stopping the abnormal termination of the program whenever runtime errors are occurring is called Exception Handling in C#. Once we handle an exception under a program, we will get the following advantages: -

- We can stop the Abnormal Termination
- We can perform any corrective action that may resolve the problem.
- Displaying a user-friendly error message, so that the user can resolve the problem provided if it is under his control.

</blockquote>

</details>

---

5. What is the procedure to handle Exceptions in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Exception Handling in C# is a 4 steps procedure:

- Preparing the exception object that is appropriate to the current logical mistake.
- Throwing that exception to the appropriate exception handler.
- Catching that exception.
- Taking necessary actions against that exception.

</blockquote>

</details>

---

6.  How is exception handling performed in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In C#, exception handling helps detect errors in code at runtime. The process is implemented using four different keywords:

`<Try>` identifies blocks of code where exceptions are activated
`<Catch>` catches the exceptions that have been identified by <Try>
`<Finally>` executes a given set of statements depending on whether an exception is thrown out or not
`<Throw>` removes the exception

</blockquote>

</details>

---

7. What is the difference between a throw exception and a throw clause in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The fundamental difference is that throw exceptions overwrite the stack trace, whereas throw clauses retain the stack information. As such, it is much harder to retrieve the original code responsible for throwing the exception with throw exceptions. 

</blockquote>

</details>

---

8. What are Custom Exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Sometimes there are some errors that need to be handled as per user requirements. Custom exceptions are used for them and are used as defined exceptions.

**Example**

```C#

using System;
class InvalidAgeException : Exception {
    public InvalidAgeException() : base() {}
    public InvalidAgeException(string msg) : base(msg) {}
}
class Person {
    private int age;
    public int Age
    {
        set {
            if ( value &gt;= 19 &amp;&amp; value &lt;= 60 )
                age = value;
            else{
                InvalidAgeException expObj = new InvalidAgeException("The Age input has to be with 19 to 60");
                throw expObj;
                }
            }
        get {
            return age;
            }
    }
}
class Test {
    public static void Main(string []args) {
        Person personObj = new Person();
        Console.Write("Enter the age : ");
        try {
            string ageInput = Console.ReadLine();
            /* convert the string value into int value
            with the help of int.parse() method */
            personObj.Age = int.Parse( ageInput );
            Console.WriteLine("Valid age input");
            }
        catch(InvalidAgeException expObj){
            Console.WriteLine( expObj.Message );
            }
    }
}

```

</blockquote>

</details>

---

9. Can multiple catch blocks be executed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

No, Multiple catch blocks can't be executed. Once the proper catch code is executed, the control is transferred to the finally block and then the code that follows the finally block gets executed.

</blockquote>

</details>

---

10. Why do we use `finally` block in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`Finally` block will be executed irrespective of exception. So, while executing the code in the try block when an exception occurs, control is returned to the catch block and at last, finally block will be executed. So, closing the connection to the database / releasing the file handlers can be kept in the finally block.

</blockquote>

</details>

---

11. What is the base class from which all the exceptions are derived?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`System.Exception`

</blockquote>

</details>

---
 

12. Does finally get executed if the code throws an error?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Yes, Finally block will get executed always.
 
</blockquote>

</details>

---

13. What is the difference between System exceptions and Application exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- System exceptions are derived directly from a base class `System.SystemException`. A System-level Exception is normally thrown when a nonrecoverable error has occurred.
- Application exceptions can be user-defined exceptions thrown by the applications. If you are designing an application that needs to create its own exceptions class, you are advised to derive custom exceptions from the `System.ApplicationException` class. It is typically thrown when a recoverable error has occurred.
 
</blockquote>

</details>

---

14. What is the difference between throw and throw ex?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

throw statement preserves the original error stack information but in throw ex, stack error of exception will be replaced with a stack trace starting with rethrow point.

</blockquote>

</details>

---

15. Will it be possible to keep the statements after the ‘finally’ block if the control is returning from the finally block itself?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

This will result in an unreachable catch block error. This is because the control will be returning from the `finally` block itself. The compiler will fail to execute the code after the line with the exception. That is why the execution will show an unreachable code error. 

</blockquote>

</details>

---

16. Explain an unreachable catch block error.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the case of multiple catch blocks, the order in which catch blocks are placed is from the most specific to the most general ones. That is, the subclasses of an exception should come first, and then the super classes will follow. In case the super classes are kept first, followed by the sub classes after it, the compiler will show an unreachable catch block error.

</blockquote>

</details>

---

17. In how many ways can we handle exceptions in C#?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Three ways we are handling the exceptions 

- Application Level
- Page Level
- Code Level

In addition to the above IIS custom handlers.

</blockquote>

</details>

---

18. What is the need of handling exceptions at three levels in C#.Net?
(or)
What is the difference between Code Level, Pagelevel or Application-Level Exception handling?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

**Code Level**: Using try, catch and finally blocks to handle the exceptions 

```C#

try
{
    //block of code
}
catch (Exception e)
{
    
}
finally
{
  
}
```

**Page Level**:

- Here also we have try, catch and finally blocks but these blocks are optional.
- We need to add the below event in the page.

```C#

void Application_Error(object sender, EventArgs e)
{
    Exception exc = Server.GetLastError();
    _________________
    _________________
}
```

- If the exception not handling at the code level, it will come to the above page level

**Application Level**:

- Here also we have try, catch and finally blocks  

- This kind of Exception will be handled in two ways

  - Using WebConfig file.
  - Using Global.asax file.

- **Using WebConfig file**:

```C#

<system.web>
    <customErrors mode="On" defaultRedirect="Page URL">
      <error statusCode="500" redirect="Page URL"/>
    </customErrors>
  </system.web>
```

- **Using Global.asax file**:

- Needs to place the below handler in  `Global.asax` file

```C#

void Application_Error(object sender, EventArgs e)
{
    Exception exc = Server.GetLastError();
    _________________
    _________________
}
```

- If an exception is not handled at the code level and page level, then it will come to the application level.

</blockquote>

</details>

---

19. Do we catch all the exceptions in C#.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Some uncatchable exceptions exist in C#.Net.

**Examples** : OutOfMemoryException and StackOverflowException etc..

</blockquote>

</details>

---
