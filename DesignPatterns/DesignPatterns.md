1.How can you describe a design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Design patterns are the reusable solutions that solve common problems of software development. These problems include repetitive code, redundant functions and logic etc. These help to save considerable effort and time required for the developers while developing software. Design patterns are commonly used in object-oriented software products by incorporating best practices and promoting reusability for developing robust code.Defining  a pattern name and the classification of design pattern in which the pattern would fall to.Defining a Problem and its corresponding solution.The variations and language-dependent alternatives for the problem that needs to be addressed.The real-time use cases and the efficiency of the software that uses these patterns.
</blockquote>

</details>

---

2. How Inversion of Control can be used as a design pattern ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Inversion of control is a pattern used to decouple the dependencies between layers and components in the system. The Dependency-Injection (DI) pattern is an example of an IoC pattern that helps in removing dependencies in the code. For example, Consider we have a class A that makes use of class B as shown below:

```java

public class A{
   private B b;
   
   public A(){
       this.b = new B();
   }
}

```

Here, we have a dependency between classes A and B. If we had the IoC pattern implemented, we would not have used the new operator to assign value to the dependent variable. It would have been something as shown below:

```java

public class A {
   private IocB b;
   public A(IocB b) {
       this.b = b;
   }
}

```

We have inverted the control of handing the dependency of instantiating the object of class B to the IoC class IocB.

</blockquote>

</details>

---

3. How can you describe the SOLID Principles of the design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- S - Single Responsibility Principle (SRP): The single responsibility principle ensures that every class or module should be accountable and responsible for only one functionality. There should be one and only one reason for changing any class.
- O - Open Closed Principle (OCP): Every class is open for extension but closed for modification. Here, we are allowed to extend the entities behaviour by not modifying anything in the existing source code.
- L - Liskov Substitution Principle(LSP): LSP principle states that the objects can be replaced by the subtype instances without affecting the correctness of the program.
- I - Interface Segregation Principle (ISP): The ISP principle states that we can use as many interfaces specific to the client’s requirements instead of creating only one general interface. Clients should not be forced to implement the functionalities that they do not require.
- D - Dependency Inversion Principle: Here, the high-level modules should not be dependent on the lower level modules or concrete implementations. Instead, they should be dependent on the abstractions.

</blockquote>

</details>

---

4. What do you understand by the Open-Closed Principle (OCP)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


The Open close principle states that any class, component or entity should be open for extension but closed for modification. A class can be extended via Inheritance, Interfaces, Composition whenever required instead of modifying the code of the class. Consider an instance where we have a class that calculates the area of a square. Later, we get the requirement of calculating the area of a rectangle. Here, instead of modifying the original class, we can create one base class and this base class can be extended by the new class rectangle.

</blockquote>

</details>

---

5. What are the design patterns used in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Decorator pattern are used by the Wrapper classes.
- Singleton pattern is used in classes like Calendar and Runtime.
- Factory pattern is used for methods like Integer.valueOf methods in wrapper classes.
- Observer pattern is used for handling event frameworks like awt, swing etc

</blockquote>

</details>

---

6.How are design principles different from design patterns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Design principles are those principles that are followed while designing software systems for any platform by making use of any programming language. SOLID principles are the design principles that we follow as guidelines to develop robust, extensible and scalable software systems. These apply to all aspects of programming.
- Design Patterns are the reusable template solutions for commonly occurring problems that can be customized as per the problem requirements. These are well-implemented solutions that are tested properly and are safe to use. Factory Design Pattern, Singleton pattern, Strategy patterns are a few of the examples of design patterns

</blockquote>

</details>

---

7. How are design patterns different from algorithms?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Both Design Patterns and Algorithms describe typical solutions to any given problem. But the main difference is that the algorithm defines a clear set of actions for achieving a goal and a design pattern provides a high-level description of any solution. Design patterns applied to two different problems might be the same but the logic of implementation would be different and is based on the requirements

</blockquote>

</details>

---

8.Explain  Factory Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Factory design pattern belongs to the category of Creational Design Patterns. Here, the objects are created without exposing the logic of creation to the client. The objects refer to the common interface.This pattern allows hiding the creation logic of the application by using interfaces and factory classes.It lets to test the seamlessness of the application by using mock or stubs.
Introduces loose coupling in the application by allowing flexibility in the implementation of methods when new classes are introduced

For example, Let’s consider 3 classes Square, Rectangle and Triangle. We will be using factory patterns to create objects of these three classes without exposing the creation logic by making use of ShapeFactory class. The Driver class would be passing the information like rectangle,square,triangle for getting the required object. 

- Create a Shape interface.

```java

   public interface Shape {
      void draw();
   }

```

- Create concrete classes Rectangle, Square, Triangle that implements the Shape interface.

```java
 
   public class Rectangle implements Shape {
      @Override
      public void draw() {
         System.out.println("Rectangle Drawn");
      }
   }
   
   public class Square implements Shape {
      @Override
      public void draw() {
         System.out.println("Square Drawn");
      }
   }
  
   public class Triangle implements Shape {
      @Override
      public void draw() {
         System.out.println("Triangle Drawn");
      }
   }

```

- Create ShapeFactory class and create a method called getShapeInstance() for generating objects of the concrete classes defined above.

```java

   public class ShapeFactory {
      //the method will be used to get object of required shape
      public Shape getShapeInstance(String type){
         if(type == null){
            return null;
         } 
         if(type.equalsIgnoreCase("TRIANGLE")){
            return new Triangle();
         } else if(type.equalsIgnoreCase("SQUARE")){
            return new Square();
         } else if(type.equalsIgnoreCase("RECTANGLE")){
            return new Rectangle();
         }
         return null;
      }
   }

```

- Implement the Driver class and utilise the factory class for getting the object of the required type.

