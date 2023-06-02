## Technical

1. What is EC2?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

EC2 is a web service provided by AWS that allows you to launch and manage virtual servers in the cloud. It provides scalable compute capacity to run applications and offers various instance types to suit different workloads.

</blockquote>
</details>

---

2. What is an instance in EC2?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An instance in EC2 refers to a virtual server that you can launch and run in the AWS cloud. It has its own operating system, storage, and networking capabilities. Instances are the basic building blocks of EC2.

</blockquote>
</details>

---

3. How do you choose the right EC2 instance type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Choosing the right instance type depends on factors like your application's resource requirements, performance needs, and cost considerations. AWS offers a variety of instance types optimized for different use cases, such as general-purpose, memory-intensive, or GPU-accelerated workloads.

</blockquote>
</details>

---

4. How do you access an EC2 instance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can access an EC2 instance using Secure Shell (SSH) for Linux instances or Remote Desktop Protocol (RDP) for Windows instances. You need the appropriate credentials (SSH key pair or administrator password) to establish a remote connection.

</blockquote>
</details>

---

5. What is an Amazon Machine Image (AMI)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An Amazon Machine Image (AMI) is a template that contains the necessary information to launch an EC2 instance. It includes the operating system, software packages, and configuration settings required for the instance.

</blockquote>
</details>

---

6. How can you scale EC2 instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can scale EC2 instances manually or automatically. Manual scaling involves launching or terminating instances based on demand. Automatic scaling can be achieved using services like AWS Auto Scaling, which adjusts the number of instances based on predefined scaling policies.

</blockquote>
</details>

---

7. How do you store data on an EC2 instance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

EC2 instances provide storage options like Amazon Elastic Block Store (EBS) and instance store. EBS volumes are network-attached storage that can be attached to EC2 instances, while instance store volumes are physically attached disks on the host server.

</blockquote>
</details>

---

8. Is it possible to use EC2 for high-performance computing (HPC) workloads?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Yes, EC2 offers instance types specifically optimized for high-performance computing (HPC). These instances provide enhanced networking capabilities, powerful processors, and high-speed storage options for demanding computational workloads.

</blockquote>
</details>

---

9. How can you secure your EC2 instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can secure EC2 instances by implementing security best practices such as using security groups to control inbound and outbound traffic, utilizing network access control lists (ACLs), enabling encryption for data at rest and in transit, and regularly updating and patching your instances.

</blockquote>
</details>

---

10. What is the difference between on-demand and spot instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

On-demand instances are charged at a fixed rate per hour, while spot instances allow you to bid on unused EC2 capacity and can result in significant cost savings. However, spot instances can be interrupted with a two-minute notice if the spot price exceeds your bid.

</blockquote>
</details>

---

11. How do you launch an EC2 instance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

To launch an EC2 instance, you need to select an AMI, choose an instance type, configure instance details such as network settings and storage, set up security groups, and launch the instance. You can use the AWS Management Console, AWS CLI, or SDKs to launch an EC2 instance.

</blockquote>
</details>

---

12. What is the difference between reserved instances and on-demand instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Reserved instances provide a significant discount compared to on-demand instances in exchange for a commitment of usage over a specific term, typically one to three years. On-demand instances, on the other hand, have no upfront commitments and are charged at the regular hourly rate.

</blockquote>
</details>

---

13. How can you share data between EC2 instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can share data between EC2 instances using various methods. This includes transferring files over SSH, using network file sharing protocols like NFS or SMB, setting up a shared storage solution like Amazon EFS, or utilizing AWS storage services like S3 for data exchange.

</blockquote>
</details>

---

14. What is an EC2 key pair?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 key pair consists of a public key and a private key. It is used for securely connecting to Linux instances via SSH. The private key is stored locally on your computer, while the public key is placed on the EC2 instance during its creation.

</blockquote>
</details>

---

15. Is it possible to change the instance type of a running EC2 instance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

No, you cannot change the instance type of a running EC2 instance. However, you can stop the instance, change its instance type, and then start it again with the new instance type.

</blockquote>
</details>

---

