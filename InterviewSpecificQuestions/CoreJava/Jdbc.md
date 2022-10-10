1.How JDBC plays a vital role in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `JDBC(Java Database Connectivity)` is a Java API, which is helpful in interacting with the database to retrieve, manipulate and process the data using SQL. 
- It will make use of JDBC drivers for connecting to the database. 
- JDBC can access tabular data stored in various types of relational databases such as Oracle, MySQL, MS Access, etc.

</blockquote>

</details>

---

2.What is the functionality of `ResultSet` in JDBC?

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

3.Why we need `Jdbc driver` in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Jdbc driver is a software component having various classes and interfaces, that enables the Java application to interact with a database.
- To connect with individual databases, It requires particular drivers for each specific database. 
- These drivers are provided by the database vendor in addition to the database. 
For example:
- MySQL Connector/J is the official Jdbc driver for MySQL and we can locate the `mysql-connector-java-<version>-bin.jar` file among the installed files. 
- On windows, this file can be obtained at `C:\Program Files (x86)\MySQL\MySQL` `Connector J\mysql-connector-java-5.1.30-bin.jar`.
- Jdbc driver of Oracle10G is `ojdbc14.jar` and it can be obtained in the installation directory of an Oracle at `…/Oracle/app/oracle/product/10.2.0/server/jdbc/lib` .
- Jdbc driver provides the connection to the database. Also, it implements the protocol for sending the query and result between client and database.

</blockquote>

</details>
  
 ---
  
 4.What is the need of `DriverManager` in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Jdbc DriverManager is a static class in Java, through which we manage the set of Jdbc drivers that are available for an application to use.
- Multiple JDBC drivers can be used concurrently by an application. 
- By using a Uniform Resource Locator(URL), each application specifies a Jdbc driver.When we load the JDBC Driver class into an application, it registers itself to the DriverManager by using `Class.forName()` or `DriverManager.registerDriver()`. 
- When we call `DriverManager.getConnection()` method by passing the details regarding database configuration, DriverManager will make use of registered drivers to obtain the connection and return it to the caller program.

</blockquote>

</details>
  
---
  
5.Which Jdbc driver is fastest and used more commonly?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Jdbc Net pure Java driver(Type 4 driver) is the fastest driver for localhost and remote connections because it directly interacts with the database by converting the Jdbc calls into vendor-specific protocol calls.

</blockquote>

</details>

---
  
6.Which data types are used for storing the image and file in the database table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `BLOB` data type is used to store the image in the database. 
- We can also store videos and audio by using the BLOB data type. 
- It stores the binary type of data.CLOB data type is used to store the file in the database. 
- It stores the character type of data.

</blockquote>

</details>

 ---
  
 7.Why we need stored procedure? Explain it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Stored procedure is a group of SQL queries that are executed as a single logical unit to perform a specific task.
- Name of the procedure should be unique since each procedure is represented by its name.For example, operations on an employee database like obtaining information about an employee could be coded as stored procedures that will be executed by an application. 
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
  
8.How can you differentiate ODBC and JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- ODBC(Open Database Connectivity):	
  - ODBC can be used for languages like C, C++, Java, etc.
  - We can use ODBC only for the Windows platform, thus it is platform-dependent.	
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
  
9.What is `Rowset` in a Resultset?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- A RowSet is an object that encapsulates a row set from either Jdbc result sets or tabular data sources such as files or spreadsheets. 
- It supports component-based development models like JavaBeans, with the help of a standard set of properties and event notifications.RowSet is easier and flexible to use.It is Scrollable and Updatable by default.

</blockquote>

</details>
  
---

10.Describe the different types of Jdbc drivers in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- There are four types of JDBC drivers in Java. 
- They are:
  - `Type I`: 
    - Jdbc - Odbc bridge driver:It acts as an interface between the client and database server. When a user uses a Java application to send requests to the database using Jdbc–Odbc bridge, it converts the Jdbc API into Odbc API and then sends it to the database. When the result is received from the database, it is sent to Odbc API and then to Jdbc API.It is platform-dependent because it uses Odbc which depends on the native library of the operating system. In this, Jdbc–Odbc driver should be installed in every client system and database must support for Odbc driver.It is easier to use but it gives low performance because it involves the conversion of Jdbc method calls to the Odbc method calls.
  - `Type II`: 
    - Native API – Partially Java Driver:It uses libraries of the client-side of the database. This Type II Driver converts the Jdbc method calls to native calls of the database native API.When the database gets the requests from the user, the requests are processed and sends the results back in the native format which is then converted into Jdbc format and pass it to the Java application.It was instantly adopted by the database vendors because it was quick and cheaper to implement. 
  - `Type III`: 
    - Network Protocol - Fully Java Driver: It uses to send the Jdbc method calls to an intermediate server. The intermediate server communicates with the database on behalf of Jdbc. The application server converts the Jdbc calls either directly or indirectly to the database protocol which is vendor-specific.
  - `Type IV`: 
    - Thin Driver - Fully Java Driver: It is platform-independent since it is written fully in Java. It can be installed inside the Java Virtual Machine(JVM) of the client, so there is no need of installing any software on the client or server side. This drive architecture is having all the logic to communicate directly with the database in a single driver.It provides better performance compared to other driver types. It permits easy deployment. It is developed by the database vendor itself so that programmers can use it directly without any dependencies on other sources.Type IV driver is directly implemented and it directly converts JDBC calls into vendor-specific database protocol. Most of the Jdbc Drivers used today are type IV drivers.