```java

   public class Driver {
      public static void main(String[] args) {
         ShapeFactory shapeFactory = new ShapeFactory();
         Shape triangle = shapeFactory.getShape("Triangle");
         triangle.draw();   
         Shape rectangle = shapeFactory.getShape("RECTANGLE");
         rectangle.draw();   
         Shape square = shapeFactory.getShape("SQUARE");
         square.draw();
      }
   }

```

- Output
  Triangle Drawn
  Rectangle Drawn
  Square Drawn

</blockquote>

</details>

---

9.Explain  an Adapter Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


The adapter design pattern falls under the category of a structural design pattern that lets incompatible objects collaborate. It acts as a wrapper between 2 different objects. The adapter catches the call for one object and transforms them to be recognizable by the second object.

Let us understand this with the help of an example of a USB to Ethernet adapter that is used when we have an ethernet interface at one end and the USB interface on the other end. The USB and ethernet are incompatible with each other which is why we require an adapter. The adapter class has a Client class that expects some object type and it has an Adaptee class that offers the same feature but by exposing a different interface. Now to make these both communicate, we have an Adapter class. The client requests the Adapter by using the target interface. The Adapter class translates the request using the Adaptee Interface on the adaptee. The Client receives the results unaware of the adapter’s role. This has been described in the class diagram as shown below:

Let us consider that we have a MediaPlayer Interface which is implemented by the AudioPlayer class. The AudioPlayer can play mp3 format by default. Consider another interface AdvancedPlayer that is being implemented by MP4Player class that plays mp4 formats and WAVPlayer that plays wav formats. If we want to make AudioPlayer class play other formats, then we make use of the MediaAdapter class that implements the MediaPlayer Interface and uses the AdvancedPlayer objects for playing the required format. The code implementation of this scenario is as follows:

```java

public interface MediaPlayer {
  public void play(String format, String file);
}

public interface AdvancedPlayer { 
  public void playMp4(String file);
  public void playWav(String file);
}

public class Mp4Player implements AdvancedPlayer{
  @Override
  public void playMp4(String file) {
     System.out.println("MP4 File "+ file + " Playing....");  
  }
  
  @Override
  public void playWav(String file) {
     
  }
}

public class WavPlayer implements AdvancedPlayer{
  @Override
  public void playMp4(String file) {
    
  }
  
  @Override
  public void playWav(String file) {
     System.out.println("WAV File "+ file + " Playing....");  
  }
}

public class MediaAdapter implements MediaPlayer {
  AdvancedPlayer advancedPlayer;
  public MediaAdapter(String format){
     if(format.equalsIgnoreCase("mp4") ){
        advancedPlayer = new Mp4Player();   
     }else if(format.equalsIgnoreCase("wav") ){
        advancedPlayer = new WAVPlayer();   
     }
  }
  @Override
  public void play(String format, String file) {
  
     if(format.equalsIgnoreCase("mp4")){
        advancedPlayer.playMp4(file);
     }
     else if(format.equalsIgnoreCase("wav")){
        advancedPlayer.playWav(file);
     }
  }
}

public class AudioPlayer implements MediaPlayer {
  MediaAdapter mediaAdapter;
  @Override
  public void play(String format, String file) {  
     
     if(format.equalsIgnoreCase("mp3")){
        System.out.println("MP3 file " + file +" Playing...");   
     } 
     
     else if(format.equalsIgnoreCase("wav") || format.equalsIgnoreCase("mp4")){
        mediaAdapter = new MediaAdapter(format);
        mediaAdapter.play(format, file);
     }
     else{
        System.out.println("Format not supported");
     }
  }   
}

public class Driver {
  public static void main(String[] args) {
     AudioPlayer audioPlayer = new AudioPlayer();
     audioPlayer.play("mp3", "music1.mp3");
     audioPlayer.play("wav", "music2.wav");
     audioPlayer.play("mp4", "music3.mp4");
     audioPlayer.play("avi", "music4.avi");
  }
}

Output:

MP3 file music1.mp3 Playing...
WAV File music2.wav Playing...
MP4 File music3.mp4 Playing...
Format not supported

```

</blockquote>

</details>

---

10.Explain  Proxy Design Pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Proxy design pattern falls under the category of structural design that represents the functionality of other classes. This pattern lets the developers provide a substitute for another object. This is called a proxy object. This helps to control the access to the original object and allows us to perform many tasks before or after the request reaches the original object. For ex, we have a ServiceInterface interface that has some operation. This interface is being implemented by a Service class and a Proxy class. The Service class has useful business logic and the Proxy class has a reference field pointing to the service object. Once the proxy finishes processing lazy initialization, logging, caching etc, the request will be passed to the service object. And finally, we have a client that works with the services and the proxies by using the interface. This helps to pass proxy objects to any piece of code

</blockquote>

</details>

---

11.Explain Bridge Design Pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The bridge pattern is a type of structural design pattern that lets to split large class or closely related classes into 2 hierarchies - abstraction and implementation. These hierarchies are independent of each other and are used whenever we need to decouple an abstraction from implementation. This is called a Bridge pattern because it acts as a bridge between the abstract class and the implementation class. In this pattern, the abstract classes and the implementation classes can be altered or modified independently without affecting the other one.

- Abstraction – This is the core of the pattern and it defines its crux. This contains a reference to the implementer.
- Refined Abstraction – This extends the abstraction and takes refined details of the requirements and hides it from the implementors.
- Implementer – This is the interface for the implementation classes.
- Concrete Implementation – These are the concrete implementation classes that implement the Implementer interface.

</blockquote>

</details>

---

12.In what scenarios we have to apply Chain of Responsibility pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Chain of Responsibility belongs to the category of a behavioural design pattern that passes requests via a chain of handlers. Whenever a request is received, the handler decides whether to process the request or pass it to the next handler of the chain. It is used for achieving loose coupling where the client request is passed through an object chain to process them.

There are 3 components of Chain of Responsibility design pattern, they are:

