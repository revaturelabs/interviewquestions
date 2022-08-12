## Runnable Interface

1. Explain about lifecycle of thread.
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

- There are 5 states that thread has
  - **New** – When a thread begins the lifecycle and at the time of creating object for thread class. (Newly born thread)
  - **Runnable** – When a thread starts its execution in JVM. Waiting for resource allocation.
  - **Running** – When the thread is scheduled for executing.
  - **Blocked** – thread will be alive but blocked for monitor lock.
  - **Terminated** – when the thread stops its execution. (Either by completing the execution or by terminated abruptly).
</blockquote>
</details>

---

2. How can we check whether the thread terminated or not?
<details>
<summary><b> Show Answer <b></summary>

>We can use `isAlive()` method that returns a boolean value whether the thread is on process or not.

``` java 
import java.util.Random;
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Thread th = new Thread(()->{
			for(int i=0; i<10; i++) {
				System.out.println("Hello");
				try {Thread.sleep(1000);} catch(InterruptedException e){ };
			}
		});
		th.start();
		System.out.println(th.isAlive()); // true
	}
}
```

>`isAlive()` will give `true` because the thread is not terminated.
</details>

---

3. What will do `join()` method when we use in  thr program?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

- The method `join()` from Thread that is used to allow the thread to complete its execution  where another thread is waiting.
- The method `join()` will throw `InterruptedException`.
</blockquote>

``` java 
public class Main {
	public static void main(String[] args) throws InterruptedException {
		Thread th = new Thread(()->{
			for(int i=0; i<5; i++) {
				System.out.println("Hello");
				try {Thread.sleep(1000);} catch(InterruptedException e){ };
			}
		});
		th.start();
		th.join();
		System.out.println("The main thread");
	}
}

```
**Output**
```
Hello
Hello
Hello
Hello
Hello
The main thread
```
<blockquote>

- Here the `The main thread` is printed at last. 
- If the method `join` is not called, the main thread is executed and it will be in dead state.
- When `join()` method is called, the main is in waiting state. After the completion other, the main thread is executed.
</blockquote>
</details>

4. Can we find the name of thread?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

  Yes, we find the name of thread Using `getName()` method that returns a string which shows the name of the thread.
</blockquote>

``` java
public class Main {
	public static void main(String[] args) throws InterruptedException {
		Thread th = new Thread(()->{
			for(int i=0; i<5; i++) {
				System.out.println("Hello");
				try {Thread.sleep(1000);} catch(InterruptedException e){ };
			}
		});
		System.out.println(th.getName())  //Thread-0;
	}
}
```
</details>

5. Can we our own name to threads?
<details>
<summary><b> Show Answer <b></summary>

>Yes, we can give the name for thread in two ways.
  >1. We can use this `setName()` method to give name to thread.
   ``` java
   public class Main {
		public static void main(String[] args) throws InterruptedException {
			Thread th = new Thread(()->{
				for(int i=0; i<5; i++) {
					System.out.println("Hello");
					try {Thread.sleep(1000);} catch(InterruptedException e){ };
				}
			});
			th.setName("Hello");
			System.out.println(th.getName());  //Hello
		}
	}
	```
   >2. While creation itself we can give the name.
	``` java
   public class Main {
		public static void main(String[] args) throws InterruptedException {
			Thread th = new Thread(()->{
				for(int i=0; i<5; i++) {
					System.out.println("Hello");
					try {Thread.sleep(1000);} catch(InterruptedException e){ };
				}
			},"Hello");
			System.out.println(th.getName());  //Hello
		}
	}
	```
</details>

----

6. How will you check a thread is in which state?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

- We can call `getState()` using the object of the thread.
- It will give the state of the thread.
</blockquote>
</details>