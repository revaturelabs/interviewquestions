## Technical

1. What is the meaning of Monolithic Application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- When all the features/functionalities of an application are coupled together in single code base, then that application is termed as Monolithic applications.
	
</blockquote> 

</details>

---

2. What do you understand by Monolithic Architectural style?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Monolithic Architectural Style` is traditional software development style.
- It is built as a unified one code base unit that is self-contained and independent from other applications.
- In Monolithic style code is tightly coupled and servers all of the business concerns together.  
- To make a change to Monolithic of application requires update to entire stack by accessing the code base and building and deploying an updated version of the service-side interface. 
- This leads to changes/updates restrictive and time-consuming. 
	
</blockquote> 

</details>

---

3. Why we should avoid Monolithic Style? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
  - There are many drawbacks of using Monolithic Style as listed below-
  - **Slower development speed**  due to large, complex monolithic application.
  - We **can’t scale individual components**.
  - As application evolves & become complex, **making changes are often expensive and time-consuming**.
  - Small change in monolithic application requires the **redeployment of the entire project**.
  - **Difficult to change framework/language** hence barrier to technology adoption.
  - Developer are **constrained by the technologies already used** in the monolith.
  - Due to one **smallest error the entire applications can be down and unavailable**.
</blockquote> 

</details>

---

4. Though we prefer Microservices over Monolithic, still do you see any advantages of building Monolithic applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
  - Yes there are too few advantages of Monolithic applications as listed below-
  - One code base, it is **easier to develop**.
  - Single build unit makes **deployment easier**.
  - **Better performance** due to centralized code base.
  - **Simplified end-to-end testing** due to single, centralized unit.
  - **Easy debugging** to locate application issues.
  - **Cost of hosting** is less compared to microservices style.
	
</blockquote> 

</details>

---

5. How do you go about designing microservices?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Microservices is an architecture style to build large scale applications that can be scaled up independently.
- In a microservice architecture design, we divide an application into suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API.
- These services are built around business capabilities and independently deployable by fully automated deployment process.
- There is a bare minimum of centralized management of these services, which may be written in different programming languages and use different data storage technologies. 
- Each service runs a unique process and manages its database. 
- A service can generate alerts, log data, support user interfaces (UIs), handle user identification or authentication, and perform various other tasks.
	
</details>

---
	
6. What if there are already complex, huge legacy applications operational for decades? Can we convert them into microservices?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Top companies in the world for example Amazon, Netflix, Uber, etc., have adopted the microservices architecture(`MSA`) style for developing their applications. 
- Over time, these enterprises dismantled their monolithic applications and refactored them into microservice-based architectures. 
- Usually, the legacy applications which involved huge capital and way complex at core takes time to slowly migrate to MSA.
- Companies are trying to migrate first the UI or client facing layer to MSA followed by slowly moving towards the core complex layers. 
- This has given them scaling advantages, greater business agility, and increased profits.
	
</blockquote> 

</details>

---
7. What is so special about Netflix and Microservices?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix is an organization that pioneered migration into microservices and became a market leader through innovation.
- Beginning In 2012, Netflix began adopting microservices.
- They made the decision to break down their monolithic legacy application into smaller, individual microservices to lower the possibility of system errors and ensure better long-term system stability.
- Switching to a microservices architecture can create exciting opportunities is proven by Netflix.
	
</blockquote> 

</details>

---
	
8. What is Netflix OSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix has created `Open-Source Software (OSS)` for creating microservices application when it was transiting from monolithic application to microservices. 
- Netflix decided to contribute these libraries and frameworks to the broader open-source community.
- These libraries and frameworks can be used by anyone who wants to create a microservices application for their business.

</blockquote> 

</details>

---
9. What is `Spring Cloud`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Just like Spring Framework, Spring Data & Spring Boot, there is another project called Spring Cloud.
- Spring Cloud project help build robust cloud applications and it provides a solution to the commonly encountered patterns when developing a distributed system. 
- Spring Cloud project provides tools for developers to quickly build both cloud and microservice-based applications.
	
</blockquote> 

</details>

---
10. What is `Spring Cloud Netflix`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Cloud` is divided into a group of sub projects for managing the challenges of development of cloud-based systems. 
- `Spring Cloud Netflix` provides Netflix OSS integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment. 
- With a few simple annotations, we can quickly enable and configure the common patterns inside our application and build large distributed systems with various Netflix components. 

