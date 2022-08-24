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






