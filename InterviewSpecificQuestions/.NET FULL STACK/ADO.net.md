## Technical

1. What is an ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
ADO.Net is commonly termed ActiveX Data Objects which is a part of the .Net Framework. ADO.Net framework has a set of classes which are used to handle data access by connecting with different databases like SQL, Access, Oracle, etc.,


</blockquote>

</details>

---

2. What are the components of ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Components of ADO.NET Components are designed for data manipulation and faster data access. Connection, Command, DataReader, DataAdapter, DataSet, and DataView are the components of ADO.NET that are used to perform database operations.

</blockquote>

</details>

---

3. What types of Applications use ADO.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- ASP.NET Web Form Applications
- Windows Applications
- ASP.NET MVC Application
- Console Applications
- ASP.NET Web API Applications

</blockquote>

</details>

---

4. What is a .NET data provider?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A .NET data provider is a software library consisting of classes that provide data access services such as connecting to a data source, executing commands at a data source, and fetching data from a data source with support to execute commands within transactions. It resides as a lightweight layer between data source and code, providing data access services with increased performance.

The .NET data provider is a component of ADO.NET, a subset of the .NET framework class library.

</blockquote>

</details>

---

5. What is Dataset Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A Dataset is set to be a collection of data with a tabular column representation. Each column in the table represents a variable and the row represents to value of a variable. This Dataset object can be obtained from the database values.

</blockquote>

</details>

---

6. What is a DataReader Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

DataReader is an object of ADO.Net that provides access to the data from the requested data source. It reads the data sequentially from a data source like Oracle, MS SQL, or MS Access.

</blockquote>

</details>

---

7. What is the role of DataService?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A Data Service is responsible to handle the interaction between the Connection Manager, Schema and Data Streamer.

</blockquote>

</details>

---

8. What are the common namespaces used in ADO.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In ADO.NET, we can connect to your database with the help of the following namespaces:

- **Data**: This namespace is used to carry the data tables from the database and can hold columns, relations, multiple tables, views and constraints.
- **Data.SqlClient**: This namespace is used to connect the .NET application with the Microsoft SQL Database by using the miscellaneous classes such as SqlConnection, SqlCommand, SqlDataAdapter etc.
- **Data.Odbc**: This namespace is used to connect with the ODBC drivers by using OdbcCommand and OdbcConnection.
- **Data.OracleClient**: This namespace is used to describe a collection of classes to access an Oracle data source.

</blockquote>

</details>

---

9. What are the different ways to populate a DataSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

We can populate a dataset by using any of the following different ways:

- Using DataAdapter objects and call the ‘fill’ method.
- Creating Datatable, Datarow, and Data column objects programmatically.
- Load data from XML Documents.
- Merge or copy from another Dataset.

</blockquote>

</details>

---

10. What is the use of a connection object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The use of the connection object is to connect data to a command object. Different connection objects are used for different providers such as an OleDbConnection object for the OLE-DB provider and SqlConnection object for the Microsoft SQL Server.

</blockquote>

</details>

---

11. What are the different layers of ADO.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The different layers of ADO.NET are:

- Business Logic Layer
- Presentation Layer
- Database Access Layer

</blockquote>

</details>

---

12. What are all the commands used with Data Adapter?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

DataAdapter retrieves data from a data source. UpdateCommand, Insertcommand, and DeleteCommand are the commands object used in DataAdapter to handle a modification on the database.

</blockquote>

</details>

---

13. What is the difference between Data Grid and Data Repeater?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**Data Grid**: Data Grid provides many features and functionality to users to perform paging and sort the data in the table easily. It can hold text object data, but it can’t hold embedded or linked object data.
**Data Repeater**: Data Repeater has offered so many features that are not offered by Data Grid such as – It can hold control of embedded and linked objects data and it can embed Data Grid in it but vice-versa is not possible. It doesn’t have support for Paging functionality but can be achieved by programming it.