</blockquote>

</details>

---
  
11.Explain the different types of statements in Jdbc? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are 3 types of JDBC Statements which are discussed below:

- `java.sql.Statement`:Statement object compiles and executes no matter whether there is a change in the query syntax or not. for example:if you are inserting 100 employees your insert query will remain same but Statement object will compile your insert query again and again for 100 times and runs.
  
```java
Statement st = conn.createStatement( );
ResultSet rs = st.executeQuery();
  
```
- `java.sql.PreparedStatement`: This type of statement is designed in such a way that it compiles only when there is a syntatical change in your query. for example:this will compile the insert statement once and executes it 100 times.

```java
String s1 = "Update emp SET salary = ? WHERE designation = ?";
PreparedStatement  ps = conn.prepareStatement(s1);
ResultSet rs = ps.executeQuery();
  
 ```
  
- `java.sql.CallableStatement`: This is sub interface of PreparedStatement and has been designed to call up PLSQL stored procedures and functions.

```java
CallableStatement cs = con.prepareCall("{call STUDENT_DETAILS}");
ResultSet rs = cs.executeQuery();

```
</blockquote>

</details>
  
---
  
12.What are the interfaces and classes in Jdbc? Explain it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- The java.sql package contains different interfaces and classes for JDBC API. 
- They are:
  - `Connection` object is an interface which is created by using getConnection() method of DriverManager class. DriverManager is the factory for connection.
  - `Statement` object is an interface which  is created by using createStatement() method of the Connection class. The Connection interface is the factory for Statement.
  - `PreparedStatement` object is an interface which is created by using prepareStatement() method of Connection class. It is used for executing the parameterized query.
  - `ResultSet` object maintains a cursor pointing to a table row,the cursor points before the first row. The executeQuery() method of the Statement interface returns the object of ResultSet.
  - `ResultSetMetaData` interface object contains the details about the data of the table such as number of columns, name of the column, column type etc. The getMetaData() method of ResultSet returns the ResultSetMetaData object.
  - `DatabaseMetaData` is an interface that has methods to get metadata of a database, like name of the database product, version of database product, driver name, name of the total number of views, name of the total number of tables, etc. The getMetaData() method that belongs to Connection interface returns the DatabaseMetaData object.
  - `CallableStatement` interface is useful for calling the stored procedures and functions. We can have business logic on the database through the usage of stored procedures and functions, which will be helpful for the improvement in the performance as these are pre-compiled. The prepareCall() method that belongs to the Connection interface returns the object of CallableStatement.
  - `DriverManager` has available drivers which handles establishing a connection between a database and the relevant driver. It contains various methods to keep the interaction between the user and drivers.
  - `BLOB` stands for Binary Large Object. It represents a collection of binary data such as images, audio, and video files, etc., which is stored as a single entity in the DBMS(Database Management System).
  - `CLOB` stands for Character Large Object. This data type is used by multiple database management systems to store character files. It is the same as BLOB except for the difference, instead of binary data, CLOB represents character stream data such as character files, etc.


</blockquote>

</details>

---

13.What is Batch processing in Jdbc?How to perform it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Batch processing is the process of executing multiple SQL statements in one transaction. 
- For example, consider the case of loading data from CSV(Comma-Separated Values) files to relational database tables. 
- Instead of using Statement or PreparedStatement, we can use batch processing which executes the bulk of queries as a single transcation for a database.
- It reduces the communication time and improves performance.
- It is easier to process a huge amount of data and consistency of data is also maintained.
- It is much faster than executing a single statement at a time because of the fewer number of database calls.
- To perform batch processing, `addBatch()` and `executeBatch()` methods are used,which are available in the Statement and PreparedStatement classes of Jdbc

</blockquote>

</details>
  
---
  
