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

</details>
</blockquote>

---



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

28. Suppose a NameNode is failed , How do we bring it up ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Suppose this situation happen , as NameNode gets fail the whole Hadoop cluster will not work. There will be no data loss only the cluster work will be shut down, because the NameNode is only point of contact to all the DataNodes and if the NameNode fails all communication will stop.

</details>
</blockquote>

---

29. How will you decide whether you need to use the Capacity Scheduler or the Fair Scheduler?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Suppose , we wants the jobs to make Equal progress ,whereas following the FIFO principle , then we need to use Fair Scheduling. 

</details>
</blockquote>

---

30. What are the daemons required to run a Hadoop cluster?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hadoop cluster has 5 daemons. 
- NameNode
- DataNode
- Secondary NameNode
- JobTracker
- TaskTracker

</details>
</blockquote>

---

31. How will you restart a NameNode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- We can stop the NameNode individually using Command like :
/sbin/hadoop-daemon.sh
After that start the NameNode using command like :
/sbin/hadoop-daemon.sh

</details>
</blockquote>

---

32. What is jps command used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to check if a specific daemon is up or not as well as It is processes that are based on the  particular user.

</details>
</blockquote>

---

33.  Is it possible to copy files across multiple clusters? If yes, how can you accomplish this?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes!
It is possible to the copy files across the multiple Hadoop clusters and this can be achieved using distributed copy.

</details>
</blockquote>

---

34. Can HDFS blocks be broken?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes!

HDFS blocks be brokento this is input split. As HDFS does not know the content of the file.While storing the data into multiple blocks, last record of each block might be broken.

</details>
</blockquote>

---

35. Does Hadoop replace data warehousing systems?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No , Hadoop never replace any datawarehouse system. 

<details><summary> Explanation </summary>

Hadoop will not replace a data warehouse because the data and its platform are two non-equivalent layers in Data warehouse architecture. 

</details>
</details>
</blockquote>

---

36. Propose a design to develop a system that can handle ingestion of both periodic data and real-time data.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Data can be streamed in the real-time or ingested in batches. When Big Data is ingested in real-time, then it is ingested immediately as soon as data arrives. When data is ingested in batches using the Data ingestion pipeline, data items are ingested in some chunks at a periodic time interval.

</details>
</blockquote>

---

37. File could be replicated to 0 Nodes, instead of 1. Have you ever come across this message? What does it mean?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

When a file is written to the HDFS, it is replicated to multiple core nodes. When you see this error, it means that the NameNode daemon does not have any available DataNode instances to write the data to in HDFS. In other words, block replication is not taking place.

</details>
</blockquote>

---

38. How Avro Serialization work in Hadoop Platform? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to Provide AvroMapper and AvroReducer class for running the Mapreduce program in hadoop. Which helps Avro Serialization work smothly in Hadoop platform. 
Basically Avro Serialization is a process of translating objects or data structures state into binary or textual data. 

</details>
</blockquote>

---

39. How can you skip the bad records in Hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

With the help of <b> SkipBadRecords class </b> , we can skip the bad records in hadoop.

</details>
</blockquote>

---

40. What is the purpose of using DistCp is hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is a tool which is used to copy large amounts of data to and from hadoop file system in parallel.

</details>
</blockquote>

---

41. Which command is used to format the NameNode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

    $ hdfs namenode -format

</details>
</blockquote>

---


42. Can the default “Hive Metastore” be used by multiple users (processes) at the same time?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

    Yes. 
    Hive Metastore allow multiple users at the same time.

</details>
</blockquote>

---

43. Why do we use HDFS for applications having large data sets and not when there are lot of small files?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hdfs is easy and efficient for handling a large number of data sets. 
It is used to maintained single file as compared to the small chunks of data stored in multiple files. 

</details>
</blockquote>

---

44. If we want to copy 10 blocks from one machine to another, but another machine can copy only 8.5 blocks, can the blocks be broken at the time of replication?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

HDFS, blocks cannot be broken down.

<details><summary> Explanation </summary>

Before copying the blocks from one machine to another, the Master node will figure out what is the actual amount of space required, how many block are being used, how much space is available, and it will allocate the blocks accordingly.

</details>
</details>
</blockquote>

---

