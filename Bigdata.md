## Interview Question

1. What will you do if NameNode is unavailable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To get the Hadoop cluster up and running, the NameNode recovery method used the following steps:

- To create a new NameNode, use the file system metadata replica (FsImage).

- Then, configure the DataNodes and clients so that they can recognise the newly created NameNode.

- After the new NameNode has finished loading the last checkpoint Fuselage (for metadata information) and received enough block reports from the DataNodes, it will begin serving the client.


</details>

</blockquote>

---

2. Will Spark overtake Hadoop? Will Hadoop be replaced by Spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- It depends on how we use "Hadoop". For some purpose we use the Hadoop whole ecosystem (HDFS, Hive, MapReduce, etc), in which case Spark is designed to fit well within the ecosystem (reading from any input source that MapReduce supports through the InputFormat interface, being compatible with Hive and YARN, etc). Others refer to Hadoop MapReduce in particular, in which case I think it's very likely that non-MapReduce engines will take over in a lot of domains, and in many cases they already have.

- Another point of view, perhaps the most interesting thing about Spark is that it shows that a lot of workloads can be captured efficiently by the same, simple generalization of the MapReduce model. Spark can achieve (and sometimes beat) state-of-the-art performance in not only simple ETL, but also machine learning, graph processing, streaming, and relational queries. Importantly, this means that applications can combine these workloads more efficiently. For example, once you ETL data in, you can easily compute a report or run a training algorithm on the same in-memory data. Furthermore, you get the same programming interface to combine these jobs in, and only one system to manage and install.

- In any case, it is a first-order goal of the system to stay compatible with the wider Hadoop ecosystem, and just give people better ways to compute on the same data. The Hadoop ecosystem is also moving quickly towards supporting alternative programming models, through efforts like YARN.

</details>

</blockquote>

---

3. How Spark is used as a data distributed System?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Basically, Spark is used as a general-purpose distributing data processing system, which is used to use in wide range.  Spark is used as Storage as well as processing. As we know, spark has its own cluster management for computation, so it uses Hadoop storage for storing data.
Component of Spark:
1.	Spark SQL 
2.	Spark Streaming 
3.	Machine Learning 
4.	Graphx

![Example](Spark.JPG)

</details>

</blockquote>

---

4. How do you copy files from local machine to hdfs?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

1.	$ hadoop fs -put /local-file-path / hdfs-file-path
        
    or

3.	$ hdfs dfs -put /local-file-path /hdfs-file-path

<details> <summary><b>Explanation</b></summary>

In order to copy a file from the local file system to HDFS, use Hadoop fs -put or hdfs dfs -put, on put command, specify the local-file-path where we wanted to copy from and then HDFS-file-path where you wanted to copy to. If the file already exists on HDFS, we  will get an error message saying “File already exists”.

</details>

</details>

</blockquote>

---

5. How Map reduce (MR) is differ from Elastic Map reduce(EMR)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Map Reduce is the way to distribute programs across a cluster to enable working on large data sets. It takes care of how the input data is split for processing across the cluster, and how results are aggregated. Hadoop Map Reduce is an open source implementation.

- Elastic Map Reduce is Amazon's platform which gives a hadoop as a service deployment so that you dont have to install hadoop and can just write and run your map reduce application on the cloud.

</details>

</blockquote>

---

6. What ensures load balancing of the server in Kafka?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- As the main role of the Leader is to perform the task of all read and write requests for the partition, whereas Followers passively replicate the leader.

- Hence, at the time of Leader failing, one of the Followers takeover the role of the Leader. Basically, this entire process ensures load balancing of the servers.

</details>

</blockquote>

---

7. What roles do Replicas and the ISR play?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Basically, a list of nodes that replicate the log is Replicas. Especially, for a particular partition. However, they are irrespective of whether they play the role of the Leader.

In addition, ISR refers to In-Sync Replicas. On defining ISR, it is a set of message replicas that are synced to the leaders.

</details>

</blockquote>

---

8. How to erase all messages from a Kafka topic? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

