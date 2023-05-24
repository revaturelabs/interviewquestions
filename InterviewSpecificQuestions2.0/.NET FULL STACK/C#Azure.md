## Technical

1.  What is Microsoft Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Microsoft Azure is a set of cloud services that help your organization to meet your business requirements. You can build, manage, and deploy different applications with the help of different frameworks and tools using Azure.

</blockquote>

</details>

---

2. Why do we use Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are many reasons and benefits to choosing Azure. All solutions are in one place. Some reasons are:

- We can easily create a web application with a few numbers of clicks
- The testing application is easy here.
- Once the development and testing will over for a particular application, we can use Azure to host the application.
- We can create a virtual machine (VM) for all the activities.

</blockquote>

</details>

---

3. What is Azure Portal?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Azure Portal is a single portal or a single place where you are accessing and managing all your applications. It helps to build, manage, and monitor your simple web applications to complex cloud applications using a single portal.

</blockquote>

</details>

---

4. What is Azure as PaaS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

PaaS is a development and deployment model to support the complete web application life cycle of building, testing, deploying, managing, and updating the application. Azure is a Platform As A Service (Paas).

</blockquote>

</details>

---

5. What are the web applications that can be deployed with Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Different web applications like .Net, PHP, WCF, Java, etc. are supported in Azure. Multiple languages are supported in Azure.

</blockquote>

</details>

---

6. What is SQL Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

SQL Azure is the cloud-based relational database that is offered by Microsoft. The service is based on SQL server technology, and it is used in a Microsoft data centre that is hardware owned and maintained by Microsoft.

</blockquote>

</details>

---

7.  What will happen when the SQL Azure database reaches the max size?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

If the SQL Azure database will reach the max size, data read or fetch operations will still work on it but create, insert, or update operations will stop with it. You can choose to drop, delete, or truncate the data in this condition.

</blockquote>

</details>

---

8. In SQL Azure, which encryption security is available?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In SQL Azure, SSL connections are only supported.

`SET encryption = TRUE`

</blockquote>

</details>

---

9. What are the different database types in SQL Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Microsoft Azure provides three different types of Azure SQL models as below,

**Standalone Database**: Standalone Database is designed for different types of applications like software-as-a-service solutions, and cloud-based applications that use a single database to store data needed.

**Managed Instance**: This model is targeted for migration activities from On-premises to the cloud environment.
Elastic pool: This model helps to reduce costs by sharing the same resources with a group of standalone databases.

</blockquote>

</details>

---

10. What is SQL Azure firewall?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Security is one of the main concerns at the present time in the IT sector. SQL Azure Firewall is used as a security mechanism that will work to block the requests based on the IP address.

</blockquote>

</details>

---

11. How many databases can you create in a single server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In the single SQL Azure server, it is possible to create 150 databases that will include a master database as well.

</blockquote>

</details>

---

12. Can you explain the SQL Azure security?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

SQL Azure services will allow you to block the request that will be based on an IP address by using the SQL Azure firewall. It will use the SQL server authentication process that will authenticate the connections. By default, SQL Azure connections are SSL encrypted.

</blockquote>

</details>

---

13. What will be the process to migrate to SQL Azure from the SQL server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

If we want to migrate from the SQL server to SQL Azure, we can use SSIS or BCP. For the schema migration, generate script wizard will be used and we can also use the tool named SQL Azure Migration Wizard for it.

</blockquote>

</details>

---

14. How will you sync SQL Azure with the on-premise SQL server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It is possible to use No code solution named DATA SYNC to sync SQL Azure with an on-premises SQL server. It is also possible to develop custom solutions by using SYNC Framework for it.

SQL Azure allows users to run their SQL server workloads as a hosted service (PaaS). 

</blockquote>

</details>

---

15.  How will you back up the SQL Azure data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Backup is important to handle the issues of hardware and 3 database replicas are used in SQL Azure for backup. For the errors based on the user level, the COPY command is used for the creation of the SQL Azure database replica. It is also possible to back up the data of SQL Azure to any local SQL server with the use of SSIS, BCP etc.

</blockquote>

</details>

---

16. What are the benefits of a Sharded Database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Allows users to take benefit of maximum resources within the cloud.
- Reduces the chances of a single point of failure.
- Reduces SQL Azure throttling and I/O bottlenecks.
- Enables users to have their own database, access other databases, and share database.
- Benefits users by offering low-cost cloud resources on-demand basis and release when done.

</blockquote>

</details>

---

17. How can you improve the performance of SQL Azure databases?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To improve the performance of SQL Azure databases, you can tune the database by using the information from the execution plan as well as statistics of the query. It is possible to use dynamic management views of SQL Azure for the monitoring and management of the SQL Azure database. Network latency and bandwidth also affect the performance of the SQL Azure database so it can be used to improve the performance.

</blockquote>

</details>

---

18. How is SQL Azure different from SQL server?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

SQL Azure is a cloud-based service and so it has its own set of pros and cons when compared to SQL servers. SQL Azure service benefits include on-demand provisioning, high availability, reduced management overhead and scalability. But SQL Azure abstracts some details from the subscriber which can be good or bad which depends on the context of the need.

</blockquote>

</details>

---

19. How many replicas are maintained for each SQL Azure database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

For each database, three replicas are maintained for each database that one provisions. One of them is a primary replica. All read/write happens on the primary replica and other replicas are kept in sync with the primary replica. If for some reason, the primary goes down, another replica is promoted to primary. All this happens under the hood.

</blockquote>

</details>

---

20.  What is Sharding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- It is a technique for partitioning large data sets, which improves performance and scalability. 
- It also enables distributed querying of data across multiple tenants.

