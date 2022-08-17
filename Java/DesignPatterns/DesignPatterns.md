1.What is Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

> Design patterns are a toolkit of tried and tested solutions to common problems in software design. Even if you never encounter these problems, knowing patterns is still useful because it teaches you how to solve all sorts of problems using principles of object-oriented design.


</details>

---

2.Explain the types of Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Creational design patterns provide solution to instantiate an object in the best possible way for specific situations.These design patterns are used when decision must be made at the time of creating an object of a class.
>- Structural design patterns provide different ways to create a class structure by using inheritance and composition to create a large object from small objects.
>- Behavioral design patterns provide solution for the better interaction between objects and how to provide loose coupling and flexibility to extend easily.

</details>

---

3.Explain the types of Creational Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Singleton pattern restricts the instantiation of a class and ensures that only one instance of the class exists in the Java virtual machine. It seems to be a very simple design pattern but when it comes to implementation, it comes with a lot of implementation concerns. 
>- Factory pattern is used when we have a superclass with multiple sub-classes and based on input, we need to return one of the sub-class. This pattern takes out the responsibility of the instantiation of a class from the client program to the factory class. We can apply a Singleton pattern on the Factory class or make the factory method static. 
>- Abstract Factory Pattern is used create an interface or abstract class for creating families of related or dependent objects but without specifying their concrete sub-classes.
>- Builder pattern solves the issue with a large number of optional parameters and inconsistent state by providing a way to build the object step-by-step and provide a method that will actually return the final Object. 
>- Prototype Pattern is used when the Object creation is a costly affair and requires a lot of time and resources and you have a similar object already existing. So, this pattern provides a mechanism to copy the original object to a new object and then modify it according to our needs. This pattern uses java cloning to copy the object. Prototype design pattern mandates that the Object which you are copying should provide the copying feature. It should not be done by any other class. However, whether to use the shallow or deep copy of the Object properties depends on the requirements and it’s a design decision. 

</details>

---

4.Explain the types of Structural Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Adapter pattern is one of the structural design patterns and it’s used so,that two unrelated interfaces can work together. The object that joins these unrelated interfaces is called an Adapter. 
>- Composite pattern is one of the Structural design patterns and is used when we have to represent a part-whole hierarchy. When we need to create a structure in a way that the objects in the structure have to be treated the same way, we can apply the composite design pattern. 
>- Proxy pattern is to provide a surrogate or placeholder for another object to control access to it. The definition itself is very clear and proxy pattern is used when we want to provide controlled access of a functionality.
>- Flyweight pattern is used when we need to create a lot of Objects of a class. Since, every object consumes memory space the flyweight design pattern can be applied to reduce the load on memory by sharing objects. String Pool implementation in java is one of the best examples of Flyweight pattern implementation. 
>- Facade pattern is used to help client applications to easily interact with the system. 
>- Bridge patterns have interface hierarchies in both interfaces as well as implementations, then the bridge design pattern is used to decouple the interfaces from implementation and hiding the implementation details from the client programs. 
>- Decorator pattern is used to modify the functionality of an object at runtime. At the same time, other instances of the same class will not be affected by this. So,individual object gets the modified behavior. 

</details>

---