- Client: This is the point of request origination and the component that accesses the handler for handling the request.
- Handler: Handler can either be a class or an interface that received the request primarily and dispatches it to the chain of handlers. This Handler knows only the first handler of the chain.
- Concrete Handlers: These are the actual request handlers in sequential order.

This pattern can be used in the following cases:
- Whenever we want to decouple the sender and the receiver of the request.
- Whenever we want multiple objects to handle a request at runtime.
- Whenever we do not want to explicitly specify handlers in the code.
- Whenever we want to issue a request to several objects without explicitly specifying handlers.

</blockquote>

</details>

---

13.Explain Decorator Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Decorator design pattern belongs to the category of structural pattern that lets users add new features to an existing object without modifying the structure. This pattern creates a class called decorator class that acts as a wrapper to the existing class by keeping the signatures of class methods intact. This pattern makes use of abstract classes and interfaces with composition for implementing the wrapper. They are mostly used to apply SRP (Single Responsibility Principle) as we divide functionalities into classes with unique concerns. This pattern is structurally similar to the chain of responsibility pattern. Following are the steps to implement decorator design pattern:

Create an interface and concrete classes that implement this interface.
Create an abstract decorator class that implements the above interface.
Create a concrete decorator class that extends the above abstract class.
Use the concrete decorator class to decorate the interface objects and verify the output.
Let us understand this with the help of an example. Here, we will be creating a Shape Interface and concrete classes- Rectangle and Triangle that implement this Shape interface. We will be creating an abstract decorator class "ShapeDecorator" that implements the Shape interface. We will create RedColorDecorator that extends ShapeDecorator. We will be then using this decorator to implement the functionalities.

```java

   public interface Shape {
       void draw();
   }

   public class Rectangle implements Shape {
       @Override 
	public void draw(){
           System.out.println("Rectangle Drawn");
       }
   }
  
   public class Triangle implements Shape {
       @Override 
	public void draw(){
           System.out.println("Triangle Drawn");
       }
   }
   public abstract class ShapeDecorator implements Shape {
       protected Shape shapeDecorated;
       public ShapeDecorator(Shape shapeDecorated{
           this.shapeDecorated = shapeDecorated;
       }
       public void draw() { 
           shapeDecorated.draw(); 
       }
   }
   public class RedColorDecorator extends ShapeDecorator {
       public RedColorDecorator(Shape shapeDecorated)
       {
           super(shapeDecorated);
       }
       @Override 
       public void draw()
       {
           shapeDecorated.draw();
           setRedBorder(shapeDecorated);
       }
       private void setRedBorder(Shape shapeDecorated)
       {
           System.out.println("Red color border added");
       }
   }
   public class Driver {
       public static void main(String[] args)
       {
           Shape triangle = new Triangle();
           Shape redTriangle = new RedColorDecorator(new Triangle());
           Shape redRectangle = new RedColorDecorator(new Rectangle());
           triangle.draw();
           System.out.println(".........");
           redTriangle.draw();
           System.out.println(".........");
           redRectangle.draw();
           System.out.println(".........");
       }
   }

Output:
   Triangle Drawn
   .........
   Triangle Drawn
   Red color border added
   .........
   Rectangle Drawn
   Red color border added
   .........

```

</blockquote>

</details>

---

14.Explain Command Design Pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The Command pattern is a type of behavioural design pattern that transforms a request into a stand-alone object containing all the details about the request. This pattern is a data-driven pattern because we make use of the information about the request by wrapping it as an object and is passed to the invoker object checks for the object that can handle the command and passes it to that object to execute the command.

We have a client that calls the invoker to run a command. We have a Command interface that acts as an abstraction to the underlying concrete classes.For example, A remote control that has only one button. Using this button, we will be controlling the behaviour of two objects tubelight and a radio. The command to control the objects will be implemented using the command design pattern.


```java

   interface Command{
       public void execute();
   }
   class TubeLight{
       public void lightOn(){
           System.out.println("TubeLight on");
       }
       public void lightOff(){
           System.out.println("TubeLight off");
       }
   }
   
   class TubeLightOnCommand implements Command {
       TubeLight tubeLight;
       public TubeLightOnCommand(TubeLight tubeLight){
         this.tubeLight = tubeLight;
       }
       public void execute(){
         tubeLight.lightOn();
       }
   }
   class TubeLightOffCommand implements Command{
       TubeLight tubeLight;
       public TubeLightOffCommand(TubeLight tubeLight) {
           this.tubeLight = tubeLight;
       }
       public void execute() {
           tubeLight.lightOff();
       }
   }
   class Radio{
       public void radioOn(){
           System.out.println("Radio on ");
       }
       public void radioOff(){
           System.out.println("Radio off");
       }
       public void setVolume(int volumeLevel){
   
         System.out.println("Radio volume set to " + volumeLevel);
       }
   }
   
   class RadioOnCommand implements Command{
       Radio radio;
       public RadioOnCommand(Radio radio){
           this.radio = radio;
       }
       public void execute(){
         radio.radioOn();
       }
   }
   
   class RadioVolumeCommand implements Command{
       Radio radio;
       int volumeLevel;
       public RadioVolumeCommand(Radio radio, int volumeLevel){
           this.radio = radio;
           this.volumeLevel=volumeLevel;
       }
       public void execute(){
         radio.setVolume(volumeLevel);
       }
   }
   class RemoteControl{
       Command button; 
       public RemoteControl(){}
       public void setCommand(Command command){
           button = command;
       }
       public void pressButton(){
           button.execute();
       }
   }

```

- Create a Driver class to implement the pattern. Here we will be first turning on the tubelight on the first click of the button, on next click, we will be turning on the radio, then we will be setting the volume of the radio to 4 and then we will be turning off the tubelight.
 
