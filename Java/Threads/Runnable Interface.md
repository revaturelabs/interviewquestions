## Runnable Interface

1. How can we create thread by extending `Thread` class?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

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

2. Can we use Lambda expression instead of creating class and implementing `Runnable`?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

- `Runnable` interface is single abstract method interface.
- We can create lambda expression for interface which single abstract method.
- So, we can use lambda expression for `Runnable` interface.
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
>When the method gets started by calling `start()` method, a new thread is created and starts executed it. On the time, the main thread will continue the remaining part. The thread will give the message `Hello` 10 times.
</details>

3. Can we pass lambda expression while creating object of `Thread` class?
<details>
<summary><b> Show Answer <b></summary>
<blockquote>

- We can pass lamba expression while creating the object of `Thread` class itself instead of creating lambda expression of `Runnable` interface.
- Beacuase the passing parameter while creating object of `Thread` class will take only `Runnable` interface implementation.

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
>When the method gets started by calling `start()` method, a new thread is created and starts executed it. On the time, the main thread will continue the remaining part. The thread will give the message `Hello` 10 times.
</details>
