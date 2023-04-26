1.What is the difference between Protected and Default access modifiers 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>
<b>Default:</b> Where the access level is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.

<b>Protected:</b> The access level is within the package and only through child class it can also be accessible outside the package.

   </blockquote>
</details>

---
2. What is a primitive data type 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

  A primitive type is predefined by the language and is named by a reserved keyword such as int, float,
boolean, byte, short, long, char and double.

   </blockquote>
</details>

---

3. what are access modifiers?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Which specifies the accessibility or scope of a field, method, constructor, or class when declared. We use 4 modifiers as Public, Private, Protected, Default in Java.

   </blockquote>
</details>

---

4. What are the OOP concepts? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

It is a programming paradigm that focuses on the use of objects to represent and manipulate data. Oops concepts in Java includes Abstraction, Polymorphism, Encapsulation and Inheritance.

   </blockquote>
</details>

---

5. What is the difference between final, finally, and finalize and what situations are they used in.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

 Final- Is used to restrict the modification of a variable or method or class.
 Finally- Will ensure a block of code will be exceuted even if the exception is thrown.
 Finalize- Cleanup action to be performed on an object before garbage collection.


</blockquote>
</details>

---

6. Can we invoke a non-static method from static method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

The only way to call a non-static method from a static method is to have an instance of the class containing the non-static method.

</blockquote>
</details>

---


 7. what is the difference between an Abstract class and an interface?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Abstract class can have abstract and non-abstract methods, Whereas interface can have only abstract methods. Since Java 8, it can have default and static methods also.
An abstract class can be extended using keyword "extends".Whereas an interface can be implemented using keyword "implements".

</blockquote>
</details>

---

8. If there are two statements in a try/catch block, the first statement catches an exception, will the second statement run or stop?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Stop. If exception occurs in try block then control immediately transfers to the catch block.

 </blockquote>
</details>

---

