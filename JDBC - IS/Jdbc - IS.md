1.How JDBC plays a vital role in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

JDBC(Java Database Connectivity) is a Java API, which is helpful in interaction with the database to retrieve, manipulate and process the data using SQL. It will make use of JDBC drivers for connecting with the database. By using JDBC, we can access tabular data stored in various types of relational databases such as Oracle, MySQL, MS Access, etc.

</blockquote>

</details>

---

2.What is the functionality of resultset in jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The `java.sql.ResultSet` interface represents the database result set, which is obtained after the execution of SQL query using Statement objects.Object of ResultSet maintains a cursor pointing to the current row of data in the result set. Initially, the cursor is located before the first row. Then the cursor is moved to the next row by using the `next()` method. The `next()` method can be used to iterate through the result set with the help of a while loop. If there are no further rows, the `next()` method will return false.

Example for the creation of ResultSet is given below:

```java

ResultSet rs = con.executeQuery(sqlQuery);

```

</blockquote>

</details>

---

3.Why we need JDBC driver in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


JDBC driver is a software component having various classes and interfaces, that enables the Java application to interact with a database.To connect with individual databases, JDBC requires particular drivers for each specific database. These drivers are provided by the database vendor in addition to the database. 

For example:

- MySQL Connector/J is the official JDBC driver for MySQL and we can locate the `mysql-connector-java-<version>-bin.jar` file among the installed files. 
- On windows, this file can be obtained at `C:\Program Files (x86)\MySQL\MySQL` `Connector J\mysql-connector-java-5.1.30-bin.jar`.
- JDBC driver of Oracle 10G is `ojdbc14.jar` and it can be obtained in the installation directory of an Oracle at `…/Oracle/app/oracle/product/10.2.0/server/jdbc/lib` .
- JDBC driver provides the connection to the database. Also, it implements the protocol for sending the query and result between client and database.

</blockquote>

</details>
  
 ---
  
 4.What is the need of DriverManager in Jdbc?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Jdbc DriverManager is a static class in Java, through which we manage the set of Jdbc drivers that are available for an application to use.Multiple JDBC drivers can be used concurrently by an application, if necessary. By using a Uniform Resource Locator(URL), each application specifies a JDBC driver.When we load the JDBC Driver class into an application, it registers itself to the DriverManager by using `Class.forName()` or `DriverManager.registerDriver()`. After this, when we call `DriverManager.getConnection()` method by passing the details regarding database configuration, DriverManager will make use of registered drivers to obtain the connection and return it to the caller program.

</blockquote>

</details>
  
---
  