</blockquote> 

</details>

---
11. Can you name few Netflix component you used in Spring Cloud project?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
  - We can leverage `Spring Cloud Netflix` project and integrate below Netflix OSS components- 
  - `Netflix Eureka` - This is Service Discovery Server
  - `Netflix Ribbon` - Dynamic Routing and Load Balancer
  - `Netflix Hystrix` -  Circuit Breaker
  - `Netflix Zuul` - API Gateway
	
</blockquote> 

</details>

---
12. What do you know about Service Discovery in Microservices?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Under distributed application development, we have a concept called Service Registration and Service Discovery.
- We have one dedicated server which is responsible for maintaining the registry of all the microservices that have been deployed and removed.
- We can understand it as a lookup service where microservices (clients) can register themselves and discover other registered microservices.
	
</blockquote> 

</details>

---
	
13. What are the Service Discovery providers you know?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix Eureka or Consul are the two popular Service Discovery providers.

</blockquote> 

</details>

---
14.   What is use of Netflix Eureka? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix Eureka is used as Service Discovery Server.
- Each client microservice need to first register with Eureka server.
- Post registration Eureka server provides metadata such as host, post, and health indicators which allows other microservices to discover it. 
- The discovery server expects a regular heartbeat message from each microservice instance. 
- If any microservice instance consistently fail to send a heartbeat, then the discovery server will remove the instance from its registry. 
- This way Eureka server maintains very stable ecosystem of microservices collaborating with each other. 
	
</blockquote> 

</details>

---
15.  Can we manually maintain addresses of each service while building microservices based applications?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- No, we don’t have to manually maintain the address of other microservices.
- This is usually one of the key responsibilities of Service Discovery Server.
- Usually, each service instance in microservices based architecture is scaled up and down as per application load.
- Also, we use a virtual host to host the services, especially in the cloud environment.
	
</blockquote> 

</details>

---
16. How do you configure Eureka Server in Spring Boot maven application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- We have to add below maven dependencies in `pom.xml`
	
```xml
  <dependencies>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-dependencies</artifactId>
		<version>Camden.SR6</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-eureka-server</artifactId>
	</dependency>
  </dependencies>
	
```
- Configure `Eureka server common port: 8761` inside application.properties file as below-
```
#Port 8761 is the common port for Eureka Servers
server.port=8761

#Indicates whether or not this instance should register its information with eureka server for discovery by others.
#In some cases, you do not want your instances to be discovered whereas you just want do discover other instances.
#Since current app is actual Eureka server hence we must keep this value as false
eureka.client.register-with-eureka=false

#Indicates whether this client should fetch eureka registry information from eureka server.
#Usually Kept false
eureka.client.fetch-registry=false

#If instance goes down what shall be done? in production we must 
#Have multiple instances of the eureka server running that is controlled using below property
#eureka.server.maxThreadsForPeerReplication=0

eureka.server.max-threads-for-peer-replication=0

#When the registry starts, it will complain (with a stacktrace) that there 
#are no replica nodes to which the registry can connect. In a production environment,
#you will want more than one instance of the registry. For our simple purposes, 
#however, it suffices to disable the relevant logging.
#logging.level.com.netflix.eureka=OFF
#logging.level.com.netflix.discovery=OFF
#https://cloud.spring.io/spring-cloud-static/Dalston.SR5/multi/multi__appendix_compendium_of_configuration_properties.html
	
```
- Annotate the Spring Boot application main class with @EnableEurekaServer annotation-

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.netflix.eureka.server.EnableEurekaServer;

@SpringBootApplication
@EnableEurekaServer
public class EurekaServerApplication {
	public static void main(String[] args) {
		SpringApplication.run(EurekaServerApplication.class, args);
	}
}
```
- Check Browser for Registry Server on http://localhost:8761/

</blockquote> 

</details>

---
17. How do we register our service into Service Discovery server?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Ensure the Service Discovery server is up and running, assuming it’s running locally on port 8761 [http://localhost:8761/]
- Now, we have to add required maven dependencies in `pom.xml`-
```xml
  <dependencies>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-dependencies</artifactId>
		<version>Camden.SR6</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-eureka-server</artifactId>
	</dependency>
  </dependencies>