```java

   public class Driver{
       public static void main(String[] args){
               RemoteControl remote = new RemoteControl();
               TubeLight tubeLight = new TubeLight();
               Radio radio = new Radio();
               remote.setCommand(new TubeLightOnCommand(tubeLight));
               remote.pressButton();
               remote.setCommand(new RadioOnCommand(radio));
               remote.pressButton();
               remote.setCommand(new RadioVolumeCommand(radio,4));
               remote.pressButton();
               remote.setCommand(new TubeLightOffCommand(tubeLight));
               remote.pressButton();
       }
   }

Output:

TubeLight on
   Radio on 
   Radio volume set to 4
   TubeLight off

```

</blockquote>

</details>

---

15.Explain Observer Design Pattern with an example?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
An observer design pattern is a type of behavioural design pattern that is used for defining the one to many dependencies between the objects. It is most useful when we want to get notified about any change in the state of an object. In this pattern, when the state of one object changes, all the dependent objects are notified automatically. The object whose state is monitored is called the Subject whereas the dependents are called the Observers. In Java, we can implement this pattern by making use of the java.util.Observable class and the java.util.Observer interface. 

This design pattern has 3 main components:

- Subject - This can be an interface or an abstract class that defines operations for attaching and detaching the observers to the subject.
- Concrete Subject - This is a concrete class of the Subject. This maintains the object state and whenever any change occurs in that state, the observers are notified about it using notifyObservers() method.
- Observer - This is an interface or an abstract class that defines the operations for notifying the object. One real work example of this pattern is Facebook or Twitter. Whenever a person updates the status, all the followers would get a notification about his update. An observer can get the notification of the subject as long as it is subscribed or keeping track of it


</blockquote>

</details>

---

16. Consider a scenario where you are writing classes for providing market data and we have the flexibility to switch to different vendors or we can be directed to the Direct Exchange Feed. How will you approach this problem to design the system?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
We can do this by having an interface called “MarketData” which will consist of the methods required by the Client. The MarketData should have the MarketDataProvider as the dependency by employing Dependency Injection. This ensures that even if the provider changes, the market data will not be impacted.

</blockquote>

</details>

---

17.Explain MVC design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
MVC stands for Model-View-Controller. This pattern is used for separating the application’s concerns as listed below:

- Model - This represents the object (Java POJO) that carries the data. It can also consist of the logic of updating the controller in case the data changes.
- View - This represents the data visualization of the model.
- Controller - This is an interface between the Model and the View by controlling the flow of data into the model and updating the view whenever the model gets updated. This ensures that the model and the views are kept separate.

</blockquote>

</details>

---

18.Explain the components of the Composite Entity pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
This pattern is used in EJB (Enterprise Java Beans) persistence mechanism. A composite entity represents the object graph and is an EJB entity. Whenever a composite entity is updated, the object beans that are internally dependent on this bean are updated automatically. There are 4 main components of the Composite Entity Pattern:

- Composite Entity - Primary entity bean that can have a coarse-grained object that is meant for persistence.
- Coarse-Grained Object - This contains the dependent objects which have their life cycle and in turn manages the lifecycle of dependent objects.
- Dependent Object - This object is dependent on the coarse-grained object throughout the persistence lifecycle.
- Strategies - These represent how to implement the composite entity.

</blockquote>

</details>

---

19.Explain the main advantage of using a prototype design pattern over object creation using a new keyword?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Prototype design pattern is used for creating duplicate objects based on the prototype of the already existing object using cloning. Doing this has a positive impact on the performance of object creation. Creating objects using the new keyword requires a lot of resources and is a heavyweight process that impacts performance. Hence, the prototype design pattern is more advantageous than the object created using a new keyword.

</blockquote>

</details>

---

20.How can you achieve thread-safe singleton patterns in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
A thread-safe singleton class is created which helps in object initialization in the presence of multiple threads. It can be done using multiple ways:

- Using Enums: Enums are the simplest means of creating a thread-safe singleton class in Java because the synchronization support is inherently done by Java itself. Enums are by default final and this also helps in preventing multiple initializations at the time of serialization.

```java

   public enum ThreadSafeSingleton{
      SINGLETON_INSTANCE;
      public void display(){
          System.out.println("Thread-safe singleton Display");
      }
   }
   ThreadSafeSingleton.SINGLETON_INSTANCE.show();

```

- Using Static Field Initialization: Thread-safe singleton can also be created by creating the instance at the time of class loading. This is achieved by making use of static fields as the Classloader guarantees that the instances are initialized during class loading and the instance is not visible until that has been fully created.

```java

   public class ThreadSafeSingleton{
      private static final ThreadSafeSingleton INSTANCE = new ThreadSafeSingleton();
      private ThreadSafeSingleton(){ }
      public static ThreadSafeSingleton getInstance(){
          return INSTANCE;
      }
      public void display(){
          System.out.println("Thread-safe Singleon");
      }
   }
   ThreadSafeSingleton.getInstance().display();

```

But the disadvantage of this way is that the initialization cannot be done lazily and the `getInstance()` method is called even before any client can call.

- Using synchronized keyword: We can make use of the synchronized keyword upon the getInstance method as shown below.In this method, we can achieve lazy initialization, and also since we use synchronized keywords, the object initialization is thread-safe.The only problem is that since the whole method is synchronized, the performance is impacted in the presence of multiple threads.

```java

   public class ThreadSafeSingleton{
    private static ThreadSafeSingleton instance;
    private ThreadSafeSingleton(){
      
    }
    synchronized public static ThreadSafeSingleton getInstance(){
      if (this.instance == null){
        this.instance = new ThreadSafeSingleton();
      }
      return this.instance;
    }
   }

```

- Double-check locking: Here, we will be using a synchronized block of code within the getInstance method instead of making the whole method synchronized. This ensures that only a handful of threads have to wait only for the first time thereby not impacting the performance.

```java

   public class ThreadSafeSingleton {
    private static ThreadSafeSingleton instance;
    private ThreadSafeSingleton(){
    
    }
    public static ThreadSafeSingleton getInstance(){
      if (instance == null){
        synchronized (ThreadSafeSingleton.class){
          if(instance==null){
            instance = new ThreadSafeSingleton();
          }
        }
      }
      return instance;
    }
   }

```

