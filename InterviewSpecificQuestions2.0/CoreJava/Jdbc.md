1. How does JDBC play a vital role in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `JDBC(Java Database Connectivity)` is a Java API, which is helpful in interacting with the database to retrieve, manipulate and process the data using SQL. 
- It will make use of JDBC drivers for connecting to the database. 
- JDBC can access tabular data stored in various types of relational databases such as Oracle, MySQL, MS Access, etc.

</blockquote>

</details>

---

2. What is the functionality of `ResultSet` in JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The `java.sql.ResultSet` interface represents the database result set, which is obtained after the execution of SQL query using Statement objects. 
- ResultSet objects maintains a cursor pointing to the current row of data in the result set. 
- Initially, the cursor is located before the first row. 
- Then the cursor is moved to the next row by using the `next()` method. The `next()` method can be used to iterate through the result set with the help of a while loop. 
- If there are no further rows, the `next()` method will return false.
- for example:

```java

ResultSet rs = con.executeQuery(sqlQuery);

```

</blockquote>

</details>

---

3. Why we need `JDBC driver` in JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- JDBC driver is a software component having various classes and interfaces, that enables the Java application to interact with a database.
- To connect with individual databases, It requires particular drivers for each specific database. 
- These drivers are provided by the database vendor in addition to the database. 
For example:
- MySQL Connector/J is the official JDBC driver for MySQL and we can locate the `mysql-connector-java-<version>-bin.jar` file among the installed files. 
- On windows, this file can be obtained at `C:\Program Files (x86)\MySQL\MySQL` `Connector J\mysql-connector-java-5.1.30-bin.jar`.
- JDBC driver of Oracle10G is `oJDBC14.jar` and it can be obtained in the installation directory of an Oracle at `…/Oracle/app/oracle/product/10.2.0/server/JDBC/lib` .
- JDBC driver provides the connection to the database. Also, it implements the protocol for sending the query and result between client and database.

</blockquote>

</details>
  
 ---
  
 4. What is the need of `DriverManager` in JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- JDBC DriverManager is a static class in Java, through which we manage the set of JDBC drivers that are available for an application to use.
- Multiple JDBC drivers can be used concurrently by an application. 
- By using a Uniform Resource Locator (URL), each application specifies a JDBC driver. When we load the JDBC Driver class into an application, it registers itself to the DriverManager by using `Class.forName()` or `DriverManager.registerDriver()`. 
- When we call `DriverManager.getConnection()` method by passing the details regarding database configuration, DriverManager will make use of registered drivers to obtain the connection and return it to the caller program.

</blockquote>

</details>
  
---
  
5. Which JDBC driver is fastest and used more commonly?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- JDBC Net pure Java driver(Type 4 driver) is the fastest driver for localhost and remote connections because it directly interacts with the database by converting the JDBC calls into vendor-specific protocol calls.

</blockquote>

</details>

---
  
6. Which data types are used for storing the image and file in the database table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `BLOB` data type is used to store the image in the database. 
- We can also store videos and audio by using the BLOB data type. 
- It stores the binary type of data. CLOB data type is used to store the file in the database. 
- It stores the character type of data.

</blockquote>

</details>

 ---
  
7. Explain why do we need stored procedure.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Stored procedure is a group of SQL queries that are executed as a single logical unit to perform a specific task.
- Name of the procedure should be unique since each procedure is represented by its name. For example, operations on an employee database like obtaining information about an employee could be coded as stored procedures that will be executed by an application. 
- Code for creating a stored procedure named `STUDENT_DETAILS`  is given below:

```java

DELIMITER $$
DROP PROCEDURE IF EXISTS `STUDENT`.`STUDENT_DETAILS`  $$
CREATE PROCEDURE `STUDENT`.`STUDENT_DETAILS`
  (IN STUDENT_ID INT, OUT STUDENT_DETAILS VARCHAR(255))
BEGIN
  SELECT first INTO STUDENT_DETAILS
  FROM Students
  WHERE ID = STUDENT_ID;
END $$
DELIMITER ;

```
- Stored procedures are called using CallableStatement class available in JDBC API. Below given code demonstrates this:

```java

CallableStatement cs = con.prepareCall("{call STUDENT_DETAILS(?,?)}");
ResultSet rs = cs.executeQuery();

```
</blockquote>

</details>

---
  
