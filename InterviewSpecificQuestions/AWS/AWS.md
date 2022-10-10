1. What is AWS?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- AWS stands for Amazon Web Services. 
- It is a service which is provided by the Amazon that uses distributed IT infrastructure to provide different IT resources on demand. 
- It provides different services such as an infrastructure as a service, platform as a service, and software as a service.

</blockquote>

</details>

---

2. What are the components of AWS?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The following are the main components of AWS are:
  - `Simple Storage Service (S3)`: S3 is a service of AWS that stores the files. It is objectbased storage, i.e., you can store the images, word files, pdf files, etc. The size of the file that can be stored in S3 is from 0 Bytes to 5 TB. It is an unlimited storage medium, i.e., you can store the data as much you want. S3 contains a bucket which stores the files. A bucket is like a folder that stores the files. It is a universal namespace, i.e., name must be unique globally. Each bucket must have a unique name to generate the unique DNS address.
  - `Elastic Compute Cloud (EC2)`: Elastic Compute Cloud is a web service that provides resizable compute capacity in the cloud. You can scale the compute capacity up and down as per the computing requirement changes. It changes the economics of computing by allowing you to pay only for the resources that you actually use.
  - `Elastic Block Store (EBS)`: It provides a persistent block storage volume for use with EC2 instances in aws cloud. EBS volume is automatically replicated within its availability zone to prevent the component failure. It offers high durability, availability, and low-latency performance required to run your workloads.
  - `CloudWatch`: It is a service which is used to monitor all the AWS resources and applications that you run in real time. It collects and tracks the metrics that measure your resources and applications. If you want to know about the CloudWatch in detail, then click on the below link: Click here
  - `Identity Access Management (IAM)`: It is a service of AWS used to manage users and their level of access to the AWS management console. It is used to set users, permissions, and roles. It allows you to grant permission to the different parts of the aws platform. If you want to know about the IAM, then click the below link: Click here
  - `Simple Email Service`: Amazon Simple Email Service is a cloud-based email sending service that helps digital marketers and application developers to send marketing, notification, and transactional emails. This service is very reliable and cost effective for the businesses of all the sizes that want to keep in touch with the customers.
  - `Route53`: It is a highly available and scalable DNS (Domain Name Service) service. It provides a reliable and cost effective way for the developers and businesses to route end users to internet applications by translating domain names into numeric IP addresses.

</blockquote>

</details>

---

3. What are Key-pairs?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- An Amazon EC2 uses public key cryptography which is used to encrypt and decrypt the login information. 
- In public key cryptography, the public key is used to encrypt the information while at the receiver's side, a private key is used to decrypt the information.
- The combination of a public key and the private key is known as key-pairs. Key-pairs allows you to access the instances securely.

</blockquote>

</details>

---

4. What is S3?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- S3 is a storage service in aws that allows you to store the vast amount of data.

</blockquote>

</details>

---

5. How many buckets can be created in S3?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- By default, you can create up to 100 buckets

</blockquote>

</details>

---

6. What is Cross Region Replication?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Cross Region Replication is a service available in aws that enables to replicate the data from one bucket to another bucket which could be in a same or different region. It provides asynchronous copying of objects, i.e., objects are not copied immediately.

</blockquote>

</details>

---

7. What are `Regions` and `Availability Zones` in aws?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- `Regions`: A region is a geographical area which consists of 2 or more availability zones. A region is a collection of data centers which are completely isolated from other regions.
- `Availability Zones`: An Availability zone is a data center that can be somewhere in the country or city. Data center can have multiple servers, switches, firewalls, load balancing. The things through which you can interact with the cloud reside inside the Data center.

</blockquote>

</details>

---

8. What is the minimum and maximum size that you can store in S3?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The minimum size of an object that you can store in S3 is 0 bytes and the maximum size of an object that you can store in S3 is 5 TB.

</blockquote>

</details>

---

9. What are `EBS Volumes`?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- `Elastic Block Store` is a service that provides a persistent block storage volume for use with EC2 instances in aws cloud. 
- EBS volume is automatically replicated within its availability zone to prevent from the component failure. 
- It offers high durability, availability, and low-latency performance required to run your workloads.

</blockquote>

</details>

---

