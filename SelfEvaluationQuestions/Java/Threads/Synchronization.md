## Synchronization

1. What will happen when we use `synchronized` keyword before a method?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- When synchronized keyword is used before the method,the method becomes thread safe.
- One thread can utilize the memory at the time.
</blockquote>

``` java
class Increament{
	int c=0;
	void increase(){
		c++;
	}
}
public class Main {
	public static void main(String[] args) throws InterruptedException {
		Increament inc = new Increament();
		Thread th1 = new Thread(()->{
			for(int i=0; i<500; i++) {
				inc.increase();
			}
		});
		Thread th2 = new Thread(()->{
			for(int i=0; i<500; i++) {
				inc.increase();
			}
		});
		th1.start();
		th2.start();
		th1.join();
		System.out.println(inc.c); // 567/678/866/...
	}
}
```
>The output will not be stable on each time the output differs due to multithreads acting.
``` java
class Increament{
	int c=0;
	synchronized void increase(){
		c++;
	}
}
public class Main {
	public static void main(String[] args) throws InterruptedException {
		Increament inc = new Increament();
		Thread th1 = new Thread(()->{
			for(int i=0; i<500; i++) {
				inc.increase();
			}
		});
		Thread th2 = new Thread(()->{
			for(int i=0; i<500; i++) {
				inc.increase();
			}
		});
		th1.start();
		th2.start();
		th1.join();
		System.out.println(inc.c); //1000
	}
}
```
>By the use of `synchronized` keyword, only one thread can act to a thread. So, the output is stable.

</details>

---

2. How will we make a method as `asynchronized`?
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- All the methods by default is asynchronized.
- There is no keyword to make method as asynchronized.
</details>

---

3. How will you move a thread to the waiting state?
	
![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- The method `wait()` will move the current thread to the waiting state.
- `wait()` method is in `java.lang` package and called only from sychronized method.
</blockquote>
</details>

---

4. How will you wake a thread from waiting state?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- We can wake a thread using the `notify()` method. 
- `notify()` method from `java.lang` package and called only from sychronized method.
- The waiting state will be released only by `notify()` or `notifyAll()` method which is object's monitor.
</blockquote>
</details>

---

5. How will we wake all thread from waiting state?
	
![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- We can wake all threads using the `notifyAll()`  method. 
- It is a method from `java.lang` package.
- This method is called only from sychronized method.
- TThe waiting state will be released only by `notify()` or `notifyAll()` method which is object's monitor.
</blockquote>
</details>

---

6. What is the use of `yield()` method?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- The `yield()` method is a static method of Thread class.
- It can be used to stop the current thread that is executing and scheduler give the chance to other thread which is in the same priority.
</blockquote>
</details>

---

7. What is the difference between `yield()` and `wait()` method?
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- The `wait()` method is used for inter communication between the threads.
- The `yield` method is used stop the current thread and give change to another thread which in the same priority.
</blockquote>
</details>

---
	
8. What is the difference between `sleep()` and `wait()` method?
	
![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
<summary><b> Show Answer </b></summary>
<blockquote markdown="1">

- The `sleep()` method is used to pause the thread for require time.
- The `wait()` method is used to make the thread in waiting state until the `notify()` or `notifyAll()` called.
</blockquote>
</details>
	
---