8. Differentiate ODBC and JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- ODBC(Open Database Connectivity):	
  - ODBC can be used for languages like C, C++, Java, etc.
  - We can use ODBC only for the Windows platform; thus it is platform-dependent.	
  - Most of the ODBC Drivers developed in native languages like C, C++	
  - It is not recommended to use ODBC for Java applications, because of low performance due to internal conversion.	
  - ODBC is procedural.	
- JDBC(Java Database Connectivity):
  - JDBC is used only for the Java language
  - We can use JDBC on any platform, thus it is platform-independent
  - JDBC drivers are developed using the Java language
  - It is highly recommended to use JDBC for Java applications because there are no performance issues.
  - JDBC is Object Oriented.

</blockquote>

</details>
  
---
  
9. What is `Rowset` in a Resultset?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- A RowSet is an object that encapsulates a row set from either JDBC result sets or tabular data sources such as files or spreadsheets. 
- It supports component-based development models like JavaBeans, with the help of a standard set of properties and event notifications. RowSet is easier and flexible to use. It is Scrollable and Updatable by default.

</blockquote>

</details>
  
---

10. Describe the different types of JDBC drivers in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- There are four types of JDBC drivers in Java. 
- They are:
  - `Type I`: 
    - JDBC - ODBC bridge driver: It acts as an interface between the client and database server. When a user uses a Java application to send requests to the database using JDBC–ODBC bridge, it converts the JDBC API into ODBC API and then sends it to the database. When the result is received from the database, it is sent to ODBC API and then to JDBC API.It is platform-dependent because it uses ODBC which depends on the native library of the operating system. In this, JDBC–ODBC driver should be installed in every client system and database must support for ODBC driver. It is easier to use but it gives low performance because it involves the conversion of JDBC method calls to the ODBC method calls.
  - `Type II`: 
    - Native API – Partially Java Driver:It uses libraries of the client-side of the database. This Type II Driver converts the JDBC method calls to native calls of the database native API.When the database gets the requests from the user, the requests are processed and sends the results back in the native format which is then converted into JDBC format and pass it to the Java application.It was instantly adopted by the database vendors because it was quick and cheaper to implement. 
  - `Type III`: 
    - Network Protocol - Fully Java Driver: It uses to send the JDBC method calls to an intermediate server. The intermediate server communicates with the database on behalf of JDBC. The application server converts the JDBC calls either directly or indirectly to the database protocol which is vendor-specific.
  - `Type IV`: 
    - Thin Driver - Fully Java Driver: It is platform-independent since it is written fully in Java. It can be installed inside the Java Virtual Machine(JVM) of the client, so there is no need of installing any software on the client or server side. This drive architecture is having all the logic to communicate directly with the database in a single driver.It provides better performance compared to other driver types. It permits easy deployment. It is developed by the database vendor itself so that programmers can use it directly without any dependencies on other sources.Type IV driver is directly implemented and it directly converts JDBC calls into vendor-specific database protocol. Most of the JDBC Drivers used today are type IV drivers.

</blockquote>

</details>

---
  
11. Explain the different types of statements in JDBC? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>

<blockquote>

There are 3 types of JDBC Statements which are discussed below:

- `java.sql.Statement`:Statement object compiles and executes no matter whether there is a change in the query syntax or not. for Example: if you are inserting 100 employees your insert query will remain same but Statement object will compile your insert query again and again for 100 times and runs.
  
```java
Statement st = conn.createStatement( );
ResultSet rs = st.executeQuery();
  
```
- `java.sql.PreparedStatement`: This type of statement is designed in such a way that it compiles only when there is a syntactic change in your query. For Example: This will compile the insert statement once and executes it 100 times.

```java
String s1 = "Update emp SET salary = ? WHERE designation = ?";
PreparedStatement  ps = conn.prepareStatement(s1);
ResultSet rs = ps.executeQuery();
  
 ```
  
- `java.sql.CallableStatement`: This is sub interface of Prepared Statement and has been designed to call up PLSQL stored procedures and functions.

```java
CallableStatement cs = con.prepareCall("{call STUDENT_DETAILS}");
ResultSet rs = cs.executeQuery();

```
</blockquote>

</details>
  
---
  
