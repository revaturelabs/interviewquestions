## Technical

1. What are Spring Beans?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Core business component defined insider Spring applications is termed as `Bean`. 
- In simple terms `Bean` is an object that is instantiated, assembled, and managed by a Spring IoC container.
- Each technology has branded their core business components by certain nomenclature. For example, Business component in `JavaEE` applications are termed as `Servlet`, in `Web Services` they are named as `Resource` in `Struts` framework they are called `ActionForm` etc.
</blockquote> 

</details>

---
2. How you decide whether to create `Singleton` bean or `Prototype` bean in application??

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Though Spring IOC container has excellent support to manage the lifecycle of different types of beans,
Spring does not manage the complete lifecycle of a prototype bean.
- The IOC container instantiates, configures, decorates, and otherwise assembles a prototype object, hands it to the client and then has no further knowledge of that `Prototype` instance.
- For most of the simple to average applications `Singleton` bean are sufficient and serve the purpose at each layer e.g. DAO, Service, Controller etc.
- Developer need to take smart decisions & identify which beans must be singleton, else multiple client requests using singleton bean can modify the state of common objects wrongly.
- Some dependent objects need a bean that has private state so that they can conduct their processing separately from other objects that depend on the bean. In this case, singletons are clearly not suitable, and we consider prototypes.
- If you have a bean that has a lot of writable state, you may find that the cost of synchronization is greater than the cost of creating a new instance to handle each request from a dependent object that time you can use prototype bean.

</blockquote> 

</details>

---

