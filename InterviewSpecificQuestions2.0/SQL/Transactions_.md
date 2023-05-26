10. What is the maximum number of records returned by a trigger at once?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The maximum number of records returned by a trigger at once depends on the database system being used. Different database systems have different limitations and it's important to consult the documentation of your specific database to determine the limit.
</blockquote>

</details>

---
30. Explain the different isolation levels

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Isolation levels in database systems define the level of concurrent access and transactional consistency in a multi-user environment. The different isolation levels provide varying degrees of data integrity, performance, and concurrency control. Here's an explanation of the commonly used isolation levels:

- **Read Uncommitted:** Allows reading uncommitted changes made by other transactions. Low level of isolation, high concurrency, but can lead to dirty reads, non-repeatable reads, and phantom reads.

- **Read Committed:** Allows reading only committed data, ignoring uncommitted changes. Prevents dirty reads but allows non-repeatable reads and phantom reads. Better data consistency than Read Uncommitted.

- **Repeatable Read:** Ensures data read during the transaction remains unchanged. Prevents dirty reads and non-repeatable reads but can result in phantom reads. Acquires shared locks on read data.

- **Serializable:** Provides the highest level of isolation. Transactions execute in a serializable order. Prevents dirty reads, non-repeatable reads, and phantom reads. Can reduce concurrency and may lead to more conflicts and rollbacks.

</blockquote>

</details>

---

31. What is a transaction within a relational database?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

- A transaction in a relational database is a sequence of database operations that are treated as a single unit of work. 
- Independent of other transactions
- It ensures that all the operations within the transaction are either completed successfully or rolled back if an error occurs.
- If anything fails, the whole transaction fails



</blockquote>

</details>

---

32. What is nested transaction? Explain with an example.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A nested transaction is one in which a new transaction is started by an instruction that is already inside another transaction. This new transaction is said to be nested. The isolation property of transaction is obeyed here because the changes made by the nested transaction are not seen or interrupted by the host transaction.

```sql
BEGIN TRANSACTION OuterTransaction

  -- Perform some database operations
  -- ...

  BEGIN TRANSACTION NestedTransaction

    -- Perform some nested database operations
    -- ...

    IF condition THEN
      COMMIT TRANSACTION NestedTransaction
    ELSE
      ROLLBACK TRANSACTION NestedTransaction
    END IF

  END TRANSACTION NestedTransaction

  -- Continue with more operations within the outer transaction
  -- ...

COMMIT TRANSACTION OuterTransaction

```
In this example, we have an outer transaction called OuterTransaction that contains a nested transaction called NestedTransaction. The nested transaction can perform its own set of operations and is either committed or rolled back based on a condition. The changes made within the nested transaction are isolated until the outer transaction is committed.


</blockquote>

</details>

---

33. How can you ensure that a group of SQL statements is treated as a single unit of work within a transaction?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To ensure that a group of SQL statements is treated as a single unit of work within a transaction:

- Begin the transaction using the BEGIN TRANSACTION statement.
- Execute the desired SQL statements within the transaction.
- Handle errors and exceptions to ensure proper rollback if needed.
- Commit the transaction to make the changes permanent or rollback to discard the changes.

</blockquote>

</details>

---

34. How do you handle exceptions or errors within a transaction and ensure proper rollback of changes?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To handle exceptions or errors within a transaction and ensure proper rollback of changes:

- Use try-catch blocks or error handling mechanisms within your programming language or database system.
- Catch any exceptions or errors that occur during the execution of the transaction.
- Rollback the transaction using the ROLLBACK statement to undo any changes made within the transaction.
- Handle the exception or error appropriately, such as logging the error, notifying the user, or taking corrective actions.
- Optionally, you can also provide a mechanism to retry the transaction or perform any necessary cleanup tasks.
- Ensure that the error handling code is executed regardless of whether an exception occurs or not to properly handle both successful and unsuccessful transactions.
</blockquote>

</details>

---

35. How do you design a transactional system that maintains consistency and avoids data anomalies in concurrent environments?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To design a transactional system that maintains consistency and avoids data anomalies in concurrent environments:

- Choose the appropriate isolation level for transactions to ensure concurrency and consistency.
- Clearly define transaction boundaries to encapsulate related database operations.
- Use locking and concurrency control mechanisms to prevent access issues and maintain data integrity.
- Handle conflicts and deadlocks that may arise during concurrent access.
- Consider optimistic concurrency control - techniques to handle concurrent updates.
- Implement error handling and recovery mechanisms to maintain system integrity.
- Properly manage transaction commit and rollback.
- Thoroughly test and tune the system for different concurrency scenarios.
- Continuously monitor and analyze system behavior for concurrency, consistency, and performance issues.
- Follow established best practices and design patterns for consistency, reliability, and scalability.