14.How can you differentiate Statement and PreparedStatement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Statement:	
  - The query is compiled every time when we  run the program.It is used in the situation where we need to run the SQL query without providing parameters at runtime.It's performance is less compared to PreparedStatement.It is suitable for executing DDL statements such as Create, Alter, Drop and Truncate.	It cannot be used for storing/retrieving images and files in the database.It executes static SQL statements.It is less secured because it enforces SQL injection.	
- PreparedStatement:
  - The query is compiled only once.It is used when we want to give input parameters to the query at runtime.It provides better performance than Statement, as it executes the pre-compiled SQL statements.It is suitable for executing DML statements such as Insert, Update and Delete.It can be used for storing/retrieving images and files in the database.It executes pre-compiled SQL statements.It is more secured as they use to bind variables, which can prevent SQL injection.

</blockquote>

</details>
  
---
  
15.What is `execute()`,`executeQuery()` and `executeUpdate()` methods in Jdbc?Explain it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `execute()`:It can be used for any SQL statements.It returns the boolean value TRUE if the result is a ResultSet object and FALSE when there is no ResultSet object.Used for executing both Select and non-Select queries.	
- `executeQuery()`:It is used to execute SQL Select queries.It returns the ResultSet object which contains the data retrieved by the SELECT statement.Used for executing only the Select Query.
- `executeUpdate()`:It is used to execute the SQL statements such as Insert or Update or Delete which will update or modify the database data.It returns an integer value which represents the number of affected rows where 0 indicates that the query returns null.It is used for executing only a non-Select query.
		

</blockquote>

</details>
  
---
  
16.How getter and setter methods used in ResultSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Getter methods: These are used for retrieving the particular column values of the table from ResultSet. As a parameter, either the column index value or column name should be passed and the getter method is represented as getXXX() methods,for example: `int getInt(string Column_Name)` statement is used to retrieve the value of the specified column index and the return type is an int data type.
- Setter Methods: These methods are used to set the value in the database. It is almost similar to getter methods, but here it requires to pass the data/values for the particular column to insert into the database and the column name or index value of that column and setter method is represented as setXXX() methods,for example: `void setInt(int Column_Index, int Data_Value)` statement is used to insert the value of the specified column index with an int value.
		
</blockquote>

</details>
  
---
  
17.What do you mean by "Dirty read" in terms of database?

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
  
18.Describe the steps for establishing a Jdbc connection in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Loading the Driver:When we need to load or register the driver before using it in the program. Registration must be done once in your program. 
  - You can register a driver by using any one of the two methods mentioned below:
    - `Class.forName()`:We load the driver’s class file into memory during runtime.`Class.forName("com.mysql.jdbc.Driver")` is used to load the MySQL driver.However, this statement is no longer needed, because as you place the MySQL Jdbc driver JAR file into the classpath of your program, the driver manager can find and load the driver.
    - `DriverManager.registerDriver()`: DriverManager is a built-in Java class with a static member register. Here we will be calling the constructor of the driver class during compile time.For registering the MySQL driver, use the below-given code:
    - `DriverManager.registerDriver((new com.mysql.jdbc.Driver());`
- Connection:After loading the driver into the program, establish connections using the code given below:
  - `Connection con = DriverManager.getConnection(url,user,password);`
  - `con`: Reference to a Connection interface.
  - `url`: Uniform Resource Locator.
  - `user`: Username from which SQL command prompt is accessed.
  - `password`: Password from which SQL command prompt is accessed.
  - url in MySQL can be created as follows:
    - `String url = "jdbc:mysql://localhost:3306/demo1";`
  - Where localhost represents hostname or IP address of the MySQL server, 3306 port number of the server and by default, it is 3306, test1 is the name of the database on the server.

- Create a statement:Once a connection establishment is done, you can interact with the database. 
  - The `Statement`, `PreparedStatement`, and `CallableStatement` Jdbc interfaces will define the methods that permit you to send SQL commands and receive data from the database.We can use JDBC Statement as follows:
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
- Close the connection:We have to sent the data to the location specified and now we are at the end of our task completion.Closing the connection, objects of Statement and ResultSet will be automatically closed. The `close()` method of the Connection interface is used for closing the connection. 

```java

con.close();

```
		
</blockquote>

</details>

---
  
19.Explain the implementation of Jdbc MySQL database connection with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

