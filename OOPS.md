1.Define OOP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Object-Oriented Programming System (OOPs) is a programming concept that works on the principles of abstraction, encapsulation, inheritance, and polymorphism. It allows users to create objects they want and create methods to handle those objects.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.Explain Object Oriented Programming Concepts?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

The object-oriented programming is basically a computer programming design philosophy or methodology that organizes/ models software design around data, or objects rather than functions and logic.
An object is referred to as a data field that has unique attributes and behavior. Everything in OOP is grouped as self-sustainable objects.It is the most popular programming model among developers. It is well suited for programs that are large, complex, and actively updated or maintained. It simplifies software development and maintenance by providing major concepts such as abstraction, inheritance, polymorphism, and encapsulation. These core concepts support OOP.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3.What is Polymorphism?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

Polymorphism in Java is a concept by which we can perform a single action in different ways. Polymorphism is derived from 2 Greek words: poly and morphs. The word "poly" means many and "morphs" means forms. So polymorphism means many forms.

There are two types of polymorphism in Java: compile-time polymorphism and runtime polymorphism. We can perform polymorphism in java by method overloading and method overriding.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4.What is encapsulation and why is it used? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

Encapsulation is a way to restrict the direct access to some components of an object, so users cannot access state values for all of the variables of a particular object. Encapsulation can be used to hide both data members and data functions or methods associated with an instantiated class or object.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.What is a constructor, and does it return a value? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

A constructor doesn't have any return type. The data type of the value retuned by a method may vary, return type of a method indicates this value. A constructor doesn't return any values explicitly, it returns the instance of the class to which it belongs.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6.How is a new object created? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

An object is created based on its class.When an object is created, memory is allocated to hold the object properties. An object reference pointing to that memory location is also created.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

7.What is inheritance and what does a class inherit? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

Inheritance is defined as a mechanism where the sub or child class inherits the properties and characteristics of the super class or other derived classes. It also supports additional features of extracting properties from the child class and using it into other derived classes.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------


8.Explain an abstract class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

A class which is declared as abstract is known as an abstract class. It can have abstract and non-abstract methods. It needs to be extended and its method implemented. It cannot be instantiated.
An abstract class must be declared with an abstract keyword.
It can have constructors and static methods also.It can have final methods which will force the subclass not to change the body of the method.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

9.Access modifiers and what they do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

The access modifiers in Java specifies the accessibility or scope of a field, method, constructor, or class. We can change the access level of fields, constructors, methods, and class by applying the access modifier on it.

There are four types of Java access modifiers:

Private: The access level of a private modifier is only within the class. It cannot be accessed from outside the class.
Default: The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.
Protected: The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.
Public: The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

10.Abstract vs Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

Abstract class can have abstract and non-abstract methods.Abstract class doesn't support multiple inheritance.Abstract class can have final, non-final, static and non-static variables.Abstract class can provide the implementation of interface.The abstract keyword is used to declare abstract class.	An abstract class can extend another Java class and implement multiple Java interfaces.	
An abstract class can be extended using keyword "extends".	
A Java abstract class can have class members like private, protected, etc.	

Interface can have only abstract methods. Since Java 8, it can have default and static methods also.Interface supports multiple inheritance.Interface has only static and final variables.Interface can't provide the implementation of abstract class.The interface keyword is used to declare interface.An interface can extend another Java interface only.An interface can be implemented using keyword "implements".Members of a Java interface are public by default.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

11. Overloading vs overriding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

Method overloading is used to increase the readability of the program.It is performed within class and parameter must be different.Method overloading is the example of compile time polymorphism.Method overloading can't be performed by changing return type of the method only. Return type can be same or different in method overloading. But you must have to change the parameter.	

Method overriding is used to provide the specific implementation of the method that is already provided by its super class.Method overriding occurs in two classes that have IS-A (inheritance) relationship and  parameter must be same.Method overriding is the example of run time polymorphism.Return type must be same or covariant in method overriding.

</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

