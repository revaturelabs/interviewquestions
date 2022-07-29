1: Explain about Method Reference.

<details><summary> Show Answer</summary>

It is to refer the method of functional interface.When using lambda expression to refer a method ,we can use method reference instead of lambda expressison.

</details>

2: List the types of Method References.

<details><summary> Show Answer</summary>

- Reference to a static method.
- Reference to an instance method.
- Reference to an instance method of an arbitrary object of a particular type
- Reference to a constructor.

</details>

3: Write the syntax for reference to a static method?

<details><summary> Show Answer</summary>

- ContainingClass::staticMethodName
- We can refer to the static method by calling its name with the class where it resides.

</details>

4: Write the syntax for Reference to an instance method of a particular object?

<details><summary> Show Answer</summary>

- containingObject::instanceMethodName
- use the instance method name of the particular object name.

</details>

5: Write the syntax for Reference to an instance method of an arbitrary object of a particular type?

<details><summary> Show Answer</summary>

- We can mention the type with the instance method name of the object.
- 	ContainingType::methodName

</details>

6: Write the syntax for Reference to a constructor?

<details><summary> Show Answer</summary>

- ClassName::new
- New is the keyword to refer the constructor with the class name.

</details>

7: Predict the output of the following code.

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
        Collections.sort(bookList ,
                         String::compareToIgnoreCase);
        bookList .forEach(System.out::println);
    }
}
``` 

<details><summary> Show Answer</summary>

   Data Strcutures and Alogrithms<br>
   Java Programming<br>
   Python Programming
   -  This is an example of Reference to an instance method of an arbitrary object of a particular type.
   -  First it will sort the list and applys compareToIgnoreCase to returns the result.

</details>

8: What should be the code in line 9  to get the result "Hello, this is static method." using reference to the static methods?

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
        sam.print();  
    }  
}  
```
<details><summary> Show Answer</summary>

 Sample sam = MethodReference::printhello;  <br>
 - Refers a static method printhello() to its functional method print() in the interface Sample declared.

 </details>

 9: Explain the parts of method reference.

 
<details><summary> Show Answer</summary>

- It has 2 parts. class/object and method/constructor.
- Seperated by :: (double colons)
- No additional parameters passed in method reference.

</details>

10: How to print all the elements in the list using method reference?

<details><summary> Show Answer</summary>

   list.forEach(System.out::println);  <br>
- Here we are using forEach method to display the elements one by one in the list.

</details>