12. What are the interfaces and classes in JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The java.sql package contains different interfaces and classes for JDBC API. 
- They are:
  - `Connection` object is an interface which is created by using getConnection() method of DriverManager class. DriverManager is the factory for connection.
  - `Statement` object is an interface which is created by using createStatement() method of the Connection class. The Connection interface is the factory for Statement.
  - `PreparedStatement` object is an interface which is created by using prepareStatement() method of Connection class. It is used for executing the parameterized query.
  - `ResultSet` object maintains a cursor pointing to a table row,the cursor points before the first row. The executeQuery() method of the Statement interface returns the object of ResultSet.
  - `ResultSetMetaData` interface object contains the details about the data of the table such as number of columns, name of the column, column type etc. The getMetaData() method of ResultSet returns the ResultSetMetaData object.
  - `DatabaseMetaData` is an interface that has methods to get metadata of a database, like name of the database product, version of database product, driver name, name of the total number of views, name of the total number of tables, etc. The getMetaData() method that belongs to Connection interface returns the DatabaseMetaData object.
  - `CallableStatement` interface is useful for calling the stored procedures and functions. We can have business logic on the database through the usage of stored procedures and functions, which will be helpful for the improvement in the performance as these are pre-compiled. The prepareCall() method that belongs to the Connection interface returns the object of CallableStatement.
  - `DriverManager` has available drivers which handles establishing a connection between a database and the relevant driver. It contains various methods to keep the interaction between the user and drivers.
  - `BLOB` stands for Binary Large Object. It represents a collection of binary data such as images, audio, and video files, etc., which is stored as a single entity in the DBMS (Database Management System).
  - `CLOB` stands for Character Large Object. This data type is used by multiple database management systems to store character files. It is the same as BLOB except for the difference, instead of binary data, CLOB represents character stream data such as character files, etc.


</blockquote>

</details>

---

13. What is Batch processing in JDBC? How to perform it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Batch processing is the process of executing multiple SQL statements in one transaction. 
- For example, consider the case of loading data from CSV(Comma-Separated Values) files to relational database tables. 
- Instead of using Statement or PreparedStatement, we can use batch processing which executes the bulk of queries as a single transcation for a database.
- It reduces the communication time and improves performance.
- It is easier to process a huge amount of data and consistency of data is also maintained.
- It is much faster than executing a single statement at a time because of the fewer number of database calls.
- To perform batch processing, `addBatch()` and `executeBatch()` methods are used,which are available in the Statement and PreparedStatement classes of JDBC

</blockquote>

</details>
  
---
  
14. Differentiate Statement and PreparedStatement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Statement:	
  - The query is compiled every time when we run the program. It is used in the situation where we need to run the SQL query without providing parameters at runtime. Its performance is less compared to PreparedStatement.It is suitable for executing DDL statements such as Create, Alter, Drop and Truncate.	It cannot be used for storing/retrieving images and files in the database. It executes static SQL statements.It is less secured because it enforces SQL injection.	
- PreparedStatement:
  - The query is compiled only once. It is used when we want to give input parameters to the query at runtime. It provides better performance than Statement, as it executes the pre-compiled SQL statements. It is suitable for executing DML statements such as Insert, Update and Delete. It can be used for storing/retrieving images and files in the database. It executes pre-compiled SQL statements. It is more secured as they use to bind variables, which can prevent SQL injection.

</blockquote>

</details>
  
---
  
15. What is `execute()`,`executeQuery()` and `executeUpdate()` methods in JDBC?Explain it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `execute()`:It can be used for any SQL statements. It returns the boolean value TRUE if the result is a ResultSet object and FALSE when there is no ResultSet object. Used for executing both Select and non-Select queries.	
- `executeQuery()`:It is used to execute SQL Select queries. It returns the ResultSet object which contains the data retrieved by the SELECT statement. Used for executing only the Select Query.
- `executeUpdate()`:It is used to execute the SQL statements such as Insert or Update or Delete which will update or modify the database data.It returns an integer value which represents the number of affected rows where 0 indicates that the query returns null.It is used for executing only a non-Select query.
		

</blockquote>

</details>
  
---
  
16. How are getter and setter methods used in ResultSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Getter methods: These are used for retrieving the particular column values of the table from ResultSet. As a parameter, either the column index value or column name should be passed and the getter method is represented as getXXX() methods,for example: `int getInt(string Column_Name)` statement is used to retrieve the value of the specified column index and the return type is an int data type.
- Setter Methods: These methods are used to set the value in the database. It is almost similar to getter methods, but here it requires to pass the data/values for the particular column to insert into the database and the column name or index value of that column and setter method is represented as setXXX() methods,for example: `void setInt(int Column_Index, int Data_Value)` statement is used to insert the value of the specified column index with an int value.
		