10. What is Auto Scaling?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- `Auto Scaling` is a feature in aws that automatically scales the capacity to maintain steady and predictable performance. 
- While using auto scaling, you can scale multiple resources across multiple services in minutes. 
- If you are already using Amazon EC2 Auto scaling, then you can combine Amazon EC2 AutoScaling with the AutoScaling to scale additional resources for other AWS services.
- Benefits of Auto Scaling
  - Setup Scaling Quickly: It sets the target utilization levels of multiple resources in a single interface. You can see the average utilization level of multiple resources in the same console, i.e., you d- not have to move to the different console.
  - Make Smart Scaling Decisions: It makes the scaling plans that automate how different resources respond to the changes. It optimizes the availability and cost. It automatically creates the scaling policies and sets the targets based on your preference. It als- monitors your application and automatically adds or removes the capacity based on the requirements.
  - Automatically maintain performance: Auto Scaling automatically optimize the application performance and availability even when the workloads are unpredictable. It continuously monitors your application to maintain the desired performance level. When demand rises, then Auto Scaling automatically scales the resources.

</blockquote>

</details>

---

11. What is AMI?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- AMI stands for Amazon Machine Image. It is a virtual image used to create a virtual machine within an EC2 instance.

</blockquote>

</details>

---

12. Can a AMI be shared?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Yes, an AMI can be shared.

</blockquote>

</details>

---

13. How can you secure the access to your S3 bucket?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- S3 bucket can be secured in two- ways:
  - ACL (Access Control List):
    ACL is used to manage the access of resources to buckets and objects. An object of each bucket is associated with ACL. It defines which AWS accounts have granted access and the type of access. When a user sends the request for a resource, then its corresponding ACL will be checked to verify whether the user has granted access to the resource or not.
    When you create a bucket, then Amazon S3 creates a default ACL which provides a full control over the AWS resources.
  - Bucket Policies
    Bucket policies are only applied to S3 bucket. Bucket policies define what actions are allowed or denied. Bucket policies are attached to the bucket not to an S3 object but the permissions define in the bucket policy are applied to all the objects in S3 bucket.
    - The following are the main elements of Bucket policy:
      - Sid: A Sid determines what the policy will do. For example, if an action that needs to be performed is adding a new user to an Access Control List (ACL), then the Sid would be AddCannedAcl. If the policy is defined to evaluate IP addresses, then the Sid would be IPAllow.
      - Effect: An effect defines an action after applying the policy. The action could be either to allow an action or to deny an action.
      - Principal: A Principal is a string that determines to whom the policy is applied. If we set the principal string as '*', then the policy is applied to everyone, but it is als- possible that you can specify individual AWS account.
      - Action: An Action is what happens when the policy is applied. For example, s3:Getobject is an action that allows to read object data.
      - Resource: The Resource is a S3 bucket to which the statement is applied. You cannot enter a simply bucket name, you need to specify the bucket name in a specific format. For example, the bucket name is javatpointobucket, then the resource would be written as "arn:aws:s3""javatpointobucket/*".

</blockquote>

</details>

---

14. What are policies and what are the different types of policies?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Policy is an object which is associated with a resource that defines the permissions. AWS evaluate these policies when user makes a request. Permissions in the policy determine whether to allow or to deny an action. Policies are stored in the form of a JSON documents.
- AWS supports six types of policies:
  - Identity-based policies
  - Resource-based policies
  - Permissions boundaries
  - Organizations SCPs
  - Access Control Lists
  - Session policies
  
