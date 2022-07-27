1: If you are a user of java application, which do you need in JDK, JRE and JVM?
   <details>
      <summary> Show Answer </summary> 

- For a user, JRE is needed.
- JDK contains Debugger and compiler which are not requiered for a user.
    </details>
    

2: Can we have two public classes in the same file?
    <details><summary>Show Answer</summary>

- No, We can have more classes in a file but only one class should be public.
- It makes the compilation faster by efficient lookup of code.
- If you have more than one public class, the error will be generated on compilation time.
    </details>


3: What does left side class and right side class denotes while creating an object?
    <details><summary>Show Answer</summary>
- The left side class of denotes reference of the object and right side denotes object of which to be created.
    Eg. B b = new A()
- B(Reference) can be respected class, abstract class or interface.
    </details>


4: Explain the difference between Heap memory and Stack memory.
    <details>
    <summary>Show Answer</summary>

- Heap memory is used through out the application.
- Objects, arrays, static variables and instance variables are the examples which are stored in heap memory
- Stack memory is used only in method or currently running methods.
- Function calls, primitive, local and reference variables are stored in this memory.    </details>


5: What is Architecture Neutral?
<details>
  <summary> Show Answer </summary>
  
- Software that is designed without regard to the target platform. 
- <span style="color:blue"> Software</span> is often written to maximize the performance of a specific hardware platform, but such     software must be modified to make it run on other hardware.

<span style="color:blue"> Example</span>

- Size of int in C is 2 bytes for 32 bit architecture and 4 bytes for 64 bit architecture.
- Size of int in Java is the same 4 bytes for both 32 bit and 64 bit architecture
 </details>


6: What is Just In time Compiler and Ahead of time Compiler?
<details>
  <summary> Show Answer </summary>

- <span style="color:blue">In Just in time compilation</span>, the source code is coverted into byte code. Where the bytecode is platform independant. It is runnable in different architecture system when it is coverted in machine code in that system. Here some of the frequently used codes are stored as code cache and used when it's required.
- <span style="color:blue">In Ahead of time compilation</span>, the souce code is directly converted into machine, So it is platform dependant. AOT is used for to manual machine code convertion.
  </details>


7: What is Intermediate Language?
<details>
  <summary> Show Answer </summary>

- A language that is generated from programming source code but it cannot be directly executed by the CPU. 
- It is platform independent. 
- It can be run in any computer environment that has a runtime engine for the language. 
- Java is an example for Inermediate language.
  </details>


8: Explain features of java.
<details>
  <summary> Show Answer </summary>

- Platform Independent
- Dynamic
- Secure
- Simple
- High Performance
- Robust
- Architecture Neutral
  </details>


9: What is javac?
<details>
  <summary> Show Answer </summary>

- A complementary tool that is a compiler used to read Java code and translates them into bytecode. 
- The bytecode runs on JVM.
</details>


10: What is javadoc?
<details>
  <summary> Show Answer </summary>

- It converts API documentation from Java source code to HTML. 
- This is useful when creating standard documentation in HTML.
  </details>