1. stop zookeeper & Kafka server, 
2. then go to 'kafka-logs' folder , there you will see list of kafka topic folders, delete folder with topic name 
3. go to 'zookeeper-data' folder , delete data inside that.

</details>

</blockquote>

---

9. Do you know how to work with aggregate functions? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes.
- Aggregate functions are definitely one of these features in SQL functions. It is a very Poweful feature same as a  MS Excel.Aggregate function are not specific to SQL, they are used often. They are part of the SELECT statement, and this allows us to have all benefits of SELECT (joining tables, filtering only rows and columns we need), combined with the power of these functions.
- Aggregate Functions:

- COUNT – counts the number of elements in the group defined
- SUM – calculates the sum of the given attribute/expression in the group defined
- AVG – calculates the average value of the given attribute/expression in the group defined
- MIN – finds the minimum in the group defined
- MAX – finds the maximum in the group defined.

</details>

</blockquote>

---

10. If 8TB is the available disk space per node (10 disks with 1 TB, 2 disk for operating system etc. were excluded.). Assuming initial data size is 600 TB. How will you estimate the number of data nodes (n)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The actual size of data to store – 600 TB
At what pace the data will increase in the future (per day/week/month/quarter/year) – Data trending analysis or business requirement justification (prediction)
We are in Hadoop world, so replication factor plays an important role – default 3x replicas
Hardware machine overhead (OS, logs etc.) – 2 disks were considered
Intermediate mapper and reducer data output on hard disk - 1x
Space utilization between 60 % to 70 % - Finally, as a perfect designer we never want our hard drive to be full with their storage capacity.

<details><summary> Explanation </summary>

Let’s do some calculation to find the number of data nodes required to store 600 TB of data:
Rough calculation:
Data Size – 600 TB
Replication factor – 3
Intermediate data – 1
Total Storage requirement – (3+1) * 600 = 2400 TB
Available disk size for storage – 8 TB
Total number of required data nodes (approx.): 2400/8 = 300 machines
Actual Calculation: Rough Calculation + Disk space utilization + Compression ratio
Disk space utilization – 65 % (differ business to business)
Compression ratio – 2.3
Total Storage requirement – 2400/2.3 = 1043.5 TB
Available disk size for storage – 8*0.65 = 5.2 TB
Total number of required data nodes (approx.): 1043.5/5.2 = 201 machines
Actual usable cluster size (100 %): (201*8*2.3)/4 = 925 TB
Case: Business has predicted 20 % data increase in a quarter and we need to predict the new machines to be added in a year
Data increase – 20 % over a quarter
Additional data:
1st quarter: 1043.5 * 0.2 = 208.7 TB
2nd quarter: 1043.5 * 1.2 * 0.2 = 250.44 TB
3rd quarter: 1043.5 * (1.2)^2 * 0.2 = 300.5 TB
4th quarter: 1043.5 * (1.2)^3 * 0.2 = 360.6 TB
Additional data nodes requirement (approx.):
1st quarter: 208.7/5.2 = 41 machines
2nd quarter: 250.44/5.2 = 49 machines
3rd quarter: 300.5/5.2 = 58 machines
4th quarter: 360.6/5.2 = 70 machines
With these numbers you can predict next year additional machines requirement for the cluster (last quarter + 24), (last quarter + 28) and so on.

</details>
</details>
</blockquote>

---

11. Imagine that you are uploading a file of 500MB into HDFS.100MB of data is successfully uploaded into HDFS and another client wants to read the uploaded data while the upload is still in progress. What will happen in such a scenario, will the 100 MB of data that is uploaded will it be displayed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Although the default blocks size is 64 MB in Hadoop 1x and 128 MB in Hadoop 2x whereas in such a scenario let us consider block size to be 100 MB which means that we are going to have 5 blocks replicated 3 times (default replication factor). 

<details><summary> Explanation </summary>

We have 5 blocks (A/B/C/D/E) for a file, a client, a namenode and a datanode. So, first the client will take Block A and will approach namenode for datanode location to store this block and the replicated copies. Once client is aware about the datanode information, it will directly reach out to datanode and start copying Block A which will be simultaneously replicated to other 2 datanodes. Once the block is copied and replicated to the datanodes, client will get the confirmation about the Block A storage and then, it will initiate the same process for next block “Block B”.

