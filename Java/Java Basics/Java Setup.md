## Java Setup

1.Why do we need to set the path for Java? 

`set path = C:\Program Files\Java\jdk1.8.0_91\bin`

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- We need tools like javac, java, etc., which are located in the JDK/bin directory to compile and run Java programs.
- Before compiling and running a Java program, we need to set the path. This informs where JDK packages are installed.
- **Note:** We don't need to set the path if we save the Java source file inside the JDK\bin directory
</blockquote>
 </details>
      
---

2.Why do we need to set environment variable for Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>
      
- Whenever we run any command in the terminal, the prompt will check for the relevant executable file present in the current directory or in system environment variables.
- When we compile a Java program by running `javac MyPrg.java` command in the terminal, it will look for the `javac.exe` file to compile.
- If current directory is not  `C:\Program Files\Java\jdk1.8.0_91\bin` (where `javac.exe` present), we'll get **javac is not recognized** error. 
- One of the way to avoid this error is by setting the Java path `C:\ProgramFiles\Java\jdk1.8.0_05\bin` in environment variables. 
</blockquote>
</details>

---

3.What is `classpath`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>
      
`classpath` is just a set of paths where the Java compiler and the JVM must find needed classes to compile or execute other classes.
<blockquote> 
</details>

---    

4.What is JDK?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- JDK stands for **J**ava **D**evelopment **K**it that contains JRE and developments tools like compilers and debuggers which are useful for developing Java applications.
- For instance, JDK contains `javac` i.e., Java compiler helps us to compiles Java source file `MyPrg.java` and generates the class file `MyPrg.class`.
 
 </blockquote>
 </details>

---

5.What is JRE?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

JRE stands for **J**ava **R**untime **E**nvironment that contains JVM and provides the libraries and libraries to run java applications. 
</blockquote>
      </details>

 ---

 6.What is JVM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- JVM stands for **J**ava **V**irtual **M**achine that uses to run java application in different platforms.
- It converts .class into java bytecode which depends up the paltform ie, the native language code.
      </blockquote>
</details>

---

 7.Why java is platform independent?
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- By use of compiler, .java file is converted into .class.
- Java Runtime Environment is supported by many platforms which contains JVM.
- Java Virtual Machine is responsible to convert .class into native bytecode.
 </blockquote>
      </details>

 ---

 8.What is the entry point of java program?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- When Java Virtual Machine runs, it will find the main method which is in the form of
``` java
public static void main(String[] args)
```
- It is not found in the java application, the java application will not be executed.
- If the method signature this main method is changed, it will not be consider as staring point.
</blockquote>
 </details>

---

9.How will you define an API?
      
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- API means Application Programming Interface, which acts as intermediate between two application to communicate between each other.
- One application may be developed in one language and other application may be developed in another application where api acts as intermediatry thats allows to communicate each other.
      </blockquote>
</details>

---

10.Why java is not a pure Object Oriented programming language?
      
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- Java supports primitive data types such as int, float, long, double, byte, char, short, boolean which are not objects.
- While using static key, their is no need to create objects to access the value or method.
      </blockquote>
</details>

---

11.If you are a user of java application, which tool do you need in JDK, JRE and JVM?
      
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- For a user, JRE is needed.
- JDK contains Debugger and compiler which are not requiered for a user.
    </blockquote>
      </details>

---

12.Can we have two public classes in the same file?
      
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>

- No, We can have more classes in a file but only one class should be public.
- It makes the compilation faster by efficient lookup of code.
- If you have more than one public class, the error will be generated on compilation time.
    </blockquote>
      </details>

---

13.What does left side class and right side class denotes while creating an object?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote> 

- The left side class of denotes reference of the object and right side denotes object of which to be created.
    Eg. B b = new A()
- B(Reference) can be respected class, abstract class or interface.
 </blockquote>
</details>

---

14.Explain the difference between Heap memory and Stack memory.
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary> 
<blockquote>  

- Heap memory is used through out the application.
- Objects, arrays, static variables and instance variables are the examples which are stored in heap memory
- Stack memory is used only in method or currently running methods.
- Function calls, primitive, local and reference variables are stored in this memory.    
   </blockquote>
</details>
      
---

15.What is Architecture Neutral?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote> 

- Software that is designed without regard to the target platform. 
- <span style="color:blue"> Software</span> is often written to maximize the performance of a specific hardware platform, but such     software must be modified to make it run on other hardware.

**Example**

- Size of int in C is 2 bytes for 32 bit architecture and 4 bytes for 64 bit architecture.
- Size of int in Java is the same 4 bytes for both 32 bit and 64 bit architecture
</blockqoute>  
</details>

---

16.What is Just In Time Compiler and Ahead of time Compiler?
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 <details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- In **Just In Time** compilation, the source code is coverted into byte code. Where the bytecode is platform independant. It is runnable in different architecture system when it is coverted in machine code in that system. Here some of the frequently used codes are stored as code cache and used when it's required.
- In **Ahead Of Time** compilation, the souce code is directly converted into machine, So it is platform dependant. AOT is used for to manual machine code convertion.
</blockqoute>  
</details>

---

17.What is Intermediate Language?
 
 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- A language that is generated from programming source code but, it cannot be directly executed by the CPU. 
- It is platform independent. 
- It can be run in any computer environment that has a runtime engine for the language. 
- Java is an example for Inermediate language.
</blockqoute>  
</details>

---

18.Explain features of java.
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote> 

- Platform Independent
- Dynamic
- Secure
- Simple
- High Performance
- Robust
- Architecture Neutral
</blockqoute>  
</details>

---

19.What is `javac`?
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- A complementary tool that is a compiler used to read Java code and translates them into bytecode. 
- The bytecode runs on JVM.
</blockqoute>  
</details>

---

20.What is `javadoc`?
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- It converts API documentation from Java source code to HTML. 
- This is useful when creating standard documentation in HTML.
 </blockquote>
  </details>

----

21.If we use wrapper class instead of primitive data type, can we call the java programing as pure object oriented?
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- When we use wrapper class while using arithmatic operations between two values there will be unboxing and auto boxing.
- Unboxing means converting object into primitive datatype and auto boxing means converting primitive into object which also deals with primitives.
- So, Java is not pure object oriented when we use wrapper class also.
</blockqoute> 
</details>

---

22.What is Java source file extention?<br>
A)`.java`<br>
B)`.class`<br>
C)`.exe`<br>
D)`.src`<br>
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>
  
   A) `.java`
 </blockqoute> 
 
 <details>
 <summary><b> Explanation </b></summary> 
  <blockquote>
   
- The source file is coded in `.java` extention before compiling.
   </blockqoute> 
 </details> 
</details>

---

23.What is extention of file which is generated by Java compiler?<br>
A)`.java`<br>
B)`.class`<br>
C)`.exe`<br>
D)`.src`<br>

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>
 
   B) `.class`
 </blockqoute> 
 
 <details>
 <summary><b> Explanation </b></summary> 
  <blockquote>
   
      - The generated file from the java compiler has the extention of `.class` .
  </blockqoute> 
   </details> </details>

---
