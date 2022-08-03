1: Why do we need to set the path for java?
<details>
      <summary> <b> Show Answer </b> </summary> 


- If we didn't set path, the command prompt will not compile.
- If we compile the java file, it will not recognise the javac.
- We need to set the path or we have save the file in the folder where jdk packages are located.
- Therefore, we have set the path to compile java files.
    </details>

---

2: What is the neccessary to set path in Enviornmental variable for java?
<details>
      <summary> <b> Show Answer </b></summary>       

- If we execute a command in command prompt, it will check the given executable file in command presents in the folder or in the operating system.
- If the command is not present in current folder, it will check with the Operating system.
- If we set the path in Environmental variable, it will consider as setting the file in os.
- While executing the code it will find the path from os.
    </details>

---

3: What is classpath?
 <details>
      <summary> <b> Show Answer </b></summary> 

- The class path is the path that is used by java runtime environment to search for classes which are used in the program.
- It is used to load the class library files and refers the developing environment.
    </details>

---    

4: What is JDK?
 <details>
      <summary> <b> Show Answer </b></summary> 

- JDK means Java Development Kit that contains JRE and developments tools like compilers and debuggers which are usefull for developing the applications.
- By the use of compiler the java .java is converted into .class file.
  
 </details>

---

5: What is JRE?
 <details>
      <summary> <b> Show Answer </b></summary> 

- JRE means Java Runtime Environment that contains JVM and provides the libraries and libraries to run java applications. 
 </details>

 ---

 6: What is JVM?
 <details>
      <summary><b> Show Answer </b></summary> 

- JVM means Java Virtual Machine that uses to run java application in different platforms.
- It converts .class into java bytecode which depends up the paltform ie, the native language code.
 </details>

---

 7: why java is platform independent?
 <details>
      <summary><b> Show Answer </b></summary> 

- By use of compiler, .java file is converted into .class.
- Java Runtime Environment is supported by many platforms which contains JVM.
- Java Virtual Machine is responsible to convert .class into native bytecode.
 </details>

 ---

 8: why main method is the starting point of java program?

 <details>
      <summary><b> Show Answer </b></summary> 

- When Java Virtual Machine runs, it will find the main method which is in the form of
``` java
public static void main(String[] args)
```
- It is not found in the java application, the java application will not be executed.
- If the method signature this main method is changed, it will not be consider as staring point.

 </details>

---

9: How will you define an API?
 <details>
      <summary><b> Show Answer </b></summary> 

- API means Application Programming Interface, which acts as intermediate between two application to communicate between each other.
- One application may be developed in one language and other application may be developed in another application where api acts as intermediatry thats allows to communicate each other.
  
</details>

---

10: Why java is not a pure Object Oriented programming language?
 <details>
      <summary><b> Show Answer </b></summary> 

- Java supports primitive data types such as int, float, long, double, byte, char, short, boolean which are not objects.
- While using static key, their is no need to create objects to access the value or method.
  
</details>

---

11: If you are a user of java application, which tool do you need in JDK, JRE and JVM?
 <details>
      <summary><b> Show Answer </b></summary> 

- For a user, JRE is needed.
- JDK contains Debugger and compiler which are not requiered for a user.
    </details>

---

12: Can we have two public classes in the same file?
 <details>
      <summary><b> Show Answer </b></summary> 

- No, We can have more classes in a file but only one class should be public.
- It makes the compilation faster by efficient lookup of code.
- If you have more than one public class, the error will be generated on compilation time.
    </details>

---

13: What does left side class and right side class denotes while creating an object?
 <details>
      <summary><b> Show Answer </b></summary> 

- The left side class of denotes reference of the object and right side denotes object of which to be created.
    Eg. B b = new A()
- B(Reference) can be respected class, abstract class or interface.
    </details>

---

14: Explain the difference between Heap memory and Stack memory.
 <details>
      <summary><b> Show Answer </b></summary> 

- Heap memory is used through out the application.
- Objects, arrays, static variables and instance variables are the examples which are stored in heap memory
- Stack memory is used only in method or currently running methods.
- Function calls, primitive, local and reference variables are stored in this memory.    </details>

---

15: What is Architecture Neutral?
 <details>
      <summary><b> Show Answer </b></summary> 

- Software that is designed without regard to the target platform. 
- <span style="color:blue"> Software</span> is often written to maximize the performance of a specific hardware platform, but such     software must be modified to make it run on other hardware.

**Example**

- Size of int in C is 2 bytes for 32 bit architecture and 4 bytes for 64 bit architecture.
- Size of int in Java is the same 4 bytes for both 32 bit and 64 bit architecture
 </details>

---

16: What is Just In time Compiler and Ahead of time Compiler?
 <details>
      <summary><b> Show Answer </b></summary> 

- <span style="color:blue">In Just in time compilation</span>, the source code is coverted into byte code. Where the bytecode is platform independant. It is runnable in different architecture system when it is coverted in machine code in that system. Here some of the frequently used codes are stored as code cache and used when it's required.
- <span style="color:blue">In Ahead of time compilation</span>, the souce code is directly converted into machine, So it is platform dependant. AOT is used for to manual machine code convertion.
  </details>

---

17: What is Intermediate Language?
 <details>
      <summary><b> Show Answer </b></summary> 

- A language that is generated from programming source code but it cannot be directly executed by the CPU. 
- It is platform independent. 
- It can be run in any computer environment that has a runtime engine for the language. 
- Java is an example for Inermediate language.
  </details>

---

18: Explain features of java.
 <details>
      <summary><b> Show Answer </b></summary> 

- Platform Independent
- Dynamic
- Secure
- Simple
- High Performance
- Robust
- Architecture Neutral
  </details>

---

19: What is javac?
<details>
      <summary><b> Show Answer </b></summary> 

- A complementary tool that is a compiler used to read Java code and translates them into bytecode. 
- The bytecode runs on JVM.
</details>

---

20: What is javadoc?
 <details>
      <summary><b> Show Answer </b></summary> 

- It converts API documentation from Java source code to HTML. 
- This is useful when creating standard documentation in HTML.
  </details>

----

21: If we use wrapper class instead of primitive data type, can we call the java programing as pure object oriented?
 <details>
      <summary><b> Show Answer </b></summary> 

- When we use wrapper class while using arithmatic operations between two values there will be unboxing and auto boxing.
- Unboxing means converting object into primitive datatype and auto boxing means converting primitive into object which also deals with primitives.
- So, Java is not pure object oriented when we use wrapper class also.
  </details>
