## Technical

1. Why Java is not a pure object oriented language?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Java contains primitive data types like char, boolean, byte, short, int, long, float, double which are not object and hence it is not a pure object oriented language.

</blockquote>

</details>

---

2. Which is related to real life entities in object oriented programming langauage.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- An object is a basic unit of Object-Oriented Programming that represents real-life entities, which has its state and behavior.

- Example - A dog is an object because it has states like color, name, breed, etc. as well as behaviors like barking, eating, etc.


</blockquote>

</details>

---

3. Which feature in object oriented programming langauage will show only the important deatils?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Data Abstraction is defined as the process of identifying and displaying only the required characteristics of an object to the user and ignoring the irrelevant details.

- Example - A car is viewed as a car rather than its individual components.

</blockquote>

</details>

---

4. Which acts as protective shield in object oriented programming langauage?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Encapsulation is defined as the wrapping up of data under a single unit. It is the mechanism that binds together the code and the data it manipulates. which also prevents the data from being accessed by the code outside. 


</blockquote>

</details>

---

5. How to achieve encapsulation in a Java program?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It can be achieved by declaring all the variables in a class as private and public methods in the class to set and get the values of the variables.

</blockquote>

</details>

---

6. How to achieve abstraction in a Java program?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It is achieved by interfaces and abstract classes. We can achieve 100% abstraction using interface in Java.

</blockquote>

</details>

---

7. Which feature is used to reuse the contents in one class to other class in object oriented programming langauage?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Inheritance is the mechanism in Java by which one class is allowed to inherit the features (fields and methods) of another class. 

</blockquote>

</details>

---

8. Which feature in object-oriented programming languages is used to differentiate between entities with the same name efficiently?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Polymorphism can be used to differntiate between entities with the help of the signature and declaration of these entities.

- Which is also defined as <b>many forms</b> (methods to perform different tasks)

</blockquote>

</details>

---

9. Assume that A is a class with 3 functions with same name and different arguments , how do you call these feature in object-oriented programming languages ?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Overloading concept, which is a type of polymorphism . Accepts same method name with different argyments in a class.

</blockquote>

</details>

---

10. How can we change the super class method according to the requirements of sub class in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It can be done by method overriding , which is a type of polymorphism. It can modify a super class method in the sub class.

</blockquote>

</details>

---

11. What happens if we change the arguments of overriding method?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

If we change the arguments of overriding method, then it will be treated as overloaded not overridden method in Java.

</blockquote>

</details>

---

12. It is possible to change the return type of overriding method from Number type to Integer type?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes. You can change ,as Integer is a sub class of Number type.

</blockquote>

</details>

---

13. How do you refer super class version of overridden method in the sub class?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Using `super` keyword, we can refer super class version of overridden method in the sub class.

</blockquote>

</details>

---

14. Which is a kind of class that contains only constants and abstract methods?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The interface in java is a mechanism to achieve abstraction. There can be only abstract methods in the java interface without the method body.

</blockquote>

</details>

---

15. Which modifiers are allowed for methods in an interface?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

 Only abstract and public modifiers are allowed for methods in interfaces.

 </blockquote>

</details>

---

16. Suppose B is an interface. Can we create an object using new B()?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

No, we cannot create an object of interface using new operator. But we can create a reference of interface which refers to objects of its implementation classes.

 </blockquote>

</details>

---

17. Can we define private and protected modifiers for fields in interfaces?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>


No, we cannot define private and protected modifiers for variables in interface because the fields (data members) declared in an interface are by default public, static, and final.

 </blockquote>

</details>

---

18. Is it possible to define an interface with a static modifier?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

Yes, from Java 8 onwards, we can define static and default methods in an interface. Prior to Java 8, it was not allowed.

 </blockquote>

</details>

---

19. Can an interface extends another interface in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

 Yes, an interface can extend another interface in Java.

</blockquote>

</details>

---

20. Does an interface implement another interface?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

No, an interface cannot implement another interface in Java

</blockquote>

</details>

---

21. Is it possible to define a class inside an interface in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote

Yes, we can define a class inside an interface.

</blockquote>

</details>

---

22. What happens if a class has implemented an interface but has not provided implementation for that method defined in Interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

The class has to be declared with an abstract modifier, which will be enforced by the Java compiler.

</blockquote>

</details>

---

23. Can a method within an interface be marked as final?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

No, it will result in compilation error, because a final method cannot be overridden in Java. But an interface method should be implemented by another class.

</blockquote>

</details>

---

24. Is it possible to re-assign a value to a variable of interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

 No, variables defined inside the interface are static and final by default, like constants. We can’t change their value once they declared.

</blockquote>

</details>

---

25. What type of a variable in an interface should be?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 Yes, we can define variable in an interface that must be declared as implicitly static and final.

 
</blockquote>

</details>

---

26. Is it necessary to implement all abstract methods of an interface?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, all the abstract methods defined in interface must be implemented.

</blockquote>

</details>

---

27. Explain about Marker Interface in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It doesn’t have any data members or methods in java. For example, Serializable, Cloneable etc.


</blockquote>

</details>

---