45. If reducers do not start before all mappers finish, then why does the progress on MapReduce job shows something like Map (50%) Reduce (10%)? Why is reducers progress percentage displayed when mapper is not finished yet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The reducer phase will be started atleast 5% of total mappers have completed the execution.So the dispatched reducers will continue to stay in copy phase until all mappers are completed.

</details>
</blockquote>

---

46. What is Fact Table and Dimension Table (When I said that I am aware of Dataware house concept)

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Basically Fact table works the dimension tables. 
It holds the data , that data must be analyzed and dimension table stores data about the ways in which the data in the fact table can be analyzed.

</details>
</blockquote>

---

47. What type of data we should store in Fact table and dimension table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Basically Fact table works the dimension tables. 
It holds the data , that data must be analyzed and dimension table stores data about the ways in which the data in the fact table can be analyzed.
It is stored the report labels whereas Dimension table contains detailed data.

</details>
</blockquote>

---

48. There is a string in a Hive column, how you will find the count of a character. For example, the string is “hdfstutorial”, then how to count number of ‘t’.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hive is used to helps in finding the position of a substring in a string. It returns only the first occurence of the given input.It will return the null value , if either of the arguments are null and it return 0 if the substring could not be found in the string.

</details>
</blockquote>

---

49. We have 10 tables, and there are certain join conditions you have to put and then the result needs to be updated in another table. How you will do it. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is possible to make relation between 10 tables. We can consider relation between tables as it will make that the number bigger. We make the restriction that each table may appear at most once, there are 2^10-1 = 1023 possibilities.

</details>
</blockquote>

---

50. Tell me some set of Analytical funtions are used in Hive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- RANK.
- DENSE_RANK.
- ROW_NUMBER.
- PERCENT_RANK.
- CUME_DIST.
- NTILE.

</details>
</blockquote>

---

51. Tell me something about bucketing ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Bucketing is used to work with large datasets that may need to be Segregated into clusters for efficient management and to be able to perform join queries with the other large datasets. 

- Hive Bucketing (Clustering) is a method to split the data into more manageable files using number of buckets to create. The value of the bucketing column will be hashed by a user-defined number into buckets

</details>
</blockquote>

---

52. what is actually hapeening in bucketing and when we apply?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Bucketing is used to work with large datasets that may need to be Segregated into clusters for efficient management and to be able to perform join queries with the other large datasets. 

- Hive Bucketing (Clustering) is a method to split the data into more manageable files using number of buckets to create. The value of the bucketing column will be hashed by a user-defined number into buckets.

</details>
</blockquote>

---

53. Why do use buckets?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Bucketing is used to work with large datasets that may need to be Segregated into clusters for efficient management and to be able to perform join queries with the other large datasets. 

- Hive Bucketing (Clustering) is a method to split the data into more manageable files using number of buckets to create. The value of the bucketing column will be hashed by a user-defined number into buckets.

</details>
</blockquote>

---

54. How bucketing is different from Partition and why we use it

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Hive Partition is a way to organize large tables into smaller logical tables based on data of columns; one partition for each distinct value. Hive, tables are created as a directory on Hadoop distributed file system such as HDFS. A table can have one or more logical tables, that correspond to a sub-directory for each logical table partition, inside a table directory.
- Hive Bucketing (Clustering) is a method to split the data into more manageable files using number of buckets to create. The value of the bucketing column will be hashed by a user-defined number into buckets.

</details>
</blockquote>

---

55.  If you have a bucketed table then can you take those records to Sqoop directly.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We would have to import the data to an intermediate table and then insert into the bucketed table.

</details>
</blockquote>

---

56. If we have 10GB and 10MB file, How do you load and process the 10 MB file in map-reduce.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Mapreduce used to process the task in a block of data at a time. Many small files mean lots of blocks which means the lots of tasks, and lots of book keeping by Application Master.

</details>
</blockquote>

---

57. Apart from Map-side and reduce side joins any other joins in map-reduce?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Map side join is usually used when one data set is large and the other data set is small. Whereas the Reduce side join can join both the large data sets.

</details>
</blockquote>

---

58. What does hadoop-metrics.properties file do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hadoop-metrics properties file  is used to control the reporting for hadoop. 

</details>
</blockquote>

---

59. How to erase all messages from a Kafka topic? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

1. stop zookeeper & Kafka server, 
2. then go to 'kafka-logs' folder , there you will see list of kafka topic folders, delete folder with topic name 
3. go to 'zookeeper-data' folder , delete data inside that.

