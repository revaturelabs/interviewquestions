## Technical

1. what is the difference between Object Oriented Programming (OOP) and Aspect-Oriented Programming (AOP)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Object Oriented Programming (OOP) and Aspect-Oriented Programming (AOP) are not mutually exclusive.
- AOP can be good addition to OOP.
- OOP is mainly used to model business logic whereas AOP helps to organize non-functional aspects (called cross cutting concerns) like Auditing, Logging, Transaction Management, Security etc.
- AOP helps to build methods without clogging up the business code with the cross-cutting concerns.
</blockquote> 

</details>

---
2. Why do we use AspectJ in Spring application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring provides simple and powerful ways of writing custom aspects (a modularization of a concern that cuts across multiple classes) by using @AspectJ annotation style. 
- @AspectJ refers to a style of declaring aspects as regular Java classes annotated with annotations. 
- The @AspectJ style was introduced by the AspectJ project as part of the AspectJ 5 release. 
- Spring interprets the same annotations as AspectJ 5, using a library supplied by AspectJ for pointcut parsing and matching. 
- Spring seamlessly integrates Spring AOP and IoC with AspectJ, to enable all uses of AOP within a consistent Spring-based application architecture.
- The @AspectJ support can be enabled with XML- or Java-style configuration. 
- In either case, we also need to ensure that AspectJ’s `aspectjweaver.jar` library is on the class path of application (version 1.8 or later). 
- This library is available in the lib directory of an AspectJ distribution or from the Maven Central repository.
- `pom.xml` sample-
```xml
    <properties>
        <aspectJ.version>1.6.11</aspectJ.version>
    </properties>
    <dependencies>
        <!-- AspectJ -->
        <dependency>
            <groupId>org.aspectj</groupId>
            <artifactId>aspectjrt</artifactId>
            <version>${aspectJ.version}</version>
        </dependency>
        <dependency>
            <groupId>org.aspectj</groupId>
            <artifactId>aspectjweaver</artifactId>
            <version>${aspectJ.version}</version>
        </dependency>
    </dependencies>
```
</blockquote> 

</details>

---
3. How do you capture all exceptions caused in repository, service & controller layer using Spring AOP

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Exception being one of the cross-cutting concern in Spring application which can be handled using Spring AOP.
- Ensure the AspectJ dependencies are added in pom.xml file.
- Define central logging class named `LoggingAspect.java` 

```java
import java.util.Arrays;
import org.aspectj.lang.JoinPoint;
import org.aspectj.lang.ProceedingJoinPoint;
import org.aspectj.lang.annotation.AfterThrowing;
import org.aspectj.lang.annotation.Around;
import org.aspectj.lang.annotation.Aspect;
import org.aspectj.lang.annotation.Pointcut;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.stereotype.Component;

@Aspect
@Component
public class LoggingAspect {
    private final Logger log = LoggerFactory.getLogger(this.getClass());
    @Pointcut("within(@org.springframework.stereotype.Repository *)" +
        " || within(@org.springframework.stereotype.Service *)" +
        " || within(@org.springframework.web.bind.annotation.RestController *)")
    public void springBeanPointcut() {
        // Method is empty as this is just a Pointcut, the implementations are in the advice.
    }
    @Pointcut("within(com.revature.dao..*)" +
        " || within(com.revature.service..*)" +
        " || within(com.revature.controller..*)")
    public void applicationPackagePointcut() {
        // Method is empty as this is just a Pointcut, the implementations are in the advice.
    }
    //Advice that logs methods throwing exceptions.
    @AfterThrowing(pointcut = "applicationPackagePointcut() && springBeanPointcut()", throwing = "e")
    public void logAfterThrowing(JoinPoint joinPoint, Throwable e) {
        log.error("Exception in {}.{}() with cause = {}", joinPoint.getSignature().getDeclaringTypeName(),
            joinPoint.getSignature().getName(), e.getCause() != null ? e.getCause() : "NULL");
    }
}
```
- In above code, we have defined pointcut expression for DAO, Service & Controller layer.
- The `..` notation means "any package or subpackage", whereas `*` at the end of the expression after `..` means "any method in any class".
</blockquote>