```
- Set below properties inside application.properties file-

```
#When Eureka server is configured with multiple zones we define them, in simple case we can keep it as default
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka

#In Eureka each service is identified by unique Id, it’s our choice to keep id as we like, e.g., combination of `serviceName:port` uniquely identifies each service.
eureka.instance.instanceId=${spring.application.name}:${server.port}

#Our service names
spring.application.name=my-producer

#Our service port number
spring.port=8080

```
- Annotate the Spring Boot application main class with @EnableDiscoveryClient annotation-

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;

//@EnableDiscoveryClient will register discovery service using the jar available in class path like Consul, Eureka, Kubernetes.
//@EnableDiscoveryClient lives in spring-cloud-commons and picks the implementation on the class path. 
//@EnableEurekaClient lives in spring-cloud-netflix and only works for Eureka. If eureka is on your class path, they are effectively the same.

@SpringBootApplication
@EnableDiscoveryClient
public class ProducerEureka2 {
	public static void main(String[] args) {
		SpringApplication.run(ProducerEureka2.class, args);
	}
}
```

- Launch application and verify the service with name `my-producer:8080` is visible on Service Discovery dashboard at http://localhost:8761/

</blockquote> 

</details>

---

18. What is the difference between @EnableDiscoveryClient and @EnableEurekaClient?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- There are multiple implementations of "Discovery Service" (Eureka, Consul, Zookeeper). 
- `@EnableDiscoveryClient` will register discovery service using the jar available in class path like Consul, Eureka, Kubernetes.
- `@EnableDiscoveryClient` lives in `spring-cloud-commons` and picks the implementation on the class path. 
- `@EnableEurekaClient` lives in `spring-cloud-netflix` and only works for Eureka. 
- If eureka is on your class path, they are effectively the same.
</blockquote> 

</details>

---

19. How to fetch service url from `Service Discovery` server using `DiscoveryClient`?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- To fetch service url from Service Discovery server we will inject `org.springframework.cloud.client.discovery.DiscoveryClient` in our service/controller layer.
- `DiscoveryClient` represents operations commonly available to Discovery service such as Netflix Eureka or Consul.
- One service might be registered with same name on multiple ports hence we first need to get list of its all instances using `getInstances(String)` method of `DiscoveryClient`.
- We can then choose any of the retrieved instances and invoke get the service's base url using getUri() method as shown below-
  
```java
	StringBuilder responseText = new StringBuilder();
	List<ServiceInstance> instances = discoveryClient.getInstances("employee-producer");
		for (int i = 0; i < instances.size(); i++) {
			System.out.println("[" + i + "]  -->  " + instances.get(i).getUri());
			responseText.append("\n[" + i + "]  -->  " + instances.get(i).getUri());
		}
		System.out.println("Using the first producer service got from DiscoveryClient:" + instances.get(0).getUri());
		responseText.append("\n\n\nUsing the first service:\n" + instances.get(0).getUri());
		ServiceInstance serviceInstance = instances.get(0);
		String baseUrl = serviceInstance.getUri().toString();
		baseUrl = baseUrl + "/employee";
```

</blockquote> 

</details>

---

20. What do you understand by load balancing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- It is the process of distributing a set of requests or tasks over a set of resources, with the intention of making their overall processing more efficient.
  
</blockquote> 

</details>

---

21. Do you know what the two types of load balancing techniques are?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Yes, there is client and server-side load balancing.
- In server-side load balancing, the clients call an intermediate reverse proxy server, which then decides which instance of the actual server or microservice) will get call.
- In client-side load balancing, the clients call an intermediate server (the API gateway - e.g., Zuul, configured with a load-balancer - e.g. Ribbon and a discovery server - e.g. Eureka), which then decides which instance of the microservice to call.
 
</blockquote> 

</details>

---
22. What is use of Netflix Ribbon?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix Ribbon is a Part of Netflix Open-Source Software (Netflix OSS). 
- This library provides client-side load balancing. 
- It automatically interacts with Netflix Service Discovery (Eureka) because it is a member of the Netflix family.
  
</blockquote> 

</details>

