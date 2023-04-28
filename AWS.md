1. What is EC2, RDS and S3?


<details><summary><b>Show Answer</b></summary>

<blockquote>

These are the Services provided by AWS.

**EC2:** EC2 stands for Elastic cloud compute, EC2 instance is a virtual machine provided by AWS for compute.

**RDS:** RDS stands for Relational Database System. It is used to host SQL databases like MySQL, PostgreSQL, and Oracle SQL etc.

**S3:** S3 stands for Simple Storage Service. It is an object storing service.

</blockquote>

</details>



2. If a database in one region went down what is your plan? 

<details><summary><b>Show Answer</b></summary>

<blockquote>

When a DB Instance is created for production, Multi-AZ(Multiple Availability Zone) option is opted. So, even when the primary database goes down in one zone, AWS will automatically fallback to the backup replica created in another zone. Region are and wildely spread grographic locations and Availability Zones are distinct regions in Regions. Its highly Impropable that the entire region goes down at once, normally a specific Availability zone goes down and the fallback zone is available.

</blockquote>

</details>


3. What is a VPC? 
   
<details><summary><b>Show Answer</b></summary>

<blockquote>

Virtual Private Network (VPC) is used to lauch the AWS resources in an isolated  virtual network. It is similar to the traditional network in a data center. Every VPC can contain subnests. subnets are specific to the availability zone. subnets are nothing but a range of ip addresses in the VPC.



</blockquote>

</details>

4. What is AWS?

<details><summary><b>Show Answer</b></summary>

<blockquote>

AWS (Amazon Web Services) is a cloud computing platform offered by Amazon. It provides a wide range of services such as computing power, storage, database, analytics, machine learning, and more, all of which can be accessed over the internet. 



</blockquote>

</details>

5. how do you configure an S3 bucket ?

<details><summary><b>Show Answer</b></summary>

<blockquote>

S3(Simple Storage Service) contains resources like buckets and objects.

Bucket: A container of objects.
Object: A file and any metadata that describes the files.

The following steps are used to configure the bucket:

1. Login to the AWS Management Console and navigate to the S3 service.
2. Click the "Create bucket" button to create a new bucket.
3. Choose a globally unique name for your bucket.
4. Select a region where you want to create your bucket.
5. Choose the properties that you want to apply to your bucket, such as versioning, encryption, logging, and so on.
6. Set the permissions that control who can access your bucket and the objects stored in it.
7. Review your settings and create your bucket.



</blockquote>

</details>

6. How to implement pipeline using EC2 ?

<details><summary><b>Show Answer</b></summary>

<blockquote>

Steps to implement the pipeline in EC2:

1. A CI/CD pipeline can be setup using the GitHub and Jenkins in EC2.

- Create an EC2 Instance
- Install Git, Jenkins and Docker in EC2
- Create a jenkins account and create a job.
- Create a webhook in GitHub for the jenkins in EC2.
- Create a jenkinsfile with stages to implement the CI/CD pipeline


Other options include:
1. CodeBuild, CodeDeploy and CodePipeline can be used to build a CI/CD pipeline for projects hosted in EC2.
2. Even Github actions and GitLabs CI/CD can be used to setup the CI/CD pipeline.



</blockquote>

</details>

7. What is Cloud Computing ?

<details><summary><b>Show Answer</b></summary>

<blockquote>





</blockquote>

</details>

8. What are the services provided by Cloud?

<details><summary><b>Show Answer</b></summary>

<blockquote>



</blockquote>

</details>

9. Are your databases on the cloud protected, private, or private protected? 

<details><summary><b>Show Answer</b></summary>

<blockquote>



</blockquote>

</details>

10. What is CloudFront?

<details><summary><b>Show Answer</b></summary>

<blockquote>

</blockquote>

</details>

<details><summary><b>Show Answer</b></summary>

<blockquote>

</blockquote>

</details>

<details><summary><b>Show Answer</b></summary>

<blockquote>

</blockquote>

</details>
