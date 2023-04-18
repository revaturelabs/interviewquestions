## Technical

1. What is an ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
ADO.NET is a set of classes that expose data access services for .NET Framework programmers. ADO.NET provides a rich set of components for creating distributed, data-sharing applications. It is an integral part of the .NET Framework, providing access to relational, XML, and application data. ADO.NET supports a variety of development needs, including the creation of front-end database clients and middle-tier business objects used by applications, tools, languages, or Internet browsers.


</blockquote>

</details>

---

2. What are the components of ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The ADO.NET Architecture is comprised of 6 important components. They are as follows:

- Connection
- Command
- DataReader
- DataAdapter
- DataSet
- DataView

From the above components, two components are compulsory. One is the command object and the other one is the connection object. Irrespective of the operations like Insert, Update, Delete and Select, the command and connection object you always need.

![ADO.Net_Components](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Components%20ADO.NET.PNG)

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

A .NET Framework data provider is used for connecting to a database, executing commands, and retrieving results. Those results are either processed directly, placed in a DataSet in order to be exposed to the user as needed, combined with data from multiple sources, or remoted between tiers. .NET Framework data providers are lightweight, creating a minimal layer between the data source and code, increasing performance without sacrificing functionality.

The following table lists the data providers that are included in the .NET Framework.

![data_providers_table](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/DataProviders_table.PNG)

</blockquote>

</details>

---

5. What is Dataset Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The DataSet object is central to supporting disconnected, distributed data scenarios with ADO.NET. The DataSet is a memory-resident representation of data that provides a consistent relational programming model regardless of the data source. It can be used with multiple and differing data sources, with XML data, or to manage data local to the application. The DataSet represents a complete set of data, including related tables, constraints, and relationships among the tables. The following illustration shows the DataSet object model.

![DataSet_Object_Model](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/DataSetObject_Model.PNG)

The methods and objects in a DataSet are consistent with those in the relational database model.

The DataSet can also persist and reload its contents as XML, and its schema as XML schema definition language (XSD) schema. 

</blockquote>

</details>

---

6. What is a DataReader Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

You can use the ADO.NET DataReader to retrieve a read-only, forward-only stream of data from a database. Results are returned as the query executes, and are stored in the network buffer on the client until you request them using the Read method of the DataReader. Using the DataReader can increase application performance both by retrieving data as soon as it is available, and (by default) storing only one row at a time in memory, reducing system overhead.

</blockquote>

</details>

---

7. What is the role of DataService?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

ADO.NET Data Services generally sit on top of the ADO.NET Entity Framework and exposes entities through a web service. It exposes these entities in a RESTful way (you can view it in a browser!) which means that the entities being exposed need to be serialized to a certain format

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

A Connection object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a Connection object may not be available.

</blockquote>

</details>

---

11. What are the different layers of ADO.NET?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The basic idea of a 3 tier application is to separate your data, business logics and the presentation.

In the data layer you have CRUD (Create, Update, Delete) methods for your tables (or other data source). You might add some minor business logics in combination with those tables (e.g. max, count, ...) and usually a singleton class is used to provide connection to the business layer.

In the business layer you have all the domain classes with their variables, properties and methods. The variables contain the status of your business entity and are hidden to the outer world by using data hiding (private, protected). Public properties provide the data of these variables to client applications while methods implement the business logics.
It's common used to have a Facade in front of your business classes to provide communication with the client application or presentation layer. A facade combines all the methods that can be used from outside in one single class and makes it easier for others to use the business layer since it's not needed to know how everything works behind the facade.

The third layer of a 3 tier application is the presentation layer. This can be any type of user interface, for ASP.NET is this a Web application.

![Layers_ADO.NET](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Layers_of_ADO.NET.PNG)

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