</details>
</blockquote>

---

60. What's the difference between a RDD and DataFrame?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

RDD work as a distributed collection of data elements spread across many machines in the cluster. It is a set of Spark/Scala objects representing data. Whereas Data Frame is a distributed collection of data organized into named columns. It is conceptually equal to a table in a relational database.

</details>
</blockquote>

---

61. How to create a Rdd in Hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

```python
1.	# parallelizing data collection
2.	my_list1 = [10, 20, 30, 40, 50]
3.	my_list1_rdd = sc.parallelize(my_list)
4.	 
5.	## 2. Referencing to external data file
6.	file_rdd = sc.textFile("path_of_file")
```

</details>
</blockquote>

---

62. How to create DataFrame using PySpark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

```python
1.	spark.createDataFrame(
2.	    [
3.	        (1, 'Aman'), # create your data here, make sure to be consistent in the types.
4.	        (2, 'John'),
5.	        .
6.	        .
7.	        .
8.	        .
9.	        (100, 'Mic')
10.	    ],
```

</details>
</blockquote>

---

63. Different types of memories in spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

1.	Execution Memory 
2.	Storage memory 

 Storage memory is used for caching purposes and execution memory is acquired for temporary structures like hash tables for aggregation, joins etc.

</details>
</blockquote>

---

64. Tell me something about the sparkContext, what is the purpose to used SparkContext in Hadoop.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

sparkContext:
Spark Context is an entry point to Spark. It is used to programmatically create Spark RDD, accumulators, and broadcast variables on the cluster. 
SparkContext in spark-shell :

```python
1.	val rdd = sc.textFile("/src/main/resources/text/file.txt")
```

use this to create Spark RDD.

```python
1.	val rdd = sparkContext.textFile("/src/main/resources/text/alice.txt")
```

</details>
</blockquote>

---

65. Tell me something about the sparkSession, what is the purpose to used SparkSession in Hadoop.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Spark Session is introduced to use in a combined class for different contexts, we used to have in SQL Context as well as Hive Cotect. 
It is a entry point of Spark which is used to creating a Spark Session. It will be created using Sparksession.builder ().
It includes all the APIs available in different contexts –
•	Spark Context,
•	SQL Context,
•	Streaming Context,
•	Hive Context.

SparkSession in spark-shell:

```python
1.	val rdd = sparkContext.textFile("/src/main/resources/text/file.txt")
```

</details>
</blockquote>

---

66. How Hadoop’s CLASSPATH plays a vital role in starting or stopping in Hadoop daemons?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Class path will contains the list of directories containing jar files required to stop/start daemons.

</details>
</blockquote>

---


67. What are the different commands used to startup and shutdown Hadoop daemons?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

stop-dfs.sh   - shutdown the DFS daemons.
start-mapred.sh  - start the map-reduce daemons.
start-all.sh  - start the all hadoop daemons.
<details><summary> Explanation </summary>

- stop-dfs.sh - Stops the Hadoop DFS daemons. 
- start-mapred.sh - Starts the Hadoop Map/Reduce daemons, the jobtracker and tasktrackers.
- tart-all.sh - Starts all the Hadoop daemons, the namenode, datanodes, the jobtracker and tasktrackers.

</details>
</details>
</blockquote>

---

68. What is configured in /etc/hosts and what is its role in setting Hadoop cluster?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

we store all the hostnames with their IP addresses in /etc/hosts so, that we can use hostnames easily instead of the IP addresses.


</details>
</blockquote>

---

69. Is it possible to provide multiple input to Hadoop? If yes then how?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Yes , it is possible to input multiple files in the same directory. 

hadoop doesnt read the directory recursively. Suppose , ultiple input files like file1, file2, file3 , file4 , etc are present in the /folder1, then Set mapreduce. input.

</details>
</blockquote>

---

70. Have you worked with SQOOP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Yes.

Basically, Sqoop  is used as a tool to transfer data between Hadoop and Relational Database servers.

</details>
</blockquote>

---

71. Have you worked with any cloud platform?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Yes.
Example:
Amazon Web Services (AWS), Google Cloud Platform, Alibaba, Microsoft Azure, and IBM Bluemix etc.

</details>
</blockquote>

---

72. Tell me about Zookeeper role in Kafka ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Kafka is a distributed system is built to use Zookeeper. Basically, it is main used to build coordination between different nodes in a cluster. It is also use Zookeeper to recover from previously committed offset if any node fails because it works as periodically commit offset.