</blockquote>

</details>
  
---
  
17. What do you mean by "Dirty read" in terms of database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Dirty read implies the meaning "read the value which may or may not be correct". 
- In the database, when a transaction is executing and changing some field value, at the same time another transaction comes and reads the changed field value before the first transaction could commit or rollback the value, which may cause an invalid value for that particular field. 
- This situation is known as a dirty read. For ex: where Transaction 2 changes a row but does not commit the changes made. Then Transaction 1 reads the uncommitted data. 
- Now, if Transaction 2 goes for roll backing its changes (which is already read by Transaction 1) or updates any changes to the database, then the view of the data may be wrong in the records related to Transaction 1. 
		
</blockquote>

</details>

  
---
  
18. Describe the steps for establishing a JDBC connection in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Loading the Driver:When we need to load or register the driver before using it in the program. Registration must be done once in your program. 
  - You can register a driver by using any one of the two methods mentioned below:
    - `Class.forName()`:We load the driver’s class file into memory during runtime.`Class.forName("com.mysql.JDBC.Driver")` is used to load the MySQL driver.However, this statement is no longer needed, because as you place the MySQL JDBC driver JAR file into the classpath of your program, the driver manager can find and load the driver.
    - `DriverManager.registerDriver()`: DriverManager is a built-in Java class with a static member register. Here we will be calling the constructor of the driver class during compile time.For registering the MySQL driver, use the below-given code:
    - `DriverManager.registerDriver((new com.mysql.JDBC.Driver());`
- Connection:After loading the driver into the program, establish connections using the code given below:
  - `Connection con = DriverManager.getConnection(url,user,password);`
  - `con`: Reference to a Connection interface.
  - `url`: Uniform Resource Locator.
  - `user`: Username from which SQL command prompt is accessed.
  - `password`: Password from which SQL command prompt is accessed.
  - url in MySQL can be created as follows:
    - `String url = "JDBC:mysql://localhost:3306/demo1";`
  - Where localhost represents hostname or IP address of the MySQL server, 3306 port number of the server and by default, it is 3306, test1 is the name of the database on the server.

- Create a statement:Once a connection establishment is done, you can interact with the database. 
  - The `Statement`, `PreparedStatement`, and `CallableStatement` JDBC interfaces will define the methods that permit you to send SQL commands and receive data from the database.We can use JDBC Statement as follows:
  - `Statement st = con.createStatement();`
  - Here, con is a reference to the Connection interface used in the earlier step.

- Execute the query: query means an SQL query. We can have various types of queries.for ex:Query for updating,
  inserting and data retrieval a table in a database. The `executeQuery()` method that belongs to the Statement interface is used for executing queries related to values retrieval from the database. This method returns the ResultSet object which can be used to get all the table records.The `executeUpdate(sql_query)` method of the Statement interface is used for executing queries related to the update/insert operation.For Example:
```java

    int s = st.executeUpdate(sql);
    if (s==1)
        System.out.println("Data inserted successfully : "+sql);
    else
        System.out.println("Data insertion failed");
    Here SQL is the SQL query of string type.
```
- Close the connection:We have to send the data to the location specified and now we are at the end of our task completion.Closing the connection, objects of Statement and ResultSet will be automatically closed. The `close()` method of the Connection interface is used for closing the connection. 

```java

con.close();

```
		
</blockquote>

</details>

---
  
19. Explain the implementation of JDBC MySQL database connection with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

```java

import java.sql.*;  
class JDBCMySql{  
   public static void main(String args[]){      
       String url = "JDBC:mysql://localhost:3306/demo1";
       String user = "root";
       String password = "root";
       try{  
           Class.forName("com.mysql.JDBC.Driver");
           Connection con=DriverManager.getConnection(url,user,password);
           Statement st = con.createStatement();
           ResultSet rs = st.executeQuery("select * from student");  
           while(rs.next())  
               System.out.println(rs.getInt(1)+" "+rs.getString(2)+" "+rs.getString(3));  
           con.close();  
       }
       catch(Exception e)
       { 
           System.out.println(e);
       }  
   }  
}  

```
		
