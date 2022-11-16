1.What is `try`with resources? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>
 
> `try`with resources
 
<details markdown="1"><summary><b> Explanation</b></summary>
 
> `try`with resources known as automatic resource management,which automatically closes the resources used within the try catch block.To use this statement, you simply need to declare the required resources within the parenthesis, and the created resource will be closed automatically at the end of the block.
</details>
</details>

---

2.How to use `try`with resources? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>
 
>- To use a class with try-with-resources statement it should implement AutoCloseable interface and the close() method of it gets invoked automatically at runtime.
>- Declaration of more than one class in try-with-resources statement and declaring multiple classes in the try block of try-with-resources statement should be closed in reverse order.
>- The declaration of resources within the parenthesis everything is the same as normal try/catch block of a try block.The resource declared in try gets instantiated just before the start of the try-block.
>- The resource declared at the try block is implicitly declared as final.
 
</details>
</details>

---

3.What is the syntax for `try`with resources? 

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>
 
>Syntax for `try`with resources 
 
<details markdown="1"><summary><b> Explanation</b></summary>
 
 ```java
try(FileReader f = new FileReader("file path")) {
// use the resource
} catch () {
// body of the catch block
}
}
 ```
</details>
</details>

---

4.Predict the output of  the following code.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

 ``` java 
import java.io.*;
public class TryResources {
   public static void main(String args[]) {
      try(FileReader f = new FileReader("C://abc.txt")) {
         char [] a = new char[100];
         f.read(a);   
         for(char c : a)
         System.out.print(c);   
      } catch (IOException e) {
         e.printStackTrace();
      }
   }
}
```
<details markdown="1"><summary><b> Show Answer</b></summary>
 
>Prints the characters from the file abc.txt 

<details markdown="1"><summary><b> Explanation </b></summary>
 
>It reads the file and prints the characters from the file and if the file does not exist then it throws an IOException.
 
</details>
</details>

---