So, during this process if 1st block of 100 MB is written to HDFS and the next block has been started by the client to store then 1st block will be visible to readers. Only the current block being written will not be visible by the readers.

</details>
</details>
</blockquote>

---

12. When decommissioning the nodes in a Hadoop Cluster, why should you stop all the task trackers?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We are aware about a complete process on how to decommission a datanode and there are loads of material available on internet to do so but what about the task tracker running a MapReduce job on a datanode which is likely to be decommissioned. Unlike the datanode, there is no graceful way to decommission a tasktracker. It is always assumed that when we want to move the same task to other node then we need to rely on making the task process to stop for failure and let it be rescheduled elsewhere on the cluster. It is possible that a task on its final attempt is running on the tasktracker and that a final failure may result in the entire job failing. Unfortunately, it’s not always possible to prevent this case from occurring. So, the idea behind decommissioning that it will stop your datanode but to move the current task to another node, we need to manually stop the task tracker running on the decommissioned node.

</details>
</blockquote>

---

13. Assume you want to generate a unique id to each record of data frame,how would you achieve it.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

we can use monotonically_increasing_id() in withColumn

</details>
</blockquote>

---


14. How would you see the running application in yarn from the command line ?And how will you kill the application.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yarn application -list

</details>
</blockquote>

---

15. Say you have data of a website contains information of logged in user ,one user may have multiple fields. But the number of fields per user may vary based on his actions.In that case which component of hadoop you will use to store the data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

nosql db.

16. There are 5000000 Records in one hive table and you have loaded it in spark -shell for development purposes. What would be the best practice to write code.Would you be processing 5000000 records in each line of code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In that case we can use limit function(say 1000 records ) ,cache it and then use it . And when the complete code is ready we can process all data.

</details>
</blockquote>

---

17. In Kafka, have you dealt with subscriber programs or consumer programs?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Kafka consumers is a part of a consumer group. When multiple consumers are subscribed to a topic and belong to the same consumer group, each consumer in the group will receive messages from a different subset of the partitions in the topic.

</details>
</blockquote>

---

18. How do you create a dataframe in spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Three ways to create a DataFrame in Spark: 
•	Create a list and parse it as a DataFrame using the toDataFrame() method from the SparkSession .
•	Convert an RDD to a DataFrame using the toDF() method.
•	Import a file into a SparkSession as a DataFrame directly.

</details>
</blockquote>

---

19. Can you perform all CRUD operations on HIVE? does HIVE allow update and delete?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

With the help of ACID operations, HIVE can perform a CRUD operation. 
We should have some minimum requirements for the CRUD operation using ACID properties in Hive. We always need to enable the properties in Hive to be used CRUD operation.

<details><summary> Explanation </summary>

Following operations need to be enabled to used CRUD operation:
•	The version of Hive should be minimum 0.14 and above
•	File format must be in ORC file format with TBLPROPERTIES(‘transactional’=’true’)
•	Table on which you want to perform the update and delete operation must be CLUSTERED BY with some Buckets
•	Properties (explained below) must be enabled. You can add these properties in Hive-Site.xml for the global changes or on the command like for the session changes.

</details>

</details>
</blockquote>

---

20. Suppose Hadoop spawned 100 tasks for a job and one of the tasks failed. What will Hadoop do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 Basically, it will restart the task again on some other TaskTracker and if the task fails more than four (By default ) times will it kill the job.

</details>
</blockquote>

---

21. Consider case scenario: In M/R system,
- HDFS block size is 64 MB
- Input format is FileInputFormat
- We have 3 files of size 64K, 65Mb and 127Mb
How will we manage this Situation In HDFS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Input splits depend upon the block size of cluster , files are splitted accordingly.

Because each files will represented as a block in HDFS, the ideal calculation should be:

If using 128 M as default block size:

- 128K file: 1 block

- 129M file: 2 blocks

- 255M file: 2 blocks

So total 5 input splits will created based on 5 blocks.