</blockquote>

</details>

---

14. What is Connection pooling?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Connection pooling refers to the task of grouping database connections in the cache to make them reusable because opening new connections every time to a database is a time-consuming process. 
- Therefore, connection pooling enables us to reuse already existing and active database connections, whenever required, increasing the performance of our application.
- We can enable or disable connection pooling in your application by setting the pooling property to either true or false in the connection string. By default, it is enabled in an application.

</blockquote>

</details>

---

15. Why is it important to close an ADO.NET application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Connections need to be closed properly because it affects the scalability and reliability of the applications.
- Open connections are always vulnerable to attack, so to be short, `Open connections as late as possible and close them as early as possible`. We can close the connections by **final** block or ‘using’ the `USING statement`.

</blockquote>

</details>

---

16. What is Databinding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Databinding is the process of binding the data with graphical elements (controls in a window form). After binding the data in a window form, you can navigate through the records with the help of the Binding Navigator Control.
- One of the advantages of data binding is, the user does not need to write the codes explicitly, for establishing the connections and creating a data set, this feature will write the necessary ADO.NET code for the user.

</blockquote>

</details>

---

17. What are the key events of SqlConnection Class?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The two key events of SqlConnection are:

**StateChange event**: This event occurred when the state of the Connection changes. The event handler receives an argument (Datatype: StateChangeEventArgs) which contains the data related to that particular event.
**InfoMessage event**: This event occurred when an info message or Warning is returned from a data source. The event handler receives an argument (Datatype: SqlInfoMessageEventArgs) which contains the data related to that event.

</blockquote>

</details>

---

18. What is the difference between a Typed and Untyped Dataset?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The differences are explained below:

**Typed Dataset**: 
 - A typed dataset is derived from the Dataset class and has an associated XML schema, which is created at the time of the creation of the dataset.
 - The XML schema contains information about the dataset structure such as tables, columns, and rows. Data is transferred from a database into a dataset and from the dataset to another component in the XML format.

**Untyped Dataset**: Untyped dataset doesn’t have an XML schema associated with it. Untyped Dataset, the tables, and columns are represented as a collection.

</blockquote>

</details>

---

19. Do we use the Stored Procedure in Ado.net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Yes, stored procedures are used in ADO.Net and they can be used for common repetitive functions.

</blockquote>

</details>

---

20. What is the difference between Dataset.clone and Dataset.copy?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**Dataset.clone** object copies structure of the dataset including schemas, relations and constraints. This will not copy data in the table.
**Dataset.copy** – Copies both structure and data from the table.

</blockquote>

</details>

---

21. What are the different methods under SQL Command?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are different methods under SqlCommand like:
- **Cancel** – Cancel the query
- **CreateParameter** – returns SQL Parameter
- **ExecuteNonQuery** – Executes and does not return a result set
- **ExecuteReader** – executes and returns data in DataReader
- **ExecuteScalar** – Executes and returns a single value
- **ExecuteXmlReader** – Executes and returns data in XMLDataReader object
- **ResetCommandTimeout** – Reset Timeout property

</blockquote>

</details>

---

22. What are the different Execute methods of Ado.net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**ExecuteScalar** – Returns a single value from the dataset
**ExecutenonQuery** – Returns resultset from the dataset and it has multiple values
**ExecuteReader** – Forwardonly resultset
**ExecuteXMLReader** – Build XMLReader object from a SQL Query

</blockquote>

</details>

---

23. What are the components of DataProviders?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

There are four components of DataProviders:
- Connection
- Commands
- DataReader
- DataAdapter

</blockquote>

</details>

---

24. What are the Parameters?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The parameters are used to exchange the information or data between the stored procedure or function and the .NET application. Anything that is placed in the parameter, is treated as the field, not as a query text, which makes your application secure.

- The parameters can be Input or Output in an SQL query. The default parameter type is Input.

</blockquote>

</details>

---