</details>
</blockquote>

---

73. How do you create a dataframe in spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Three ways to create a DataFrame in Spark: 
•	Create a list and parse it as a DataFrame using the toDataFrame() method from the SparkSession .
•	Convert an RDD to a DataFrame using the toDF() method.
•	Import a file into a SparkSession as a DataFrame directly.

</details>
</blockquote>

---

74. In Kafka, have you deal with subscriber programs or consumer programs?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Kafka consumers is a part of a consumer group. When multiple consumers are subscribed to a topic and belong to the same consumer group, each consumer in the group will receive messages from a different subset of the partitions in the topic.

</details>
</blockquote>

---

75. Why is block size set to 128 MB in Hadoop HDFS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Having 128MB(huge) block size is to minimize the cost of seek and reduce the data information generated to per block.


</details>
</blockquote>

---

76. How data or file is written into HDFS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


If we want to write a file in HDFS , we need to intract with namenode. 
Basicaly Namenode is used to provides the address of a datanode.
now datanode will create the data write pipeline.

</details>
</blockquote>

---

77. How data or file is read in HDFS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

If we want to read a file in HDFS , we need to intract with namenode. 
Basicaly Namenode is used to provides the address of a datanode.
Now it will interact directly with the respective datanodes to read the data blocks.

</details>
</blockquote>

---

78. What is a Heartbeat in HDFS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

It  is a signal from Datanode to Namenode to indicate that it is alive.

</details>
</blockquote>

---


79. Suppose you are running a spark job 3 to 4 times everyday. And it loads the data into hive table.what would be the best approach to distinguish the data on the basis of time when it is loaded.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

We can use Hive table to create as well as insert data. 

We can us below command to get the current time which will act as batchtime in hive table

var batchtime=System.currentTimeMillis()

And data frame which is storing data to partitioned table can have column batchtime which will act as partition column

df.withColumn(“batchtime”,lit(batchtime))

</details>
</blockquote>

---

80. Assume We want to generate a unique id to each record of data frame,how would we achieve it.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

With the help of  monotonically_increasing_id()

</details>
</blockquote>

---

81. How will get a hdfs file into local directory.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Hadoop fs – get hdfsdir local dir

</details>
</blockquote>

---

82. How would we see the running application in yarn from the command line ?And how we will kill the application.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Yarn application -list

Yarn application -kill appid

</details>
</blockquote>

---

83. How would we handle it efficiently so that it can be processed by other applications and also reduce the data storage?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Using Parquet file in hive. After that we can deleting the old HDFS data and then Create a partition in hive. 

</details>
</blockquote>

---

84. Will Spark overtake Hadoop? Will Hadoop be replaced by Spark?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Apache Hadoop is a big old package that comes to rescue for various problems like storage, NoSQL, Datawarehouse, data ingestion, fault tolerance, maintaining configuration information, naming, providing distributed synchronization, and providing group services. These services are provided with the use of various tools like HBase, Hive, Sqoop, Zookeeper, etc.

</details>
</blockquote>

---

85. What exactly is Apache Spark and how does it work? What does a cluster computing system mean?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Open source: Spark original code is made public and freely available for the people to access and contribute as well
- Unified analytics engine: Common processing engine to combine data across different channels and convert it into a consumable manner that is ready for analysis.
- Large scale data processing: Used in distributed computing space to handle and process huge volumes of data.

</details>
</blockquote>

---

86. Why rack awareness is necessary ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

It is used to chooses closer Datanodes based on the rack information. Which helps to improve the network traffic while reading/writing HDFS files in large clusters of Hadoop.Rack-Awareness is to prevent data loss if the entire rack fails. It also improves network bandwidth.

</details>
</blockquote>

---

87. What is the default block size and how is it defined?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

In the Hadoop the default block size is 128 MB.

<details><summary> Explanation </summary>

In HDFS data is stored in the terms of Block. It is the size of the file that get divided into when the file is store in any node. In the Hadoop the default block size is 128 MB.

</details>
</details>
</blockquote>

---

88. How do you get the report of hdfs file system? About disk availability and no.of active nodes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Run the fsck command on namenode as $HDFS_USER: su - hdfs -c "hdfs fsck / -files -blocks -locations > dfs-new-fsck-1.log" .
- Run hdfs namespace and report.
- Compare the namespace report before the upgrade and after the upgrade.
- Verify that read and write to hdfs works successfully.