---
23. How to configure & use Netflix Ribbon in Spring application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Ensure the Service Discovery Eureka server is up and running, assuming it’s running locally on port 8761 [http://localhost:8761/].
- Ensure you have multiple instances of one service already registered on Eureka with unique ids as `serviceName:portNo` e.g., `my-service:8080`, `my-service:7070` & `my-service:9090`.
- For using Netflix Ribbon, we need to add below one additional dependency inside pom.xml file along with usual dependencies-

```xml
<dependencies>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-dependencies</artifactId>
		<version>Camden.SR6</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-eureka-server</artifactId>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-ribbon</artifactId>
	</dependency>
</dependencies>
```
- To use client-side load balancer we will inject `org.springframework.cloud.client.loadbalancer.LoadBalancerClient` in our service/controller layer.
- With the help of LoadBalancerClient object we will fetch service url as below-
```java
		StringBuilder responseText = new StringBuilder();
		ServiceInstance serviceInstance = loadBalancer.choose("my-service");
		System.out.println("Using the only producer service got from LoadBalancerClient:" + serviceInstance.getUri());
		responseText.append("Using the only producer service got from LoadBalancerClient:\n" + serviceInstance.getUri());
		String baseUrl = serviceInstance.getUri().toString();
		baseUrl = baseUrl + "/employee";
```
- Once the service url is retrieved we will invoke service normally (e.g., using RestTemplate)

</blockquote> 

</details>

---
24. What do you understand by Circuit Breaker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Circuit Breaker is a design pattern used in software development. 
- It is used to detect failures and encapsulates the logic of preventing a failure from constantly recurring, during maintenance, temporary external system failure or unexpected system difficulties.
- The Circuit Breaker design pattern stops sending the request to the service which is not working or taking too long to respond.
- Circuit Breaker aims in building fault-tolerant and resilient systems.
</blockquote> 

</details>

---
25. How Spring Cloud supports Circuit Breaker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Cloud’s Circuit Breaker library provides an implementation of the Circuit Breaker pattern.
- When we wrap a method call in a circuit breaker, Spring Cloud Circuit Breaker watches for failing calls to that method.
- In case failure occurs, Spring Cloud Circuit Breaker opens the circuit so that subsequent calls automatically fail. 
- While the circuit is open, Spring Cloud Circuit Breaker redirects calls to our specified `fallback method`.
	
</blockquote> 

</details>

---
26. Which circuit breaker implementations does Spring cloud supports?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Cloud Circuit Breaker supports many different circuit breaker implementations including, Resilience4J, Netflix Hystrix, Sentinal, and Spring Retry etc. 
</blockquote> 

</details>

---

27. How to configure and use Netflix Hystrix?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Ensure the Service Discovery Eureka server is up and running, assuming it’s running locally on port 8761 [http://localhost:8761/].
- For using Netflix Hystrix, we need to add below additional dependency inside pom.xml file along with usual dependencies under the service provider end -

```xml
<dependencies>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-dependencies</artifactId>
		<version>Camden.SR6</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-eureka-server</artifactId>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-hystrix</artifactId>
	</dependency>
</dependencies>
```
- In the service provider side, we need to mark the target method as `@HystrixCommand` where circuit breaker will be enabled.
- We also need to mention fallbackMethod attribute which is our handler method invoked in case the target method execution fails.
  
```java
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;
import com.revature.model.Employee;
import com.netflix.hystrix.contrib.javanica.annotation.HystrixCommand;

@RestController
public class ProducerController {
	@GetMapping(value = "/info")
	public String getAllTodos() {
		return "This is 'employee-producer-eureka-ribbon-hystrix4' service";
	}
	@GetMapping(value = "/employee")
	@HystrixCommand(fallbackMethod = "getDataFallBack")
	public Employee firstPage() {
		Employee emp = new Employee();
		emp.setName("A");
		if (emp.getName().equalsIgnoreCase("A"))
			throw new RuntimeException();
		return emp;
	}
	public Employee getDataFallBack() {
		Employee emp = new Employee();
		emp.setName("fallback-emp1");
		emp.setDesignation("fallback-manager");
		emp.setEmpId("fallback-1");
		emp.setSalary(0);
		return emp;
	}
}
```
- Annotate the Spring Boot application main class with additional @EnableCircuitBreaker annotation-

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.circuitbreaker.EnableCircuitBreaker;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;

@SpringBootApplication
@EnableCircuitBreaker
@EnableDiscoveryClient
public class ProducerEurekaHystrix {
	public static void main(String[] args) {
		SpringApplication.run(ProducerEurekaHystrix.class, args);
	}
}

```
</blockquote> 

</details>

---
28. What do you understand by `API Gateway`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In simple term, the API Gateway is responsible to take requests and redirects them to the right service.
- We can expose multiple services (REST, SOAP, etc.) through a single API Gateway. 
- We can create micro-services to implement our business logic and expose them to external users/system by publishing those service as an API in a API Gateway. 
- Apart from simple routing API Gateway, also provide various other features like-
  - Security (User authentication & authorization)
  - Throttling management
  - Reporting
  - Traffic monitoring
  - API documentation
  - Rate Limiting
  - Caching
  - Versioning
  - Routing
	
</blockquote> 

</details>

---
29. What is use of Netflix Zuul?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix Zuul is an API Gateway server.
- Zuul Server dynamically routes the requests to the respective backend microservice application.
- For Example, all request starting with /api/account are mapped to account service and those starting with /api/sales are mapped to the sales service. 
- It works as a front door for all the requests. 
- Zuul is built to enable dynamic routing, monitoring, resiliency, and security. 
- Zuul is a JVM-based router and server-side load balancer from Netflix.
</blockquote> 

</details>

---
30. How to configure and use Netflix Zuul in Spring cloud application?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Zuul is a JVM-based router and server-side load balancer from Netflix.
- Ensure the Service Discovery Eureka server is up and running, assuming it’s running locally on port 8761 [http://localhost:8761/].
- We need to create separate service for API Gateway by adding one additional dependency inside pom.xml file along with usual dependencies-

```xml
<dependencies>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-dependencies</artifactId>
		<version>Camden.SR6</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-eureka-server</artifactId>
	</dependency>
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-zuul</artifactId>
	</dependency>
</dependencies>
```
- We need to create Zuul filters (i.e., PreFilter, PostFilter, RouteFilter, ErrorFilter)  by extending `com.netflix.zuul.ZuulFilter` .
- Set zuul routes properties inside application.properties file-

```
#All requests http://localhost:8079/product-producer/ will be diverted to this resource http://localhost:10000/info
zuul.routes.product-producer.url=http://localhost:10000/info
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka
server.port=8079
```
- Annotate the Spring Boot application main class with @EnableZuulProxy annotation-
```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;
import org.springframework.cloud.netflix.zuul.EnableZuulProxy;
import org.springframework.context.annotation.Bean;
import com.revature.filter.ErrorFilter;
import com.revature.filter.PostFilter;
import com.revature.filter.PreFilter;
import com.revature.filter.RouteFilter;

@SpringBootApplication
@EnableDiscoveryClient
@EnableZuulProxy
public class EmployeeZuulGatwayApplication {
	public static void main(String[] args) {
		SpringApplication.run(EmployeeZuulGatwayApplication.class, args);
	}
	@Bean
	public PreFilter preFilter() {
		return new PreFilter();
	}
	@Bean
	public PostFilter postFilter() {
		return new PostFilter();
	}
	@Bean
	public ErrorFilter errorFilter() {
		return new ErrorFilter();
	}
	@Bean
	public RouteFilter routeFilter() {
		return new RouteFilter();
	}
}
```
- Now all the requests to http://localhost:8079/product-producer/ will be diverted to this resource http://localhost:10000/info due to Zuul routing.

</blockquote> 

</details>

---
31. What are Zuul Filter & its types?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Netflix Zuul mainly comprises of four types of filters.
- Filter enable us to intercept the traffic in different timeline of the request processing. 
- We can add any number of filters for a particular url pattern.
  - `Pre filters` – Invoked before the request is routed.
  - `Post filters` – Invoked after the request has been routed.
  - `Route filters` – Used to route the request.
  - `Error filters` – Invoked when an error occurs while handling the request.
	
</blockquote> 

</details>

---
32.  What is meaning of Blue/Green Deployments?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- A blue/green deployment is an application deployment strategy.
- First we create two separate, but identical environments. 
- One environment (blue) is running the current application version and one environment (green) is running the new application version. 
- Using a blue/green deployment strategy increases application availability and reduces deployment risk by simplifying the rollback process if a deployment fails. 
- Once testing has been completed on the green environment, live application traffic is directed to the green environment and the blue environment is deprecated.
	
</blockquote> 

</details>

---
