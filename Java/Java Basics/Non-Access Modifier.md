## Non-Access Modifier

1.What are Non-Access Modifiers?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

 - Non-Access Modifiers will not change the scope but it will add some functionality. There are three types of Non-Access Modifires:
    - `final`
    - `static`
    - `abstract`
</blockqoute>  
</details>

---

2.What is `final` non-access modifier?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>
	
`final` is the keyword that can be used with class, variable, and method.
  1.	Final variable – The value can’t be changed
  2.	Final method – The method can’t be overridden
  3.	Final class – No subclasses can be created
</blockqoute>  
</details>

---

3.What is `static` non-access modifier?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote> 
  
- When we use static before variable or method that will not belong to any object,it belongs to the class. 
- There is no need to create an object for the class to access the static variable or static method. We can use the class name to call them with respect to the       access modifier.
- If we use the object name to call the static method or variable, the compiler will replace the name of the object with class.
</blockqoute>
</details>

---

4.What is `abstract` non-access modifier?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- If we add `abstract` keyword with method, we can't add method definition to the method and abstract method presents in abstract class.
- If we add `abstract` keyword with class, we can't make the class extended from another class. It can be extended from only another abstract class.
- we can't create object for abstract class.
</blockqoute>  
</details>

---

5.Can we use instance variable in static method?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

>No, we can't use instance variable in static method because instance variable belongs to the property of object where static method belongs to the property of class. So, we can use static variable in static method.
</blockqoute>  
</details>

---

6.How can we call the non-static method from static method, if both the methods present in the class?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- We need to create an object to call the non-static method from static method where both the methods presents in the same class.
- In general, non-static methods are called using objects and static methods are called using class name.
</blockqoute>  
</details>

---

7.Can we write a method inside another method in java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

No, we can't directly write a method inside method in java. If we want to create a method inside method, we have to create a local class inside the method then we can add method inside it.

**Example**
``` java
class Greeting {
	void hello() {
		class Hi {
			void hiMethod() {
				System.out.println("Hi Good Morning");
			}
		}
		Hi hi = new Hi();
		hi.hiMethod();
	}
}

public class Main {
	public static void main(String[] args) {
		Greeting greeting = new Greeting();
		greeting.hello();
	}
}
```
**Output**
```
Hi Good Morning
```

>In the above code, the `hello` method has local class `Hi` that consists `hiMethod`. We need to create object to access the method.
</blockqoute>  
</details>

---

8: Debugg below the code.

``` java 

package com.example;

class Greeting {
	abstract void hello();
}

class Hello extends Greeting{
	@Override
	void hello() {
		System.out.println("Hello");
	}
}

public class Main {
	public static void main(String[] args) {
		Greeting greeting = new Hello();
		greeting.hello();
	}
}

```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- The method `hello()` is an abstract method that should be in abstract class.
- Therefore, the class `Greeting` should be `abstract`.
</blockqoute>
</details>