![AWS policies](https://user-images.githubusercontent.com/110088496/194527269-0253981a-25fe-44bb-bcd0-6827827c99e0.png)
  
- Identity-based policies: Identity-based policies are the permissions stored in the form of JSON format. This policy can be attached to an identity user, group of users or role. It determines the actions that the users can perform, on which resources, and under what conditions.
- Identity-based policies are further classified into two- categories:
  - Managed Policies: Managed Policies are the identity-based policies which can be attached to multiple users, groups or roles. There are two- types of managed policies:
  - AWS Managed Policies: AWS Managed Policies are the policies created and managed by AWS. If you are using the policies first time, then we recommend you to use AWS Managed Policies.
  - Custom Managed Policies: Custom Managed Policies are the identity-based policies created by user. It provides more precise control over the policies than AWS Managed Policies.
  - Inline Policies: Inline Policies are the policies created and managed by user. These policies are encapsulated directly into a single user, group or a role.
  - Resource-Based Policies: Resource-based policies are the policies which are attached to the resource such as S3 bucket. Resource-based policies define the actions that can be performed on the resource and under what condition, these policies can be applied.
  - Permissions boundaries: Permissions boundaries are the maximum permissions that identity-based policy can grant to the entity.
  - Service Control Policies (SCPs): Service Control Policies are the policies defined in a JSON format that specify the maximum permissions for an organization. If you enable all the features in an Organization, then you can apply Service Control Policies to any or all of your AWS accounts. SCP can limit the permission on entities in member accounts as well as AWS root user account.
  - Access Control Lists (ACLs): ACL defines the control that which principals in another AWS account can access the resource. ACLs cannot be used to control the access of a principal in a different AWS account. It is the only policy type which does not have the JSON policy document format.

</blockquote>

</details>

---

15. What are different types of instances?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Following are the different types of instances:
  - `General Purpose` Instance type: 
    - General purpose instances are the instances mainly used by the companies. 
    - There   are two- types of General Purpose instances: Fixed performance (eg. M3 and M4) and Burstable performance (eg. T2). 
    - Some of the sectors use this instance such as Development environments, build servers, code repositories, low traffic websites and web applications, micro-services, etc.
    - Following are the General Purpose Instances:
      - `T2` instances: T2 instances are the instances that receive CPU credits when they are sitting idle and they use the CPU credits when they are active. These instances d- not use the CPU very consistently, but it has the ability to burst to a higher level when required by the workload.
      - `M4` instances: M4 instances are the latest version of General purpose instances. These instances are the best choice for managing memory and network resources. They are mainly used for the applications where demand for the micro-servers is high.
      - `M3` instances: M3 instance is a prior version of M4. M4 instance is mainly used for data processing tasks which require additional memory, caching fleets, running backend servers for SAP and other enterprise applications.
  - `Compute Optimized` Instance type:
    - Compute Optimized Instance type consists of two- instance types: C4 and C3.
      - `C3` instance: C3 instances are mainly used for those applications which require very high CPU usage. These instances are mainly recommended for those applications that require high computing power as these instances offer high performing processors.
      - `C4` instance: C4 instance is the next version of C3 instance. C4 instance is mainly used for those applications that require high computing power. It consists of Intel E5-2666 v3 processor and use Hardware virtualization. According to the AWS specifications, C4 instances can run at a speed of 2.9 GHz, and can reach to a clock speed of 3.5 GHz.
      - `GPU` Instances: GPU instances consist of G2 instances which are mainly used for gaming applications that require heavy graphics and 3D application data streaming. It consists of a high-performance NVIDIA GPU which is suitable for audio, video, 3D imaging, and graphics streaming kinds of applications. To run the GPU instances, NVIDIA drivers must be installed.
  - `Memory Optimized` Instances:
    - Memory Optimized Instances consists of R3 instances which are designed for memory- intensive applications. R3 instance consists of latest Intel Xeon lvy Bridge processor. R3 instance can sustain a memory bandwidth of 63000 MB/sec. R3 instance offers a high- performance databases, In memory analytics, and distributed memory caches.
  - `Storage Optimized` Instances:
    - Storage Optimized Instances consist of two- types of instances: I2 and D2 instances.
      - `I2` instance: It provides heavy SSD which is required for the sequential read, and write access to a large data sets. It als- provides random I/- operations to your applications. It is best suited for the applications such as high-frequency online transaction processing systems, relational databases, NoSQL databases, Cache for in-memory databases, Data warehousing applications and Low latency Ad- Tech serving applications.
      - `D2` instance: D2 instance is a dense storage instance which consists of a high-frequency Intel Xeon E5-2676v3 processors, HDD storage, High disk throughput.

</blockquote>

</details>

---

16. What is the default storage class in S3?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The default storage class is Standard Frequently Accessed.

</blockquote>

</details>

---

17. Difference between Stopping and Terminating the instances?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- `Stopping`: You can stop an EC2 instance and stopping an instance means shutting down the instance. Its corresponding EBS volume is still attached to an EC2 instance, s- you can restart the instance as well.
- `Terminating`: You can als- terminate the EC2 instance and terminating an instance means you are removing the instance from your AWS account. When you terminate an instance, then its corresponding EBS is als- removed. Due to this reason, you cannot restart the EC2 instance.

</blockquote>

</details>

---

18.  How many Elastic IPs can you create?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- 5 elastic IP addresses that you can create per AWS account per region.

</blockquote>

</details>

---

19. What is a Load Balancer?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Load Balancer is a virtual machine that balances your web application load that could be Http or Https traffic that you are getting in. It balances a load of multiple servers s- that n- web server gets overwhelmed.

</blockquote>

</details>

---

20. What is VPC?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- VPC stands for Virtual Private Cloud. It is an isolated area of the AWS cloud where you can launch AWS resources in a virtual network that you define. It provides a complete control on your virtual networking environment such as selection of an IP address, creation of subnets, configuration of route tables and network gateways.

</blockquote>

</details>

---

21. What is VPC peering connection?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- A VPC peering connection is a networking connection that allows you to connect one VPC with another VPC through a direct network route using private IP addresses.
- By using VPC peering connection, instances in different VPC can communicate with each other as if they were in the same network.
- You can peer VPCs in the same account as well as with the different AWS account

</blockquote>

</details>

---

22. How can you control the security to your VPC?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- You can control the security to your VPC in two- ways:
  - Security Groups:  It acts as a virtual firewall for associated EC2 instances that control both inbound and outbound traffic at the instance level. 
  - Network access control lists (NACL):  It acts as a firewall for associated subnets that control both inbound and outbound traffic at the subnet level. 

</blockquote>

</details>

---

23. What are the different database types in RDS?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Following are the different database types in RDS:
  - Amazon Aurora:
    - It is a database engine developed in RDS. Aurora database can run only on AWS infrastructure not like MySQL database which can be installed on any local device. 
    - It is a MySQL compatible relational database engine that combines the speed and availability of traditional databases with the open source database.
  - Postgre SQL:
    - PostgreSQL is an open source relational database for many developers and startups.
    - It is easy to set up, operate, and can als- scale PostgreSQL deployments in the cloud.
    - You can als- scale PostgreSQL deployments in minutes with costoefficient.
    - PostgreSQL database manages time-consuming administrative tasks such as PostgreSQL software installation, storage management, and backups for disaster recovery.
  - MySQL:
    - It is an open source relational database.
    - It is easy to set up, operate, and can als- scale MySQL deployments in the cloud.
    - By using Amazon RDS, you can deploy scalable MySQL servers in minutes with costoefficient.
  - MariaDB:
    - It is an open source relational database created by the developers of MySQL.
    - It is easy to set up, operate, and can als- scale MariaDB server deployments in the cloud.
    - By using Amazon RDS, you can deploy scalable MariaDB servers in minutes with costoefficient.
    - It frees you from managing administrative tasks such as backups, software patching, monitoring, scaling and replication.
  - Oracle:
    - It is a relational database developed by Oracle.
    - It is easy to set up, operate, and can als- scale Oracle database deployments in the cloud.
    - You can deploy multiple editions of Oracle in minutes with costoefficient.
    - It frees you from managing administrative tasks such as backups, software patching, monitoring, scaling and replication.
    - You can run Oracle under two- different licensing models: "License Included" and "Bring Your Own License (BYOL)".- In License Included service model, you d- need have to purchase the Oracle license separately as it is already licensed by AWS. In this model, pricing starts at $0.04 per hour. If you already have purchased the Oracle license, then you can use the BYOL model to run Oracle databases in Amazon RDS with pricing starts at $0.025 per hour.
  - SQL Server
    - SQL Server is a relational database developed by Microsoft.
    - It is easy to set up, operate, and can als- scale SQL Server deployments in the cloud.
    - You can deploy multiple editions of SQL Server in minutes with costoefficient.
    - It frees you from managing administrative tasks such as backups, software patching, monitoring, scaling and replication.
</blockquote>

</details>

---

24.  What is Redshift?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Redshift is a fast, powerful, scalable and fully managed data warehouse service in the cloud.
- It provides ten times faster performance than other data warehouse by using machine learning, massively parallel query execution, and columnar storage on high-performance disk.
- You can run petabytes of data in Redshift datawarehouse and exabytes of data in your data lake built on Amazon S3.

</blockquote>

</details>

---

25. What are the different types of routing policies in route53?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Following are the different types of routing policies in route53:
- Simple Routing Policy:
  - Simple Routing Policy is a simple round-robin policy which is applied to a single resource doing the function for the domain, For example, web server is sending the content to a website where web server is a single resource.
  It responds to DNS queries based on the values present in the resource.
- Weighted Routing Policy:
  - Weighted Routing Policy allows you to route the traffic to different resources in specified proportions. For example, 75% in one server, and 25% in another server.
  - Weights can be assigned in the range from 0 to 255.
  - Weight Routing policy is applied when there are multiple resources accessing the same function. For example, web servers accessing the same website. Each web server will be given a unique weight number.
  - Weighted Routing Policy associates the multiple resources to a single DNS name.
- Latency-based Routing Policy:
  - Latentobased Routing Policy allows Route53 to respond to the DNS query at which data center gives the lowest latency.
  - Latency-based Routing policy is used when there are multiple resources accessing the same domain. Route53 will identify the resource that provides the fastest response with lowest latency.
- Failover Routing Policy
- Geolocation Routing Policy

</blockquote>

</details>

---

26. What is the maximum size of messages in SQS?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The maximum size of message in SQS IS 256 KB.

</blockquote>

</details>

---

27. Differences between Security group and Network access control list?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

| **Security Group**                                                                                                                                                                                                                   | **NACL (Network Access Control List)**                                                                                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| It supports only allow rules, and by default, all the rules are denied. You cannot deny the rule for establishing a connection.                                                                                                      | It supports both allow and deny rules, and by default, all the rules are denied. You need to add the rule which you can either allow or deny it.                                                                                                                          |
| It is a stateful means that any changes made in the inbound rule will be automatically reflected in the outbound rule. For example, If you are allowing an incoming port 80, then you als- have to add the outbound rule explicitly. | It is a stateless means that any changes made in the inbound rule will not reflect the outbound rule, i.e., you need to add the outbound rule separately. For example, if you add an inbound rule port number 80, then you als- have to explicitly add the outbound rule. |
| It is associated with an EC2 instance.                                                                                                                                                                                               | It is associated with a subnet.                                                                                                                                                                                                                                           |
| All the rules are evaluated before deciding whether to allow the traffic.                                                                                                                                                            | Rules are evaluated in order, starting from the lowest number.                                                                                                                                                                                                            |
| Security Group is applied to an instance only when you specify a security group while launching an instance.                                                                                                                         | NACL has applied automatically to all the instances which are associated with an instance.                                                                                                                                                                                |
| It is the first layer of defense.                                                                                                                                                                                                    | It is the second layer of defense.                                                                                                                                                                                                                                        |

</blockquote>

</details>

---

28. What are the two- types of access that you can provide when you are creating users?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- There are two- types of access:
  - Console Access
    If the user wants to use the Console Access, a user needs to create a password to login in an AWS account.
  - Programmatic access
    If you use the Programmatic access, an IAM user need to make an API calls. An API call can be made by using the AWS CLI. To use the AWS CLI, you need to create an access key ID and secret access key.

</blockquote>

</details>

---

29. What is subnet?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- When large section of IP address is divided into smaller units is known as subnet.
![Subnet](https://user-images.githubusercontent.com/110088496/194527648-c1ac304a-84c0-457f-8940-f581216d9c97.png)
- A Virtual Private Cloud (VPC) is a virtual network provided to your AWS account. When you create a virtual cloud, you need to specify the IPv4 addresses which is in the form of CIDR block. After creating a VPC, you need to create the subnets in each availability zone. Each subnet has a unique ID. When launching instances in each availability zone, it will protect your applications from the failure of a single location.

</blockquote>

</details>

---

30. Differences between Amazon S3 and EC2?

![Easy](<https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg>)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- S3
  - It is a storage service where it can store any amount of data.
  - It consists of a REST interface and uses secure HMAC-SHA1 authentication keys.
- EC2
  - It is a web service used for hosting an application.
  - It is a virtual machine which can run either Linux or Windows and can als- run the applications such as PHP, Python, Apache or other databases.

</blockquote>

</details>

---
