1. Brief AWS in short?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud, offering over 200 fully featured services from data centers globally. Millions of customers—including the fastest-growing startups, largest enterprises, and leading government agencies—are using AWS to lower costs, become more agile, and innovate faster.
It provides those services as :

### Infrastructure as a Service (IaaS)

- **Infrastructure as a Service (IaaS)** is a self-service model for managing remote data center infrastructures. AWS offers IaaS in the form of data centers.
  - **Example** : Amazon Web Services, Microsoft Azure, and Google Compute Engine

### Platform as a Service (PaaS)

- **Platform as a Service (PaaS)** allows organizations to build, run and manage applications without the IT infrastructure. This makes it easier and faster to develop, test and deploy applications.
  - **Example** : AWS Elastic Beanstalk, Google App Engine,

### Software as a Service (SaaS)

- **Software as a service (SaaS)** replaces the traditional on-device software with software that is licensed on a subscription basis. It is centrally hosted in the cloud. A good example is Salesforce.com.
  - **Example** : Gmail, Slack, and Microsoft Office 365



</blockquote>

</details>

------


2. Can you brief a few components of AWS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

AWS provides over 200 fully featured services from data centers to millions of customers globally.
Some of the AWS services that I have used are as follows

- **Simple Storage Service (S3) :** Amazon S3, at its core, facilitates object storage, providing leading scalability, data availability, security, and performance. Businesses of vast sizes can leverage S3 for storage and protect large sums of data for various use cases, such as websites, applications, backup, and more.
- **Elastic Compute Cloud (EC2) :** Elastic Compute Cloud is a web service that provides resizable compute capacity in the cloud.
- **Elastic Beanstalk :** It provides services to deploy a different application which is available in different platforms or languages like java, nodejs etc.
- **Relational Database Service (Amazon RDS) :** is a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud. Choose from seven popular engines — Amazon Aurora with MySQL compatibility, Amazon Aurora with PostgreSQL compatibility, MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server — and deploy on-premises with Amazon RDS on AWS Outposts.


</blockquote>

</details>

------


3. Can you explain the Key-pairs in detail?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- A key pair, consisting of a public key and a private key, is a set of security credentials that you use to prove your identity when connecting to an Amazon EC2 instance.
Amazon EC2 stores the public key on your instance, and you store the private key.
Anyone who possesses your private key can connect to your instances, so it's important that you store your private key in a secure place.

When you launch an instance, you can specify a key pair. If you plan to connect to the instance using SSH, you must specify a key pair. You can choose an existing key pair or create a new one.


</blockquote>

</details>

------


4. In general, S3 service can have how many buckets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- By default, you can create up to 100 buckets.


</blockquote>

</details>

------


5. How will you explain the term “Cross Region Replication”?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- Amazon S3 supports cross-region replication (CRR), a feature that automatically replicates data across AWS regions.
Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets.
With cross-region replication, every object uploaded to an S3 bucket is automatically replicated to a destination bucket in a different AWS region that you choose.
For example, you can use cross-region replication to provide lower-latency data access in different geographic regions.
Cross-region replication can also help if you have a compliance requirement to store copies of data hundreds of miles apart. There is no additional charge for using cross-region replication.
You pay Amazon S3’s usual charges for storage, requests, and inter-region data transfer for the replicated copy of data.


</blockquote>

</details>

------


6. What is the meaning of Regions and Zones in aws?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

**Availability Zone (AZ) :** An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. AZs give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center. All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. All traffic between AZs is encrypted. The network performance is sufficient to accomplish synchronous replication between AZs.

**Regions :** AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS Region offers advantages for customers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

**Edge Locations :** Edge locations are AWS data centers designed to deliver services with the lowest latency possible. Amazon has dozens of these data centers spread across the world. They’re closer to users than Regions or Availability Zones, often in major cities, so responses can be fast and snappy.
 

</blockquote>

</details>

------


7. Can you predict the minimum and maximum size S3 bucket?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- The minimum size of an object that you can store in S3 is 0 bytes and the maximum size of an object that you can store in S3 is 5 TB.
 
 
</blockquote>

</details>

------


