## Technical

1. What is Generics?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

It forces the Java programmer to store specific type of objects to make it type-safe which makes the code stable by detecting the bugs at compile time.

Before generics, we can store any type of objects in the collection, i.e., non-generic. 


</blockquote>

</details>


---

2. Why should we use Generics?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

The Object is the superclass of all other classes, and Object reference can refer to any object which leads to lack of type safety. So, we should use Generic to make it type safe. 

<b>Example</b>: The  `HashSet`, `ArrayList`, `HashMap` classes in collections  will use generics.

</blockquote>

</details>



---

3. List the type parameters Generics in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

The common type parameters used are:

`T` – Type

`E` – Element

`K` – Key

`N` – Number

`V` – Value

</blockquote>
</details>



---

4. List the main advantages of Generics.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- <b>Type-safety</b>-should have single type of objects in generics.
- <b>Type casting is not required</b>-No need to typecast the object.
- <b>Compile-Time Checking</b>-Since it checks at compile time, error will not occur at run time.

</blockquote>

</details>



---

5. How to invoke and instantiate a generic type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- For `generic type invocation`, we should replace `T` with some concrete value, such as `Integer`. Like a normal invocation instead of passing an argument to a method, you are passing a `type argument — Integer`. The `integerBox` will hold the reference. An invocation of a generic type is generally known as a <b>parameterized type</b>.

    `Draw<Integer> integerBox;`

- To instantiate the class, will use `new` keyword, but we should place `<Integer>` between the class name and the parenthesis

    `Draw<Integer> integerBox = new Box<Integer>();`

</details>

</blockquote>

---
6. Explain about wildcards in Java generics.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- Wildcard element means any type represented by the `? (question mark)` symbol. It can be used as a type 
  of a parameter, field, return type, or local variable.
- If we write `<? extends Number>`, it means any child class of Number, e.g., Integer, Float, and 
  double. Now,we can call the method of Number class through any child class object.

 </blockquote>
 
</details>

---

7. List the ways of declaring wildcards in Java generics.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- It can be used in three ways −

    - <b>Upper bound Wildcard</b> − `? extends Type`.

    - <b>Lower bound Wildcard</b> − `? super Type`.

    - <b>Unbounded Wildcard</b>− `?`

 </blockquote>
 
</details>

---

8. How to decide on which type of wildcard best suits the condition?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- It is based on the type of parameters passed to a method as <b>in</b> and <b>out</b> parameter.
    - <b>in variable</b> −which provides data to the code. For example, copy(src, dest). Here, src acts as <b>in variable</b> data to be copied.

    - <b>out variable</b> −which holds data updated by the code. For example, copy(src, dest). Here, dest acts as <b>out variable</b> having copied data.

 </blockquote>
 
</details>

---

9. Can Java generics be applied to primitive types?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

No 

 </blockquote>

<details><summary><b>Explanation</b></summary>

<blockquote>

Java generics cannot be applied to primitive types, because the parameters in generics are of non-primitive data types.
 
</blockquote>
 
</details>

</details>

--- 

## Problem Solving

10. Write a Java program to show the working of user defined Generic class to display the message <b>"Generic methods will have own type parameters"</b>?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

``` java

class Test<T> {
    T obj;
    Test(T obj) { this.obj = obj; } // constructor
    public T getObject() { return this.obj; }
}
class Main {
    public static void main(String[] args)
    {
        Test<String> sObj
            = new Test<String>("Generic methods will have own type parameters");
        System.out.println(sObj.getObject());
    }
}
```
 </blockquote>
<details><summary><b>Explanation</b></summary>

<blockquote>

 - used `< >` to specify Parameter type and an object of type `T` is declared. By creating an instance of String type to display the mentioned message.

</blockquote>

 
</details>

</details>

---

11. Write a Java program to show the working of user defined Generic functions to display the message <b>"Generic methods"</b> and value <b>1.0</b>?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

``` java

class Test {
    static <T> void genericDisplay(T element)
    {
        System.out.println(element.getClass().getName()
                           + " = " + element);
    }
    public static void main(String[] args)
    {
        genericDisplay("Generics methods");
        genericDisplay(1.0);
    }
}
```

 </blockquote>
<details><summary><b>Explanation</b></summary>

<blockquote>

 `genericDisplay` is the generic method with parametrized type using string and double type to display the message.

 </blockquote>
 
</details>

</details>

---
12. How would you write the below class into a class using generics?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<blockquote>

``` java
 public class Draw {
    private Object object;

    public void set(Object object) { this.object = object; }
    public Object get() { return object; }
}
```
</blockquote>

<details><summary><b>Show Answer</b></summary>

<blockquote>

``` java

public class Draw<T> {
    private T t;

    public void set(T t) { this.t = t; }
    public T get() { return t; }
}

```
</blockquote>

<details><summary><b>Explanation</b></summary>

<blockquote>

- In the class Draw<T> introduces the type variable, T, that can be used anywhere inside the class.
- All occurrences of `object` is changed with the type variable `<T>` which can be of any primitive type.


</blockquote>

</details>

</details>


---