5.Explain the types of Behavioral Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Template method pattern is a behavioral design pattern and it’s used to create a method stub and deferring some of the steps of implementation to the subclasses. The template method defines the steps to execute an algorithm and it can provide a default implementation that might be common for all or some of the subclasses. 
>- Mediator pattern is used to provide a centralized communication medium between different objects in a system. The mediator design pattern is very helpful in an enterprise application where multiple objects are interacting with each other. If the objects interact with each other directly, the system components are tightly coupled with each other which makes maintainability cost higher and not flexible to extend easily. The mediator pattern focuses on to provide a mediator between objects for communication and help in implementing loose-coupling between objects. 
>- Chain of responsibility pattern is used to achieve loose coupling in software design where a request from the client is passed to a chain of objects to process them. Then the object in the chain will decide who will be processing the request and whether the request is required to be sent to the next object in the chain or not. We know that we can have multiple catch blocks in a try-catch block code. Here every catch block is kind of a processor to process that particular exception. So,when an exception occurs in the try block, it’s sent to the first catch block to process. If the catch block is not able to process it, it forwards the request to the next object in chain i.e next catch block. If even the last catch block is not able to process it, the exception is thrown outside of the chain to the calling program. 
>- Observer  pattern is useful when you are interested in the state of an object and want to get notified whenever there is any change. In observer pattern, the object that watches on the state of another object is called Observer and the object that is being watched is called Subject. Java provides an inbuilt platform for implementing Observer pattern through java.util.Observable class and java.util.Observer interface. 
>- Strategy pattern is used when we have multiple algorithms for a specific task and the client decides the actual implementation be used at runtime. A strategy pattern is also known as Policy Pattern. We define multiple algorithms and let client applications pass the algorithm to be used as a parameter. One of the best examples of this pattern is the Collections.sort() method that takes the Comparator parameter. Based on the different implementations of Comparator interfaces, the Objects are getting sorted in different ways. 
>- Command pattern is used to implement loose coupling in a request-response model. In command pattern, the request is send to the invoker and invoker pass it to the encapsulated command object. Command object passes the request to the appropriate method of receiver to perform the specific action. Let’s say we want to provide a File System utility with methods to open, write, and close the file and it should support multiple operating systems such as Windows and Unix. To implement our File System utility, first of all, we need to create the receiver classes that will actually do all the work. Since, we code in terms of Java interfaces, we can have FileSystemReceiver interface and it’s implementation classes for different operating system flavors such as Windows, Unix, Solaris, etc. 
>- State pattern is used when an Object changes its behavior based on its internal state. If we have to change the behavior of an object based on its state, we can have a state variable in the Object and use if-else condition block to perform different actions based on the state. The state pattern is used to provide a systematic and loosely coupled way to achieve this through Context and State implementations. 
>- Visitor pattern is used when we have to perform an operation on a group of similar kinds of Objects. With the help of a visitor pattern, we can move the operational logic from the objects to another class. For example, think of a Shopping cart where we can add a different type of items (Elements), when we click on the checkout button, it calculates the total amount to be paid. Now we can have the calculation logic in item classes or we can move out this logic to another class using the visitor pattern. 
>- Interpreter pattern is used to defines a grammatical representation for a language and provides an interpreter to deal with this grammar. The best example of this pattern is a java compiler that interprets the java source code into byte code that is understandable by JVM. 
>Iterator pattern in one of the behavioral patterns and it’s used to provide a standard way to traverse through a group of Objects. Iterator pattern is widely used in Java Collection Framework where Iterator interface provides methods for traversing through a collection. 
>- Memento pattern is used when we want to save the state of an object so that we can restore later on. Memento pattern is used to implement this in such a way that the saved state data of the object is not accessible outside of the object, this protects the integrity of saved state data. Memento pattern is implemented with two objects – Originator and Caretaker. The originator is the object whose state needs to be saved and restored and it uses an inner class to save the state of Object. The inner class is called Memento and it’s private so that it can’t be accessed from other objects. 

</details>

---

6.Write the missing code in  the following program.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
import java.io.*;      
abstract class EBPlan{  
         protected double rate;  
         abstract void getRate();  
         public void calculateBill(int units){  
              System.out.println(units*rate);  
          }  
}

class  DomesticPlan extends EBPlan{  
         public void getRate(){  
             rate=1.50;              
        }  
   }

class  CommercialPlan extends EBPlan{    
    public void getRate(){   
        rate=6.50;  
   }   

class  InstitutionalPlan extends EBPlan{   
    public void getRate(){   
        rate=3.50;  
   }  




// write the missing code here



class BillDemo{  
    public static void main(String args[])throws IOException{  
      Plan bill = new Plan();  
        
      System.out.println("Enter the name of plan for which the bill will be generated: ");  
      BufferedReader br=new BufferedReader(new InputStreamReader(System.in));  
  
      String planName=br.readLine();  
      System.out.println("Enter the number of units for bill will be calculated: ");  
      int units=Integer.parseInt(br.readLine());  
  
      EBPlan p = bill.getPlan(planName);  
      
  
       System.out.print("Bill amount for "+planName+" of  "+units+" units is: ");  
           p.getRate();  
           p.calculateBill(units);  
            }  
    }
```
<details><summary><b> Show Answer</b></summary>

```java
class Plan{  
       public EBPlan getPlan(String planType){  
            if(planType == null){  
             return null;  
            }  
          if(planType.equalsIgnoreCase("Domesticplan")) {  
                 return new DomesticPlan();  
               }   
           else if(planType.equalsIgnoreCase("Commercialplan")){  
                return new CommercialPlan();  
            }   
          else if(planType.equalsIgnoreCase("Institutionalplan")) {  
                return new InstitutionalPlan();  
          }  
      return null;  
   }  
}
```

<details><summary><b> Explanation</b></summary>
<blockquote>
Enter the name of plan for which the bill will be generated:Domestic Plan
Enter the number of units for bill will be calculated: 100
Bill amount for Domestic Plan of  100 units is:150
</blockquote>

>- Create an EBPlan abstract class and create the concrete classes that extends EBPlan abstract class. >- Create a Plan class to generate object of concrete classes based on given information and use getPlan method to get object of type Plan class.  
>- Create a  BillDemo by using the Plan class to get the object of concrete classes by passing an information such as type of plan Domesticplan or Commercialplan or INSTITUTIONALPLAN.
>- call getRate() method and calculateBill()method of DomesticPaln.  

</details>
</details>

___

7.Write some code to create a early instantiation in Singleton design pattern. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

``` java 
class Singleton1{  
 private static Singleton1 obj=new Singleton1(); 
 private Singleton1(){}  
   
