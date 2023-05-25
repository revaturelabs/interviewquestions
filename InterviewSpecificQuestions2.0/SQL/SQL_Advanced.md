1. What is difference between Table and View in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `table` in SQL is a database object that stores data in `rows` and `columns`, whereas a `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. 

</blockquote>

</details>

---

2. What is a View?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. `Views` are used to simplify complex queries, hide the complexity of underlying tables, and restrict access to certain data for security purposes.

</blockquote>

</details>

---

3. Does a view contain any data in it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, a `view` does not contain any data in it. It is a virtual table that presents data from one or more tables in a structured manner. The data in a `view` is stored in the underlying `tables` and is retrieved and presented by the `view` as if it were a table.

</blockquote>

</details>

---

4. Can you create a view from another view?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, you can create a view from another view in SQL. This is known as a `nested view`. The syntax for creating a nested view is similar to creating a regular view. However, instead of specifying a table as the source of data, you specify another view. 

Here is an example syntax for creating a nested view:

```sql
CREATE VIEW nested_view AS
SELECT column1, column2, ...
FROM another_view
WHERE condition;
```

</blockquote>

</details>

---

5. How do you create a table view?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a table view in SQL, you use the `CREATE VIEW` statement. The syntax for creating a view is similar to that of creating a table, but instead of specifying the columns and data types, you specify the columns and data that you want to include in the view. Here is an example syntax:

```sql
CREATE VIEW my_view AS
SELECT column1, column2, ...
FROM my_table
WHERE condition;
```

In this example, `my_view` is the name of the view, `column1`, `column2`, etc. are the columns that you want to include in the view, `my_table` is the name of the table that the view is based on, and `condition` is the optional condition that filters the data in the view.

</blockquote>

</details>

---

6. How to use 'as' with unions and views. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In the case of a `UNION` operation, the `AS` keyword can be used to provide an alias for the resulting combined table. For example:

```sql
SELECT column1, column2
FROM table1
UNION
SELECT column1, column2
FROM table2
AS combined_table;
```

In this query, the resulting table from the `UNION` operation will be named "combined_table" due to the use of the `AS` keyword.

Similarly, the `AS` keyword can be used in a `CREATE VIEW` statement to give an alias for a view or to rename columns in the view's result set. For example:

```sql
CREATE VIEW my_view AS
SELECT column1 AS new_name1, column2 AS new_name2
FROM my_table;
```

In this query, the resulting view will be named "my_view" and the column names in the view's result set will be "new_name1" and "new_name2" instead of "column1" and "column2" from the original table.

</blockquote>

</details>

---

7. What is the best practice for using triggers?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Triggers are powerful tools in SQL, but they should be used with caution to avoid unintended consequences. Here are some best practices for using triggers:

1. Only use triggers when necessary: Triggers should only be used when there is no other alternative for achieving the same result. In some cases, a stored procedure or application code may be a better option.

2. Keep triggers simple: Triggers should be simple and easy to understand. Avoid complex logic or multiple triggers on the same table.

3. Test thoroughly: Before deploying a trigger to a production environment, it should be thoroughly tested in a development or test environment.

4. Document: Triggers should be clearly documented, including the purpose, functionality, and any potential side effects.

5. Use caution with `DML` statements: Triggers that execute DML statements (such as `INSERT`, `UPDATE`, `DELETE`) can have a significant impact on performance. Use caution when using `DML` statements in triggers.

</blockquote>

</details>

---

8. Create a trigger to delete an account if it has more than zero contacts.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Assuming a table named "accounts" with a primary key "id" and a table named "contacts" with a foreign key "account_id" that references "accounts.id":

```SQL
CREATE TRIGGER delete_account_trigger
BEFORE DELETE ON accounts
FOR EACH ROW
BEGIN
  DECLARE contact_count INT;
  SELECT COUNT(*) INTO contact_count FROM contacts WHERE account_id = OLD.id;
  IF contact_count > 0 THEN
    SIGNAL SQLSTATE '45000' SET MESSAGE_TEXT = 'Cannot delete account with contacts';
  END IF;
