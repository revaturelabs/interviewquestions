## Runnable Interface

1. How `Runnable` interface is used to create threads?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- The class which we want to make as thread should implement the interface `Runnable`.
- After implementing `Runnable` interface, the class should override the `run` method.
- After creating object for the class, we can't use `start()` method to run the method like thread creation by `Thread` class.
- Therefore, the object should be passed while creating object of thread class.
- While creating object for `Thread` class, we can pass the object which is created from class that implements `Runnable`.
- Now, we can use `start()` method.
</blockquote>

``` java
class Greeting implements Runnable{
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
		Thread th = new Thread(greeting);
		th.start();
	}
}
```

>When the method gets started by calling `start()` method, a new thread is created and starts executed it. On the time, the main thread will continue the remaining part. The thread will give the message `Hello` 10 times.
</details>
	
---

2. Is there way to create thread without implementing `Runnable` interface?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- `Runnable` interface is a Functional Interface which has only one abstract method - `run()`
-  We can create lambda expression for `Runnable` interface and create a thread.
``` java 

public class Main {
	public static void main(String[] args) {
		Runnable greeting = ()->{
			for(int i=0; i<10; i++) {
				System.out.println("Hello");
				try {Thread.sleep(1000);} catch(InterruptedException e){ };
			}
		};
		Thread th = new Thread(greeting);
		th.start();
	}
}
```
Above code, creates the thread and start printing "Hello" for 10 times in 1000ms interval.					   
</details>

---
	
3. Can we pass lambda expression while creating object of `Thread` class?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- Yes,We can pass lamba expression while creating the object of `Thread` class itself instead of creating lambda expression of `Runnable` interface.
- Becauase the passing parameter while creating object of `Thread` class will take only `Runnable` interface implementation.

``` java
public class Main {
	public static void main(String[] args) {
		Thread th = new Thread(()->{
			for(int i=0; i<10; i++) {
				System.out.println("Hello");
				try {Thread.sleep(1000);} catch(InterruptedException e){ };
			}
		});
		th.start();
	}
}
```
Above code, creates the thread and start printing "Hello" for 10 times in 1000ms interval.
</details>

---
