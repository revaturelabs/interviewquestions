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