</details>

---
4. How do you measure performance (or time taken by method execution) using spring AOP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
To measure the performance or time taken by method execution using Spring AOP, you can utilize the `@Around` advice provided by Spring AOP. Here's how you can do it:

1. Define an aspect class that includes the `@Around` advice:
```java
@Aspect
@Component
public class PerformanceAspect {

    @Around("execution(* com.example.myapp.service.*.*(..))")
    public Object measurePerformance(ProceedingJoinPoint joinPoint) throws Throwable {
        long startTime = System.currentTimeMillis();
        Object result = joinPoint.proceed();
        long endTime = System.currentTimeMillis();
        long executionTime = endTime - startTime;
        System.out.println("Method " + joinPoint.getSignature().getName() + " executed in " + executionTime + "ms");
        return result;
    }
}
```
In this example, the `measurePerformance` method is annotated with `@Around`, which allows you to wrap the target method's execution. The `execution(* com.example.myapp.service.*.*(..))` expression specifies the pointcut, indicating that the advice should be applied to all methods within the `com.example.myapp.service` package.

2. Enable Spring AOP in your Spring Boot application by adding `@EnableAspectJAutoProxy` annotation to your configuration class:
```java
@Configuration
@EnableAspectJAutoProxy
public class AppConfig {
    // Configuration code...
}
```

With this setup, the `measurePerformance` method will be executed around the target method, allowing you to measure the execution time. The execution time will be printed to the console for each method invocation.

Note: Make sure to include the necessary dependencies for Spring AOP in your project.


</blockquote> 

</details>

---

5. Why do we use pointcut expression in Spring application.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Pointcut is an expression language of spring AOP which is basically used to match the target methods to apply the advice.
</blockquote> 

</details>

---
6. Why do we use @EnableAspectJAutoProxy?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Enables support for handling components marked with AspectJ's @Aspect annotation. 
- This annotation is usually defined on class marked with @Configuration.
```java
 @Configuration
 @EnableAspectJAutoProxy
 public class AppConfig {
    @Bean
     public FooService fooService() {
        return new FooService();
    }
    @Bean
    public MyAspect myAspect() {
        return new MyAspect();
    }
 }
```
</blockquote> 

</details>

---

7. How does Spring AOP handle cross-cutting concerns in an application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Spring AOP handles cross-cutting concerns in an application by using aspects. 
- Aspects are modules that encapsulate cross-cutting concerns, such as logging, transaction management, security, and caching. - By defining pointcuts, which specify where in the application's execution flow the cross-cutting concerns should be applied, Spring AOP intercepts method invocations and weaves the aspect's behavior into the target objects. 
- This allows for the separation of concerns and promotes modular and reusable code. 
- With Spring AOP, the cross-cutting concerns are applied declaratively, reducing the need for boilerplate code and making the codebase cleaner and more maintainable.

</blockquote>

</details>

---

8. what is a cross-cutting concern? Give an example of a cross-cutting concern you could use AOP to address

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A cross-cutting concern is a behavior or functionality that cuts across multiple components or modules in an application. It is a concern that cannot be encapsulated within a single module or class and affects multiple parts of the application.

- An example of a cross-cutting concern is logging. Logging is a common functionality that needs to be implemented across various components of an application to capture important information such as method invocations, error messages, or performance metrics. Rather than duplicating the logging code in multiple classes or modules, we can use AOP to address this cross-cutting concern.

- With AOP, we can define an aspect that contains the logging logic, and apply it to specific join points (such as method invocations) throughout the application. This allows us to separate the logging code from the core business logic, promoting better modularity and reusability. The logging aspect can be applied to different classes or modules without modifying their original code, making it an effective approach for addressing cross-cutting concerns.

</blockquote>

</details>

---

9. What is Join point ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A join point in AOP represents a specific point in the execution of a program, such as the execution of a method, the handling of an exception, or the modification of a field. In AOP terminology, a join point is a point in the flow of the program where an aspect can be applied to add additional behavior.

</blockquote>

</details>

---

10. Define Pointcut

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
 A pointcut in AOP defines a set of join points. It specifies the criteria or conditions that determine which join points in the program's execution should be intercepted by an aspect. In other words, a pointcut defines the specific locations or events within the program's execution where the advice (additional behavior) defined by an aspect should be applied.