3. When do you used `Session` and `Request` bean in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Both of the beans are used mainly in Web Application.
- If the bean scope is `Request`, then on every request (from same user or different user) a new bean will be created.
- If the bean scope is `Session` then on every request same bean would be returned as long as requests are within the same user session also made from a client which is capable of maintaining the session (`curl` command can't maintain the user session unless pass cookie/session identifier header).
- `Session` beans are not destroyed until session timeout up or session destroyed.

</details>
    
</blockquote> 

---

4. How a IOC container is configured in a spring console based application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Spring IOC container is primarily responsible for holding all business components termed as `Bean`.
- Few of these beans are added by spring framework and rest all are defined by developers.
- These beans can be configured using XML configuration file (usually named as `applicationContext.xml`) or using Java Configuration class (usually named as `AppConfig.java`).
- **`applicationContext.xml` sample** -
```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://www.springframework.org/schema/beans
     http://www.springframework.org/schema/beans/spring-beans-4.3.xsd">

    <bean id="intelProcessor" class="com.revature.model.Intel">
        <property name="modelName" value ="Intel i7"/>
        <property name="cacheMemory" value="64MB" />
        <property name="price" value="6700.00"/>
        <property name="numberOfCores" value="7 Cores" />
    </bean>
    <bean id="myLaptop" class="com.revature.model.Laptop" autowire="no">
        <property name="modelName" value="Lenovo Think PagEdge" />
        <property name="price" value="78900.00" />
        <property name="processor" ref="intelProcessor" />
    </bean>
    <bean id="yourLaptop" class="com.revature.model.Laptop" autowire="no">
        <constructor-arg value="Alienware"></constructor-arg>
        <constructor-arg value="98900.00"></constructor-arg>
        <constructor-arg ref="intelProcessor" ></constructor-arg>
    </bean>
</beans>
```
- **`AppConfig.java` sample** -

```java
package com.revature.config;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.context.annotation.Description;
import org.springframework.context.annotation.Scope;
//Assume below model classes exist in the application
import com.revature.model.Intel;
import com.revature.model.Laptop;

@Configuration
public class AppConfig {
    @Bean(name = "i7")
    @Description("This bean is used to injection dependency inside Laptop class")
    public Intel getIntelProcessor() {
        return new Intel("Intel i7", "64MB", 6700.0, "7 Cores");
    }

    @Bean
    @Description("My Lenovo Laptop Bean")
    public Laptop myLaptop() {
        // This is JavaConfig Alternative for Setter Based Injection
        Laptop myLappy = new Laptop();
        myLappy.setModelName("Lenovo Think PagEdge");
        
        // In applciationContext.xml this value will be in double quotes unlike
        // java developers who want it without double quotes
        myLappy.setPrice(78900.00);
        myLappy.setProcessor(getIntelProcessor());
        return myLappy;
    }

    @Bean
    @Description("Your Mac Book Pro Laptop Bean")
    @Scope("singleton")
    public Laptop yourLaptop() {
        // This is JavConfig Alternative for Constructor Based Injection
        Laptop yourLappy = new Laptop("Mac Book Pro",149000.0, getIntelProcessor());
        return yourLappy;
    }

    /* --- Comparison ---
        @Configuration  //== applicationContext.xml
        class AppConfig
        @Bean   //== <bean>
        public Amd amd(){  // id=amd class="com.revature.model.Amd"
        Amd a= new Amd();
        a.setPrice();     // <property name="price" value="23232"/>
        ....
        ....
        return a;
        }
    */
}
```
- The Spring IOC container can be programmatically accessed using two interfaces namely: `BeanFactory` & `ApplicationContext`.
- It's always advisable to use ApplicationContext which is child interface of BeanFactory.
- There are multiple implementations available of ApplicationContext depending upon your bean configuration.
- For `applicationContext.xml` based bean configuration we use `ClassPathXmlApplicationContext` class.
```java
package com.revature.client;
import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;
import com.revature.model.Laptop;
public class App {
    public static void main(String[] args) {
        Laptop lenovoLaptop, secondLaptop;
        ApplicationContext appContext = new ClassPathXmlApplicationContext("applicationContext.xml");
        lenovoLaptop = (Laptop) appContext.getBean("myLaptop");
        System.out.println(lenovoLaptop);
        secondLaptop = (Laptop) appContext.getBean("yourLaptop");
        System.out.println(secondLaptop);
        ((ClassPathXmlApplicationContext) appContext).close();
    }
}
```
- For `AppConfig.java` based bean configuration we use `AnnotationConfigApplicationContext` class.

```java
package com.revature.client;
import org.springframework.context.annotation.AnnotationConfigApplicationContext;
import com.revature.config.AppConfig;
//Assume below model classes exist in the application
import com.revature.model.Laptop;
import com.revature.model.Processor;
public class App {
    public static void main(String[] args) {
        AnnotationConfigApplicationContext  appContext = new AnnotationConfigApplicationContext(AppConfig.class);
        Laptop lenovoLaptop, secondLaptop;
        Processor intelProcessor;

        System.out.println("/////////////////////////////////");
        intelProcessor= (Processor) appContext.getBean("i7");
        System.out.println(intelProcessor);
        
        System.out.println("/////////////////////////////////");
        lenovoLaptop = (Laptop) appContext.getBean("myLaptop");
        System.out.println(lenovoLaptop);
        
        System.out.println("/////////////////////////////////");
        secondLaptop = (Laptop) appContext.getBean("yourLaptop");
        System.out.println(secondLaptop);
            
        appContext.close();
        
    }
}
```

</blockquote> 
    
</details>

---

5. How to decide upon choosing BeanFactory or ApplicationContext in Spring application?.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Spring IOC container can be programmatically accessed using two interfaces namely: `BeanFactory` & `ApplicationContext`
- The BeanFactory is the root interface and the ApplicationContext extends the features of BeanFactory.
- BeanFactory loads beans on-demand (`Lazy Loading`), while ApplicationContext loads all beans at startup(`Eager Loading`). 
- BeanFactory is lightweight as compared to ApplicationContext.
- BeanFactory only supports two scopes — Singleton and Prototype, but ApplicationContext supports all types of bean scopes. 
- ApplicationContext enhances BeanFactory to provide several features that are suitable for enterprise applications.
- ApplicationContext provides messaging (`i18n` or internationalization) functionality, event publication functionality, annotation-based dependency injection, and easy integration with Spring AOP features.
- It's always advisable to use ApplicationContext.
- We should use BeanFactory only when memory consumption is critical.
    
</blockquote> 

</details>

---

6. What are the ways through which the Spring beans are configured?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
    
<blockquote> 

- There are broadly two ways in which Spring beans are configured in application-
    - Using XML configuration – We usually define xml file with standard name as `applicationContext.xml` inside `src/main/resources` folder of your maven project.
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <beans xmlns="http://www.springframework.org/schema/beans"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans-4.3.xsd">
        <bean id="intelProcessor" class="com.revature.model.Intel">
            <property name="modelName" value ="Intel i7"/>
            <property name="cacheMemory" value="64MB" />
            <property name="price" value="6700.00"/>
            <property name="numberOfCores" value="7 Cores" />
        </bean>
    </beans>
    ```
    - Using Annotation configuration - `@Bean`, `@Component`, `@Service`, `@Repository`, `@Controller`, `@RestController`
    ```java
    @Component("employeeDtoForReport")  // Bean id - employeeDtoForReport
    public class EmployeeDto{
    //.....
    }

    @RestController // Bean id - employeeRestController 
    public class EmployeeRestController {
    //.....
    }

    @Repository   //Bean id - DepartmentRepository 
    public interface DepartmentRepository extends JpaRepository<Department, Long> {
    //.....
    }

    @Service //Bean id - employeeServiceImpl
    public class EmployeeServiceImpl implements EmployeeService {
    //.....
    }

    @Controller
    public class PayrollController {
    //.....
    }
    
    @Configuration
    public class AppConfig {
        @Bean 
        public void beanName(){   
            //.....
        }
    }
    ```
</blockquote> 

</details>

---
7. How Spring supports connection pooling? Elaborate what is connection pooling?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
    
<blockquote> 

- Database connections are expensive operation.
- A connection pool is like a collection of open connections. 
- If a connection is established or created it should be added to the connection pool.
- When a connection is released, it's actually returned back to the pool, so other clients can reuse it.
- While the connection is open it can be used again and again.
- Spring support connection pooling by supporting configuration of DataSource inside application.
- Spring provides `DriverManagerDataSource` for testing application during development phase.
- There are third party DB connection pooling providers like `Apache DBCP`, `Hikari CP` etc. which can also be configured in application.
- `DriverManagerDataSource` sample -

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <beans xmlns="http://www.springframework.org/schema/beans"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:context="http://www.springframework.org/schema/context"
        xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans-4.3.xsd
            http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context-4.3.xsd">

        <bean id="accountDao" class="com.revature.dao.AccountDaoImpl"
            autowire="no">
            <!-- Setter based IOC/DI -->
            <property name="jdbcTemplate" ref="jdbcTemplate" />
        </bean>
        <bean id="jdbcTemplate" class="org.springframework.jdbc.core.JdbcTemplate">
            <!-- Constructor based IOC/DI -->
            <constructor-arg ref="dataSource" />
        </bean>
        <bean id="dataSource"
            class="org.springframework.jdbc.datasource.DriverManagerDataSource">
            <property name="driverClassName" value="com.mysql.cj.jdbc.Driver" />
            <property name="url" value="jdbc:mysql://localhost/gd_hibernate"></property>
            <property name="username" value="root"></property>
            <property name="password" value="admin"></property>
        </bean>
    </beans>
    ```
- `Apache DBCP` maven dependency(ies)-

    ```xml
    <!-- Apache DBCP jar -->
        <dependency>
            <groupId>commons-dbcp</groupId>
            <artifactId>commons-dbcp</artifactId>
            <version>1.4</version>
        </dependency>
    ```
- `Apache DBCP` sample -

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <beans xmlns="http://www.springframework.org/schema/beans"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:p="http://www.springframework.org/schema/p"
        xmlns:context="http://www.springframework.org/schema/context"
        xsi:schemaLocation="http://www.springframework.org/schema/beans  
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd  
    http://www.springframework.org/schema/context  
    http://www.springframework.org/schema/context/spring-context-3.0.xsd">

        <context:component-scan base-package="com.revature" />
        <bean
            class="org.springframework.web.servlet.view.InternalResourceViewResolver">
            <property name="viewClass" value="org.springframework.web.servlet.view.JstlView"></property>
            <property name="prefix" value="/WEB-INF/jsp/"></property>
            <property name="suffix" value=".jsp"></property>
        </bean>
        <bean id="dao" class="com.revature.dao.EmpDao">
            <property name="template" ref="jt"></property>
        </bean>
        <bean id="jt" class="org.springframework.jdbc.core.JdbcTemplate">
            <property name="dataSource" ref="ds"></property>
        </bean>
        <bean id="ds" class="org.apache.commons.dbcp.BasicDataSource">
            <property name="driverClassName" value="com.mysql.cj.jdbc.Driver" />
            <property name="url" value="jdbc:mysql://localhost/gd_hibernate"></property>
            <property name="username" value="root"></property>
            <property name="password" value="admin"></property>
            <property name="initialSize" value="2" />
            <property name="maxActive" value="10" />
        </bean>
    </beans>  
    ```
</blockquote> 

</details>

---

8. What is usual cause of `org.springframework.beans.factory.NoUniqueBeanDefinitionException`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Exception thrown when a BeanFactory is asked for a bean instance for which multiple matching candidates have been found when only one matching bean was expected.
- To understand problem consider below situation where we have three input interfaced namely `Keyboard`, `Mouse` and `Joystick` implementing `Usb` interface.
- The class `Counterstrike` has one dependency called `gameControl` of type `Usb`.
- The Spring container while injecting dependency gameControl has confusion, as there are three qualifying beans for desired match, hence we will get `NoUniqueBeanDefinitionException` exception.

    ```java
    @Component
    public class Keyboard implements Usb{
        //....
    }
    @Component
    public class Mouse implements Usb{
        //....
    }
    @Component
    public class Joystick implements Usb{
        //....
    }

    @Component
    public class Counterstrike {
        @Autowired
        private Usb gameControl;
        //....
    }
    ```
- The solution for the exception will be using `@Qualifier` annotation with exact matching bean name-
    ```java
    @Component
    public class Counterstrike {
        @Autowired
        @Qualifier("joystick")
        private Usb gameControl;
        //....
    }
    ```
</blockquote> 

</details>

---
9. Have you configured Init & Destroy spring bean lifecycle hooks? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring provides several ways through which you can tap into the bean lifecycle. 
- For example, once a bean is instantiated, you might need to perform some initialization to get the bean into a usable state. 
- Similarly, you might need to clean up resources before a bean is removed from the container.
- These actions can be achieved by configuring Init and Destroy lifecycle hooks into Spring application.
- `@PostConstruct` Annotation:
    - Whenever we annotate a method in Spring Bean with `@PostConstruct` annotation, it gets executed after the spring bean is initialized. 
    - We can have only one method annotated with `@PostConstruct` annotation. 
- `@PreDestroy` Annotation: 
    - When we annotate a Spring Bean method with PreDestroy annotation, it gets called when the bean instance is getting removed from the context.
    - Note: if your spring bean scope is `Prototype` then it’s not completely managed by the spring container and the PreDestroy method won’t get called. 
- Both of the above annotation are part of Common Annotations API and it’s part of JDK module `javax.annotation-api`. 
- Lets look at simple example below:
- `MailService.java` file-
```java
package com.revature;
import java.util.HashMap;
import java.util.Map;
import javax.annotation.PostConstruct;
import javax.annotation.PreDestroy;
import org.springframework.beans.factory.config.ConfigurableBeanFactory;
import org.springframework.context.annotation.Scope;
import org.springframework.stereotype.Component;

@Component
@Scope(scopeName = ConfigurableBeanFactory.SCOPE_SINGLETON)
public class MailService {
   private Map<String, String> map=null;
   public MailService() {
      map=new HashMap<>();
   }
   public void send(String mailTo){
      //Send mail code
      System.out.println("Inside send email method - "+mailTo);
   }
   @PostConstruct
   public void init() {
      map.put("host", "mail.gd.com");
      map.put("port", "25");
      map.put("from", "example@gd.com");
      System.out.println("Inside init method - "+map);
   }
   @PreDestroy
   public void destroy() {
      map.clear();
      System.out.println("Inside destroy method - "+map);
   }
}
```
- `MainApp.java` file-

```java
package com.revature.app;
import org.springframework.context.annotation.AnnotationConfigApplicationContext;
import com.revature.MailService;

public class MainApp {
   public static void main(String[] args) {
      AnnotationConfigApplicationContext context = 
            new AnnotationConfigApplicationContext(AppConfig.class);
      // Send mail 1
      MailService mailService1 = (MailService) context.getBean("mailService");
      mailService1.send("coupancodes@gd.com");
      // Send mail 2
      MailService mailService2 = context.getBean(MailService.class);
      mailService2.send("newletters@gd.com");
      context.close();
   }
}

```
</blockquote> 

</details>

---
10. How you decide as developer to choose among `.properties` or `.yaml` configuration file in Spring Boot application? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In Spring Boot we use an external configuration to define our properties.
- This allows us to use the same application code in different environments.
- We can use properties files, YAML files, environment variables and command-line arguments.
- `application.properties` file, which uses a key-value format:
    - Here each line is a single configuration, so we need to express hierarchical data by using the same prefixes for our keys. 
```
management.endpoint.health.group.custom.include=*
management.endpoint.health.group.custom.show-components=always
management.endpoint.health.group.custom.show-details=always
```
- `application.yml` file, which uses a key-value format:
    - YAML is a convenient format for specifying hierarchical configuration data. 
    - The below code is more readable than .properties file alternative, due to lack of repeated prefixes.
```yml
management:
  endpoints:
    web:
      base-path: /
  endpoint:
    health:
      show-details: ALWAYS
      probes:
        enabled: true
      group:
        readiness:
          include: db, diskSpace
```
</blockquote>

</details>

---
11. Can we achieve DI with Core Java without using Spring framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Yes, Dependency Injection is a concept rather and then a framework. 
- When the application under question is small, we can always meet the needs by injecting dependencies manually, without using any framework like Spring.
- We can use Factory Design Pattern and create dependencies which will then be passed to required classes.
- Though such code cannot replace the DI framework like Spring which provide much more extensive set of features.
</blockquote> 

</details>

---

12. Brief us on Spring Framework.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Spring Framework is a Java platform that provides comprehensive infrastructure support for developing Java applications. Spring handles the infrastructure so application developer can focus on your application.

</blockquote>

</details>

---

13. What is Dependency Injection? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Dependency Injection (DI) is a design pattern that removes the dependency from the programming code so that it can be easy to manage and test the application. Dependency Injection makes our programming code loosely coupled.

</blockquote>

</details>

---

14. How many types of spring beans are there? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are 5 type of bean scope is in Spring :-

1)**Singleton:-** It return a single bean instance per spring IOC Container.
2)**Prototype:-** It return a new bean instance each time when requested.
3)**Request:-** It return a single instance for every HTTP request call.
4)**Session:-** It returns a single instance for every HTTP request call.
5)**Global session:-** Global session scope is equal as session scope on portlet-based web applications.

</blockquote>

</details>

---
