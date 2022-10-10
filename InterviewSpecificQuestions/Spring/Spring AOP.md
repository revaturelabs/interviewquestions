## Technical

1. Is there difference between Object Oriented Programming (OOP) and Aspect-Oriented Programming (AOP)?

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
2. Why we need to use AspectJ in Spring application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring provides simple and powerful ways of writing custom aspects(a modularization of a concern that cuts across multiple classes) by using @AspectJ annotation style. 
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
3. You have to capture all exceptions caused in repository, service & controller layer using Spring AOP, how you can do it?

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
- In above code we have defined pointcut expression for DAO, Service & Controller layer.
- The `..` notation means "any package or subpackage", whereas `*` at the end of the expression after `..` means "any method in any class".
</blockquote>

</details>

---
4. You have to measure performance (or time taken by method execution) how can you achieve it with AOP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Apart from standard cross cutting concerns like Auditing, Logging, Transaction Management, Security etc. there are occasions were
we want to deal with custom cross cutting concerns.
- Measuring performance of the method execution can be one of such example of cross cutting concerns.
- Ensure the AspectJ dependencies are added in pom.xml file.
- Define central logging class named `ExecutionTimeAspect.java` 
```java
package com.revature.aop;
import org.aspectj.lang.ProceedingJoinPoint;
import org.aspectj.lang.annotation.Around;
import org.aspectj.lang.annotation.Aspect;

@Aspect
public class ExecutionTimeAspect {
    @Around("execution(public String com.revature.service.RefundService.process(Long))")
    public Object measureExecutionTime(ProceedingJoinPoint joinPoint) throws Throwable {
        long start = System.currentTimeMillis();
        Object proceed = joinPoint.proceed();
        long executionTime = System.currentTimeMillis() - start;
        System.out.println(joinPoint.getSignature() + " executed in " + executionTime + "ms");
        return proceed;
    }
}
```
- In above code we have defined pointcut expression to measure performance of `public String com.revature.service.RefundService.process(Long)` method.
</blockquote> 

</details>

---

5. Why we use pointcut expression in Spring application.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Pointcut is an expression language of spring AOP which is basically used to match the target methods to apply the advice.
</blockquote> 

</details>

---
6. Why we use @EnableAspectJAutoProxy?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Enables support for handling components marked with AspectJ's @Aspect annotation. 
- This annotaion is usually defind on class marked with @Configuration.
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