</blockquote>

</details>

---

21. What is code near application topology?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Code near application topology means that the SQL Azure database and the windows azure hosted service consuming the data are hosted in the same Azure data center.

</blockquote>

</details>

---

22. What is the index requirement in SQL Azure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

All tables must have clustered indexes. We can't have a table without a clustered index.

</blockquote>

</details>

---

23. How do you handle datasets larger than 50 Gb?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

As of now, we have to build a custom solution at the application level that can handle the scale out of underlying SQL Azure databases. But Microsoft has announced, SQL Azure Federations that will assist in scaling out of SQL Azure databases. And scale-out means that we are splitting the data into smaller subsets spread across multiple databases.

</blockquote>

</details>

---

24.  What is Federation?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The federation is where you define the data type (e.g., Customer ID, Product ID) you’ll share. 
- As with creating the root database, you can create a federation through the SQL Azure database management portal, with SQLAzureMW or by using this T-SQL script while connected to your root database:

```SQL
CREATE FEDERATION <FederationName>(<DistributionKeyName> <DistributionType> RANGE)
```
In this example, 

- `<FederationName>` is the name of the federation (not the name of the physical database, which is a System-GUID). 
- `<DistributionKeyName>` is the name for the distribution key, 
- `<DistributionType>` is the distribution data type that data will be sharded on. 
- The valid distribution data types are int, bigint, uniqueidentifier and varbinary (up to 900).

</blockquote>

</details>

---
  
25.What is Azure Redis Cache?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It is an open-source, in-memory Redis cache system provided and maintained by Azure.
It helps the web applications to improve the performance by fetching data from the backend database and storing it into the Redis cache for the first request and then fetching data from the Redis cache for all subsequent requests.
Azure Redis Cache provides powerful and secure caching mechanisms by making use of the Azure cloud.

</blockquote>

</details>

---

26.What do you need to do when drive failure occurs?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The following steps need to be performed when the drive failure occurs:

To make sure that the Azure Storage functions without fail, we need to ensure that the drive is not mounted.
Replace the drive so that the drive gets remounted and formatted.

</blockquote>

</details>

---

27.What would happen when the maximum failed attempts are reached during the process of Azure ID Authentication?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In case of maximum failed attempts, the azure account would get locked and the method of locking is dependent on the protocol that analyzes the entered password and the IP addresses of the login requests.
  
</blockquote>

</details>

---
  
28.What is a Resource group?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
A resource group is a logical container for created resources in Azure. An ARM resource can exist only in one resource group. A resource group is created in a region and it can have the resources from the other regions. All resources within the resource group share the common lifecycle. 
  
</blockquote>

</details>

---
  
29.What are the different ways to host web sites in Azure?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
 
Azure supports multiple ways to Host like App Service (PaaS), Virtual Machine (IaaS) and Service Fabric.

App Service is the best option for Most of the web sites. It allows quick deployment, scalability, management & also cost-effective.

A Virtual Machine is an option if your existing Web Sites require Custom Configurations in IIS Level, Cannot Fit into App Service etc.

Service Fabric is an option if you are writing a Microservice application that requires Massive Scaling, Stateful Services etc.
  
</blockquote>

</details>

---
  
30.How the app services can be scaled?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
An app service supports two types of scaling - vertical (up/down) and horizontal (out/in). During scaling, there is no impact on service availability.

In vertical scaling, VM size can be increased or decreased as per your need.
  
In horizontal scaling, identical VMs of the desired size will be created or removed as per your need
  
Autoscaling is supported by standard and premium based on matrices (response time, memory, CPU, data uses etc.)
  
</blockquote>

</details>

---
  
31.What is Azure Function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
Azure Function is a Serverless Compute Service that Runs code on Demand like Events or External-Invoke. Azure Functions can Scale up Automatically based on Demand. Azure functions are the evolution of Web Jobs. You can develop functions in C#, Node, Java, Python etc. Internally, Azure functions use App services.
  
We can use Functions for Backend Services, Event-based Processing like Data Table creation on File Upload, Scheduled Tasks etc.
  
</blockquote>

</details>

---
  
32.In terms of Azure, what are public, private, and hybrid cloud?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
Public Cloud: Each component which the user uses in an application is operating only on Azure

Private Cloud: Azure services are being run within an on-premises data center. Such data centers are utilized by the user to either host applications or systems.

Hybrid Cloud: It blends features of Public and Private cloud. Certain of the user’s components are executed on Azure whereas others run within an on-premises datacenter.
  
</blockquote>

</details>

---
  
33.What are the different roles in Azure?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
There are three types of roles in Azure – Web Role, Worker Role, and VM.

The Web role is basically dedicated to the website deployments.
The Worker role is used to manage background processes in Azure.
VM role is required to manage or schedule tasks. He is responsible for customizing machines and managing other Azure roles too.
  
</blockquote>

</details>

--- 

34.What are the available options for deployment environments provided by Azure?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
Azure provides two deployment environments, they are:

Staging Environment: This environment is used for validating the changes of our application before making them live into the main environment.
Here, the application is identified by means of GUID (Globally Unique Identifier) of Azure which has the URL as: GUID.cloudapp.net
Production Environment: This is the main environment where our application goes live and can be accessed by the target audience which can be accessed by means of DNS friendly URL: appName.cloudapp.net
  
</blockquote>

</details>

--- 
  
35.In Azure, define role instance ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
A role instance is a virtual computer where application code is run in conjunction with running role specifications. In accordance with the specification in the cloud service configuration files, a role may have more than one instance.
  
</blockquote>

</details>

--- 