</blockquote>

</details>
  
---
  
20. Explain the implementation to call Stored procedures in JDBC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Stored procedures are a set of SQL queries that are compiled in the database and will be executed from JDBC API. For executing Stored procedures in the database, JDBC CallableStatement can be used. The syntax for initializing a CallableStatement is given below:

```java

CallableStatement cs = con.prepareCall("{call insertStudent(?,?,?,?,?)}");
stmt.setInt(1, studentid);
stmt.setString(2, studentname);
stmt.setString(3, studentphone);
stmt.setString(4, studentaddress);
stmt.setString(5, studentfees);
cs.registerOutParameter(5, java.sql.Types.VARCHAR);
cs.executeUpdate();

```

We must register the OUT parameters before executing the CallableStatement.
		
</blockquote>

</details>

21. When does "No suitable driver" error occur in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- "No suitable driver" error occurs during a call to the DriverManager.getConnection() method, when it is unable to load the appropriate JDBC drivers before calling the getConnection() method.
- It can specify an invalid or wrong JDBC URL, which cannot be recognized by the JDBC driver.
- When one or more shared libraries required by the JDBC bridge cannot be loaded.
		
</blockquote>

</details>

---
	
22. Explain the types of JDBC architecture?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

JDBC has 2 types of architecture models to access the database. They are:
- Two-tier Architecture: This architecture connects java programs explicitly to the database. It doesn’t require any mediator such as an application server for connecting with the database except the JDBC driver. It is also called client-server architecture.	
- Three-tier Architecture: This architecture has no explicit communication between the JDBC driver or java application with the database. It will make use of an application server as a mediator between them. Java code will send the request to an application server, then the server will send it to the database and receive the response from the database.

</blockquote>

</details>

---
	
23. Explain the ACID properties in JDBC Transaction Management and why is it needed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The sequence of SQL statements served as a single unit that is called a transaction. Transaction Management places an important role in RDBMS-oriented applications to maintain data consistency and integrity.Transaction Management can be described by using ACID properties. ACID stands for Atomicity, Consistency, Isolation, and Durability.
- Atomicity: If all queries are successfully executed, then only data will be committed to the database.
- Consistency: It ensures bringing the database into a consistent state after any transaction.
- Isolation:It ensures that the transaction is isolated from other transactions.
- Durability:If a transaction has been committed once, it will remain always committed, even in the situation of errors, power loss, etc.

- Need for Transaction Management: When creating a connection to the database, the auto-commit mode will be selected by default. This implies that every time when the request is executed, it will be committed automatically upon completion. We might want to commit the transaction after the execution of few more SQL statements. In such a situation, we must set the auto-commit value to False. So that data will not be able to commit before executing all the queries. In case if we get an exception in the transaction, we can `rollback()` changes made and make it like before.

</blockquote>

</details>

---
24. Explain the Transaction Management methods in JDBC.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The connection interface is having 5 methods for transaction management. They are given below:

`setAutocommit()`:The value of AutoCommit is set to true by default.when the SQL statement executes, it will be committed automatically. By using this method we can set the value for AutoCommit.
	
Syntax: `conn.setAutoCommit(boolean_value)`;
boolean_value is set to true for enabling autocommit mode for the connection, false for disabling it.
	
`commit()`:The `commit()` method is used for committing the data. When the SQL statement executes, we can call the `commit()` method. It will commit the changes made by the SQL statement.
	
Syntax: `conn.commit()`;
	
`rollback()`:The `rollback()` method is used to undo the changes made till the last commit has occurred. If we face any problem or exception in the SQL statements execution flow, we may roll back the transaction.
	
Syntax: `conn.rollback()`;
	
`setSavepoint()`:If you have set a savepoint in the transaction i.e.,group of SQL statements, you can use the `rollback()` method to undo all the changes till the savepoint or after the `savepoint()`, if something goes wrong within the current transaction. The `setSavepoint()` method is used to create a new savepoint which refers to the current state of the database within the transaction.
	
Syntax:`Savepoint sp= conn.setSavepoint("Mysavepoint");`
	
`releaseSavepoint()`:It is used for deleting or releasing the created savepoint.
	
Syntax:`conn.releaseSavepoint("Mysavepoint");`

</blockquote>

</details>
	
---