</blockquote>

</details>

---

11. What is Advice?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In AOP, advice represents the additional behavior that is applied at a join point in the program's execution. It defines the action to be taken at a particular pointcut. There are different types of advice in AOP, including "before" advice (executed before a join point), "after" advice (executed after a join point), "around" advice (wraps a join point and can control its execution), and more. Advice is the actual implementation of the cross-cutting concern and is executed when the corresponding join point is reached during program execution.

</blockquote>

</details>

---

12. What are the different types of advice supported by Spring AOP?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Aspect-Oriented Programming (AOP), there are several types of advice that can be applied at join points in the program's execution. The different types of advice are:

1. Before advice: This advice is executed before the join point and allows you to perform some actions or validations before the actual execution of the join point.

2. After returning advice: This advice is executed after the join point completes successfully (i.e., without throwing an exception). It allows you to perform additional actions based on the return value of the join point.

3. After throwing advice: This advice is executed after the join point throws an exception. It allows you to handle exceptions or perform error handling logic.

4. After (finally) advice: This advice is executed regardless of the outcome of the join point (whether it completes successfully or throws an exception). It is useful for performing cleanup or resource release tasks.

5. Around advice: This advice wraps around the join point and has the most powerful capabilities. It can control the execution of the join point by proceeding with or skipping the execution. It can also modify the input arguments or the return value of the join point.

These different types of advice provide flexibility in implementing cross-cutting concerns and allow you to add behavior at specific points in the program's execution.

</blockquote>

</details>

---

13. What access modifier must Spring bean methods have to be proxied using Spring AOP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To be proxied using Spring AOP, Spring bean methods must have either `public` or `protected` access modifiers.

</blockquote>

</details>

---

14. What is an aspect in Spring AOP and how is it defined?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

An aspect in Spring AOP is a modular unit of cross-cutting concern implementation. It is defined using a combination of pointcuts (to specify join points) and advice (to define the behavior at those join points). Aspects provide a way to modularize and separate cross-cutting concerns from the core business logic in an application.

</blockquote>

</details>

---

15. How can you apply AOP in Spring using XML configuration?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 


In Spring, you can apply AOP using XML configuration by defining the aspects, pointcuts, and advice in the XML file. Here are the steps:

1. Define the aspect using the `<aop:aspect>` element in the XML configuration file.
2. Inside the `<aop:aspect>` element, define the pointcut using the `<aop:pointcut>` element. Specify the expression that matches the join points where the advice will be applied.
3. Define the advice using the `<aop:advisor>` element. Specify the advice type (such as `<aop:before>`, `<aop:after>`, etc.) and the method to be executed.
4. Associate the pointcut with the advice using the `<aop:advisor>` element inside the `<aop:aspect>` element.
5. Import the AOP schema by including the `xmlns:aop` declaration in the XML configuration file.
6. Register the aspect bean in the application context.


</blockquote>

</details>

---

16. How can you apply AOP in Spring using annotations?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring, you can apply AOP using annotations by following these steps:

1. Enable AspectJ support in your Spring configuration by adding the `<aop:aspectj-autoproxy>` element to your XML configuration file, or by using the `@EnableAspectJAutoProxy` annotation on a configuration class.
2. Create an aspect class and annotate it with the `@Aspect` annotation.
3. Define pointcut expressions using the `@Pointcut` annotation to specify where the advice should be applied.
4. Define advice methods within the aspect class and annotate them with specific annotations such as `@Before`, `@After`, `@Around`, etc., to define the type of advice and when it should be executed.
5. Optionally, use the `@Order` annotation to specify the execution order of multiple aspects.
6. Register the aspect bean in the application context.


</blockquote>

</details>

---

17. What are the limitations and drawbacks of Spring AOP?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 


Spring AOP has the following limitations and drawbacks:

1. Limited to method-level interception: Spring AOP is primarily focused on intercepting method invocations. It may not support other types of join points like field access or constructor invocations.