</details>
</blockquote>

---


89. What is Hadoop balancer and why is it necessary?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

The HDFS balancer re-balances data across the DataNodes, moving blocks from the overutilized to underutilized nodes. As the system administrator, we can run the balancer from the command-line as necessary .for example, after adding the new DataNodes to the cluster.

</details>
</blockquote>

---

90. What are the main actions performed by the Hadoop admin?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

The responsibilities of a Hadoop admin include deploying a hadoop cluster, maintaining a hadoop cluster, adding and the removing nodes using cluster monitoring tools like Ganglia Nagios or Cloudera Manager, configuring the NameNode high availability and keeping a track of all the running hadoop jobs.

</details>
</blockquote>

---

91. What is the purpose to use Kerberos?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Kerberos was designed to the provide secure authentication to services over an insecure network. Kerberos uses tickets to authenticate a user and the completely avoids sending passwords across the network.

</details>
</blockquote>

---

92. How to check the logs of a Hadoop job submitted in the cluster and how to terminate already running process?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Click on HDFS ----> Configs -------> type log in filter box. The picture below shows how to locate log directory for Apache Oozie using grep command of Unix. log directories will have three types of files . Logs of running daemons will be available here in this .

We can configure the maximum number of times a particular map or reduce the task can fail before the entire job fails through the following properties:
- mapred. map. max. attempts - The maximum number of attempts per map task.
- mapred. reduce. max. attempts - Same as above, but for reduce tasks.


</details>
</blockquote>

---

93. What details are in the “fsimage” file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

FsImage is a file stored on the OS filesystem that contains the complete directory structure namespace of the HDFS with details about the location of the data on the Data Blocks and the which blocks are stored on the which node. This file is used by the NameNode when it is started.

</details>
</blockquote>

---

94. What log file loaders did you use in Pig?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Pig, is a repository of user-submitted UDF, contains a custom loader function CommonLogLoader to load Apache's Common Log Format files into pig.

</details>
</blockquote>

---

95.  Filter – What did you filter out?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Use filters to temporarily hide some of the data in a table, so you can focus on the data you want to see.


</details>
</blockquote>

---

96. What do you mean by Flume?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Flume is an open-source, powerful, reliable and flexible system used to collect, aggregate and move large amounts of unstructured data from multiple data sources into HDFS/Hbase (for example) in a distributed fashion via it's strong coupling with the Hadoop cluster.

</details>
</blockquote>

---

97. Tell me the process of Configure slots in Hadoop 2.0 and Hadoop 1.0.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Each Map Reduce Jobs are split into task and Task tracker runs each task on a fixed number of map and reduce slots inside a data node based on a static configuration.
- In Hadoop 1.0 we need to specify in mapred-site.xml the following parameter to Configure the number of map slots and reduce slots.
- Hadoop 2 now supports Automatic Failover of the YARN ResourceManager. Because of many such enterprise ready features, Hadoop is making news and the positive predictions.


</details>
</blockquote>

---

98. In case of high availability, if the connectivity between Standby and Active NameNode is lost. How will this impact the Hadoop cluster?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Active Name Node and standby Name Node is not directly connected. They are connected through a medium, journal. Read and write operation is through journal only. If the network is down then only connectivity between the NameNode and Standby Name Node will be lost. There is no impact on hadoop cluster till then your Name Node is Up and running.

</details>
</blockquote>

---

99. What is the minimum number of ZooKeeper services required in Hadoop 2.0 and Hadoop 1.0?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Group of ZooKeeper servers. The minimum number of the nodes that is required to form an ensemble is 3.


</details>
</blockquote>

---

100.  If the hardware quality of few machines in a Hadoop Cluster is very low. How will it affect the performance of the job and the overall performance of the cluster?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Installing Hadoop cluster in production is just half the battle won. It is extremely important for a Hadoop admin to tune the Hadoop cluster setup to gain maximum performance. During the Hadoop installation, the cluster is configured with default configuration settings which are on par with the minimal hardware configuration. 

</details>
</blockquote>

---

101. Explain the difference between blacklist node and dead node.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

When the JobTracker submits jobs to the TaskTracker and the tasks on that the node have failed too many times, the JobTracker will blacklisted a TaskTracker.Dead Node , which are not in the cluster or configure but not showing into the cluster.

