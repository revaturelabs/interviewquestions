## Non-Access Modifier

1: What are non-access modifiers?
<details>
  <summary> <b> Show Answer </b></summary> 

 - It will not change the scope but it will add some functionality. There are three types of non-access modifires. They are,
    - Final
    - Static
    - Abstract

</details>

---

2: What is final non-access modifier?
- Final is the keyword that can be used with class, variable, and method.
    1.	Final variable – The value can’t be changed
    2.	Final method – The method can’t be overridden
    3.	Final class – No subclasses can be created

</details>

---

3: What is static non-access modifier?
<details>
  <summary> <b> Show Answer </b></summary> 
  
- When we use static before variable or method that will not belong to any object. It belongs to the class. 
- There is no need to create an object for the class to access the static variable or static method. We can use the class name to call them
- If we use the object name to call the static method or variable, the compiler will replace the name of the object with class.

</details>

---

4: What is abstract non-access modifier?
<details>
  <summary> <b> Show Answer </b></summary> 

- If we add abstract keyword with method, we can't add method definition to the method.
- If we add abstract keyword with class, we can't make the class extended from another class. It can be extended from only another abstract class.
- we can't create object for abstract class.

</details>

---

5: Can we use instance variable in static method?
<details>
  <summary> <b> Show Answer </b></summary> 

>No, we can't use instance variable in static method because instance variable belongs to the property of object where static method belongs to the property of class. So, we can use static variable in static method.
</details>

---

6: How can we call the non-static method from static method, if both the methods present in the class?
<details>
  <summary> <b> Show Answer </b></summary> 

- We need to create an object to call the non-static method from static method where both the methods presents in the same class.
- In general, non-static methods are called using objects and static methods are called using class name.
</details>

---

7: Can we write a method inside another method in java?
<details>
  <summary> <b> Show Answer </b></summary> 

>No, we can't directly write a method inside method in java. If we want to create a method inside method, we have to create a local class inside the method then we can add method inside it.

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
<details>
  <summary> <b> Show Answer </b></summary> 

>In the above code, the `hello` method has local class `Hi` that consists `hiMethod`. We need to create object to access the method.
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
<details>
  <summary> <b> Show Answer </b></summary> 

- The method `hello()` is an abstract method that should be in abstract class.
- Therefore, the class `Greeting` should be `abstract`.