```java

import java.sql.*;  
class JdbcMySql{  
   public static void main(String args[]){      
       String url = "jdbc:mysql://localhost:3306/demo1";
       String user = "root";
       String password = "root";
       try{  
           Class.forName("com.mysql.jdbc.Driver");
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
  
20.Explain the implementation to call Stored procedures in Jdbc?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Stored procedures are a set of SQL queries that are compiled in the database and will be executed from Jdbc API. For executing Stored procedures in the database, Jdbc CallableStatement can be used. The syntax for initializing a CallableStatement is given below:

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

21.When "No suitable driver" error occurs in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- "No suitable driver" error occurs during a call to the DriverManager.getConnection() method, when it is unable to load the appropriate Jdbc drivers before calling the getConnection() method.
- It can specify an invalid or wrong Jdbc url, which cannot be recognized by the Jdbc driver.
- When one or more shared libraries required by the Jdbc bridge cannot be loaded.
		
</blockquote>

</details>

---
	
22.Explain the types of Jdbc architecture?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Jdbc has 2 types of architecture models  to access the database. They are:
- Two-tier Architecture: This architecture connects java programs explicitly to  the database. It doesn’t require any mediator such as an application server for connecting with the database except the Jdbc driver. It is also called client-server architecture.	
- Three-tier Architecture: This architecture has no explicit communication between the Jdbc driver or java application with the database. It will make use of an application server as a mediator between them. Java code will send the request to an application server, then the server will send it to the database and receive the response from the database.

</blockquote>

</details>

---
	
23.Explain the ACID properties in Jdbc Transaction Management and why is it needed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The sequence of SQL statements served as a single unit that is called a transaction. Transaction Management places an important role in RDBMS-oriented applications to maintain data consistency and integrity.Transaction Management can be described by using ACID properties. ACID stands for Atomicity, Consistency, Isolation, and Durability.
- Atomicity:If all queries are successfully executed, then only data will be committed to the database.
- Consistency:It ensures bringing the database into a consistent state after any transaction.
- Isolation:It ensures that the transaction is isolated from other transactions.
- Durability:If a transaction has been committed once, it will remain always committed, even in the situation of errors, power loss, etc.

- Need for Transaction Management:When creating a connection to the database, the auto-commit mode will be selected by default. This implies that every time when the request is executed, it will be committed automatically upon completion.We might want to commit the transaction after the execution of few more SQL statements. In such a situation, we must set the auto-commit value to False. So that data will not be able to commit before executing all the queries. In case if we get an exception in the transaction, we can `rollback()` changes made and make it like before.

</blockquote>

</details>

---
	
24:How can you differentiate between PreparedStatement and Statement? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

PreparedStatement performs faster compared to the Statement because the Statement needs to be compiled each time when we run the code whereas the PreparedStatement is compiled once and then executed only on runtime.It can execute parametrized queries. But Statement can only run static queries.
The query used in PreparedStatement looks similar each time, so the database can reuse the previous access plan. Statement inline the parameters into the string, so the query doesn’t look to be the same every time which prevents reusage of cache.

</blockquote>

</details>

---
	
25:Explain the  Transaction Management methods in Jdbc.

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

26:Explain the common exceptions in Jdbc.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- `java.sql.SQLException`:It is the base class for Jdbc exceptions.
- `java.sql.BatchUpdateException`: It occurs during the batch update operation. It depends on the jdbc driver type that the base SQLException may throw instead.
- `java.sql.SQLWarning`:It is displayed as a warning message of various SQL operations.
- `java.sql.DataTruncation`:This exception occurs when data values are unexpectedly truncated due to exceeding MaxFieldSize.

</blockquote>

</details>

---
	
27:How two-phase commit is performed in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Two-phase commit is useful for a distributed environment where numerous processes take part in the distributed transaction process.A transaction is executing and it is affecting multiple databases then a two-phase commit will be used to make sure that all databases are synchronized with each other.
The main process or co-ordinator process take a vote of all other process that they have completed their process successfully and ready to commit, if all the votes are "yes" then they continue for the next phase. And if "No" then rollback will be performed. As per vote, if all the votes are "yes" then commit is done.when any transaction changes multiple databases after transaction execution, it will issue a pre-commit command on each database and all databases will send an acknowledgment. Based on acknowledgment, if all are positive transactions then it will issue the commit command otherwise rollback will be done

</blockquote>

</details>

---
	
28:How to create a table dynamically from java using jdbc?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

```java

import java.io.*;
import java.sql.*;

public class dynamicjdbctable{
 public static void main(String[] args)throws SQLException,IOException{
   BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
   Class.forName("com.mysql.jdbc.Driver");
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
	
29:How is it possible to connect to multiple databases using single statement object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

It is possible to connect to multiple databases, at the same time, but it depends on the specific driver.To update and extract data from the different database we can use the single statement. But we need middleware to deal with multiple databases or a single database.

</blockquote>

</details>

---
	
30.How do you insert images into database using Jdbc?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Images in the database inserted using the BLOB datatype wherein the image stored as a byte stream. Below code is showing how to insert the image into DB.

```java

Connection con = null;
PreparedStatement ps = null;
InputStream is = null;

Class.forName("com.mysql.jdbc.Driver");
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