</details>
</blockquote>

---

102. How can you increase the NameNode heap memory?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Blocksize=128 MB, Replication=1.
- Cluster capacity in MB: 200 * 24,000,000 MB = 4,800,000,000 MB (4800 TB).
- Disk space needed per block: 128 MB per block * 1 = 128 MB storage per block.
- Cluster capacity in blocks: 4,800,000,000 MB / 128 MB = 36,000,000 blocks.

</details>
</blockquote>

---

103. After restarting the cluster, if the MapReduce jobs that were working earlier are failing now, what could have gone wrong while restarting?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


The cluster could be in a safe mode after the restart of a namenode. The administrator needs to wait for the namenode to exit the safe mode before restarting the jobs again.


</details>
</blockquote>

---

104. Explain the steps to add and remove a DataNode from the Hadoop cluster.


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Decommission the DataNode role. When asked to select the role instance to decommission, select the DataNode role instance.
- Stop the DataNode role.
- Verify the integrity of the HDFS service.
- After all errors are resolved, perform the following steps.

</details>
</blockquote>

---

105. When NameNode is down, what does the JobTracker do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

if Namenode is down then data requested by the client and gives the block information.JobTracker is responsible for the job to be completed and the allocation of resources to the job.

</details>
</blockquote>

---

106.  When configuring Hadoop manually, which property file should be modified to configure slots?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


There could be a separate configuration file for configuring the properties of these and job ACLs are checked for authorizing view and the modification of jobs.

</details>
</blockquote>

---

107. How will you add a new user to the cluster?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

To create the HDFS home directory[ie. /user/] on edge node.

</details>
</blockquote>

---

108. What is the advantage of speculative execution? Under what situations, Speculative Execution might not be beneficial?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


It will reduce the job execution time; however, the clustering efficiency is affected due to duplicate tasks. 

</details>
</blockquote>

---

109. How Serialization used in Hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Serialization is the process of the0 converting an object into a stream of bytes to store the object or transmit it to memory, a database, or a file.

</details>
</blockquote>

---

110. How to remove the duplicate records from a hive table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Use Insert Overwrite and DISTINCT Keyword.
- GROUP BY Clause to Remove Duplicate.
- Use Insert Overwrite with row_number() analytics functions.

</details>
</blockquote>

---


111. How to find the number of delimiter from a file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


We need to read a lines , count the number of commas and the number of tabs and compare them. If there's 20 commas and no tabs, it's in the CSV. If there's 20 tabs and 2 commas , it's in TSV.

</details>
</blockquote>

---

112. What is cogroup in pig?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


The COGROUP operator works more or less in the same way as the GROUP operator. The only difference between the two operators is that the group operator is normally used with one relation, while the cogroup operator is used in the statements involving two or more relations.

</details>
</blockquote>

---

113. How we can join two big tables in Hive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


We will use a Inner Join to join a two big table in Hive. 

</details>
</blockquote>

---

114.  Which language you use in flume configuration

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Flume agent configuration is stored in a local configuration file. Configurations for that the one or more agents can be specified in the same configuration file.

</details>
</blockquote>

---

115.  Write a command to import customer table in Hadoop

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


The following syntax is used to import data into HDFS.

- $ sqoop import (generic-args) (import-args)

- $ sqoop-import (generic-args) (import-args)

</details>
</blockquote>

---

116. What is the mapper in Sqoop and how you decide the number of mapper in Sqoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Number of mappers indicates how parallel our Sqoop job is running .

</details>
</blockquote>

---

117. Where we can specify the input and output location in MapReduce program.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

No, it is not mandatory to set the input and output type/format in MapReduce.

</details>
</blockquote>

---

118. What type of data we should store in Fact table and dimension table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Fact table is defined by their grain or its most atomic level whereas Dimension table should be wordy, descriptive, complete, and quality assured. Fact table helps to store report labels whereas Dimension table contains the detailed data.

</details>
</blockquote>

---

119. How bucketing is different from Partition and why we use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Bucketing decomposes data into more manageable or equal parts. With partitioning, there is a possibility that you can create the multiple small partitions based on column values. If we go for bucketing,we are restricting the number of buckets to store the data. This number is defined during the table creation scripts.

</details>
</blockquote>

---