<details><summary> Explanation </summary>

1. 128K file size : 

128k/64MB = ! Block = 1 Input Split. 

Note:  blocks-size does not mean the per file size on the disc, it means the unit for replication in HDFS and input split in Map Reduce.
</details>
</details>
</blockquote>

---

22. Explain how is data partitioned before it is sent to the reducer if no custom partitioner is defined in Hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hash Partion is the default partioner in hadoop which is handled by Hadoop internally if no partioner has been defined.

</details>
</blockquote>

---

23. Is Spark is a replacement of Hadoop? If yes, do you want to suggest to use mapreduce to or just spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. 

Yes , definitely ,Spark is much better than Map reduce , we can call it is an enhancement but not a replacement.

<details><summary> Explanation </summary>

Spark is definitely faster than mapreduce as all the processing is done in the memory, where the data is stored. So fast access to data is possible making it quicker.

In Mapreduce the data is stored in disks, so it is slower.

At the same time for batch processing where huge sets of data is there and time limit is not a factor mapreduce is definitely preferred, whereas for smaller datasets where we need quick to and fro access to the data, Spark is preferred.

</details>
</details>
</blockquote>

---

24. Is it  possible to put  our data sets through the reduction phase twice in a map reduce?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes it is possible. 

<details><summary> Explanation </summary>

- Scenario- one mapper and one reducer. The simple approach in that case would be before you place your input in hdfs make a copy and use it twice you will get two sets of output. In this approach you can't expect a different out come in both run if you have the Same keys in mapper. If in case you have one set of keys for your mapper during first run and a different set for second run then is possible.
- scenario - multiple mappers and one reducer in this case two set of map keys and one reducer so you can run the i out against two different mapper keys simultaneously.

</details>
</details>
</blockquote>

---

25. Where does the process of Shuffle and sort take place in map reduce framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The Shuffle and Sort process takes place on the Data Nodes (DNs), the same DNs where the Mappers executed and where the Reducers will execute.

<details><summary> Explanation </summary>

When a MapReduce program starts, the Mappers execute on the DNs on which blocks of the input file(s) are stored in HDFS. The Mappers execute against the splits of the input file(s). Once the Mappers finish execution, like keys and their associated values are sent to the same DN as input to a Reducer. This is the Shuffle phase.

All of the work of the MapReduce program is performed on the DNs. That is where the data that the MR program works on resided.

</details>
</details>
</blockquote>

---

26. Does creating checkpoints in various phases (map, combiner, shuffle, reduce) of a map reduce the chance to avoid phase level failures and improve fault tolerance?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Failure detection and recovery in hadoop happens at a task level. If a task fails, it is rerun on another available node. This requires recomputing the task from scratch, which for a long running task adds up a lot of delay to the application. A common thought of solution is checkpointing the latest state of the program in a stable storage, and resume the program for the last saved checkpoint , in case a failure happens. 

The reasons being -

- Checkpointing requires the intermediate state to be saved on a stable storage. For an application like mapreduce, which produces a lot of intermediate results, this would severely affect the performance of the application.
- Maintaining checkpoint information requires a lot of bandwidth and resources, which again is a bottleneck for mapreduce applications.
- Recovering a task from a checkpoint also requires a lot of IO and network, which would affect our applications.

<details><summary> Explanation </summary>

Saving the intermediate results at various phases in mapreduce is a good idea, but it has to be implemented thoughtfully. First, local checkpointing should be utilized for this purpose, i.e local disk of the tasks should be used to write task progress. No replicas should be transferred over the network, to avoid congestion. This should be done at the time the tasks were going to write intermediate results to disk anyway, otherwise it would create delays. Second, instead of blindly recovering the intermediate data from checkpoints, some important changes can be made, like increasing the memory size and split size, before recovering, owing to the fact that a lot of task failures happen due to heap space issues. This would prevent the tasks from continuously failing and re-running.

</details>
</details>
</blockquote>

---

27. In Hadoop MapReduce, is it possible to support multiple reduce methods for the same Mapper input?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

yes you can do it - but it may be a pretty bad idea.

</details>
</blockquote>

---

