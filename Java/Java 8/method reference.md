## Technical
1: Explain Method Reference.

<details><summary><b> Show Answer </b></summary>

It is to refer the method of functional interface. While using a lambda expression to refer to a method, we can use a method reference instead of a lambda expressison.

</details>
 
 ---

2: List the types of Method References.

<details><summary><b> Show Answer </b></summary>

- Reference to a static method.
- Reference to an instance method.
- Reference to an instance method of an arbitrary object of a particular type
- Reference to a constructor.

</details>

 ---
 
3: Write the syntax for referring to a static method?

<details><summary><b> Show Answer </b></summary>

- ContainingClass::staticMethodName
- We can refer to the static method by calling its name with the class where it resides.

</details>
 
 ---

4: Write the syntax for Reference to an instance method of a particular object?

<details><summary><b> Show Answer </b></summary>

- containingObject::instanceMethodName
- use the instance method name of the particular object name.

</details>

 ---
 
5: Write the syntax for Reference to an instance method of an arbitrary object of a particular type?

<details><summary><b> Show Answer </b></summary>

- We can mention the type with the instance method name of the object.
- ContainingType::methodName

</details>
 
 ---

6: Write the syntax for Reference to a constructor?

<details><summary><b> Show Answer </b></summary>

- ClassName::new
- new is the keyword to refer to the constructor with the class name.

</details>

 ---
 
 7: Explain the parts of the method reference.

 
<details><summary><b> Show Answer </b></summary>

- It has 2 parts. class/object and method/constructor.
- Separated by :: (double colons)
- No additional parameters are passed in method reference.

</details>
 
 ---

8: How to print all the elements in the list using method reference?

<details><summary><b> Show Answer </b></summary>


 ``` java 
 list.forEach(System.out::println);  
 ``` 
<details><summary><b>Explanation</b></summary>
 
- Here we are using the forEach method to display the elements one by one in the list.

</details>
 
 </details>

 ---
 
## Problem Solving

9: Predict the output of the following code.

``` java
import java.io.*;
import java.util.*;
public class MethodReference{
    public static void main(String[] args)
    {
        List<String> bookList = new ArrayList<>();
        bookList .add("Java Programming");
        bookList .add("Data Strcutures and Alogrithms");
        bookList .add("Python Programming");
        Collections.sort(bookList ,String::compareToIgnoreCase);
        bookList .forEach(System.out::println);
    }
}
``` 

<details><summary><b> Show Answer </b></summary>

   Data Structures and Alogrithms<br>
   Java Programming<br>
   Python Programming
 
 <details><summary><b>Explanation</b></summary>
  
   -  This is an example of Reference to an instance method of an arbitrary object of a particular type.
   -  First, it will sort the list and apply compareToIgnoreCase to return the result.

</details>
 
 </details>

 ---
 
10: What should be the code in line 9  to get the result "Hello, this is a static method." using a reference to the static methods?

``` java
interface Sample{  
    void print();  
}  
public class MethodReference {  
    public static void printhello(){  
        System.out.println("Hello, this is static method.");  
    }  
    public static void main(String[] args) {  
        // Line 9
        sample.print();  
    }  
} 
```
<details><summary><b> Show Answer </b></summary>
 
 ``` java

 Sample sample = MethodReference::printhello; 
 
 ```
 
 <details><summary><b>Explanation</b></summary>
  
 - Here the static method reference printhello() refers to its functional method print() in the interface Sample.

 </details>
 
 </details>
 
 ---