120. What is Fact Table and Dimension Table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Dimension table Dimension table is a table which contain attributes of measurements stored in the fact tables. Fact table contains the measurement of business processes, and it contains foreign keys for the dimension tables.


</details>
</blockquote>

---


121. What are sinks and sources in Apache Flume when working with Twitter data?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Our Source is the Twitter, from where we are streaming the data and our Sink is HDFS, where we are writing the data. In source configuration, we are passing the Twitter source type as org. apache. flume.


</details>
</blockquote>

---

122. What is heap error and how can you fix it?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Heap errors can occur when your code inadvertently overwrites control information that the memory management functions use to the control heap usage. The application that you are debugging must have been built with the heap check capability.


</details>
</blockquote>

---


123. How many joins does MapReduce have and when will you use each type of join?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


There are two types of join operations in MapReduce are: Map Side Join: As the name implies, the join operation is performed in the map phase itself. 

</details>
</blockquote>

---

124. If you have configured Java version 8 for Hadoop and Java version 7 for Apache Spark, how will you set the environment variables in the basic configuration file?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

The environment variables store data that is used by the operating system and the other programs. For example, the WINDIR environment variable contains the location of the Windows installation directory. 

</details>
</blockquote>

---

125. Differentiate between bash and basic profile.


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Basic profile is read and executed when Bash is invoked as an interactive login shell, while . bash is executed for an interactive non-login shell. Basic profile to run commands that should run only once, such as customizing the $PATH environment variable .


</details>
</blockquote>

---

126.  How is Hadoop different from other parallel computing systems?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Hadoop is a distributed file system, which lets you store and the handle massive amount of data on a cloud of machines, handling data redundancy. Each node can process the data stored on it instead of spending time in moving it over the network.


</details>
</blockquote>

---

127. How can you debug Hadoop code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


- Add hadoop-mapreduce-client-jobclient maven dependency. The very first step to debug Hadoop map reduce code locally is to add the hadoop-mapreduce-client-jobclient maven dependency.
- Set the local file system. Set either local or file:/// in fs.
- Set the Number of mappers and reducers.

</details>
</blockquote>

---

128. How is security achieved in Hadoop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

- First step in securing an Hadoop cluster is to enable the encryption in transit and at rest. 

- Authentication and Kerberos rely on secure communications, so before you even go down the road of enabling authentication and the Kerberos you must enable encryption of data-in-transit.

</details>
</blockquote>

---

129. Why does one remove or add nodes in a Hadoop cluster frequently?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


In a Hadoop cluster a Manager node will be deployed on a reliable hardware with the high configurations, the Slave node's will be deployed on commodity hardware. So chance's of data node crashing is more . So more frequently you will see admin's remove and add new data node's in a cluster.


</details>
</blockquote>

---

130. What is Hadoop Streaming?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


It is a utility which comes under Hadoop distribution. It allows to create and run the mapreduce job easily. 


</details>
</blockquote>

---


131. Does Hadoop support Streaming data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Yes, its support the streamming data easily . 

<details><summary> Explanation </summary>

With streaming data integration for Hadoop, we can easily feed your Hadoop and NoSQL solutions continuously with real-time, pre-processed data from enterprise databases, log files, messaging systems too. 

</details>
</details>
</blockquote>

---

132. Can you give a detailed overview about the Big Data being generated by Facebook?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

Every day, we feed Facebook's data beast with mounds of information. Every 60 seconds, 136,000(approx.) photos are uploaded, 510,000 (approx.) comments are posted, and 293,000 (approx.) status updates are posted. Facebook generates 4 petabytes of data per day — that's a million gigabytes.


</details>
</blockquote>

---


133. Give examples of some companies that are using Hadoop structure?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>


Aprrox. 361 companies reportedly use Hadoop in their tech stacks, including Uber, Airbnb, and Shopify.

<details><summary> Explanation </summary>

Here are five businesses successfully using Hadoop:

- Marks and Spencer. In 2015, Marks and Spencer adopted Cloudera Enterprise to analyze its data from multiple sources. ...
- Royal Mail. ...
- Royal Bank of Scotland. ...
- British Airways. ...
- Expedia.

</details>
</details>
</blockquote>

---


134. Since the data is replicated thrice in HDFS, does it mean that any calculation done on one node will also be replicated on the other two?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

No, calculations will be done only on the original data.


</details>
</blockquote>

---