16. What is the difference between an EC2 instance store and Amazon EBS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 instance store provides temporary block-level storage that is physically attached to the host server. The data on an instance store volume is lost if the instance is stopped or terminated. Amazon Elastic Block Store (EBS), on the other hand, offers persistent block storage that can be attached to EC2 instances and retains data even if the instance is stopped or terminated.

</blockquote>
</details>

---

17. How can you monitor the performance of your EC2 instances?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

AWS provides CloudWatch, a monitoring service that collects and tracks metrics for EC2 instances. You can view metrics such as CPU utilization, network traffic, and disk performance. Additionally, you can set up alarms to notify you when certain thresholds are exceeded.

</blockquote>
</details>

---

18. What is an EC2 placement group?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 placement group is a logical grouping of instances within a single Availability Zone. It allows you to influence the placement of instances to achieve low-latency network performance or meet specific hardware requirements.

</blockquote>
</details>

---

19. Is it possible to use EC2 instances in a virtual private cloud (VPC)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Yes, EC2 instances are typically launched within a VPC. A VPC provides a virtual network in the AWS cloud, allowing you to isolate your EC2 instances and control their networking environment, including IP addressing, subnets, and security settings.

</blockquote>
</details>

---

20. What is the difference between a public IP address and an elastic IP address?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

A public IP address is assigned to an EC2 instance by default at launch and can change if the instance is stopped and started. An elastic IP address, on the other hand, is a static, public IP address that you can allocate to your AWS account and associate with an EC2 instance. It remains fixed until you release it.

</blockquote>
</details>

---

21. How does EC2 Auto Scaling work?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

EC2 Auto Scaling automatically adjusts the number of EC2 instances in a fleet based on predefined scaling policies. It uses Amazon CloudWatch alarms to monitor resource utilization metrics and launches or terminates instances to maintain desired capacity levels. This helps ensure optimal performance and cost-efficiency.

</blockquote>
</details>

---

22. What are EC2 instance metadata and user data?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

EC2 instance metadata provides information about an instance, such as instance ID, instance type, and public IP address. User data is a script or data that can be passed to an EC2 instance at launch. It can be used to perform instance configuration, install software, or execute custom initialization tasks.

</blockquote>
</details>

---

23. How do you share an Amazon EBS volume between multiple EC2 instances?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

To share an Amazon EBS volume between multiple EC2 instances, you can create the EBS volume and attach it to one instance. Then, you can detach it from that instance and attach it to another instance. However, simultaneous read/write access to the same EBS volume from multiple instances is not possible.

</blockquote>
</details>

---

24. What is an EC2 dedicated host?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 dedicated host is a physical server dedicated to a single AWS account. When you launch instances on a dedicated host, the instances run on the isolated hardware of the host. Dedicated hosts are useful when you have specific licensing requirements, need instance placement control, or want to meet compliance or regulatory needs.

</blockquote>
</details>

---

25. How can you achieve high availability for your EC2 instances?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can achieve high availability for EC2 instances by distributing them across multiple Availability Zones (AZs) within a region. By using an Auto Scaling group, you can automatically launch instances in different AZs, and if one AZ experiences an issue, the instances in the other AZs continue to serve traffic.

</blockquote>
</details>

---

26. What is Amazon EFS, and how does it differ from EBS?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Amazon EFS (Elastic File System) is a scalable file storage service provided by AWS. It provides shared file storage across multiple EC2 instances and supports concurrent access. In contrast, Amazon EBS (Elastic Block Store) provides block-level storage volumes that can be attached to EC2 instances, offering persistent and low-latency storage.

</blockquote>
</details>

---

27. How can you secure your EC2 instances at the network level?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

You can secure EC2 instances at the network level by using security groups and network ACLs. Security groups act as virtual firewalls, controlling inbound and outbound traffic at the instance level. Network ACLs operate at the subnet level, filtering traffic between subnets, and provide an additional layer of control.

</blockquote>
</details>

---

28. What are EC2 instance types optimized for GPU workloads?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote> 

AWS offers EC2 instance types optimized for GPU workloads, such as the P3, G4, and G3 instance families. These instances are equipped with powerful GPUs and are suitable for tasks like machine learning, video encoding, 3D rendering, and scientific simulations.