</blockquote>

</details>

---

21.Explain the benefits of design patterns in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Design patterns provide a template for developers which they can use in multiple projects. Design patterns in Java help the programmer design flexible and smart code and easily identify unwanted code. It benefits me as I can be faster at my job because of the ability to customise the architecture of multiple systems instead of repeatedly coding everything by hand.

</blockquote>

</details>

---

22. How is the bridge pattern different from the adapter pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The adapter and bridge patterns are very similar. They are both considered a form of encapsulation and facilitate more control over code changes without impacting the class structure. However, the main difference between the two is that using a bridge pattern separates the essential data from its implementation. In contrast, an adapter pattern allows incompatible classes to an interface without changing the source code.

</blockquote>

</details>

---

23. Which design pattern is used to get a way to access the elements of a collection object in sequential manner?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Iterator pattern is used to get a way to access the elements of a collection object in sequential manner.

</blockquote>

</details>

---

24. What is the difference between Strategy and State design Patterns in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The strategy design pattern defines a set of algorithms to carry out a specific behavior, whereas the State design pattern allows an object to alter its behavior when its internal state changes.
- The strategy design pattern does not allow us to store a reference to the context object, whereas the state design pattern stores the reference to the context object which contains them.
- In the strategy design pattern, the client is aware of the strategy which is chosen for implementation, whereas in the state design pattern, the client does not decide which state to be chosen for implementation.
- Strategy pattern deals with HOW an object performs a certain task, whereas the state design pattern deals with what an object is.
- There is no successor/predecessor relationship present in strategy design pattern, whereas states are related to one/another as successor & predecessor in state design pattern states.

</blockquote>

</details>

---

25. When to use the Composite design pattern in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Composite pattern is also a core Java design pattern, which allows you to treat both whole and part object to treat similarly. Client code, which deals with a Composite or individual object, doesn't differentiate between them, it is possible because the Composite class also implements the same interface as their individual part. One of the good examples of the Composite pattern from java is the JPanel class, which is both Component and Container.  When the paint() method is called on JPanel, it is internally called the paint() method of individual components and let them draw themselves.

</blockquote>

</details>

---

26.When to use the Template method design pattern in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The template pattern outlines an algorithm in the form of a template method and lets the subclass implement individual steps.The template method should be final so that the subclass can not override and change the steps of the algorithm. Still, the same time individual steps should be abstract, so that child classes can implement them.

</blockquote>

</details>

---

27.When to use Setter and Constructor Injection in the Dependency Injection pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
We can use setter injection to provide optional dependencies of an object and use Constructor injection to provide a mandatory dependency of an object, without which it can not work. Since Spring provides an IOC container, it also gives you a way to specify dependencies either by using setter methods or constructors.

</blockquote>

</details>

---

28.Explain Structural Patterns in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Structural patterns are used to provide solutions and efficient standards regarding class compositions and object structures. They depend on the concept of inheritance and interfaces to allow multiple objects or classes to work together and form a single working whole.Structural design patterns are responsible for how classes and objects can be composed to form larger structures.

</blockquote>

</details>

---

29.Describe in how many ways can you create a singleton pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
There are two ways of creating a Singleton pattern.

- Early Instantiation: It is responsible for the creation of instance at load time.

- Lazy Instantiation: It is responsible for the creation of instance when required.

</blockquote>

</details>

---

30.What is the proxy pattern, and what does it do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The term Proxy stands for an object representing another object. The proxy pattern provides a substitute or placeholder for another purpose to control access to it.According to Gangs of four, a Proxy Pattern "provides control for accessing the original object."We can perform many security operations like hiding the information of the original object, on-demand loading, etc.It is also called as placeholder or surrogates.

</blockquote>

</details>

---

31. How can you differentiate Dependency Injection and Service Locator patterns?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
The service locator is used to create class dependencies. The Class is still responsible for creating its dependencies no matter whether if it is using service locator or not.Service locators are also used to hide dependencies. We can't say by looking at an object whether it connects with a database or not when it obtains connections from a locator.

With Dependency injection, the class which contains its dependencies neither knows nor cares where they came from.One significant difference is that Dependency injection is much easier to unit test because we can pass in it mock implementations of its dependent objects. We could combine the two objects and apply the service locator.

</blockquote>

</details>

---

32. Explain the Intercepting Filter Design Pattern and also mention its benefits?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 

The intercepting filter design pattern is used to intercept and manipulate a request and response before and after the request processing. Filters perform the authentication/ authorization/ logging or tracking of request and then forward the requests to corresponding handlers. The basic entities of Intercepting design pattern.

- Filter:It performs a certain task before or after the execution of request by request handler.

- Filter Chain:It contains multiple filters and helps to execute them in defined order on target.

- Target:The target object is the request handler

- Filter Manager:It manages the filters and Filter Chain.

- Client:The client object is one who sends a request to the Target object.

- The Benefits of Intercepting Filter Design Pattern are Filter pattern provides central control with loosely coupled handlers.It expands reusability.The new filter can be added at any time without affecting the client's code.Filters can be selected dynamically during program execution.

</blockquote>

</details>

---

33. Explain Data Access Object (DAO) pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
 
Data Access Object Pattern is used to isolate low-level data accessing API or actions from high-level business services. Following are the components in the DAO Pattern.

- Data Access Object Interface:DAO interface describes the standard actions to be performed on a model objects.

- Data Access Object concrete class:This class implements a DAO interface. This class is accountable to get data from a data source which can be Xml/database or any other storage mechanism.

- Model Object or Value Object:This object is a plain old java object containing get/set methods to store data retrieved using DAO class.

</blockquote>

</details>

---

34. Explain how can you create a Singleton class in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We have to make the constructor private so that new operator cannot be used to instantiate the class and return an object if not null otherwise create the object and return the same via a method.

</blockquote>

</details>

---