28. Can we declare a class as Abstract without having any abstract method?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes we can create an abstract class by using abstract keyword before class name even if it doesn’t have any abstract method.If a class has even one abstract method, it must be declared as abstract otherwise it will give an error.

</blockquote>

</details>

---

29. How can we pass arguments to a function by reference or pass by value in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 In java, we can pass argument to a function only by value and not by reference.

 </blockquote>

</details>

---

30. Can we call the constructor of a class more than once for an object?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It’s called only once for an object automatically at the time of object creation using new keyword. we can’t invoke the constructor again for an object after its creation.

</blockquote>

</details>

---

31. There are two classes named classBird and classParrot. Both classes are in the same package. Can a private member of classBird can be accessed by an object of classParrot?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, Private members of a class are not accessible outside the scope of that class and any other class even in the same package cannot access them in Java

 </blockquote>

</details>

---

32. How can we make copy of a java object?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can use the concept of cloning to create copy of an object. Using clone, we create copies with the actual state of an object by implementing Cloneable interface. 

 </blockquote>

</details>

---

33. How can we stop inherting a class from other class in Java?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If we want a class not to be extended further by any class, we can use the keyword `Final` with the class name.

In the following example, Stone class is Final and can’t be extended

``` java
public Final Class Stone {
	// Class methods and Variables
}
```

 </blockquote>

</details>

---

34. Can we use a default constructor of a class even if an explicit constructor is defined?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. Java provides a default no argument constructor if no explicit constructor is defined in a class. But if an explicit constructor has been defined, default constructor can’t be invoked and developer can use only those constructors which are defined in the class.

 </blockquote>

</details>

---

35. Can a constructor have different name than a Class name in Java?

  ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Constructor in Java must have same name as the class name and if the name is different, it doesn’t act as a constructor and compiler thinks of it as a normal method.

 </blockquote>

</details>

---

36. Is it possible to re-reach and use an object once it has been garbage collected?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No,  Once an object has been destroyed by garbage collector, it no longer exists on the heap and it can’t be accessed again. There is no way to reference it again.

 </blockquote>

</details>

---

37. If i want my class to be developed in a way that no other class (even derived class) can create its objects. How can I do so?


 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If we declare the constructor of a class as private, it will not be accessible by any other class and hence, no other class will be able to instantiate it and formation of its object will be limited to itself only.

 </blockquote>

</details>

---

38. Is the following class declaration correct?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java

public abstract final class testClass {
	// Class methods and variables
}
```


<details><summary> Show Answer </summary>

<blockquote>

The above class declaration is incorrect as an abstract class can’t be declared as Final.

 </blockquote>

</details>

---

39. How are destructors used in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 There are no destructors defined in the Java class. Beacause it has its own garbage collection mechanism which does the job automatically by destroying the objects when no longer used.

  </blockquote>

</details>

---

40. Can a variable be local and static at the same time?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


No, variable can’t be static as well as local at the same time. Defining a local variable as static gives compilation error.


  </blockquote>

</details>

---

41. Is it possible to change the value of any variable defined in the class implementing an interface?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

No, we can’t change the value of any variable of an interface in the implementing class as all variables defined in the interface are by default public, static and Final. final variables are like constants which can’t be changed later

  </blockquote>

</details>

---

42. What part of memory (Stack/Heap) is cleaned in garbage collection process?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

Heap. Because when Java programs run on the JVM, objects are created on the heap,

  </blockquote>

</details>

---

43. What would be the result if a class extends two interfaces and both have a method with same name and signature? Assume that the class is not implementing that method.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 
<details><summary> Show Answer </summary>

<blockquote>

 It will throw compile time error- In case of such conflict, compiler will not be able to link a method call due to ambiguity. 


  </blockquote>

</details>

---

44. Which is the superclass of String and StringBuffer classes in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

 `java.lang` is the superclass for String and StringBuffer.

   </blockquote>

</details>

---

45. Can we achieve method overloading by changing the return type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

No, We cannot achieve method overloading through return type in Java.

</blockquote>

</details>

---

46. Can we extend a String class?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, String is a final class, therefore we cannot extend or inherit it.

</blockquote>

</details>

---

47. Is it possible to access non-static members of outer class inside a static nested class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote

No, we can’t access non-static members of outer class inside a static nested class. We can access only static members of outer class inside a static nested class.

</blockquote>

</details>

---

48. Can we declare local inner classes as private or protected or public?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. Local inner classes can’t be declared with access modifiers.They can’t be private or protected or public.

</blockquote>

</details>

---

49. What is the condition to use local variables inside a local inner class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The local variables must be final inside a local inner class in Java. We can’t use non-final local variables inside a local inner class.

</blockquote>

</details>

---

50. Differentaite between static and non-static nested classes?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The main difference between static and non-static nested classes is that you need not to instantiate the outer class to access static nested classes. But, to access non-static nested classes, you have to instantiate the outer class.

</blockquote>

</details>

---

51. How many .class files are created when you compile a file with inner classes in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


When an inner class enclosed by with an outer class is compiled,then two .class files are created: one for each inner class and one for the outer class.

</blockquote>

</details>

---

52. Which `java.util classes` and interfaces support event handling?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `EventObject class` and the `EventListener interface` support event processing.

</blockquote>

</details>

---


53. Can an object’s `finalize()` method be invoked while it is reachable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

An object’s `finalize()` method cannot be invoked by the garbage collector while the object is still reachable. However, an object’s `finalize()` method may be invoked by other objects.

</blockquote>

</details>

---

54. Explain about inner class in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In Java, we can define a class inside a class and they are called nested classes. Any nested class which is non-static are known as inner class. 

</blockquote>

</details>

---

55. How does break statement with label works in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which will skip the current iteration of the outermost loop in the program.

</blockquote>

</details>

---


56. what will be the value stored in the String array passed into the `main()` method, when no argument is passed in command line?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>
 
The value will be empty if no arguments passed in command line in Java.

</blockquote>

</details>

---

57. What if the static modifier is removed from the signature of the `main()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Program compiles. But it will throws an error "NoSuchMethodError" at runtime.