8. Can you define Auto Scaling and its advantages?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes. The service provides a simple, powerful user interface that lets you build scaling plans for resources including Amazon EC2 instances. AWS Auto Scaling makes scaling simple with recommendations that allow you to optimize performance, costs, or balance between them.
Advantages of Auto Scaling
**SETUP SCALING QUICKLY**
- AWS Auto Scaling lets you set target utilization levels for multiple resources in a single, intuitive interface. You can quickly see the average utilization of all of your scalable resources without having to navigate to other consoles. For example, if your application uses Amazon EC2 and Amazon DynamoDB, you can use AWS Auto Scaling to manage resource provisioning for all of the EC2 Auto Scaling groups and database tables in your application.
**MAKE SMART SCALING DECISIONS**
- AWS Auto Scaling lets you build scaling plans that automate how groups of different resources respond to changes in demand. You can optimize availability, costs, or a balance of both.
**AUTOMATICALLY MAINTAIN PERFORMANCE**
- Using AWS Auto Scaling, you maintain optimal application performance and availability, even when workloads are periodic, unpredictable, or continuously changing. AWS Auto Scaling continually monitors your applications to make sure that they are operating at your desired performance levels. When demand spikes, AWS Auto Scaling automatically increases the capacity of constrained resources so you maintain a high quality of service.
**PAY ONLY FOR WHAT YOU NEED**
- AWS Auto Scaling can help you optimize your utilization and cost efficiencies when consuming AWS services so you only pay for the resources you actually need. When demand drops, AWS Auto Scaling will automatically remove any excess resource capacity so you avoid overspending. AWS Auto Scaling is free to use, and allows you to optimize the costs of your AWS environment.

 
</blockquote>

</details>

------


9. Can you explain AMI?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

AMI stands for Amazon Machine Image.It is a virtual image used to create a virtual machine within an EC2 instance.
An Amazon Machine Image (AMI) is a supported and maintained image provided by AWS that provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you require multiple instances with the same configuration. You can use different AMIs to launch instances when you require instances with different configurations.

An AMI includes the following:

- One or more Amazon Elastic Block Store (Amazon EBS) snapshots, or, for instance-store-backed AMIs, a template for the root volume of the instance (for example, an operating system, an application server, and applications).

- Launch permissions that control which AWS accounts can use the AMI to launch instances.

- A block device mapping that specifies the volumes to attach to the instance when it's launched.

 
</blockquote>

</details>

------


10. Can you make AMI shareable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- Yes, an AMI can be shared.

 
</blockquote>

</details>

------


11. Can you explain some security models in the S3 bucket?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- S3 bucket can be secured in two ways:
-	ACL (Access Control List)
ACL is used to manage the access of resources to buckets and objects. An object of each bucket is associated with ACL. It defines which AWS accounts have granted access and the type of access. When a user sends the request for a resource, then its corresponding ACL will be checked to verify whether the user has granted access to the resource or not. When you create a bucket, then Amazon S3 creates a default ACL which provides full control over the AWS resources.
-	Bucket Policies
Bucket policies are only applied to S3 buckets. Bucket policies define what actions are allowed or denied. Bucket policies are attached to the bucket, not to an S3 object but the permissions defined in the bucket policy are applied to all the objects in the S3 bucket.


</blockquote>

</details>

------


12. Why do you use policies in AWS and how many types of policies are in AWS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

The policy is an object which is associated with a resource that defines the permissions.AWS evaluate these policies when the user makes a request.Permissions in the policy determine whether to allow or deny an action.Policies are stored in the form of JSON documents.
The following policy types, listed in order from most frequently used to less frequently used, are available for use in AWS. 

- **Identity-based policies –** Attach managed and inline policies to IAM identities (users, groups to which users belong, or roles). Identity-based policies grant permissions to an identity.

- **Resource-based policies –** Attach inline policies to resources. The most common examples of resource-based policies are Amazon S3 bucket policies and IAM role trust policies. Resource-based policies grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts.

- **Permissions boundaries –** Use a managed policy as the permissions boundary for an IAM entity (user or role). That policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions. Permissions boundaries do not define the maximum permissions that a resource-based policy can grant to an entity.

- **Organizations SCPs –** Use an AWS Organizations service control policy (SCP) to define the maximum permissions for account members of an organization or organizational unit (OU). SCPs limit permissions that identity-based policies or resource-based policies grant to entities (users or roles) within the account, but do not grant permissions.

- **Access control lists (ACLs) –** Use ACLs to control which principals in other accounts can access the resource to which the ACL is attached. ACLs are similar to resource-based policies, although they are the only policy type that does not use the JSON policy document structure. ACLs are cross-account permissions policies that grant permissions to the specified principal. ACLs cannot grant permissions to entities within the same account.

- **Session policies –** Pass advanced session policies when you use the AWS CLI or AWS API to assume a role or a federated user. Session policies limit the permissions that the role or user's identity-based policies grant to the session. Session policies limit permissions for a created session, but do not grant permissions. For more information, see Session Policies.


