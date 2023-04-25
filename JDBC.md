1. What is JDBC?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JDBC stands for Java Database Connectivity. It is a Java API which is used to interact with relational databases. JDBC provides a standard set of interfaces that allow the user to connect to a database and retrieve or modify data in the database. 

</blockquote>

</details>

---

2. How do you make a connection to the database using jdbc?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To make a connection to the database using jdbc first we have to load the JDBC driver for the database you want to connect to using the `Class.forName()` method. then we can create a create a `Connection` object using the `DriverManager.getConnection()` method and providing the URL, username, and password for the database. Then create a `Statement` using the `Connection.createStatement()` method. Then we can use `executeQuery()` method to run the queries on the database and fetch the result. The result received by the database can be stored in `ResultSet` object.

</blockquote>

</details>

---

3. What code do I write to set up the Driver?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To set up the driver in a Java application, first, you need to download the JDBC driver JAR file and add it to the project's classpath. Then, you can load the JDBC driver class using the `Class.forName()` method. Once the driver class is loaded, you can establish a connection to the database using the `DriverManager.getConnection()` method, which takes the database's URL, username, and password as parameters. However, the `DriverManager.getConnection()` method may throw an `SQLException`, so it is important to write exception-handling code to handle any errors that may occur.

</blockquote>

</details>

---


4. What should be imported in JDBC?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