</blockquote>
</details>

---

29. How can you migrate your on-premises servers to EC2 instances?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

AWS provides several migration services like AWS Server Migration Service (SMS), AWS Database Migration Service (DMS), and the AWS Application Discovery Service to assist with migrating on-premises servers to EC2 instances. These services help streamline the process of replicating and transitioning workloads to the cloud.

</blockquote>
</details>

---

30. What is the difference between stopping and terminating the instances?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Stopping: You can stop an EC2 instance and stopping an instance means shutting down the instance. Its corresponding EBS volume is still attached to an EC2 instance, so you can restart the instance as well.

- Terminating: You can also terminate the EC2 instance and terminating an instance means you are removing the instance from your AWS account. When you terminate an instance, then its corresponding EBS is also removed. Due to this reason, you cannot restart the EC2 instance.


</blockquote>
</details>

---

31. How many Elastic IPs can you create?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- 5 elastic IP addresses that you can create per AWS account per region.


</blockquote>
</details>

---

32. What is an EC2 instance profile, and how is it different from IAM roles?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 instance profile is a container for an IAM role that can be assigned to an EC2 instance. It allows applications running on the instance to access AWS resources securely without the need to embed and manage AWS credentials. An IAM role, on the other hand, is a set of permissions that determine what actions can be performed on AWS resources.

</blockquote>
</details>

---

33. How can you achieve cross-region replication for your EC2 instances?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

To achieve cross-region replication for EC2 instances, you can use services like AWS Database Migration Service (DMS) or AWS Server Migration Service (SMS) to replicate the data and configurations of your instances to another region. You can then launch instances in the target region using the replicated data.

</blockquote>
</details>

---

34. What is the purpose of an EC2 fleet?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

An EC2 fleet is a combination of EC2 instances with defined capacity settings, instance types, and purchase options. It allows you to specify the required capacity, flexibility, and cost structure for launching instances. EC2 fleets simplify the management of instance launches by automating the selection of optimal instances based on your requirements.

</blockquote>
</details>

---

35. How does Amazon EC2 Spot Instances work, and what are the best use cases for them?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Amazon EC2 Spot Instances allow you to bid on unused EC2 capacity and can result in significant cost savings compared to on-demand instances. Spot Instances are allocated to the highest bidders until the Spot price exceeds their bid. Spot Instances are suitable for fault-tolerant workloads, batch processing, and other applications that can handle interruptions or have flexible start and end times.

</blockquote>
</details>

---

36. What are EC2 instance hibernation and instance store hibernation?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

EC2 instance hibernation is a feature that allows you to pause and resume EC2 instances. When an instance is hibernated, its in-memory state is saved to persistent storage (Amazon EBS) and can be restored when the instance is resumed. Instance store hibernation, on the other hand, refers to the ability to hibernate instances that use instance store volumes, preserving their data across instance restarts.

</blockquote>
</details>

---

37. Is it possible to attach more than one Elastic IP address to an EC2 instance?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Yes, you can attach multiple Elastic IP addresses to an EC2 instance, as long as you do not exceed the default limit or request a higher limit from AWS. However, it is recommended to use Elastic IP addresses judiciously and consider alternative approaches, such as DNS aliases or load balancers, to handle traffic distribution.

</blockquote>
</details>

---

38. What is the difference between Amazon EC2 dedicated instances and dedicated hosts?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Amazon EC2 dedicated instances are EC2 instances that run on single-tenant hardware, ensuring that the underlying physical host is dedicated to your account. Dedicated instances provide isolation and compliance benefits. Dedicated hosts, on the other hand, provide physical servers dedicated exclusively to your account and offer complete control over the host's placement, enabling you to use your existing server-bound software licenses.

</blockquote>
</details>

---

39. How can you achieve secure communication between EC2 instances located in different VPCs?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

To achieve secure communication between EC2 instances in different VPCs, you can set up VPC peering. VPC peering establishes a private network connection between VPCs, allowing instances to communicate using private IP addresses across VPC boundaries. You can also use VPN connections or AWS Direct Connect for secure communication between VPCs.

</blockquote>
</details>

---