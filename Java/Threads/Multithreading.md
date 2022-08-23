## Multithreading

1. What is multithreading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>
<blockquote>

- Thread is termed as a lightweight process. A process is divided into parts, each part called Thread.
- Multithreading is the process of executing one or more threads simultaneously. 
- In multithreading, threads will share a common memory and the execution will also be faster.
</blockquote>
</details>

---

2. Which is the default thread?<br>
A)Main<br>
B)Default<br>
C)Runnable<br>
D)Run<br>

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>
<blockquote>

A)Main
</blockquote>
<details>
<summary><b> Explanation </b></summary>
<blockquote>

If there is no thread is created, the main thread will execute the process by default.
</blockquote>
</details>
</details>

---

3. How can we create threads in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>
<blockquote>

- We can create threads in two ways.
  - By implementing `Runnable` interface
  - By extending `Thread` class 
</blockquote>
</details>

---

4.Is there any class in java which help us to create a thread? Explain how?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>
<blockquote>
	
- Yes, there is a `Thread` class in java helps us to create a thread.
- Create a class and extend that class by Thread class. Then, the created class will act as thread in java. 
- After extending `Thread` class, the class should override the `run` method.
- After creating object for the class, we can use `start()` method to run the method.

``` java
class Greeting extends Thread{
	public void run() {
		for(int i=0; i<10; i++) {
			System.out.println("Hello");
		}
	}
}

public class Main {
	public static void main(String[] args) {
		Greeting greeting = new Greeting();
		greeting.start();
	}
}
```

- When the method gets started by calling `start()` method, a new thread is created and starts executed it. 
- On the time, the main thread will continue the remaining part. The thread will give the message `Hello` 10 times.
	
</blockquote>
</details>

---

5. Explain the use of `sleep()` method in `Thread` class.
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>
<blockquote>

- The `sleep()` method definition: 
```java
public static void sleep(long millis) throws InterruptedException
```
- sleep()` method takes milliseconds as parameter, makes the current running thread to hold for that given milliseconds.
- This method will throw `InterruptedException`. So, we need to handle the exception, either by adding `throws` statement or by enclosing that within `try-catch` block.

``` java
class Greeting extends Thread{
	public void run() {
		for(int i=0; i<10; i++) {
			System.out.println("Hello");
			try {Thread.sleep(1000);} catch(InterruptedException e){ };
		}
	}
}

public class Main {
	public static void main(String[] args) {
		Greeting greeting = new Greeting();
		greeting.start();
	}
}
```
- When the `sleep()` method is called, the thread is hold by 1000 millisecond that is 1 second. 
- So, The thread will give the message `Hello` 10 times for every second.
</blockquote>
</details>

---

6. Explain about thread priority.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary> <b>Show Answer</b> </summary>
<blockquote>

 - Each thread has a priority. Priorities are represented by a number between 1 and 10.  
 - Where the thread scheduler schedules the threads according to their priority known as <b> preemptive scheduling</b>.

 </blockquote>

 </details>

 ---
 7. List the methods related to the thread priority.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- There are two methods `setter` and `getter` in thread priority.
    - `public final int getPriority()`:Returns the priority of the given thread  by using the `java.lang.Thread.getPriority()` method.
    - `public final void setPriority(int newPriority)`: Updates or assign the priority of the thread to `newPriority` using the `java.lang.Thread.setPriority()` method.

 </blockquote>

 </details>

 ---

 8. What are the 3 priority constants defined in `Thread` class?

  ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- `public static int MIN_PRIORITY`-It holds the value 1.
- `public static int NORM_PRIORITY`-It holds the value 5 and it is the Deafult priority of a thread.
- `public static int MAX_PRIORITY`-It holds the value 10.

</blockquote>

 </details>

 ---

9. What happens if the value of priority is not in between 1(minimum) and 10(maximum)?

  ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- If the value of the parameter `newPriority` of the method `getPriority()` goes out of the range (1 to 10), then the method throws `IllegalArgumentException`.

</blockquote>

 </details>

 ---

 
 10. Explain <b>fixed-priority pre-emptive scheduling</b> algorithm.

  ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 This scheduling algorithm is supported by the JVM to serve the thread with the highest priority first, since all Java threads have a priority. 

 </blockquote>

 </details>

 ---

 ## Problem Solving

11. Write a program using methods `set priority` and `get priority` to display the priority of the thread?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 <details><summary> Show Answer </summary>

<blockquote>

``` java
import java.lang.*;  
public class ThreadPriority extends Thread   
{  
public void run()  
{  
System.out.println("Inside the run() method");  
}  
public static void main(String argvs[])  
{  
Thread.currentThread().setPriority(6);  
System.out.println("Priority of the main thread is : " + Thread.currentThread().getPriority());  
ThreadPriority th1 = new ThreadPriority();  
System.out.println("Priority of the thread th1 is : " + th1.getPriority());  
}  
} 
```
</blockquote>

 <details><summary> Explanation </summary>

<blockquote>

- Using `currentThread()`,`getPriority())` and `setPriority(6)`methods, here the priority is displayed.
If there are two threads that have the same priority. 
- The execution then is dependent on the thread scheduler's algorithm (First Come First Serve, Round-Robin, etc.).

</blockquote>

 </details>

 
 </details>

 ---
 12. Write a program to throw an ` IllegalArgumentException` exception in thread?

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 <details><summary> Show Answer </summary>

<blockquote>

``` java
import java.lang.*;  
public class IllegalArgumentException extends Thread   
{  
public static void main(String argvs[])  
    {  
        Thread.currentThread().setPriority(17);  
        System.out.println("Priority of the main thread is : " + Thread.currentThread().getPriority());  
    }  
} 
```

</blockquote>

 <details><summary> Explanation </summary>

<blockquote>

-  The priority of the main thread is set to 17, which is greater than 10 (not in the range between minimum and maximum value), so it throws `IllegalArgumentException` exception.

</blockquote>

 </details>

 
 </details>
 ---

13. What is Daemon Thread and how it differs from normal thread?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)	
<details><summary> Show Answer </summary>

<blockquote>

- A Daemon thread is a low priority thread which always runs in the background.
- User is the high priority thread which runs in the foregground
 </details>

 ---
 14. How will you make the thread as Daemon thread?
	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details><summary> Show Answer </summary>
<blockquote>

- We have to use `setDaemonthread()` pass the boolean value to make the thread as Daemon thread.
- The `isDaemon()` returns a boolen value to check thread daemon or not.
``` java
public class Main {
	public static void main(String[] args) throws InterruptedException {
		Thread th0 = new Thread(() -> {
			for (int i = 0; i < 5; i++) {
				System.out.println("Hello from Thread-0");
			}
		});
		th0.setDaemon(true);
		System.out.println(th0.isDaemon());	//true
	}
}
```
 </details>