35. Which pattern is useful when one has to pass data with multiple attributes in one shot from client to server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Transfer Object Pattern is useful when one has to pass data with multiple attributes in one shot from client to the server. Transfer object is also known as Value Object. Transfer Object is a simple POJO class having getter/setter methods and is serializable so that it can be transferred over the network. It does not have any behavior. Server Side business class normally fetches data from the database and fills the POJO and send it to the client or pass it by value. For client, transfer object is read-only. Client can create its own transfer object and pass it to server to update values in database in one shot. Following are the entities of this type of design pattern.

</blockquote>

</details>

---

36. Explain in singleton pattern whether it is better to make the whole getinstance() method synchronized or just critical section is enough? Which one is preferable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Synchronization of whole getinstance() method is costly and is only needed during the initialization on singleton instance, to stop creating another instance of Singleton. Therefore it is better to only synchronize critical section and not the whole method.

</blockquote>

</details>

---

37. Explain how can you prevent creating another instance of singleton using clone() method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The preferred way to prevent creating another instance of a singleton is by not implementing Cloneable interface and if you do just throw an exception from clone() method "not to create a clone of singleton class".

</blockquote>

</details>

---

38. What is the limitation of using singleton pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The singleton pattern ensures that a class has only one instance and to provide a global point of access to it. But at the same time this becomes its limitation as most classes in an application will need to create multiple instances.

</blockquote>

</details>

---

39. What are the drawbacks of using a singleton design pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Singleton causes code to be tightly coupled. The singleton object is exposed globally and is available to a whole application. Thus, classes using this object become tightly coupled; any change in the global object will impact all other classes using it.
- They hide dependencies instead of exposing them.
- Singleton Pattern does not support inheritance.
- Singleton principle can be violated by techniques such as cloning. If an application is running on multiple JVM’s, then, in this case, Singleton might be broken.

</blockquote>

</details>

---

40. Explain DAO design pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Data Access Object Pattern or DAO pattern is used to separate low level data accessing API or operations from high level business services. Following are the participants in Data Access Object Pattern.

- Data Access Object Interface:This interface defines the standard operations to be performed on a model objects.

- Data Access Object concrete class:This class implements above interface. This class is responsible to get data from a data source which can be database / xml or any other storage mechanism.

- Model Object or Value Object:This object is simple POJO containing get/set methods to store data retrieved using DAO class.

```java

public class Student {
   private String name;
   private int rollNo;

   Student(String name, int rollNo){
      this.name = name;
      this.rollNo = rollNo;
   }

   public String getName() {
      return name;
   }

   public void setName(String name) {
      this.name = name;
   }

   public int getRollNo() {
      return rollNo;
   }

   public void setRollNo(int rollNo) {
      this.rollNo = rollNo;
   }
}


import java.util.List;

public interface StudentDao {
   public List<Student> getAllStudents();
   public Student getStudent(int rollNo);
   public void updateStudent(Student student);
   public void deleteStudent(Student student);
}

import java.util.ArrayList;
import java.util.List;

public class StudentDaoImpl implements StudentDao {
	
   
   List<Student> students;

   public StudentDaoImpl(){
      students = new ArrayList<Student>();
      Student student1 = new Student("Alice",0);
      Student student2 = new Student("Ben",1);
      students.add(student1);
      students.add(student2);		
   }
   @Override
   public void deleteStudent(Student student) {
      students.remove(student.getRollNo());
      System.out.println("Student: Roll No " + student.getRollNo() + ", deleted from database");
   }

  
   @Override
   public List<Student> getAllStudents() {
      return students;
   }

   @Override
   public Student getStudent(int rollNo) {
      return students.get(rollNo);
   }

   @Override
   public void updateStudent(Student student) {
      students.get(student.getRollNo()).setName(student.getName());
      System.out.println("Student: Roll No " + student.getRollNo() + ", updated in the database");
   }
}

public class DaoPatternDemo {
   public static void main(String[] args) {
      StudentDao studentDao = new StudentDaoImpl();
      for (Student student : studentDao.getAllStudents()) {
         System.out.println("Student: [RollNo : " + student.getRollNo() + ", Name : " + student.getName() + " ]");
      }

      Student student =studentDao.getAllStudents().get(0);
      student.setName("Michael");
      studentDao.updateStudent(student);
      studentDao.getStudent(0);
      System.out.println("Student: [RollNo : " + student.getRollNo() + ", Name : " + student.getName() + " ]");		
   }
}

Output:

Student: [RollNo : 0, Name : Alice ]
Student: [RollNo : 1, Name : Ben ]
Student: Roll No 0, updated in the database
Student: [RollNo : 0, Name : Michael ]

```

</blockquote>

</details>
	
---

41. Explain front controller design pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The front controller design pattern is used to provide a centralized request handling mechanism so that all requests will be handled by a single handler. This handler can do the authentication/ authorization/ logging or tracking of request and then pass the requests to corresponding handlers. Following are the entities of this type of design pattern.

- Front Controller:Single handler for all kinds of requests coming to the application (either web based/ desktop based).

- Dispatcher:Front Controller may use a dispatcher object which can dispatch the request to corresponding specific handler.

- View:Views are the object for which the requests are made.

```java

public class HomeView {
   public void show(){
      System.out.println("Displaying Home Page");
   }
}

public class StudentView {
   public void show(){
      System.out.println("Displaying Student Page");
   }
}

public class Dispatcher {
   private StudentView studentView;
   private HomeView homeView;
   
   public Dispatcher(){
      studentView = new StudentView();
      homeView = new HomeView();
   }

   public void dispatch(String request){
      if(request.equalsIgnoreCase("STUDENT")){
         studentView.show();
      }
      else{
         homeView.show();
      }	
   }
}

public class FrontController {
	
   private Dispatcher dispatcher;

   public FrontController(){
      dispatcher = new Dispatcher();
   }

   private boolean isAuthenticUser(){
      System.out.println("User is authenticated successfully.");
      return true;
   }

   private void trackRequest(String request){
      System.out.println("Page requested: " + request);
   }

   public void dispatchRequest(String request){
      trackRequest(request);
      if(isAuthenticUser()){
         dispatcher.dispatch(request);
      }	
   }
}

public class FrontControllerPatternDemo {
   public static void main(String[] args) {
      FrontController frontController = new FrontController();
      frontController.dispatchRequest("Home");
      frontController.dispatchRequest("Student");
   }
}

Output:

Page requested: Home
User is authenticated successfully.
Displaying Home Page
Page requested: Student
User is authenticated successfully.
Displaying Student Page

```