25. Explain the common exceptions in JDBC.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `java.sql.SQLException`:It is the base class for JDBC exceptions.
- `java.sql.BatchUpdateException`: It occurs during the batch update operation. It depends on the JDBC driver type that the base SQLException may throw instead.
- `java.sql.SQLWarning`:It is displayed as a warning message of various SQL operations.
- `java.sql.DataTruncation`:This exception occurs when data values are unexpectedly truncated due to exceeding MaxFieldSize.

</blockquote>

</details>

---
	
26. How two-phase commit is performed in JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Two-phase commit is useful for a distributed environment where numerous processes take part in the distributed transaction process.A transaction is executing and it is affecting multiple databases then a two-phase commit will be used to make sure that all databases are synchronized with each other.
The main process or co-ordinator process take a vote of all other process that they have completed their process successfully and ready to commit, if all the votes are "yes" then they continue for the next phase. And if "No" then rollback will be performed. As per vote, if all the votes are "yes" then commit is done.when any transaction changes multiple databases after transaction execution, it will issue a pre-commit command on each database and all databases will send an acknowledgment. Based on acknowledgment, if all are positive transactions then it will issue the commit command otherwise rollback will be done

</blockquote>

</details>

---
	
27. How to create a table dynamically from java using JDBC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

```java

import java.io.*;
import java.sql.*;

public class dynamicJDBCtable{
 public static void main(String[] args)throws SQLException,IOException{
   BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
   Class.forName("com.mysql.JDBC.Driver");
   Connection con=DriverManager.getConnection(url,user,password);
   Statement st = con.createStatement();
   System.out.println(“Enter table name”);
   String tablename = br.readLine();
   st.executeUpdate("create table"+tablename+"(studentno number,studentname varchar2(10),studentphone number,studentaddress varchar2(20))");
   System.out.println("Table created successfully");
   con.close();
 }
}

```

</blockquote>

</details>

---
	
28. Is it possible to connect to multiple databases using a single statement object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

It is possible to connect to multiple databases, at the same time, but it depends on the specific driver.To update and extract data from the different database we can use the single statement. But we need middleware to deal with multiple databases or a single database.

</blockquote>

</details>

---
	
29. How do you insert images into database using JDBC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Images in the database inserted using the BLOB datatype wherein the image stored as a byte stream. Below code is showing how to insert the image into DB.

```java

Connection con = null;
PreparedStatement ps = null;
InputStream is = null;

Class.forName("com.mysql.JDBC.Driver");
Connection con=DriverManager.getConnection(url,user,password);
ps = con.prepareCall("insert into student values (?,?)");
ps.setInt(1,401);
is = new FileInputStream(new File("student_img.jpg"));
ps.setBinaryStream(2, is);
int count = ps.executeUpdate();


```

</blockquote>

</details>

---

30. What is the jdbc connection string and how is it used, give an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A JDBC (Java Database Connectivity) connection string is a string that contains information required to connect to a database. It typically includes information such as the database server name or IP address, the port number, the database name, and any additional connection parameters.

Here is an example JDBC connection string for connecting to a MySQL database:
```java
jdbc:mysql://localhost:3306/mydatabase?user=root&password=mypassword
```
In this example, the connection string contains the following information:

- jdbc:mysql://: This specifies the JDBC driver to use (mysql) and the protocol to use (jdbc).

- localhost: This specifies the name or IP address of the database server.

- 3306: This specifies the port number on which the database server is listening.

- mydatabase: This specifies the name of the database to connect to.

- user=root: This specifies the username to use when connecting to the database.

- password=mypassword: This specifies the password to use when connecting to the database.

To use this connection string in Java, we would typically create a Connection object using the DriverManager.getConnection() method, like this:
```java
String url = "jdbc:mysql://localhost:3306/mydatabase?user=root&password=mypassword";
Connection conn = DriverManager.getConnection(url);
```
This code uses the url string to connect to the MySQL database and creates a Connection object that can be used to execute SQL queries against the database.
</blockquote>

</details>

---

31. What types of operation do you use in result sets?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

In JDBC, a ResultSet object represents a set of rows returned by a SQL query. It provides methods to iterate over the rows and retrieve data from each column. Some of the common operations that you can perform on a ResultSet include:

- Moving the cursor: You can move the cursor to the next row using the next() method. You can also move the cursor to a specific row using the absolute() or relative() methods.