</blockquote>

</details>

------


13. Can you guess the default storage class in S3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

Each object in Amazon S3 has a storage class associated with it. For example, if you list the objects in an S3 bucket, the console shows the storage class for all the objects in the list. Amazon S3 offers a range of storage classes for the objects that you store. You choose a class depending on your use case scenario and performance access requirements. All of these storage classes offer high durability.

### Storage classes for frequently accessed objects
For performance-sensitive use cases (those that require millisecond access time) and frequently accessed data, Amazon S3 provides the following storage classes:

- **S3 Standard –** The default storage class. If you don't specify the storage class when you upload an object, Amazon S3 assigns the S3 Standard storage class.

- **Reduced Redundancy –** The Reduced Redundancy Storage (RRS) storage class is designed for noncritical, reproducible data that can be stored with less redundancy than the S3 Standard storage class.

### Storage class for automatically optimizing data with changing or unknown access patterns
- **S3 Intelligent-Tiering** is an Amazon S3 storage class that's designed to optimize storage costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead. S3 Intelligent-Tiering is the only cloud storage class that delivers automatic cost savings by moving data on a granular object level between access tiers when access patterns change. S3 Intelligent-Tiering is the ideal storage class when you want to optimize storage costs for data that has unknown or changing access patterns. 

### Storage classes for infrequently accessed objects
- The **S3 Standard-IA** and **S3 One Zone-IA** storage classes are designed for long-lived and infrequently accessed data. *(IA stands for infrequent access.)* S3 Standard-IA and S3 One Zone-IA objects are available for millisecond access (similar to the S3 Standard storage class). Amazon S3 charges a retrieval fee for these objects, so they are most suitable for infrequently accessed data.

### Storage classes for archiving objects
- The **S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval, and S3 Glacier Deep Archive** storage classes are designed for low-cost data archiving. These storage classes offer the same durability and resiliency as the S3 Standard and S3 Standard-IA storage classes


</blockquote>

</details>

------


14. How do you differentiate the terms, stopping the instances and terminating the instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- Stopping: You can stop an EC2 instance and stopping an instance means shutting down the instance. Its corresponding EBS volume is still attached to an EC2 instance, so you can restart the instance as well.

- Terminating: You can also terminate the EC2 instance and terminating an instance means you are removing the instance from your AWS account. When you terminate an instance, then its corresponding EBS is also removed. Due to this reason, you cannot restart the EC2 instance.


</blockquote>

</details>

------


15. How many Elastic IPs can you create?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- 5 elastic IP addresses that you can create per AWS account per region.


</blockquote>

</details>

------


16. Do you have any idea about the Load Balancer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- A load Balancer is a virtual machine that balances your web application load which could be Http or Https traffic that you are getting in. It balances a load of multiple servers so that no web server gets overwhelmed.


</blockquote>

</details>

------


17. Can you explain a few RDS types?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- Yes, few are here:
    -	Amazon Aurora
    -	Postgre SQL
    -	MySQL
    -	MariaDB
    -	Oracle
    -	SQL Server


</blockquote>

</details>

------


18. Have you listened to routing policies in route53?  if yes then can you explain some?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- Yes, a few are given below:
    -	Simple Routing Policy
Simple Routing Policy is a simple round-robin policy which is applied to a single resource doing the function for the domain, for example, the web server is sending the content to a website where the web server is a single resource.

    - 	Weighted Routing Policy
A weighted Routing Policy allows you to route the traffic to different resources in specified proportions. For example, 75% in one server, and 25% in another server. Weights can be assigned in the range of 0 to 255. Weight Routing policy is applied when there are multiple resources accessing the same function. For example, web servers accessing the same website. Each web server will be given a unique weight number.

    - 	Latency-based Routing Policy
Latent-based Routing Policy allows Route53 to respond to the DNS query at which the data centre gives the lowest latency.

    -	Failover Routing Policy
    -	Geolocation Routing Policy etc.


</blockquote>

</details>

------


19. While creating users, can you explain the access type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Explanation</b> </summary>

<blockquote>

- There are two types of access:
    - 	Console Access
If the user wants to use the Console Access, a user needs to create a password to login into an AWS account.

    - 	Programmatic access
If you use the Programmatic access, an IAM user needs to make API calls. An API call can be made by using the AWS CLI. To use the AWS CLI, you need to create an access key ID and secret access key.

</blockquote>

</details>

------