</blockquote>

</details>

---

58. What will happen if you decalre the constructor as static?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It will throw an compile time error, because static concept belongs to the class, not the object. Since Constructors are invoked only when the object is created, there is no sense to make the constructors static. 

</blockquote>

</details>

---

59. Is it possible to make the abstract methods static in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If we make the abstract methods as static, It will become the part of the class and can directly call it (unnecessary). Calling an undefined method is completely useless therefore it is not allowed.

</blockquote>

</details>

---

60. Differentiate between aggregation and composition?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Aggregation represents the weak relationship whereas composition represents the strong relationship. For example, the car has an indicator (aggregation), but the car has an engine (composition).

</blockquote>

</details>

---

61. Can you use `this()` and `super()` both in a constructor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, because `this()` and `super()` must be the first statement in the Java class constructor.

</blockquote>

</details>

---

62. Differentiate between a path and classPath in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Path specifies the location of .exe files. Classpath specifies the location of bytecode (.class files).

</blockquote>

</details>

---

63. How many times does the garbage collector calls the `finalize()` method for an object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The garbage collector calls the `finalize()` method only once for an object.

</blockquote>

</details>

---

64. When does a finally block does not get executed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The only time finally won’t be called is if you call `System.exit()` or if the JVM crashes first.


</blockquote>

</details>

---

## Problem Solving

65. Choose the right access modifier for the line 7 in the below code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java
public class Shape {
    protected void display() {
        System.out.println("Display-base");
    }
}
public class Circle extends Shape { <
    -------void display() {
        System.out.println("Display-derived");
    }
}
```

<details><summary> Show Answer </summary>

<blockquote>

 public and protected both can be used.

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

We can provide only a less restrictive or same-access modifier when overriding a method.

</blockquote>

</details>

</details>

---

66. Identify the error in the following code.

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
interface Sample {
 int x;	
 void display();
}
public class B implements Sample {
 int x = 20;
public void display{
  System.out.println("Welcome"); 	
 }
}
```

<details><summary> Show Answer </summary>

<blockquote>

A variable(x) in an interface must be initialized at the time of declaration.

</blockquote>

</details>

---

67. Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

Predict the output of the following code:

class Animal{
	public Animal() {
		System.out.println("Parent class");
	}
}

class Cat extends Animal {
	public Cat() {
		System.out.println("Sub class");
	}
}

class Kitten extends Cat {
	public Kitten() {
		System.out.println("child class");
	}
}

public class Tester {
	public static void main(String[] args) {
		Kitten K = new Kitten();
	}
}
```

<details><summary> Show Answer </summary>

<blockquote>

Parent class Sub class child class

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

When a child class object is created, the child class constructor implicitly invokes the parameterless constructor of the parent class.

</blockquote>

</details>

</details>

---

68. Predict the output of the following Java code?


 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

    class output 
    {
        public static void main(String args[])
        {
            char ch;
            ch = "goodmorning".charAt(1);
            System.out.println(ch);
        }
   }
   ```
   <details><summary> Show Answer </summary>

<blockquote>

o

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

"goodmorning" is a String literal, method `charAt()` returns the character specified at the index position. Character at index position 1 is e of goodmorning, hence ch contains o.

</blockquote>

</details>

</details>

---

69. Can a class be a super class and a sub-class at the same time? Give example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 Yes, If there is a hierarchy of inheritance used, a class can be a super class for another class and a sub-class for another one at the same time.
 
 Example : 

 ```java

 public class Animal{
..........
}
public class Cat extends Animal {
............
}
public class Kitten extends Cat {
......................
}
```

</blockquote>

</details>

---


70. What will be the output of the following Java program?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
    class Example
    {
        public static void main(String args[])
        {
            char chars[] = {'a', 'b', 'c'};
            String s = new String(chars);
            System.out.println(s);
        }
   }
   ```

<details><summary> Show Answer </summary>

<blockquote>

abc

</blockquote>

<details><summary> Explanation </summary>

<blockquote>


   String(chars) is a constructor of class string, it initializes string s with the values stored in character array chars, therefore s contains “abc”.

</blockquote>

</details>

</details>

---