END
```

This trigger will prevent the deletion of any account that has one or more contacts associated with it.

</blockquote>

</details>

---

9. List the Types of triggers in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are two types of triggers in SQL:

1. DML Triggers: DML triggers execute automatically in response to certain data manipulation language (DML) events, such as `INSERT`, `UPDATE`, and `DELETE` statements.

2. DDL Triggers: DDL triggers execute automatically in response to certain data definition language (DDL) events, such as `CREATE`, `ALTER`, and `DROP` statements.

Both types of triggers can be defined as either "BEFORE" or "AFTER" triggers. BEFORE triggers execute before the triggering statement, and can be used to modify the data before it is inserted, updated, or deleted. AFTER triggers execute after the triggering statement, and can be used to audit changes or enforce business rules.

</blockquote>

</details>

---

10. What is the maximum number of records returned by a trigger at once?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The maximum number of records returned by a trigger at once depends on the database system being used. Different database systems have different limitations and it's important to consult the documentation of your specific database to determine the limit.
</blockquote>

</details>

---

11. What are triggers?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In SQL, a `trigger` is a special type of stored procedure that automatically executes in response to certain events or changes in the database. Triggers can be used to enforce business rules, maintain data integrity, and perform complex tasks based on changes to the data. There are two main types of triggers: "before" triggers and "after" triggers, which fire before or after the event or change occurs.

</blockquote>

</details>

---

12. What are procedures in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

SQL procedures are a set of pre-written SQL codes that are saved in the database server. These procedures can be called and executed by applications or other database users. SQL procedures help in simplifying the development process by creating reusable code that can be called multiple times.
</blockquote>

</details>

---

13. What is a stored procedure?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `stored procedure` is a type of SQL procedure that is stored in the database server. `Stored procedures` are precompiled SQL codes that can be executed multiple times by different applications or users. They help in improving the performance of database applications by reducing network traffic and database overhead. `Stored procedures` can take input parameters, perform data manipulation operations, and return output values.
</blockquote>

</details>

---

14. How to check the performance of a stored procedure?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are different ways to check the performance of a stored procedure in SQL. Some of them are:

1. Using Execution Plan: Execution plan shows the performance of a stored procedure by displaying the query optimization and execution path. To view the execution plan of a stored procedure, use the "SET SHOWPLAN_TEXT" command or use the "Display Estimated Execution Plan" option in SQL Server Management Studio.

2. Using Profiler: SQL Server Profiler is a tool that helps in analyzing and monitoring the performance of SQL queries and stored procedures. You can use this tool to trace the stored procedure execution and identify any performance issues.

3. Using Execution Statistics: SQL Server provides execution statistics for stored procedures that show the performance details like execution time, CPU time, memory usage, and I/O usage. You can view the execution statistics using the "SET STATISTICS TIME ON" command or the "Include Actual Execution Plan" option in SQL Server Management Studio.

</blockquote>

</details>

---

15. What is the difference between a stored procedure and a function in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
A `stored procedure` is a set of precompiled SQL statements that perform a specific task or a series of tasks. It is used to encapsulate a set of operations that are frequently used together and can be called multiple times. `Stored procedures` can be called from within another SQL statement, such as a `SELECT`, `INSERT`, or `UPDATE` statement.

A `function` is a precompiled SQL statement that returns a single value or a table. Functions are usually used in the `SELECT` statement or as a part of a `WHERE` clause. Unlike a stored procedure, a `function` cannot modify the database state, and it can be used in a SQL expression.

</blockquote>

</details>

---


16. Where do we use SQL procedures?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
SQL procedures can be used in many places, such as:

- To encapsulate business logic that needs to be executed frequently
- To improve performance by precompiling and caching frequently executed statements
- To enforce security by restricting access to sensitive data or operations
- To implement complex data validation rules and data transformations
- To automate repetitive tasks and reduce the workload on the application layer
- To create a standard interface for data access and manipulation that can be reused across multiple applications

</blockquote>

</details>

---

17. How to write a stored procedure?


![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
To write a `stored procedure` in SQL, you can use the following syntax:

```sql
CREATE PROCEDURE procedure_name
    @parameter1 data_type,
    @parameter2 data_type,
    ...
AS
BEGIN
    /* SQL statements */