**Data Grid**:
- Data grid has advanced features and facilitates you to do many things like paging and sorting your data without much effort.
- Data grid can hold text data, but not linked or embedded objects.
**Data Repeater**:
- A data repeater doesn’t have the paging feature, but it can be done by coding.
- A data repeater can hold other controls and can embed objects.
- A data repeater can embed a data grid within it but vice versa is not possible.

</blockquote>

</details>

---

14. What is Connection pooling?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Connecting to a data source can be time consuming. To minimize the cost of opening connections, ADO.NET uses an optimization technique called connection pooling, which minimizes the cost of repeatedly opening and closing connections. Connection pooling is handled differently for the .NET Framework data providers.

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

18. What is the difference between a Typed and Untyped DataSet?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The differences are explained below:

**Typed DataSet**: 
 - A typed dataset is derived from the Dataset class and has an associated XML schema, which is created at the time of the creation of the dataset.
 - The XML schema contains information about the dataset structure such as tables, columns, and rows. Data is transferred from a database into a dataset and from the dataset to another component in the XML format.

**Untyped Dataset**: Untyped dataset doesn’t have an XML schema associated with it. Untyped Dataset, the tables, and columns are represented as a collection.

</blockquote>

</details>

---

19. Do we use the Stored Procedure in ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Yes, stored procedures are used in ADO.Net and they can be used for common repetitive functions.

</blockquote>

</details>

---

20. What is the difference between DataSet.clone and DataSet.copy?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**DataSet.clone** object copies structure of the dataset including schemas, relations and constraints. This will not copy data in the table.
**DataSet.copy** – Copies both structure and data from the table.

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

25. What is the difference between ExecuteScalar and ExecuteNonQuery?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

1. **ExecuteScalar** returns output value where as ExecuteNonQuery does not return any value but the number of rows affected by the query. 

2. **ExecuteScalar** used for fetching a single value and ExecuteNonQuery used to execute Insert and Update statements.

</blockquote>

</details>

---

26. What are all the classes that are available in System.Data Namespace? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Following are the classes that are available in System.Data Namespace:
- DataSet.
- DataTable.
- DataColumn.
- DataRow.
- DataRelation.
- Constraint.

</blockquote>

</details>

---

27. What is the difference between DataReader and DataSet?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Datareader is FORWARD and READ only
- Dataset used to UPDATE records.

- Datareader is CONNECTED architecture
- Dataset is DISCONNECTED Recordset

- Datareader contains single table
- Datareader can contains multiple tables.

- Datareader Occupies Less Memory
- Dataset Occupies More memory

</blockquote>

</details>

---

28. What is Object Pooling?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Object pooling is nothing but a repository of the objects in memory which can be used later. This object pooling reduces the load of object creation when it is needed. Whenever there is a need of object, object pool manager will take the request and serve accordingly.

</blockquote>

</details>

---

29. What is Connected and Disconnected architecture in ADO.Net?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**Disconnected Architecture** - Disconnected architecture means, you don’t need to connect always to get data from the database. You can get data into DataAdapter, disconnect the database, manipulate the DataAdapter and resubmit the data. It is fast and robust(data will not lose in case of any power failure).

![Disconnected_Architecture](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Disconnected_Architecture_ADO.NET.PNG)

**Connected Architecture** - Connected architecture means you are directly interacting with database but it is less secure and not robust.

![Connected_Architecture](https://github.com/revaturelabs/interviewquestions/blob/Feature/Kaveri-Revamped-IS-ques/InterviewSpecificQuestions/.NET%20FULL%20STACK/images/Connected_Architecture.PNG)

</blockquote>

</details>

---

30. What do you mean by performing Asynchronous Operation using Command Object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Sometimes the execution of the commands in the database may take a large amount of time to complete as they are linked to each other.

A solution for such a situation has asynchronously executed the commands against the database without waiting for the command execution to finish, which can be handy in the situation in which, when you try to execute the long-running base commands.

`Advantages of Asynchronous Execution`:

- Improves performance.
- Improve responsiveness of the client application.

</blockquote>

</details>

---

