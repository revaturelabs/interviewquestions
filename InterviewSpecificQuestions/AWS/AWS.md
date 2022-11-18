1.Brief AWS in short?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- AWS stands for Amazon Web Services.It is an Amazon product which is used to manage distributed IT infrastructure.
 It provides different services such as 
    - infrastructure as a service
    - platform as a service
    - software as a service.



</blockquote  markdown="1">

</details markdown="1">

------


2.Can you brief a few components of AWS?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Yes, a few components of AWS are:
	Simple Storage Service (S3) : S3 is a service of aws that stores files.
	Elastic Compute Cloud: Elastic Compute Cloud is a web service that provides resizable compute capacity in the cloud.
	Elastic Beans Talk: It provides services to deploy a different application which is available in different platforms or languages like java, nodejs etc..


</blockquote  markdown="1">

</details markdown="1">

------


3.Can you explain the Key-pairs in detail?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- AWS uses public key cryptography to encrypt and decrypt the login information.In public key cryptography, the public key is used to encrypt the information on the receiver's side, a private key is used to decrypt the information.The combination of a public key and the private key is known as a key-pairs.Key pairs allow you to access the instances securely.


</blockquote  markdown="1">

</details markdown="1">

------


4.In general, S3 service can have how many buckets?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- By default, you can create up to 100 buckets.


</blockquote  markdown="1">

</details markdown="1">

------


5.How will you explain the term “Cross Region Replication”?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Cross Region Replication is a service available in aws that enables to replicate of the data from one bucket to another bucket which could be in the same or different region.It provides asynchronous copying of objects, i.e., objects are not copied immediately.


</blockquote  markdown="1">

</details markdown="1">

------


6.What is the meaning of Regions and Zones in aws?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Regions: A region is a geographical area which consists of 2 or more availability zones.A region is a collection of data centres which are completely isolated from other regions.
- Availability zones: An Availability zone is a data centre that can be somewhere in the country or city.Data centres can have multiple servers, switches, firewalls, and load balancing.The things through which you can interact with the cloud reside inside the Datacenter.
 

</blockquote  markdown="1">

</details markdown="1">

------


7.Can you predict the minimum and maximum size S3 bucket?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- The minimum size of an object that you can store in S3 is 0 bytes and the maximum size of an object that you can store in S3 is 5 TB.
 
 
</blockquote  markdown="1">

</details markdown="1">

------


8.Can you define Auto Scaling and its advantages?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Auto Scaling is a feature in AWS that automatically scales the capacity to maintain steady and predictable performance.

Advantages of Auto Scaling
- 	Setup Scaling Quickly
It sets the target utilization levels of multiple resources in a single interface.You can see the average utilization level of multiple resources in the same console, i.e., you do not have to move to a different console.
- 	Make Smart Scaling Decisions
It makes the scaling plans that automate how different resources respond to the changes.It optimizes availability and cost.It automatically creates the scaling policies and sets the targets based on your preference.It also monitors your application and automatically adds or removes the capacity based on the requirements.
- 	Automatically maintain performance
Auto Scaling automatically optimizes the application performance and availability even when the workloads are unpredictable.It continuously monitors your application to maintain the desired performance level.When demand rises, then Auto Scaling automatically scales the resources.

 
</blockquote  markdown="1">

</details markdown="1">

------


9.Can you explain AMI?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- AMI stands for Amazon Machine Image.It is a virtual image used to create a virtual machine within an EC2 instance.

 
</blockquote  markdown="1">

</details markdown="1">

------


10.Can you make AMI shareable?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Yes, an AMI can be shared.

 
</blockquote  markdown="1">

</details markdown="1">

------


11.Can you explain some security models in the S3 bucket?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- S3 bucket can be secured in two ways:
-	ACL (Access Control List)
ACL is used to manage the access of resources to buckets and objects.An object of each bucket is associated with ACL.It defines which AWS accounts have granted access and the type of access.When a user sends the request for a resource, then its corresponding ACL will be checked to verify whether the user has granted access to the resource or not.When you create a bucket, then Amazon S3 creates a default ACL which provides full control over the AWS resources.
-	Bucket Policies
Bucket policies are only applied to S3 buckets.Bucket policies define what actions are allowed or denied.Bucket policies are attached to the bucket, not to an S3 object but the permissions defined in the bucket policy are applied to all the objects in the S3 bucket.


</blockquote  markdown="1">

</details markdown="1">

------


12.Why do you use policies in AWS and how many types of policies are in AWS?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- The policy is an object which is associated with a resource that defines the permissions.AWS evaluate these policies when the user makes a request.Permissions in the policy determine whether to allow or deny an action.Policies are stored in the form of JSON documents.

AWS supports six types of policies:
- 	Identity-based policies
-	Resource-based policies
-	Permissions boundaries
-	Organizations SCPs
-	Access Control Lists
-	Session policies


</blockquote  markdown="1">

</details markdown="1">

------


13.Can you guess the default storage class in S3?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- The default storage class is Standard Frequently Accessed.


</blockquote  markdown="1">

</details markdown="1">

------


14.How do you differentiate the terms, stopping the instances and terminating the instances?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Stopping: You can stop an EC2 instance and stopping an instance means shutting down the instance.Its corresponding EBS volume is still attached to an EC2 instance, so you can restart the instance as well.

- Terminating: You can also terminate the EC2 instance and terminating an instance means you are removing the instance from your AWS account.When you terminate an instance, then its corresponding EBS is also removed.Due to this reason, you cannot restart the EC2 instance.


</blockquote  markdown="1">

</details markdown="1">

------


15.How many Elastic IPs can you create?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- 5 elastic IP addresses that you can create per AWS account per region.


</blockquote  markdown="1">

</details markdown="1">

------


16.Do you have any idea about the Load Balancer?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- A load Balancer is a virtual machine that balances your web application load which could be Http or Https traffic that you are getting in.It balances a load of multiple servers so that no web server gets overwhelmed.


</blockquote  markdown="1">

</details markdown="1">

------


17.Can you explain a few RDS types?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Yes, few are here:
    -	Amazon Aurora
    -	Postgre SQL
    -	MySQL
    -	MariaDB
    -	Oracle
    -	SQL Server


</blockquote  markdown="1">

</details markdown="1">

------


18.Have you listened to routing policies in route53?  if yes then can you explain some?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- Yes, a few are given below:
    -	Simple Routing Policy
Simple Routing Policy is a simple round-robin policy which is applied to a single resource doing the function for the domain, for example, the web server is sending the content to a website where the web server is a single resource.

    - 	Weighted Routing Policy
A weighted Routing Policy allows you to route the traffic to different resources in specified proportions.For example, 75% in one server, and 25% in another server.Weights can be assigned in the range of 0 to 255.Weight Routing policy is applied when there are multiple resources accessing the same function.For example, web servers accessing the same website.Each web server will be given a unique weight number.

    - 	Latency-based Routing Policy
Latent-based Routing Policy allows Route53 to respond to the DNS query at which the data centre gives the lowest latency.

    -	Failover Routing Policy
    -	Geolocation Routing Policy etc.


</blockquote  markdown="1">

</details markdown="1">

------


19.While creating users, can you explain the access type?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
<summary> <b>Explanation</b> </summary>

<blockquote markdown="1">

- There are two types of access:
    - 	Console Access
If the user wants to use the Console Access, a user needs to create a password to login into an AWS account.

    - 	Programmatic access
If you use the Programmatic access, an IAM user needs to make API calls.An API call can be made by using the AWS CLI.To use the AWS CLI, you need to create an access key ID and secret access key.

</blockquote  markdown="1">

</details markdown="1">

------
