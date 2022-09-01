1.How JDBC plays a vital role in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

JDBC(Java Database Connectivity) is a Java API, which is helpful in interacting with the database to retrieve, manipulate and process the data using SQL. It will make use of JDBC drivers for connecting to the database. JDBC can access tabular data stored in various types of relational databases such as Oracle, MySQL, MS Access, etc.

</blockquote>

</details>

---

2.What is the functionality of resultset in jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The `java.sql.ResultSet` interface represents the database result set, which is obtained after the execution of SQL query using Statement objects. ResultSet objects maintains a cursor pointing to the current row of data in the result set. Initially, the cursor is located before the first row. Then the cursor is moved to the next row by using the `next()` method. The `next()` method can be used to iterate through the result set with the help of a while loop. If there are no further rows, the `next()` method will return false.for example:

```java

ResultSet rs = con.executeQuery(sqlQuery);

```

</blockquote>

</details>

---

3.Why we need Jdbc driver in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Jdbc driver is a software component having various classes and interfaces, that enables the Java application to interact with a database.To connect with individual databases, It requires particular drivers for each specific database. These drivers are provided by the database vendor in addition to the database. 

For example:

- MySQL Connector/J is the official Jdbc driver for MySQL and we can locate the `mysql-connector-java-<version>-bin.jar` file among the installed files. 
- On windows, this file can be obtained at `C:\Program Files (x86)\MySQL\MySQL` `Connector J\mysql-connector-java-5.1.30-bin.jar`.
- Jdbc driver of Oracle10G is `ojdbc14.jar` and it can be obtained in the installation directory of an Oracle at `…/Oracle/app/oracle/product/10.2.0/server/jdbc/lib` .
- Jdbc driver provides the connection to the database. Also, it implements the protocol for sending the query and result between client and database.

</blockquote>

</details>
  
 ---
  
 4.What is the need of DriverManager in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Jdbc DriverManager is a static class in Java, through which we manage the set of Jdbc drivers that are available for an application to use.Multiple JDBC drivers can be used concurrently by an application. By using a Uniform Resource Locator(URL), each application specifies a Jdbc driver.When we load the JDBC Driver class into an application, it registers itself to the DriverManager by using `Class.forName()` or `DriverManager.registerDriver()`. when we call `DriverManager.getConnection()` method by passing the details regarding database configuration, DriverManager will make use of registered drivers to obtain the connection and return it to the caller program.

</blockquote>

</details>
  
---
  
5.Which Jdbc driver is fastest and used more commonly?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Jdbc Net pure Java driver(Type 4 driver) is the fastest driver for localhost and remote connections because it directly interacts with the database by converting the Jdbc calls into vendor-specific protocol calls.

</blockquote>

</details>

---
  
6.Which data types are used for storing the image and file in the database table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

BLOB data type is used to store the image in the database. We can also store videos and audio by using the BLOB data type. It stores the binary type of data.CLOB data type is used to store the file in the database. It stores the character type of data.

</blockquote>

</details>

 ---
  
 7.Why we need stored procedure?Explain it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Stored procedure is a group of SQL queries that are executed as a single logical unit to perform a specific task. Name of the procedure should be unique since each procedure is represented by its name.For example, operations on an employee database like obtaining information about an employee could be coded as stored procedures that will be executed by an application. Code for creating a stored procedure named `STUDENT_DETAILS`  is given below:

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
Stored procedures are called using CallableStatement class available in JDBC API. Below given code demonstrates this:

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

ODBC(Open Database Connectivity):	
- ODBC can be used for languages like C, C++, Java, etc.
- We can use ODBC only for the Windows platform, thus it is platform-dependent.	
- Most of the ODBC Drivers developed in native languages like C, C++	
- It is not recommended to use ODBC for Java applications, because of low performance due to internal conversion.	
- ODBC is procedural.	

JDBC(Java Database Connectivity):
- JDBC is used only for the Java language
- We can use JDBC on any platform, thus it is platform-independent
- JDBC drivers are developed using the Java language
- It is highly recommended to use JDBC for Java applications because there are no performance issues.
- JDBC is Object Oriented.

</blockquote>

</details>
  
---
  
9.What is Rowset in a Resultset?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A RowSet is an object that encapsulates a row set from either Jdbc result sets or tabular data sources such as files or spreadsheets. It supports component-based development models like JavaBeans, with the help of a standard set of properties and event notifications.RowSet is easier and flexible to use.It is Scrollable and Updatable by default.

</blockquote>

</details>
  
---

10.Describe the different types of Jdbc drivers in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


There are four types of JDBC drivers in Java. They are:

- Type I: Jdbc - Odbc bridge driver:It acts as an interface between the client and database server. When a user uses a Java application to send requests to the database using Jdbc–Odbc bridge, it converts the Jdbc API into Odbc API and then sends it to the database. When the result is received from the database, it is sent to Odbc API and then to Jdbc API.It is platform-dependent because it uses Odbc which depends on the native library of the operating system. In this, Jdbc–Odbc driver should be installed in every client system and database must support for Odbc driver.It is easier to use but it gives low performance because it involves the conversion of Jdbc method calls to the Odbc method calls.

- Type II: Native API – Partially Java Driver:It uses libraries of the client-side of the database. This Type II Driver converts the Jdbc method calls to native calls of the database native API.When the database gets the requests from the user, the requests are processed and sends the results back in the native format which is then converted into Jdbc format and pass it to the Java application.It was instantly adopted by the database vendors because it was quick and cheaper to implement. 

- Type III: Network Protocol - Fully Java Driver: It uses to send the Jdbc method calls to an intermediate server. The intermediate server communicates with the database on behalf of Jdbc. The application server converts the Jdbc calls either directly or indirectly to the database protocol which is vendor-specific.

- Type IV: Thin Driver - Fully Java Driver: It is platform-independent since it is written fully in Java. It can be installed inside the Java Virtual Machine(JVM) of the client, so there is no need of installing any software on the client or server side. This drive architecture is having all the logic to communicate directly with the database in a single driver.It provides better performance compared to other driver types. It permits easy deployment. It is developed by the database vendor itself so that programmers can use it directly without any dependencies on other sources.Type IV driver is directly implemented and it directly converts JDBC calls into vendor-specific database protocol. Most of the Jdbc Drivers used today are type IV drivers.

</blockquote>

</details>