2. Proxy-based approach: Spring AOP uses proxies to apply advice to target objects. This can introduce some performance overhead and may not work with classes that cannot be proxied, such as final classes.

3. Limited pointcut expressions: Spring AOP supports a subset of AspectJ pointcut expressions, which may not provide the same level of flexibility and expressiveness as AspectJ.

4. Runtime weaving: Spring AOP performs AOP at runtime using proxies or CGLIB. This can impact performance compared to compile-time weaving offered by tools like AspectJ.

5. Aspect ordering: Ordering multiple aspects can become complex, especially when dealing with a large number of aspects.

6. Tight coupling with Spring: Spring AOP is tightly integrated with the Spring framework and may not be suitable for projects that are not based on Spring or require AOP to work independently.


</blockquote>

</details>

---

18. What is the difference between Spring AOP and AspectJ?

 ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring AOP is a lightweight AOP framework provided by the Spring framework, while AspectJ is a full-featured AOP framework that can be used independently of Spring. 

The main differences between Spring AOP and AspectJ are:
1. Configuration: Spring AOP uses proxy-based AOP, where it creates dynamic proxies to apply aspects to the target objects. AspectJ, on the other hand, uses compile-time or load-time weaving to directly modify the bytecode of the target objects.
2. Feature Set: AspectJ provides a broader range of AOP features, including advanced pointcut expressions, inter-type declarations, and more powerful weaving capabilities. Spring AOP, being a subset of AspectJ, provides a simpler set of AOP features.
3. Integration: Spring AOP integrates seamlessly with the Spring framework, allowing easy configuration and usage within Spring applications. AspectJ can be used independently of Spring but requires additional configuration and setup.
4. Performance: Spring AOP, with its proxy-based approach, may introduce some runtime overhead due to the proxy creation and method invocations. AspectJ, with its bytecode modification, can achieve better performance but requires more configuration and setup.

</blockquote>

</details>

---

19. How can you control the order of aspect execution in Spring AOP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring AOP, you can control the order of aspect execution by using the `@Order` annotation or implementing the `Ordered` interface.

1. Using `@Order` annotation: You can annotate your aspect classes with `@Order` and specify a numeric value to indicate the desired order of execution. Aspects with lower values are executed before aspects with higher values. If no `@Order` annotation is specified, the default order is `Ordered.LOWEST_PRECEDENCE`.

2. Implementing `Ordered` interface: Alternatively, you can implement the `Ordered` interface in your aspect classes and override the `getOrder()` method to provide a custom order value. The lower the return value, the higher the priority of execution.

By specifying the order of aspects, you can control the sequence in which they are applied to the target objects during runtime.

</blockquote>

</details>

---

20.  Discuss the various pointcut expressions supported by Spring AOP.
 
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring AOP, various pointcut expressions can be used to define the join points where advice should be applied. Some of the commonly used pointcut expressions are:

1. `execution`: This pointcut expression matches the execution of methods. It allows you to specify the fully qualified method signature or use wildcards to match multiple methods.

2. `within`: This pointcut expression matches the execution of methods within certain types. It allows you to specify a package, class, or interface to match.

3. `args`: This pointcut expression matches the execution of methods that have specific argument types. You can specify the types of arguments to match.

4. `this`: This pointcut expression matches the execution of methods on objects that are instances of a specific type or implement a specific interface.

5. `target`: This pointcut expression matches the execution of methods on objects that are instances of a specific target class.

6. `annotation`: This pointcut expression matches the execution of methods that are annotated with a specific annotation.

These pointcut expressions can be combined using logical operators (`&&`, `||`, `!`) to create more complex pointcut expressions. By defining pointcut expressions, you can precisely specify the join points where your advice should be applied.


</blockquote>

</details>

---
21. How can you use custom annotations with Spring AOP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To use custom annotations with Spring AOP, you can follow these steps:

1. Create a custom annotation: Define your custom annotation using the `@interface` syntax. Specify any attributes or elements that you want to include in the annotation.

2. Annotate your target methods: Annotate the methods or classes where you want to apply the aspect with your custom annotation.

3. Define a pointcut: Create a pointcut expression that matches the execution of methods or classes annotated with your custom annotation. You can use the `@annotation` pointcut expression to match methods annotated with your custom annotation.