9. how do you remove duplicates from an arraylist?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Using Hashset datastructure we can remove duplicated in arraylist.(Set doesn't allow duplicates in Java)

 </blockquote>
</details>

---

10. is static public void main possible

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Yes, we can change the order of `public static void main()` to `static public void main()` in Java.(we can declare access modifiers in any order).

 </blockquote>
</details>

---

11. how do you call another constructor from a constructor? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

Which can be done in 2 ways:
- `this()` keyword: To call the constructor within the same class. 
- `super()` keyword: To call the superclass constructor from the base class.

 </blockquote>
</details>

---

12. what is the difference between the super keyword and this keyword regarding local variables 


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

- this keyword is to refer instance variable of current class
- super keyword is used to refer super-class’s instance as well as static members.

 </blockquote>
</details>

---

13. What are the control statements (ifelse, switch)

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

- Which is used to change the flow of execution of statements.
- ifelse- if the given condition is true, the statement inside if block will be executed or else block will be executed.
- switch-multi way branch statement based on the value of switch expression.

 </blockquote>
</details>

---

14. What is encapsulation in OOP 


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Which is about Packing of data variables and methods in single unit and preventing them from being accessed by other classes.

  </blockquote>
</details>

---

15. Explain fundamentals of java  


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Java is an object-oriented(which revolves around classes and objects), and platform independent language(can run anywhere).

  </blockquote>
</details>

---

16. what are the pillars in Java

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b>Show Answer</b></summary>

 <blockquote>

Java defines OOP concepts as following 4 pillars:
- Abstraction- Hiding the information 
- Encapsulation- Binding data variable and methods
- Inheritance- Properties of a class can be inherited into a sub class.
- Polymorphism- many forms

  </blockquote>
</details>

---

17. What is a constructor  

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Which is a special type of method to initialize an object in a class. By calling the constructor, memory for the object is allocated in the memory.

   </blockquote>
</details>

---

18. What is an abstract class  

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

The abstract class will be declared as abstract, which can have both abstract and non-abstract methods. It needs to be extended and its method implemented and it cannot be instantiated.

   </blockquote>
</details>

---

19. What is an interface  


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 Interface is an blueprint of a class used to specify the behavior of a class. A Java interface contains static constants and abstract methods. A class can implement multiple interfaces. In Java, interfaces are declared using the interface keyword. Which is used to achieve abstraction.

</blockquote>
</details>

---

20. what does the final keyword mean and how is it implemented  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

- Which is a non-access modifier, makes them non-changeable (impossible to inherit or override).
- The final keyword in java is used to restrict the user. The java final keyword can be used in a variable/method/class. 


</blockquote>
</details>

---

21. What is Exception handling , how is it done.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>


- Which is the powerful mechanism to handle the runtime errors so that the normal flow of the application cannot be interupted. It can be implemented by using try-catch block.
- try block is used to have a block of code that might throw an exception.
- catch block is used to handle the Exception by declaring the type of exception within the parameter


</blockquote>
</details>

---

22. Describe abstraction.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Abstraction is the process of hiding certain information and showing only essential details to the user.
Which can be achieved by using either abstract classes or interfaces.


</blockquote>
</details>

---

23. describe a class and an object   

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

- Objects- An object is an instance of a class, which have states and behaviors. Example: A dog has states - color, name, breed as well as behaviors -barking, eating. 
- Class − A class is a user-defined blueprint or prototype from which objects are created. 

</blockquote>
</details>

---

24. what is inheritance?    

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Which is a mechanism of one class acquires the property of another class. For example, a child class inherits the properties(variables/methods) of a parents class.

</blockquote>
</details>

---

25. Can you have multiple inheritance in Java?   

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote

No, Multiple inheritances is not allowed in java to prevent ambiguity.Which can be achieved using Interfaces.

</blockquote>
</details>

---

26. You can inheret from multiple interfaces, but can you do the same with classes? 

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 No, We cannot inherit from multiple classes as it will create ambiguity.Which is not supported in Java. 

</blockquote>
</details>

---

27. What is an object in java.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Which is a member (also called an instance) of a Java class. Each object has an identity, a behavior and a state.The state of an object is stored in fields (variables), while methods (functions) display the object's behavior.


</blockquote>
</details>

---

28. Difference between int and Integer in Java

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

- Int is one of the primitive datatype stores whole number
- Integer is an wrapper class that wraps a primitive type int in an object.


</blockquote>
</details>

---

29. Why use static? can you remove it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

Static is used mainly for managing memory in Java.Static method of a class can be called by using the class name only without creating an object of a class.

If you don't add the 'static' modifier in your main method, the proram will compile but will throw `NoSuchMethodError` error during execution. 

</blockquote>
</details>

---

30. What is collections API ?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

- The Collection API in Java is a framework that provides an architecture to store and manipulate the group of objects.Which has:
- Interfaces and its implementations, i.e., classes
- Algorithm

</blockquote>
</details>

---

31. What's unique about a map?  

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Map is an collection interface contains values on basis of key and value pair, which contains only unique keys. It may have one null key and multiple null values.

</blockquote>
</details>

---

32. What's unique about a set?   

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Set is an collection interface which is an unordered collection of objects where duplicate values cannot be stored. 

</blockquote>
</details>

---

33. Explain multithreading basics.

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

  Which allows parallel execution of two or more parts of a program for maximum utilization of CPU. Each part of such program is called a thread.

  </blockquote>
</details>

---

34. What does System.out.println() mean.

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 System.out.println() is a statement which display results on the monitor by taking the argument passed to it. 

   </blockquote>
</details>

---

35. What is private classes and can they be inherited

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

The access level of a private modifier is only within the class. It cannot be accessed from outside the class.So a subclass does not inherit the private members of its parent class.

   </blockquote>
</details>

---

36. whats are benefits of inheritance.

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

 - Main advantage of inheritance is Reusability.(When a class inherits or derives another class, it can access all the functionality of inherited class)
 - Reusability enhanced reliability. 
 - Avoiding Duplication of Code

    </blockquote>
</details>

---

37. what is wrapper class in java?

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Which converts primitive data types into object and object into primitive type.(through autoboxing and unboxing).

</blockquote>
</details>

---

38. How to implement interface in java

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

```java

   interface drawable{  
void draw();  
}  
class sketch implements drawable{  
public void draw(){System.out.println("Hello");}  
  
public static void main(String args[]){  
sketch  obj = new sketch ();  
obj.draw();  
 }  
}  
```
</blockquote>
</details>

---

39.  create an Arrays and give some values then print them  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

   <blockquote>

   ```java
   public class Array {

    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};

        for (int element: array) {
            System.out.println(element);
        }
    }
}
```

</blockquote>
</details>

---

40. What is Java explain in detail.

[Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

 <blockquote>

Java is an object-oriented programming language which is platform independent that produces software for multiple platforms.

</blockquote>
</details>

---