END
```

Here, `procedure_name` is the name of the stored procedure, and `@parameter1`, `@parameter2`, etc. are the input parameters that the procedure can accept. The `AS` keyword is used to start the body of the procedure, which contains the SQL statements that will be executed when the procedure is called.

</blockquote>

</details>

---

18. What is a UNION?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Answer</b></summary>
  
<blockquote>

`UNION` is a SQL operator used to combine the result sets of two or more SELECT statements into a single result set. The resulting data set will contain all the distinct rows from all the SELECT statements in the UNION. UNION operation is used when we want to combine two or more tables with the same structure into one table. The columns in each SELECT statement must be in the same order and must have compatible data types. 
</blockquote>

</details>

---

19. What is the difference between UNION and UNION ALL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Answer</b></summary>
  
<blockquote>
UNION and UNION ALL are used to combine the result sets of two or more SELECT statements, but there is a significant difference between them. 

- UNION returns only distinct values whereas UNION ALL returns all the rows, including duplicates.
- UNION operation eliminates duplicate rows from the result set, whereas UNION ALL does not.
- UNION requires more overhead compared to UNION ALL because it has to sort the combined result set to remove duplicates.
- UNION ALL is faster than UNION when combining large data sets because it does not have to perform a sort operation.

So, we use UNION when we want to combine two or more tables with the same structure and eliminate duplicate rows, whereas UNION ALL is used when we want to combine two or more tables with the same structure, including duplicates.
</blockquote>

</details>

---

20. What is the difference between clustered index and non-clustered index?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A clustered index determines the physical order of data in a table, which means it determines how the data is stored on disk. There can be only one clustered index per table, and it is automatically created when the primary key is defined. A non-clustered index, on the other hand, does not affect the physical order of data in a table. It is stored separately from the data and contains a sorted list of references to the data. Multiple non-clustered indexes can be created per table. 
</blockquote>

</details>

---

21. What are indexes in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Indexes are database structures that improve the performance of queries by enabling quick retrieval of data from the database. They are created on one or more columns of a table and contain a sorted list of values that reference the physical location of the data. Indexes are used to speed up data retrieval operations, such as searching, sorting, and grouping, by reducing the number of disk I/O operations required to access the data. However, indexes can also slow down write operations, such as INSERT, UPDATE, and DELETE, because the index must be updated whenever the data is changed. 
</blockquote>

</details>

---

22. Where would you place a COUNT() in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
You can place COUNT() function in the SELECT clause of a SQL query to return the number of rows that match the specified condition.

Example for COUNT() function in given below:

```sql
SELECT COUNT(*) FROM customers;
```
This will return the total number of rows in the table "customers".
</blockquote>

</details>

---

23. What are aggregate functions?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Aggregate functions are SQL functions that are used to perform calculations on a set of values and return a single value. The most commonly used aggregate functions in SQL are COUNT(), SUM(), AVG(), MIN(), and MAX().
</blockquote>

</details>

---


24. How do you use the MIN(), MAX() aggregation function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
The MIN() and MAX() functions are used to return the minimum and maximum value of a column in a table, respectively. 

Here's an example of using the MIN() function to find the minimum value in a table:

```sql
SELECT MIN(column_name)
FROM table_name;
```

Similarly, you can use the MAX() function to find the maximum value in a table:

```sql
SELECT MAX(column_name)
FROM table_name;
```

</blockquote>

</details>

---

25. Explain SQL GROUP BY clause.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `GROUP BY` clause in SQL is used to group rows based on one or more columns. When you use `GROUP BY`, the result set is divided into groups based on the values in the specified columns. You can then use aggregate functions, such as `SUM`, `COUNT`,` AVG`, `MIN`, or `MAX`, to perform calculations on each group.

For example, if you have a table of sales data that includes columns for Salesperson, Product, and SalesAmount, and you want to group the data by Salesperson and Product and display the total sales for each combination of Salesperson and Product, you could use the following SQL statement:

```sql
SELECT Salesperson, Product, SUM(SalesAmount) as TotalSales
FROM Sales
GROUP BY Salesperson, Product;
```

This statement groups the sales data by the Salesperson and Product columns and calculates the sum of the SalesAmount column for each group. The output includes the Salesperson, Product, and TotalSales columns.

</blockquote>

</details>

---

26 List the aggregate functions

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- **AVG():** This function is used to returns the average value from specified columns.
- **COUNT():** This function is used to returns the number of table rows, including rows with null values.
- **MAX():** This function is used to returns the largest value among the group.
- **MIN():** This function is used to returns the smallest value among the group.
- **SUM():** This function is used to returns the total summed values(non-null) of the specified column.

</blockquote>

</details>

---



27. Explain SQL GROUP BY clause.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The GROUP BY clause in SQL is used to group rows based on one or more columns. When you use GROUP BY, the result set is divided into groups based on the values in the specified columns. You can then use aggregate functions, such as SUM, COUNT, AVG, MIN, or MAX, to perform calculations on each group.

For example, if you have a table of sales data that includes columns for Salesperson, Product, and SalesAmount, and you want to group the data by Salesperson and Product and display the total sales for each combination of Salesperson and Product, you could use the following SQL statement:

```sql
SELECT Salesperson, Product, SUM(SalesAmount) as TotalSales
FROM Sales
GROUP BY Salesperson, Product;
```

This statement groups the sales data by the Salesperson and Product columns and calculates the sum of the SalesAmount column for each group. The output includes the Salesperson, Product, and TotalSales columns.

</blockquote>

</details>

---

28. What is the difference between GROUP BY and ORDER BY?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`GROUP BY` and `ORDER BY` are both clauses used in SQL, but they serve different purposes. 

`GROUP BY` is used to group rows based on one or more columns. When you use `GROUP BY`, the result set is divided into groups based on the values in the specified columns. You can then use aggregate functions, such as `SUM`, `COUNT`, `AVG`, `MIN`, or `MAX`, to perform calculations on each group.

`ORDER BY`, on the other hand, is used to sort the result set based on one or more columns. You can specify one or more columns in the `ORDER BY` clause and indicate whether you want the result set sorted in ascending or descending order for each column.

For example, if you have a table of customer orders with columns for OrderID, CustomerID, OrderDate, and OrderTotal, and you want to group the orders by customer and display the total order amount for each customer in descending order, you could use the following SQL statement:

```sql
SELECT CustomerID, SUM(OrderTotal) AS TotalAmount
FROM Orders
GROUP BY CustomerID
ORDER BY TotalAmount DESC;
```

This statement groups the orders by the CustomerID column and calculates the sum of the OrderTotal column for each customer group. It then orders the result set in descending order based on the TotalAmount column.

</blockquote>

</details>

---

29. List the scalar functions in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

SQL has a variety of built-in scalar functions that can be used to manipulate data in various ways. Here are some of the commonly used scalar functions in SQL:

- String Functions: `CONCAT`, `SUBSTRING`, `LENGTH`, `REPLACE`, and more.
- Numeric Functions: `ABS`, `CEILING`, `FLOOR`, `MOD`,and more.
- Date and Time Functions: `GETDATE`, `DATEADD`, `DATEDIFF`, YEAR.
- Aggregate Functions: COUNT, SUM, AVG, MIN, MAX, and more.
- Miscellaneous Functions: ISNULL, COALESCE, NULLIF, and more.

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

37. What is a schema in a database?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A schema in a database is a logical structure that represents the organization of data in a database. It defines the tables, columns, and relationships between the data, as well as the data types and other constraints for each column.

</blockquote>

</details>

---

38. What is an ERD?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An entity-relationship diagram (ERD) is a graphical representation of the relationships between entities in a database. It is used to design and model databases and to communicate the structure of a database to stakeholders. ERDs use symbols and notation to represent the entities, attributes, and relationships in the database.

</blockquote>

</details>

---

40. Consider a database schema for an online shopping application. The schema consists of the following tables:

 - Customers (customer_id, name, email, address)
 - Orders (order_id, customer_id, order_date, total_amount)
 - OrderItems (order_item_id, order_id, product_id, quantity, price)
 - Products (product_id, name, price, description)
 - Categories (category_id, name)

Write an SQL query to retrieve the total revenue generated by each category, ordered by the highest revenue first.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT c.name AS category, SUM(oi.quantity * oi.price) AS revenue
FROM Categories c
JOIN Products p ON c.category_id = p.category_id
JOIN OrderItems oi ON p.product_id = oi.product_id
GROUP BY c.name
ORDER BY revenue DESC;


```

</blockquote>

</details>

---

41. How do you grant or revoke privileges on database objects in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

you can grant or revoke privileges on database objects using the GRANT and REVOKE statements. Here's how you can use these statements:

To grant privileges:

```sql

GRANT privilege_name ON object_name TO user_or_role;

```

The privilege_name can be specific privileges such as SELECT, INSERT, UPDATE, DELETE, or ALL. The object_name represents the name of the database object (e.g., table, view, procedure) on which the privileges are granted. The user_or_role specifies the user or role to whom the privileges are granted.

For example, to grant SELECT and INSERT privileges on a table called "employees" to a user named "john":

```sql

GRANT SELECT, INSERT ON employees TO john;

```

To revoke privileges:

```sql
REVOKE privilege_name ON object_name FROM user_or_role;

```

The privilege_name, object_name, and user_or_role have the same meaning as in the GRANT statement.

For example, to revoke the INSERT privilege on the "employees" table from the user "john":

```sql

REVOKE INSERT ON employees FROM john;

```


</blockquote>

</details>

---