- Retrieving data: You can retrieve data from each column of the current row using methods like getString(), getInt(), getDouble(), etc. These methods take the column index or column name as a parameter.

- Updating data: You can update the data in a ResultSet by calling the updateXXX() methods (such as updateString(), updateInt(), etc.) to modify the value of a column in the current row. After updating the data, you need to call the updateRow() method to save the changes to the database.

- Inserting data: You can insert a new row into a ResultSet by calling the moveToInsertRow() method to position the cursor on the insert row, and then calling the updateXXX() methods to set the values of the columns. Finally, you need to call the insertRow() method to insert the new row into the database.

- Deleting data: You can delete the current row from a ResultSet by calling the deleteRow() method. Note that this operation actually deletes the row from the database.

- Closing the ResultSet: After you have finished processing a ResultSet, you should close it by calling the close() method. This releases any resources held by the ResultSet, such as database connections or network sockets.

</blockquote>

</details>

---
32. What is sql injection? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

SQL injection is a type of security vulnerability that can occur when using JDBC or any other technology that allows the use of dynamic SQL statements. It happens when an attacker is able to inject malicious SQL code into a query, potentially allowing them to access, modify or delete data from the database without proper authorization.

For example, consider the following code that constructs a SQL query using user input:
```java
String username = request.getParameter("username");
String password = request.getParameter("password");
String sql = "SELECT * FROM users WHERE username = '" + username + "' AND password = '" + password + "'";
PreparedStatement stmt = conn.prepareStatement(sql);
ResultSet rs = stmt.executeQuery();
```
In this code, the username and password parameters are concatenated directly into the SQL query, which makes it vulnerable to SQL injection attacks. An attacker can craft a malicious input value that includes SQL code, such as username = 'admin'; -- which comments out the rest of the query and allows the attacker to log in as an administrator without a password.

To prevent SQL injection attacks, you should always use prepared statements or parameterized queries instead of building SQL queries using string concatenation. This ensures that user input is treated as data rather than executable code, and reduces the risk of malicious SQL injection.

</blockquote>

</details>

---
33. How do you prevent SQL injection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Here is an example of how to prevent SQL injection by using a prepared statement instead of building a SQL query using string concatenation:
```java
String username = request.getParameter("username");
String password = request.getParameter("password");
String sql = "SELECT * FROM users WHERE username = ? AND password = ?";
PreparedStatement stmt = conn.prepareStatement(sql);
stmt.setString(1, username);
stmt.setString(2, password);
ResultSet rs = stmt.executeQuery();
```
In this code, the sql variable contains placeholders (?) for the username and password values. Instead of concatenating the values directly into the SQL query, we use a PreparedStatement object to set the values of the placeholders. This ensures that user input is treated as data rather than executable code, and reduces the risk of SQL injection.

Note that this is just a simple example to illustrate the use of prepared statements. In practice, you should always use input validation and sanitization techniques to ensure that user input is safe and does not contain any malicious code.

</blockquote>

</details>

---
34. How to connect using JDBC to AWS?  

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

To connect to an Amazon Web Services (AWS) Relational Database Service (RDS) instance using JDBC, you will need to perform the following steps:

- Obtain the endpoint and port number of your RDS instance from the AWS Management Console.

- Download and install the appropriate JDBC driver for your RDS instance's database engine. You can download the JDBC driver from the database engine's official website or from the AWS documentation.

- Add the JDBC driver JAR file to your Java project's classpath.

- Use the following code to create a JDBC connection to your RDS instance:
```java
String dbURL = "jdbc:mysql://<endpoint>:<port>/<database>";
String username = "<username>";
String password = "<password>";
Connection conn = DriverManager.getConnection(dbURL, username, password);
```
Replace `<endpoint>`, `<port>`, `<database>`, `<username>`, and `<password>` with the appropriate values for your RDS instance. For example:
```java
String dbURL = "jdbc:mysql://my-db-instance.abcdefg123.us-east-1.rds.amazonaws.com:3306/mydb";
String username = "myusername";
String password = "mypassword";
Connection conn = DriverManager.getConnection(dbURL, username, password);
```
Note that you will need to configure your RDS instance's security group to allow incoming connections from the IP address or range of IP addresses that your Java application will be running on. You can do this from the AWS Management Console by adding an inbound rule to the security group.

</blockquote>

</details>

---