</blockquote>

</details>

---

5. What are the properties a transaction must follow?
 
 ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Yes, ACID is an acronym that stands for Atomicity, Consistency, Isolation, and Durability. It is a set of properties that guarantee that database transactions are processed reliably. Here's what each of the properties means:

`Atomicity`: This property ensures that each transaction is treated as a single, indivisible unit of work. Either the entire transaction is processed or none of it is processed.

`Consistency`: This property ensures that the database remains in a consistent state after a transaction is processed. In other words, the database must transition from one valid state to another valid state.

`Isolation`: This property ensures that each transaction is executed in isolation from other transactions, as if it is the only transaction being processed. This prevents transactions from interfering with each other and causing data inconsistencies.

`Durability`: This property ensures that once a transaction is committed, its changes are permanent and will survive any subsequent system failures or crashes.

</blockquote>

</details>

---

23. How to update room database based on server response?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

This is the general approach to update a local room database to reflect a database from the server, you would typically follow these steps:

- Retrieve the updated data from the server in the form of JSON, XML, or other format.
- Parse the data to extract the relevant information and convert it into the appropriate data types.
- Compare the updated data with the existing data in the local database to identify any changes.
- Apply the changes to the local database by inserting, updating, or deleting records as needed.
- Update any associated data structures or views to reflect the changes in the database.
- Notify any relevant components of the application that the database has been updated.

</blockquote>

</details>

---


13. What is the difference between DELETE, TRUNCATE, and DROP?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- DELETE, TRUNCATE, and DROP are all SQL commands used to remove data or objects from a database, but they differ in their scope and level of impact.

- DELETE is a DML (Data Manipulation Language) command that removes rows of data from a table. It is used to selectively remove specific rows of data based on a condition specified in the WHERE clause. DELETE only removes data from the table and does not remove the table itself.

- TRUNCATE is a DDL (Data Definition Language) command that removes all rows from a table, but does not remove the table structure. TRUNCATE is much faster than DELETE because it does not need to log the individual row deletions, but it also cannot be rolled back once it is executed. TRUNCATE also resets the identity seed value for the table, so any subsequent inserts will start with the initial value.

- DROP is a DDL command that removes a table or other database object from the database. When a table is dropped, all data, indexes, and constraints associated with the table are also removed. DROP is a very powerful command and should be used with caution, as it can lead to data loss if used incorrectly.

- In summary, DELETE is used to remove individual rows of data based on a condition, TRUNCATE is used to remove all rows from a table, and DROP is used to remove a table or other database object entirely. The level of impact and scope of each command should be considered carefully before using it in a production environment.

</blockquote>

</details>

---

14. Will a sql database throw an exception?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- Yes, a SQL database can throw exceptions or errors when there is an issue with executing a SQL statement.

- For example, if you try to insert a row into a table with a primary key value that already exists, the database will throw a primary key violation error. Similarly, if you try to create a table with a column name that already exists in another table, the database will throw a column name conflict error.

- In addition to syntax errors, databases can also throw exceptions for various reasons such as constraints violations, transaction failures, deadlocks, and other issues.

- It's important to handle these exceptions properly in your application code to ensure that your application can recover from errors gracefully and provide a good user experience.

</blockquote>

</details>

---


32. What is the use of COMMIT in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In SQL, COMMIT is a command that is used to permanently save the changes made to a database by a transaction. When a transaction is executed in a database, the changes made by the transaction are not saved until the transaction is committed. COMMIT is the command that signals the end of a transaction and makes its changes permanent in the database.

Here's an example of how to use the COMMIT command:
```sql
BEGIN TRANSACTION;
UPDATE customers SET email = 'newemail@example.com' WHERE customer_id = 1;
COMMIT;
```
In this example, a transaction is started using the BEGIN TRANSACTION command. The UPDATE statement modifies the email address of a customer with ID 1. Finally, the COMMIT command is used to permanently save the changes made by the transaction.

It's important to note that once a transaction is committed, its changes cannot be undone. Therefore, it's essential to ensure that a transaction is properly executed and tested before committing it. If a transaction needs to be rolled back, the ROLLBACK command can be used to cancel the transaction and undo its changes.

</blockquote>

</details>

---


33. What is the difference between Commit, save point, and Rollback in Oracle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

COMMIT, SAVEPOINT, and ROLLBACK are all Transaction Control Language (TCL) commands that are used to manage transactions in a relational database. Here's a brief overview of each command and their differences:

- COMMIT: The COMMIT command is used to permanently save the changes made by a transaction. When a transaction is committed, its changes are made permanent in the database. Once a transaction is committed, its changes cannot be undone.

- SAVEPOINT: The SAVEPOINT command is used to create a point in a transaction where it can be rolled back to if necessary. A SAVEPOINT is like a bookmark within a transaction. If a transaction encounters an error, it can be rolled back to the last SAVEPOINT created, rather than rolling back the entire transaction.

- ROLLBACK: The ROLLBACK command is used to undo changes made by a transaction. When a transaction is rolled back, all the changes made by the transaction are undone, and the database is returned to its previous state. A transaction can be rolled back in full or to a specific SAVEPOINT created during the transaction.

In summary, COMMIT is used to permanently save changes made by a transaction, ROLLBACK is used to undo changes made by a transaction, and SAVEPOINT is used to create a point in a transaction where it can be rolled back to if necessary. While all three commands are used to manage transactions in Oracle, they serve different purposes and are used in different scenarios.

</blockquote>

</details>

---
36. What are the potential considerations to keep in mind when working with long-running transactions?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

When working with long-running transactions, there are several potential pitfalls and considerations to keep in mind:

- **Increased resource usage:**Long-running transactions can tie up database resources such as locks, memory, and disk space for an extended period of time, potentially impacting the performance of other transactions.

- **Lock contention:** Long-running transactions holding locks for an extended period can lead to lock contention issues and hinder concurrency, causing delays for other transactions.

- **Data consistency risks:** Long-running transactions increase the risk of data inconsistencies, especially if the data being modified or accessed by the transaction is also being modified by other concurrent transactions.

- **Limited scalability:** Long-running transactions can limit the scalability of the system as they may prevent other transactions from executing concurrently, reducing overall throughput.

- **Transaction failure and rollback complexity:** The longer a transaction runs, the higher the chances of failure. Rolling back a long-running transaction can be complex and time-consuming, potentially leaving the system in an inconsistent state.

- **Resource leaks:** Long-running transactions may inadvertently hold on to resources such as connections, cursors, or locks, leading to resource leaks and impacting system performance.

- **Increased risk of deadlocks:** Long-running transactions that acquire multiple resources can increase the likelihood of deadlocks, where two or more transactions are waiting for resources held by each other, resulting in a deadlock situation.

- **Longer recovery time:** In case of a system failure or crash, the recovery time for long-running transactions can be longer, as the system needs to ensure data consistency and restore the transaction to a consistent state.

- **Reduced transactional integrity:** Long-running transactions increase the window of time during which inconsistencies or errors can occur, potentially compromising the transactional integrity of the system.

</blockquote>

</details>

---
21. Is `truncate` and `delete` both are the same command? 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> No, `truncate` is a DDL command, used to delete all the records from the table. Whereas `delete` is a DML command, used to delete the records based on some condition as well as it can delete all the data from the table as well.

</details>

---

22. Give the syntax of `delete`, `truncate` and `drop` commands in SQL.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> Syntax of `delete` 
```sql
delete from table_name where condition;
```
> Syntax of `truncate`
```sql
truncate table table_name;
```
> Syntax of `drop` 
```sql
drop table table_name;
```

</details>

---

23. Henry has created a table as "school" with id and name field and now he wants to insert 5 records into it. What query he has to use to insert the data into a table? 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> He has to use the `insert` command for inserting the data:  
```sql
insert into school(id, name) values(01, "Jack");
insert into school(id, name) values(02, "Henry");
insert into school(id, name) values(03, "Tom");
insert into school(id, name) values(04, "Tim");
insert into school(id, name) values(05, "EVE");
```

</details>

---

24. After inserting some of the documents into the "school" table, Tom wants to update the name of one student to EVA where id is 05. Write the query for it.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
update school
set name = "EVA" 
where id = 05;
```

</details>

---

25. A user has to remove all of the data from the "order" table without removing the structure of the table. What query he has to write for this? 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> He can use `delete from` statement or `truncate table` statement to delete all the records from the table.
```sql
delete from order;
truncate table order;
```


</details>

---

26. Let's imagine Amazon Prime no longer wishes to rent out the "Blue" movie and its movie id is 20. As an intern of Amazon company, what query you will write to remove that movie from the "movies" table?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

>
```sql
delete from movies where id =20; 
```

</details>

---
31. Tim is asking you to add him as a user in SQL so that he can access and manage the database. So, how will you add them?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> To add a user in SQL, we can use the `create user` statement.  
```sql
create user 'Tim' identified by 'password';
```


</details>

---