 public static Singleton1 getA(){  
  return obj;  
 }  
  
 public void doSomething(){  
 
 }  
}  
```

<details><summary><b> Explanation</b></summary>

we create the instance of the class at the time of declaring the static data member.So,instance of the class is created at the time of classloading.

</details>
</details>

---

8.what are the advantages and usages of Abstract Factory Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Abstract Factory Pattern isolates the client code from concrete (implementation) classes.It eases the exchanging of object families.
It promotes consistency among objects.
>- When the system needs to be independent of how its object are created, composed, and represented.When the family of related objects has to be used together, then this constraint needs to be enforced.When you want to provide a library of objects that does not show implementations and only reveals interfaces.When the system needs to be configured with one of a multiple family of objects.

</details>

---

9.Write some code to create a lazy  instantiation  in  Singleton design pattern.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

``` java 
class Lazy{  
 private static Lazy obj;  
 private Lazy(){}  
   
 public static Lazy getA(){  
   if (obj == null){  
      synchronized(Singleton.class){  
        if (obj == null){  
            obj = new Singleton(); 
        }  
    }              
    }  
  return obj;  
 }  
  
 public void doSomething(){  
  
 }  
}  
```

<details><summary><b> Explanation</b></summary>

we create the instance at the request time.
</details>
</details>

---

10.Write some code to create a concrete classes and abstract class for abstract factory design pattern.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

``` java 

import java.io.*;     
interface Bank{  
        String getBankName();  
}  
abstract class Loan{  
   protected double rate;  
   abstract void getInterestRate(double rate);  
}
abstract class Bank1{  
  public abstract Bank getBank(String bank);  
  public abstract Loan getLoan(String loan);  
}  

class DiffBank extends Bank1{  
   public Bank getBank(String bank){  
      if(bank == null){  
         return null;  
      }  
      if(bank.equalsIgnoreCase("Kotak")){  
         return new Kotak();  
      } else if(bank.equalsIgnoreCase("idfc")){  
         return new idfc();  
      } else if(bank.equalsIgnoreCase("idbi")){  
         return new idbi();  
      }  
      return null;  
   }  
  public Loan getLoan(String loan) {  
      return null;  
   }  
}
```

<details><summary><b> Explanation</b></summary>

we create a concrete classes DiffBank and abstract classes  for Loan and Bank1 and inherited the classes.
</details>
</details>
 
 ---

11.what are the advantages and usages  of Prototype Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Prototype Pattern reduces the need of sub-classing.It hides complexities of creating objects.The clients can get new objects without knowing which type of object it will be.It lets you add or remove objects at runtime.
>- When the classes are instantiated at runtime.When the cost of creating an object is expensive or complicated.When you want to keep the number of classes in an application minimum.When the client application needs to be unaware of object creation and representation.

</details>

---

12.Write some code to create an adapter class for adapter factory design pattern.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

``` java 
public class Bank{  
    private String BankName;  
    private String AccountHolderName;  
    private long AccountNumber;  
      