</blockquote>

</details>

---
	
42. Explain service locator design pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The service locator design pattern is used when we want to locate various services using JNDI lookup. Considering high cost of looking up JNDI for a service, Service Locator pattern makes use of caching technique. For the first time a service is required, Service Locator looks up in JNDI and caches the service object. Further lookup or same service via Service Locator is done in its cache which improves the performance of application to great extent. Following are the entities of this type of design pattern.

- Service:The Actual Service which will process the request. Reference of such service is to be looked upon in JNDI server.

- Context / Initial Context:JNDI Context carries the reference to service used for lookup purpose.

- Service Locator:Service Locator is a single point of contact to get services by JNDI lookup caching the services.

- Cache:Cache to store references of services to reuse them

- Client:Client is the object that invokes the services via ServiceLocator.

```java


public interface Service {
   public String getName();
   public void execute();
}

public class Service1 implements Service {
   public void execute(){
      System.out.println("Executing Service1");
   }

   @Override
   public String getName() {
      return "Service1";
   }
}

public class Service2 implements Service {
   public void execute(){
      System.out.println("Executing Service2");
   }

   @Override
   public String getName() {
      return "Service2";
   }
}

public class InitialContext {
   public Object lookup(String jndiName){
   
      if(jndiName.equalsIgnoreCase("SERVICE1")){
         System.out.println("Looking up and creating a new Service1 object");
         return new Service1();
      }
      else if (jndiName.equalsIgnoreCase("SERVICE2")){
         System.out.println("Looking up and creating a new Service2 object");
         return new Service2();
      }
      return null;		
   }
}

import java.util.ArrayList;
import java.util.List;

public class Cache {

   private List<Service> services;

   public Cache(){
      services = new ArrayList<Service>();
   }

   public Service getService(String serviceName){
   
      for (Service service : services) {
         if(service.getName().equalsIgnoreCase(serviceName)){
            System.out.println("Returning cached  " + serviceName + " object");
            return service;
         }
      }
      return null;
   }

   public void addService(Service newService){
      boolean exists = false;
      
      for (Service service : services) {
         if(service.getName().equalsIgnoreCase(newService.getName())){
            exists = true;
         }
      }
      if(!exists){
         services.add(newService);
      }
   }
}

public class ServiceLocator {
   private static Cache cache;

   static {
      cache = new Cache();		
   }

   public static Service getService(String jndiName){

      Service service = cache.getService(jndiName);

      if(service != null){
         return service;
      }

      InitialContext context = new InitialContext();
      Service service1 = (Service)context.lookup(jndiName);
      cache.addService(service1);
      return service1;
   }
}

public class ServiceLocatorPatternDemo {
   public static void main(String[] args) {
      Service service = ServiceLocator.getService("Service1");
      service.execute();
      service = ServiceLocator.getService("Service2");
      service.execute();
      service = ServiceLocator.getService("Service1");
      service.execute();
      service = ServiceLocator.getService("Service2");
      service.execute();		
   }
}

Output:

Looking up and creating a new Service1 object
Executing Service1
Looking up and creating a new Service2 object
Executing Service2
Returning cached  Service1 object
Executing Service1
Returning cached  Service2 object
Executing Service2

```

</blockquote>

</details>

---
	
43. Describe Transfer Object pattern with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Transfer Object pattern is used when we want to pass data with multiple attributes in one shot from client to server. Transfer object is also known as Value Object. Transfer Object is a simple POJO class having getter/setter methods and is serializable so that it can be transferred over the network. It does not have any behavior. Server Side business class normally fetches data from the database and fills the POJO and send it to the client or pass it by value. For client, transfer object is read-only. Client can create its own transfer object and pass it to server to update values in database in one shot. Following are the entities of this type of design pattern.

- Business Object:Business Service fills the Transfer Object with data.

- Transfer Object:Simple POJO having methods to set/get attributes only.

- Client:Client either requests or sends the Transfer Object to Business Object.

```java

public class StudentVO {
   private String name;
   private int rollNo;

   StudentVO(String name, int rollNo){
      this.name = name;
      this.rollNo = rollNo;
   }

   public String getName() {
      return name;
   }

   public void setName(String name) {
      this.name = name;
   }

   public int getRollNo() {
      return rollNo;
   }

   public void setRollNo(int rollNo) {
      this.rollNo = rollNo;
   }
}


import java.util.*;

public class StudentBO {
	
   
   List<StudentVO> students;

   public StudentBO(){
      students = new ArrayList<StudentVO>();
      StudentVO student1 = new StudentVO("Robinson",0);
      StudentVO student2 = new StudentVO("Abraham",1);
      students.add(student1);
      students.add(student2);		
   }
   public void deleteStudent(StudentVO student) {
      students.remove(student.getRollNo());
      System.out.println("Student: Roll No " + student.getRollNo() + ", deleted from database");
   }

   public List<StudentVO> getAllStudents() {
      return students;
   }

   public StudentVO getStudent(int rollNo) {
      return students.get(rollNo);
   }

   public void updateStudent(StudentVO student) {
      students.get(student.getRollNo()).setName(student.getName());
      System.out.println("Student: Roll No " + student.getRollNo() +", updated in the database");
   }
}

public class TransferObjectPatternDemo {
   public static void main(String[] args) {
      StudentBO studentBusinessObject = new StudentBO();

      for (StudentVO student : studentBusinessObject.getAllStudents()) {
         System.out.println("Student: [RollNo : " + student.getRollNo() + ", Name : " + student.getName() + " ]");
      }

      StudentVO student = studentBusinessObject.getAllStudents().get(0);
      student.setName("Michael");
      studentBusinessObject.updateStudent(student);
      student = studentBusinessObject.getStudent(0);
      System.out.println("Student: [RollNo : " + student.getRollNo() + ", Name : " + student.getName() + " ]");
   }
}

Output:
Student: [RollNo : 0, Name : Robinson ]
Student: [RollNo : 1, Name : Abraham]
Student: Roll No 0, updated in the database
Student: [RollNo : 0, Name : Michael ]

```

