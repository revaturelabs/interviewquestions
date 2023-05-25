## Technical

1. What is Spring Beans?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Core business component defined insider Spring applications is termed as `Bean`. 
- In simple terms `Bean` is an object that is instantiated, assembled, and managed by a Spring IoC container.
- Each technology has branded their core business components by certain nomenclature. For example, Business component in `JavaEE` applications are termed as `Servlet`, in `Web Services` they are named as `Resource` in `Struts` framework they are called `ActionForm` etc.
</blockquote> 

</details>

---
2. How do you determine whether to create a Singleton bean or a Prototype bean in an application?

![Medium ](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

3. When do you use `Session` and `Request` bean in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Both beans are used mainly in Web Application.
- If the bean scope is `Request`, then on every request (from same user or different user) a new bean will be created.
- If the bean scope is `Session` then on every request same bean would be returned if requests are within the same user session also made from a client which is capable of maintaining the session (`curl` command can't maintain the user session unless pass cookie/session identifier header).
- `Session` beans are not destroyed until session timeout up or session destroyed.

</details>
    
</blockquote> 

---

4. How can an IOC container be configured in a console-based Spring application?

![Medium ](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In a console-based Spring application, you can configure an IOC (Inversion of Control) container, such as the `ApplicationContext`, to manage and instantiate your beans. Here's how you can configure it:

1. Include Spring Dependencies: Add the necessary Spring dependencies to your project's build configuration. This typically includes the `spring-context` dependency, which provides the core Spring IOC container functionality.

2. Create a Configuration Class: Create a Java class to serve as the configuration class for your Spring application. Annotate this class with `@Configuration` to indicate that it contains bean definitions.

3. Define Beans: Inside the configuration class, define your beans using various annotations such as `@Bean` or `@Component`. These annotations specify the creation and configuration of your beans.

4. Create ApplicationContext: In your console application's entry point, create an `ApplicationContext` by instantiating the appropriate implementation class, such as `AnnotationConfigApplicationContext`. Pass your configuration class as a parameter to the constructor.

5. Retrieve Beans: Use the `getBean()` method of the `ApplicationContext` to retrieve the instances of your beans. You can retrieve the beans by their type or by their names.

Here's an example of a console-based Spring application configuration:

```java
@Configuration
public class AppConfig {
    
    @Bean
    public MyBean myBean() {
        return new MyBean();
    }
    
    // Define other beans...
    
    public static void main(String[] args) {
        ApplicationContext context = new AnnotationConfigApplicationContext(AppConfig.class);
        
        MyBean myBean = context.getBean(MyBean.class);
        // Use the bean...
    }
}
```

In this example, `MyBean` is a custom bean defined using the `@Bean` annotation within the configuration class. The `ApplicationContext` is created using `AnnotationConfigApplicationContext` and the configuration class `AppConfig`. Finally, the `MyBean` instance is retrieved from the context using `getBean()`.

By following these steps, you can configure and use an IOC container in a console-based Spring application to manage your beans and their dependencies.

</blockquote> 
    
</details>

---

5. How do you make a decision between choosing BeanFactory or ApplicationContext in a Spring application?

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

6. What are ways to configure spring bean ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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
7. what is connection pooling and also elaborate on How Spring supports connection pooling ?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
    
<blockquote> 

- Database connections are expensive operation.
- A connection pool is like a collection of open connections. 
- If a connection is established or created it should be added to the connection pool.
- When a connection is released, it's returned back to the pool, so other clients can reuse it.
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

8. What is the usual cause of `org.springframework.beans.factory.NoUniqueBeanDefinitionException` in spring?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Exception thrown when a BeanFactory is asked for a bean instance for which multiple matching candidates have been found when only one matching bean was expected.
- To understand problem, consider below situation where we have three input interfaced namely `Keyboard`, `Mouse` and `Joystick` implementing `Usb` interface.
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

9. How to configure initialization and destruction hooks for Spring beans?

![Complex ](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
In Spring, you can configure initialization and destruction hooks for beans using the `@PostConstruct` and `@PreDestroy` annotations or implementing the `InitializingBean` and `DisposableBean` interfaces. Here's how you can do it:

1. Using the `@PostConstruct` and `@PreDestroy` annotations:
   - Import the necessary annotations: `import javax.annotation.PostConstruct;` and `import javax.annotation.PreDestroy;`.
   - Add the `@PostConstruct` annotation on a method that should be called after the bean initialization.
   - Add the `@PreDestroy` annotation on a method that should be called before the bean destruction.

   Example:
   ```java
   import javax.annotation.PostConstruct;
   import javax.annotation.PreDestroy;

   public class MyBean {
       @PostConstruct
       public void init() {
           // Initialization logic here
       }

       @PreDestroy
       public void destroy() {
           // Destruction logic here
       }
   }
   ```

2. Implementing the `InitializingBean` and `DisposableBean` interfaces:
   - Implement the `InitializingBean` interface and override the `afterPropertiesSet()` method to define initialization logic.
   - Implement the `DisposableBean` interface and override the `destroy()` method to define destruction logic.

   Example:
   ```java
   import org.springframework.beans.factory.DisposableBean;
   import org.springframework.beans.factory.InitializingBean;

   public class MyBean implements InitializingBean, DisposableBean {
       @Override
       public void afterPropertiesSet() throws Exception {
           // Initialization logic here
       }

       @Override
       public void destroy() throws Exception {
           // Destruction logic here
       }
   }
   ```

3. Using custom initialization and destruction methods:
   - Define custom initialization and destruction methods in your bean class.
   - Configure these methods in the Spring bean configuration XML file or using the `@Bean` annotation in a configuration class.

   Example:
   ```java
   public class MyBean {
       public void customInit() {
           // Custom initialization logic here
       }

       public void customDestroy() {
           // Custom destruction logic here
       }
   }
   ```

   XML configuration:
   
   ```xml
   <bean id="myBean" class="com.example.MyBean" init-method="customInit" destroy-method="customDestroy" />
   ```

By configuring these initialization and destruction hooks, you can perform specific tasks when a bean is initialized or destroyed within the Spring container. This allows you to handle any necessary setup or cleanup operations for your beans.

</blockquote> 

</details>

---
10. What factors should a developer consider when choosing between using a `.properties` file or a `.yaml` file for configuration in a Spring Boot application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In Spring Boot, we use an external configuration to define our properties.
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
11. Is it possible to achieve dependency injection with Core Java without using Spring framework? if so how ?

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

12. Explain Spring Framework.

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

14. Explain the different Bean scopes

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are 5 types of bean scope in Spring :-

1. **Singleton:-** It return a single bean instance per spring IOC Container.
2. **Prototype:-** It return a new bean instance each time when requested.
3. **Request:-** It return a single instance for every HTTP request call.
4. **Session:-** It returns a single instance for every HTTP request call.
5. **Global session:-** Global session scope is equal as session scope on portlet-based web applications.

</blockquote>

</details>

---

15. What are the different types of Dependency Injection in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are three types of Dependency Injection in Spring:
- **Constructor Injection:** Dependencies are injected through the class constructor.
- **Setter Injection:** Dependencies are injected using setter methods.
- **Field Injection:** Dependencies are injected directly into class fields.

</blockquote>

</details>

---

16. What is IOC and what does the IOC Container do?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- IOC in Spring is a design pattern and a way of implementing the Inversion of Control principle. 
- It allows the Spring container (IOC container) to take control of managing object creation and their dependencies. Instead of objects creating and managing their dependencies directly, the dependencies are provided or injected into the objects by the container.


</blockquote>

</details>

---

17.  List some stereotype annotations.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- **@Component:** This annotation is a generic stereotype for any Spring-managed component. It serves as a base annotation for more specific stereotype annotations and can be used to mark any class as a Spring component.

- **@Repository:** This annotation is used to indicate that a class is a repository or data access object (DAO). It is typically used for classes that interact with a database or other persistent storage.

- **@Service:** This annotation is used to mark a class as a service component. It represents the business logic layer of the application and is often used to encapsulate and handle complex business operations.

- **@Controller:** This annotation is used to mark a class as a controller component in a Spring MVC application. It handles incoming HTTP requests, performs request processing, and returns responses to the client.



</blockquote>

</details>

---

18. What is @configuration and @bean in spring?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- **@Configuration**
The @Configuration annotation is used to mark a class as a configuration class in Spring. It indicates that the class contains bean definitions and other application-wide configuration settings.
- **@Bean:**
The @Bean annotation is used to declare a method as a producer of a bean within a Spring configuration class. It indicates that the method returns a bean instance that should be managed by the Spring container.

</blockquote>

</details>

---

19.What is the purpose of using @Value?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- @Value annotation is used to assign default values to variables and method argument
- We can read spring environment variables as well as system variables using @Value annotation. 

</blockquote>

</details>

---

20. What is bean wiring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- bean wiring is the process of connecting or establishing dependencies between beans. It involves configuring the relationships between different beans so that they can collaborate and work together.

</blockquote>

</details>

---

21. What is Auto wiring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Autowiring in Spring is a feature that automatically resolves dependencies between beans. 
- It eliminates the need for manual configuration and wiring of dependencies by allowing Spring to automatically inject the required dependencies into a bean.

</blockquote>

</details>

---

22. What is the Spring Bean lifecycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The Spring Bean lifecycle refers to the series of steps that a bean goes through from its creation to its destruction within a Spring container. The lifecycle consists of several phases:

1. Instantiation: The bean instance is created either through XML configuration or using annotations.
2. Population of Dependencies: Dependencies are injected into the bean, either through constructor injection or setter injection.
3. Bean Post-Processing: Spring applies any registered BeanPostProcessor implementations to modify the bean instance before it is fully initialized.
4. Initialization: If the bean implements the InitializingBean interface or defines an initialization method, it is invoked to perform any necessary initialization tasks.
5. Ready for Use: The bean is now fully initialized and available for use.
6. Destruction: If the bean implements the DisposableBean interface or defines a destroy method, it is invoked when the bean is being removed from the container or the container is being shut down.



</blockquote>

</details>

---

23. What is the difference between constructor injection and setter injection in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Constructor injection enforces the dependencies to be provided at the time of object creation, while setter injection allows dependencies to be provided or changed after object creation.
- Constructor injection promotes immutability and ensures that a fully initialized object is created, while setter injection allows for more flexibility in managing dependencies.
- Constructor injection provides a clear contract for required dependencies, making it easier to understand the dependencies of a class, while setter injection allows for optional dependencies and can lead to a less strict contract.annotation. 

</blockquote>

</details>

---

24.  What is the purpose of the @Autowired annotation in Spring?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The purpose of the `@Autowired` annotation in Spring is to automatically wire or inject dependencies into a bean. 
- It allows Spring to automatically detect and wire the appropriate bean dependency based on the declared type.
-  By using `@Autowired`, you don't need to manually instantiate or look up dependencies, as Spring takes care of resolving and injecting them for you. 
- This annotation helps to achieve loose coupling and promotes dependency injection, making the code more modular and maintainable.

</blockquote>

</details>

---

25.  What are the key features of the Spring Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The key features of the Spring Framework are:

1. Inversion of Control (IoC): The Spring Framework implements the principle of IoC, where the control of object creation and dependency injection is shifted from the application code to the framework. This promotes loose coupling and easier testing of components.

2. Dependency Injection (DI): Spring provides a powerful DI mechanism, allowing dependencies to be injected into objects without requiring explicit instantiation or configuration. DI helps in achieving loose coupling, modular design, and easier unit testing.

3. Aspect-Oriented Programming (AOP): Spring supports AOP, which allows separating cross-cutting concerns such as logging, caching, and security from the core application logic. AOP enables modularization and reusability of code.

4. Spring MVC: The Spring MVC framework provides robust support for building web applications based on the Model-View-Controller (MVC) architectural pattern. It offers features like request mapping, data binding, validation, and view resolution for building flexible and scalable web applications.

5. Transaction Management: Spring offers a comprehensive transaction management framework that supports both programmatic and declarative transaction management. It integrates seamlessly with various transaction APIs, including Java Transaction API (JTA) and JDBC, and supports distributed transactions.

6. Data Access Abstraction: Spring provides a consistent abstraction layer for working with different data access technologies, including JDBC, JPA, Hibernate, and MyBatis. It simplifies database operations and supports seamless switching between different data access technologies.

7. Spring Security: Spring offers a powerful security framework that provides authentication, authorization, and other security features for web applications. It integrates well with other Spring modules and supports various authentication mechanisms, including form-based, OAuth, and JWT.

8. Testing Support: Spring provides excellent support for testing applications, including unit testing, integration testing, and mocking. It offers integration with popular testing frameworks like JUnit and Mockito, making it easier to write and execute tests.

9. Internationalization (i18n) and Localization (l10n): Spring supports internationalization and localization of applications by providing features like message bundles, locale resolution, and support for different languages and regions.

10. Lightweight and Modular: The Spring Framework is designed to be lightweight and modular, allowing developers to pick and choose the required modules based on their application needs. This helps in keeping the application footprint small and improves performance.

These are some of the key features that make the Spring Framework popular and widely used in enterprise Java development.

</blockquote>

</details>

---

26.  What is the concept of component scanning and how would you set it up?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The concept of component scanning in Spring is a way to automatically detect and register Spring beans based on predefined conventions. It eliminates the need for explicit bean configuration and simplifies the development process.

To set up component scanning in Spring, you need to follow these steps:

1. Add the `@ComponentScan` annotation to your configuration class or XML configuration file.
2. Specify the base package(s) where Spring should scan for components. This can be done by providing the package name(s) as an argument to `@ComponentScan` annotation or configuring it in the XML file.
3. Optionally, you can further customize the component scanning behavior by specifying filters to include or exclude certain components based on annotations, interface implementations, or other criteria.

By enabling component scanning, Spring will automatically scan the specified packages and register the detected components as beans in the application context. This allows you to use them throughout your application without explicitly defining them in the configuration files.

</blockquote>

</details>

---

27.  What are Spring Projects and Spring Modules?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

 Spring Projects and Spring Modules refer to different components and extensions that provide additional functionality and features on top of the core Spring framework.

1. Spring Projects: Spring Projects are individual sub-projects within the Spring ecosystem that address specific domains or technologies. Each Spring Project focuses on a particular aspect of application development and provides dedicated features and APIs. Some popular Spring Projects include Spring Boot, Spring Data, Spring Security, Spring Cloud, and Spring Integration.

2. Spring Modules: Spring Modules, on the other hand, are modular components within the core Spring framework that provide specific functionality. These modules are designed to be used together to build enterprise applications. Examples of Spring Modules include the Core Container module (providing the fundamental Spring container and dependency injection features), the Data Access module (providing support for working with databases and data access frameworks), the AOP module (providing aspect-oriented programming capabilities), and the Web module (providing support for web application development).


</blockquote>

</details>

---

28. What is the typical Bean life cycle in Spring Bean Factory Container?  

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the Spring framework, the typical lifecycle of a bean within the Bean Factory container follows these steps:

1. Instantiation: The bean is created by invoking the bean's constructor.

2. Populating Properties: Dependencies and properties of the bean are injected using setter methods or constructor arguments.

3. BeanNameAware and BeanFactoryAware: If the bean implements the `BeanNameAware` or `BeanFactoryAware` interfaces, the corresponding callback methods are invoked to provide the bean with its bean name and reference to the Bean Factory.

4. BeanPostProcessor: If there are any BeanPostProcessor implementations registered in the container, the post-processing methods are called. These processors can modify the bean instance or provide additional initialization logic.

5. InitializingBean and custom init methods: If the bean implements the `InitializingBean` interface, the `afterPropertiesSet()` method is invoked. Alternatively, if the bean defines a custom initialization method, that method is called.

6. DisposableBean and custom destroy methods: If the bean implements the `DisposableBean` interface, the `destroy()` method is called when the container is shutting down. Similarly, if the bean defines a custom destroy method, that method is called.

During these stages, the Spring container manages the lifecycle of the bean, including instantiation, dependency injection, initialization, and destruction. The container ensures that the beans are properly initialized and released based on their configuration and lifecycle callbacks.


</blockquote>

</details>

---

29. Describe some of the standard Spring events  

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the Spring framework, there are several standard events that can be published and handled within the application. Some of the commonly used standard Spring events include:

1. ContextRefreshedEvent: This event is published when the ApplicationContext is initialized or refreshed. It indicates that all beans have been loaded, initialized, and are ready for use.

2. ContextStartedEvent: This event is published when the ApplicationContext is started using the start() method. It is typically used to resume any paused application functionality.

3. ContextStoppedEvent: This event is published when the ApplicationContext is stopped using the stop() method. It is often used to perform any cleanup or shutdown tasks.

4. ContextClosedEvent: This event is published when the ApplicationContext is closed using the close() method. It indicates that the application context is being shut down, and any necessary cleanup can be performed.

5. RequestHandledEvent: This event is published when an HTTP request has been handled by a Spring MVC handler. It provides information about the request, including the handler method and execution time.

6. ApplicationEvent: This is a general base class for all application-specific events. Developers can create custom events by extending this class and publishing them within the application.

These events can be used to perform various tasks such as logging, auditing, caching, and triggering specific actions based on the occurrence of certain events in the application. By subscribing to these events, components within the Spring application can respond and react accordingly.


</blockquote>

</details>

---

30. Does Spring Bean provide thread safety? Justify your answer.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- No, Spring Beans do not inherently provide thread safety.
- Whether a Spring Bean is thread-safe or not depends on how it is implemented and managed by the developer.
- The Spring framework itself does not enforce or guarantee thread safety for beans. 
- It is the responsibility of the developer to design and implement thread-safe beans if they are required in a concurrent environment.

</blockquote>

</details>

---

31. What is Spring Expression Language? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Spring Expression Language (SpEL) is a powerful expression language that allows you to dynamically evaluate expressions at runtime in the Spring framework.
-  It provides a wide range of capabilities, including accessing and manipulating object properties, invoking methods, performing mathematical and logical operations, conditional expressions, collection manipulation, and more.
-  SpEL is commonly used in various Spring components, such as bean definitions, annotations, XML configurations, and runtime expressions. 
- It provides a concise and flexible way to configure and manipulate application logic in a Spring application.

</blockquote>

</details>

---

32. What is the difference between $ and # in @value expressions?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring's `@Value` expressions, the symbols `$` and `#` have different meanings:

1. `$` (Dollar Sign): It is used for value injection, where the value is directly resolved from property placeholders or environment variables. For example, `@Value("${app.name}")` will inject the value of the property `app.name` from the configuration file or environment variable.

2. `#` (Hash Sign): It is used for expression evaluation, where the value is evaluated dynamically using Spring Expression Language (SpEL). This allows you to perform complex evaluations, access object properties, invoke methods, perform mathematical operations, etc. For example, `@Value("#{someBean.someProperty}")` will evaluate the expression `someBean.someProperty` using SpEL.

In summary, the `$` symbol is used for simple value injection, while the `#` symbol is used for dynamic expression evaluation using SpEL.


</blockquote>

</details>

---