    public String getBankName() {  
        return BankName;  
    }  
    public void setBankName(String bankName) {  
        this.BankName = BankName;  
    }  
    public String getAccountHolderName() {  
        return AccountHolderName;  
    }  
    public void setAccountHolderName(String AccountHolderName) {  
        this.AccountHolderName= AccountHolderName;  
    }  
    public long getAccountNumber() {  
        return AccountNumber;  
    }  
    public void setAccNumber(long AccountNumber) {  
        this.AccountNumber = AccountNumber;  
    }  
} 
```

<details><summary><b> Explanation</b></summary>

The Bank class is a wrapper class which implements the setter and getter methods and modifies the specific request available from the Adapter class.

</details>
</details>

---

13:What are the elements  of Composite Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

>- Component declares the interface for objects in composition.It implements default behavior for the interface common to all classes as appropriate.
It declares an interface for accessing and managing its child components.
>- Leaf represents leaf objects in composition. A leaf has no children.It defines behavior for primitive objects in the composition.
>- Composite defines behavior for components having children.It Stores child component.It implements child related operations in the component interface.
>- Client manipulates objects in the composition through the component interface.

</details>

---

14:Write some code to create a class for Composite design pattern? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

``` java 
import java.util.*;  
public interface Employee {  
    public  int getId();  
    public String getName();  
    public double getSalary();  
       public void print();  
    public void add(Employee employee);  
       public void remove(Employee employee);  
       public Employee getChild(int i);  
}

  
public class Bank implements Employee {  
     private int id;  
     private String name;  
     private double salary;  
  
     public Bank(int id,String name,double salary) {  
      this.id=id;      
      this.name = name;  
      this.salary = salary;  
     }  
         List<Employee> employees = new ArrayList<Employee>();  
      
     public void add(Employee employee) {  
        employees.add(employee);  
     }  
        
     public Employee getChild(int i) {  
      return employees.get(i);  
     }  
     
     public void remove(Employee employee) {  
      employees.remove(employee);  
     }    
      
     public int getId()  {  
      return id;  
     }  
      
     public String getName() {  
      return name;  
     }  
    
     public double getSalary() {  
      return salary;  
     }  
     
     public void print() {  
      System.out.println("==========================");  
      System.out.println("Id ="+getId());  
      System.out.println("Name ="+getName());  
      System.out.println("Salary ="+getSalary());  
      System.out.println("==========================");  
        
      Iterator<Employee> t = employees.iterator();  
        
          while(t.hasNext())  {  
            Employee employee = t.next();  
            employee.print();  
         }  
     }  
}
```

<details><summary><b> Explanation</b></summary>

The Bank class is a Composite class which implements the setter and getter methods and implements the methods which are declared in the employee interface.
</details>
</details>
 
---

15:Write the missing  code in the main method for implementing the singleton? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java 
public final class Singleton {
    private static Singleton instance;
    public String value;

    private Singleton(String value) {
        try {
            Thread.sleep(1000);
        } catch (InterruptedException ex) {
            ex.printStackTrace();
        }
        this.value = value;
    }

    public static Singleton getInstance(String value) {
        if (instance == null) {
            instance = new Singleton(value);
        }
        return instance;
    }
}

public class DemoSingleThread {
    public static void main(String[] args) {
       
// Write the missing code
    }
}


```
<details><summary><b> Show Answer</b></summary>

``` java 
public class DemoSingletonThread {
    public static void main(String[] args) {
        System.out.println("RESULT:" + "\n");
        Singleton singleton = Singleton.getInstance("REVATURE");
        Singleton anotherSingleton = Singleton.getInstance("INDIA");
        System.out.println(singleton.value);
        System.out.println(anotherSingleton.value);
    }
}
```
<details><summary><b> Explanation</b></summary>
If you see the same value, then singleton was reused and If you see different values, then 2 singletons were created.
</details>
</details>

---

16:What are the steps to create a Factory Design Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Define an interface or abstract class for creating an object, but let the subclass decide which class to instantiate.
- Promotes loose-coupling by eliminating the need to directly interact with the subclass.
- Steps to implement Factory pattern:
- Define an abstract class or interface
- Define multiple child classes
- Define a Factory class that creates the child class and returns the parent class reference.
- Creation of child classes should happen only through the factory method.

</blockquote>
</details>

---

17:Write the missing  code in the main method for implementing the Factory Design Pattern? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java 
public class FactoryPattern {
        public static class PersonFactory {
            public static Person getPerson(String name, String gender) {
                if(gender.equalsIgnoreCase("M")) {
		     return new Male(name);
               } else if(gender.equalsIgnoreCase("F")) {
                    return new Female(name);
                } 
               return null;
            }
        }
  }
    static abstract class Person {
        Person(String name) {
            this.name = name;
        }
        private String name;
        abstract String getSalutation();
        String getNameAndSalutation() {   
        }
    }
    static class Male extends Person {
        public Male(String name) {
            super(name);
        }
        String getSalutation() {
            return "Mr";
        }
    }
    static class Female extends Person {
       public Female(String name) {
            super(name);
        }