4. Write advice: Implement the advice logic that should be executed when the pointcut matches. This can be done using the appropriate advice types such as `@Before`, `@After`, `@Around`, etc.

5. Enable Spring AOP: Configure Spring AOP in your application context, either through XML configuration or using annotations such as `@EnableAspectJAutoProxy`.

6. Apply the aspect: Declare your aspect as a Spring bean and ensure it is picked up by the Spring AOP proxying mechanism. This can be done by annotating the aspect class with `@Aspect`.


</blockquote>

</details>

---

22. What is the concept of target object and proxy object in Spring AOP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring AOP, the target object represents the original object that is being advised by one or more aspects. It is the object on which the advised methods are invoked. The target object is typically a Spring bean or a POJO (Plain Old Java Object).

On the other hand, the proxy object is the dynamically generated object that wraps the target object and intercepts method invocations to apply the advice. The proxy object is responsible for applying the cross-cutting concerns defined by the aspects before, after, or around the method invocations on the target object.

The proxy object implements the same interfaces as the target object, allowing it to be used in place of the target object. When a method is invoked on the proxy object, the advice associated with the method is executed before or after delegating the actual method execution to the target object.

The proxy object acts as a middle layer between the caller and the target object, allowing the aspects to intercept and modify the behavior of the target object's methods without modifying the original code of the target object.


</blockquote>

</details>

---

23. How can you enable/disable AOP for specific beans or packages in a Spring application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In a Spring application, you can enable or disable AOP for specific beans or packages by configuring the AOP proxy behavior through pointcut expressions and the use of the `@EnableAspectJAutoProxy` annotation.

To enable AOP for specific beans or packages, you can use the `@EnableAspectJAutoProxy` annotation at the configuration class level. This annotation enables support for handling aspects and creates AOP proxies for the beans that are eligible for advice. By default, Spring uses a default auto-proxy creator that creates JDK dynamic proxies. However, if CGLIB is available on the classpath, it uses CGLIB to create subclass-based proxies.

Once the `@EnableAspectJAutoProxy` annotation is applied, you can define your aspects using the `@Aspect` annotation and specify the pointcuts to determine which methods or classes the aspect should be applied to. Pointcut expressions allow you to define rules for matching specific methods or classes based on their name, package, annotations, or other criteria.

If you want to disable AOP for specific beans or packages, you can exclude them from being processed by the auto-proxy creator. This can be done by using the `exclude` attribute of the `@EnableAspectJAutoProxy` annotation and specifying the specific beans or packages that should be excluded.

By enabling or disabling AOP for specific beans or packages, you have fine-grained control over which parts of your application are advised by aspects and which parts are not, allowing you to selectively apply AOP based on your requirements.

</blockquote>

</details>

---

24. Explain the concept of aspectj-autoproxy and how it works with Spring AOP.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The concept of `aspectj-autoproxy` in Spring AOP refers to the automatic proxying of beans using AspectJ-style aspects. It allows you to apply aspect-oriented programming (AOP) concepts and features, such as advice and pointcuts, to Spring beans.

When `aspectj-autoproxy` is enabled, Spring AOP creates proxies for beans that have been annotated with `@Aspect` or have been declared as advice beans. These proxies intercept method invocations on the target beans and apply the specified advice based on the defined pointcut expressions.

Under the hood, Spring AOP uses either JDK dynamic proxies or CGLIB proxies to create the proxies. The choice between the proxying mechanisms depends on whether the target bean implements interfaces or not. If the target bean implements at least one interface, JDK dynamic proxies are used. Otherwise, CGLIB proxies are used, which subclass the target bean.

The `aspectj-autoproxy` mechanism integrates the powerful features of AspectJ with the Spring IoC container, allowing you to leverage AspectJ-style syntax and expressions for defining aspects, pointcuts, and advice. This provides a more advanced and flexible AOP solution within the Spring framework.

By enabling `aspectj-autoproxy`, you can easily apply aspects to your Spring beans, intercept method invocations, and apply cross-cutting concerns in a declarative and configurable manner, enhancing the modularity and maintainability of your application.

</blockquote>

</details>

---