</blockquote>

</details>

---

44. How do you create a  Singleton Design pattern?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Define a private static attribute in the "single instance" class.
- Define a public static accessor function in the class.
- Do "lazy initialization" (creation on first use) in the accessor function.
- Define all constructors to be protected or private.
- Clients may only use the accessor function to manipulate the Singleton.

```java

public class Singleton {
   private static Singleton singletonInstance = new Singleton()

   private Singleton(){}

   public static Singleton getInstance(){
      return instance;
   }

   public void showMessage(){
      System.out.println("Hello");
   }
}

public class SingletonDemo {
   public static void main(String[] args) {
	
	Singleton object = Singleton.getInstance();
	object.showMessage();
   }
}


```

</blockquote>

</details>
	
---

45. Explain  eager initialization in singleton?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

In eager initialization, the instance of Singleton Class is created at the time of class loading.This is the easiest method but it has a drawback that instance is created even though it might not be using it by any client.If singleton class is not using a lot of resources, this is the approach to use.
But in most of the scenarios, Singleton classes are created for resources such as Database connections etc and we should avoid the instantiation until client calls the getInstance method.

```java

public class EagerInitialized{
    
    private static final EagerInitialized instance = new EagerInitialized();
    
    private EagerInitialized(){}

    public static EagerInitialized getInstance(){
        return instance;
    }
}


```

</blockquote>

</details>
	
---

46. Explain Lazy Initialization in Singleton?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Lazy initialization method to implement Singleton pattern creates the instance in the global access method. Here is the sample code for creating Singleton class with this approach.The below implementation works fine incase of single threaded environment but when it comes to multithreaded systems. It can cause issues if multiple threads are inside the if loop at the same time. It will destroy the singleton pattern and both threads will get the different instances of singleton class.

```java

public class LazyInitialized {

    private static LazyInitialized instance;
    
    private LazyInitialized(){}
    
    public static LazyInitialized getInstance(){
        if(instance == null){
            instance = new LazyInitialized();
        }
        return instance;
    }
}

```

</blockquote>

</details>
	
---
	
47. How to implement singleton class with Serialization in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Lazy initialization method to implement Singleton pattern creates the instance in the global access method. Here is the sample code for creating Singleton class with this approach.The below implementation works fine incase of single threaded environment but when it comes to multithreaded systems. It can cause issues if multiple threads are inside the if loop at the same time. It will destroy the singleton pattern and both threads will get the different instances of singleton class.Sometimes in distributed systems, we need to implement Serializable interface in Singleton class.So that we can store it’s state in file system and retrieve it at later point of time. Here is a small singleton class that implements Serializable interface also.The problem with this serialized singleton class is that whenever we deserialize it, it will create a new instance of the class. 

```java

import java.io.Serializable;

public class SerializedSingleton implements Serializable{

    private static final long serialVersionUID = -1;

    private SerializedSingleton(){}
    
    private static class SingletonHelper{
        private static final SerializedSingleton instance = new SerializedSingleton();
    }
    
    public static SerializedSingleton getInstance(){
        return SingletonHelper.instance;
    }
    
}

import java.io.*;

public class SingletonSerializedTest {

    public static void main(String[] args) throws FileNotFoundException, IOException, ClassNotFoundException {
        SerializedSingleton instanceOne = SerializedSingleton.getInstance();
        ObjectOutput out = new ObjectOutputStream(new FileOutputStream("abc.ser"));
        out.writeObject(instanceOne);
        out.close();
        ObjectInput in = new ObjectInputStream(new FileInputStream( "abc.ser"));
        SerializedSingleton instanceTwo = (SerializedSingleton) in.readObject();
        in.close();
        System.out.println("instanceOne hashCode="+instanceOne.hashCode());
        System.out.println("instanceTwo hashCode="+instanceTwo.hashCode());
        
    }

}

So it destroys the singleton pattern, to overcome this scenario all we need to do it provide the implementation of readResolve() method.

protected Object readResolve() {
    return getInstance();
}

Output:
instanceOne hashCode=4011113421
instanceTwo hashCode=209678522

```

</blockquote>

</details>
	
---
	
48. When will you prefer to use a Factory Pattern?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- A class does not know which class of objects it must create.
- Factory pattern can be used where we need to create an object of any one of sub-classes depending on the data provided.

</blockquote>

</details>

---

49. Differentiate Factory Vs Builder Design Pattern Vs Strategy Design Pattern ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Factory Pattern deals with creation of objects delegated to a separate factory class whereas Builder pattern is the extension of Factory pattern wherein the Builder class builds a complex object in multiple steps.  

- Factory is a creational design pattern whereas Strategy is behavioral design pattern. Factory revolves around the creation of object at runtime whereas Strategy or Policy revolves around the decision at runtime.  

</blockquote>

</details>

<details><summary><b> Explanation </b></summary>

<blockquote>
	
---

50. What specific problems builder pattern solves?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

This pattern was introduced to solve some of the problems with Factory and Abstract Factory design patterns.When the Object contains a lot of attributes. Builder pattern solves the issue with large number of optional parameters and inconsistent state by providing a way to build the object step-by-step and provide a method that will actually return the final Object. 

</blockquote>

</details>
	
----
	