        String getSalutation() {
           return "Miss/Mrs";
        }
    }
    public static void main(String[] args) {

   //Write the missing code


    }

```
<details><summary><b> Show Answer</b></summary>

``` java 
 public static void main(String[] args) {
        Person male = PersonFactory.getPerson("Socrates", "M");
        System.out.println(male.getNameAndSalutation);
        Person female = PersonFactory.getPerson("Alice", "F");
        System.out.println(female.getNameAndSalutation);
    }
```
<details><summary><b> Explanation</b></summary>

This code implements a PersonFactory. This class has a static method named getPerson() that accepts a person’s name and gender as parameters. Depending on the gender String passed in, it either returns a Male or a Female object.If somebody wants to create a male person, they invoke the getPerson() method on the PersonFactory with a gender argument of "M". Similarly, you can create a female person by invoking the getPerson() method on the PersonFactory with a gender argument of "F".We are passing in an identifier of the type of object we need, at the time of creation, while still referring to the generic type, Person.The Male and Female classes are hidden behind the PersonFactory implementation.

</details>
</details>

---

18:Explain with a conceptual example for Chain of Responsibility Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The best example of this pattern can be seen in the exception handling mechanism of most programming languages.If you have a method1() calling method2(), and method2(), in turn, calls method3(). Assume that method3() throws an exception.If method3() has no exception handling, then the exception is passed on to method2()to handle it. If again method2() has no exception handling inside it, then the exception is passed on to method1(). If even method1() cannot handle it, it gets thrown out of method1() as well.
- In Chain Of Responsibility pattern, we have a chain of objects that are ready and wait to process requests. When a new request enters the system, it goes to the first object in the chain to attempt processing. Depending on the processing condition, the request travels up the chain and gets fully processed at some level, or maybe not processed at all.
</blockquote>
</details>

---

19:Write the missing  code for implementing the State Pattern? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java 
 public class StatePattern {
        static class FanWallControl {
            private SpeedLevel current;
            public FanWallControl() {
                current = new Off();
            }
            public void set_state(SpeedLevel state) {
                current = state;
            }
            public void rotate() {
                current.rotate(this);
            }
            public String toString() {
                return String.format("Fan Wall Control [current = %s]", current);
            }
        }

        interface speedLevel {
            void rotate(FanWallControl fanWallControl);
        }

 //Write down the missing code which implements the speedLevel interface for various speed levels.
    }




```
<details><summary><b> Show Answer</b></summary>

``` java 
        static class Off implements SpeedLevel {
            public void rotate(FanWallControl fanWallControl) {
                fanWallControl.set_state(new SpeedLevel1());
            }
        }
        static class SpeedLevel1 implements SpeedLevel {
            public void rotate(FanWallControl fanWallControl) {
                fanWallControl.set_state(new SpeedLevel2());
            }
        }

        static class SpeedLevel2 implements SpeedLevel {
            public void rotate(FanWallControl fanWallControl) {
                fanWallControl.set_state(new SpeedLevel3());
            }
        }
        static class SpeedLevel3 implements SpeedLevel {
            public void rotate(FanWallControl fanWallControl) {
                fanWallControl.set_state(new Off());
            }
        }
```
<details><summary><b> Explanation</b></summary>
<blockquote>

The fan wall control controls the speed with a fan rotates. It has speed levels ranging from 0 to 5. When it is at level 0, the fan does not rotate, and it rotates the fastest at level 5.When you rotate the knob of the fan control, the level changes, and this causes the speed of the fan to change as well. This is a classic case of a change in state (level) causing a change in behavior (speed).A FanwallControl object is composed of a SpeedLevel object. SpeedLevel is an interface that has four different implementations. Initially, the level is at Off, and when you click rotate at that time, the new speed is at SpeedLevel1. The happens successively, and if you rotate at SpeedLevel3, the level returns to Off.In case you need to define an additional speed level, just add in a new class that implements the SpeedLevel interface and implement its rotate method.

</blockquote>
</details>
</details>

---

20:What are the benefits of State Pattern? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

State Pattern keeps the state-specific behavior.It makes any state transitions explicit.When the behavior of object depends on its state and it must be able to change its behavior at runtime according to the new state.It is used when the operations have large, multipart conditional statements that depend on the state of an object.

</blockquote>
</details>


