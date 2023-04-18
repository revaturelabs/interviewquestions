
## Technical

1. What is an ORM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Object Relational Mapping, also known as Mapping Tool, in computer science is a programming technique used to convert data between systems of incompatible types through object-oriented programming languages.

In simple terms, it is as if the ORM creates a “virtual database” and reflects this “virtual database” in a traditional database, such as SQL Server for example.

</blockquote>

</details>

---

2. What is Entity Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

ADO.NET EF is an ORM (object-relational mapping) which creates a higher abstract object model over ADO.NET components. So rather than getting into dataset, datatables, command, and connection objects as shown in the below code, you work on higher level domain objects like customers, suppliers, etc.

</blockquote>

</details>

---

3.  What are various entity framework approaches?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The various approaches in Entity Framework are:

- Database First
- Model First
- Code First

</blockquote>

</details>

---

4. What is the code first approach in the entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Code First approach in Entity Framework helps in allowing the creation of a model and its relations with the help of classes from which the database is created. Thus, the developer has the ability to work in an object-oriented manner without having worries about the structure of the database.

</blockquote>

</details>

---

5. What is the database first approach in the entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Database First approach in Entity Framework is used for making an entity model from an existing database and then decreases the amount of code that must be written.

</blockquote>

</details>

---

6. What is the model first approach in the entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

In the Model First approach in the Entity Framework, the model classes are created and their relationships are also created first by taking the help of the ORM. After that the physical database is generated from the model. Therefore, a diagram of entity and relations are converted into the code model.

</blockquote>

</details>

---

7. Which approach is best in an entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The choice of the development approach depends on the project. If the database is present, then for the programmer the Database First approach is the best suited. If model classes and databases are not present then the programmer should go with the Model First approach. If the developer has domain classes then the Code First approach is the best choice for the programmer.

</blockquote>

</details>

---

8.  What are the types of property in Entity Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Three types of property in the entity framework are as follows:

- Scalar property
- Navigation Property
- Complex Property

</blockquote>

</details>

---

9. What is a navigation property in the entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Navigation properties in Entity Framework are a way to represent a foreign key relationship within the database. Navigation properties help in enabling the user to describe the relationships between the entities such that they are coherent in the object-oriented language.

</blockquote>

</details>

---

10. What are the types of loading available in entity framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The types of loading that are available in the Entity Framework are-

- Eager Loading
- Lazy Loading
- Explicit Loading

</blockquote>

</details>

---

11. What is lazy loading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Lazy loading is defined as the way for returning only the used objects. When you query the database model, lazy loading is able to return the immediate tables needed by the user. All related tables are returned when they are used. This means we are able to reserve the memory and storage when we work with large programs. It also means that the objects are created until we are having the requirement of them, so that it can make our program faster.

</blockquote>

</details>

---

12. What is eager loading?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Eager loading is the opposite of lazy loading. When you query for objects, eager loading helps in the returning all the objects including the related objects. For instance, when we are querying a list of customers and orders, eager loading loads all of the objects including the customers and the orders instead of just what you originally need (customers).

</blockquote>

</details>

---

13. How to disable the lazy loading framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

We can disable the lazy loading by the `context.ContextOptions.LazyLoadingEnabled = false;`

</blockquote>

</details>

---

14. Is Entity Framework an open source?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Yes, Entity Framework (EF) is an open source object-relational mapping (ORM) framework for the ADO.NET. It was a part of .NET Framework, but since Entity framework version 6 it is separated from .NET framework.

</blockquote>

</details>

---

15. How does Entity Framework work?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Entity Framework maps domain classes to the database schema translate as well as executes LINQ queries to SQL and tracks the changes in the entities. It also saves the changes to the database.

</blockquote>

</details>

---

16.  How to retrieve data from the database using Entity Framework in MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The steps for retrieving the data are as follows-

- Create a new project.
- From Nugget package manager, add the reference of the Entity Framework.
- Then create a new class in the model within the table structure.
- Add connection string in the web.config.connection string name such that it matches with the context.
- Open the Global.asax.cs classes and then add the additional namespace of Entity Framework and finally initialize the database.
- Right-click on the Controller folder and then add a new controller and model reference in the section for the namespace.
- Right-click on the controller name and add the sections you want to view.

</blockquote>

</details>

---

17. What is Entity Data Model? How to create EDM?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Entity Data Model happens to be an expanded style of the Entity-relationship prototype which helps in stating the fundamental prototype of the data utilizing several modeling procedures. It also helps in depicting a set of fundamentals which helps in explaining the data formation disregarding its collected form. EDM is hence the connection between the database and the prototype.

For creating an Entity Data Model, one can

- Right-click on one’s project in the Solution Explorer window.
- Choose Add>New Item from the menu option.
- Choose the ADO.Net Entity Data Model arrangement or template.
- Add name and click on the Add button.

</blockquote>

</details>

---

18.  What is dbcontext and dbset in Entity Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- DbContext is defined as the class in Entity Framework API that helps in forming a connection between a domain or entity class and the database. It is primarily responsible for communicating with the database.
- The DbSet is defined as another class that helps in representing an entity set for reading, creating, updating, and deleting operations.

</blockquote>

</details>

---

19. What is the difference between ADO.Net and Entity Framework?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The differences between ADO.Net and Entity Framework are as follows-

- ADO.Net helps in creating the several data layer codes that Entity Framework is not able to create.
- Unlike ADO.Net, Entity Framework automatically helps in generating the codes for the intermediate layers, data access layers and mapping codes. This helps to cut down on development time whereas ADO.Net is not able to do this.
- ADO.Net is faster than the Entity Framework based on performance.

</blockquote>

</details>

---

20. What is LINQ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Language-Integrated Query (LINQ) is a way to query the data without cumbersome stored procedures. Previously, programmers needed to create the stored procedures and then call these stored procedures from their code. With Entity framework, we can pull data and query it using the language which is similar to SQL.

</blockquote>

</details>


---

21. Explain POCO classes in Entity Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

POCO stands for Plain Old CLR Objects. This class of objects does not depend on any framework-specific base class, unlike a normal .NET class. They support most of the LINQ queries that Entity Object derived entities support.

</blockquote>

</details>

---

22. How to connect entity framework to sql server?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

The entity framework can be connected to the SQL Server in the following ways:

- A console application is to be created.
- Create a class by right clicking on the application.
- Create the variables of the class and set the required properties.
- Save the class. Add one more class in the same way.
- Right-click and create a new folder for generating the Framework Dynamic Link Library (DLL).
- The folder can be renamed as the developer requirements.
- Save the application before adding any framework.
- Right-click the Program.cs file and select the required properties for copying the program’s address.
- Right-click on the window of the program and copy the required address for adding the DLL framework.
- After copying the address, put it in the c: drive bar and search for the folder previously added.
- After finding the folder then adding the Entity framework DLL.
- Right-clicking on the references and then adding it to browse the DLL framework.
- The application configuration file is added.
- The DB path name and database name should be declared by making use of the App. Config file.
- In the main program one must declare the context and objects.
- Press F5 to execute

</blockquote>

</details>

---

23. How to prevent sql injection in entity framework?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- The SQL injection is a technique for code injection that can attack data-driven applications and can destroy the database. The SQL injection is one of the most commonly used web hacking procedures that injects malicious codes in the SQL statements through the input of the web page.

- LINQ helps in preventing the SQL injection in the entity framework. This takes place due to the passing of all data to the database with the help of the QL parameters. LINQ queries are not considered as susceptible to the attacks by SQL injection as they are made by implying the concatenation or manipulation of the string.

</blockquote>

</details>

---

24. What is fluent API in MVC?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- Fluent API is a way of specifying the configuration of the model that helps in covering everything which is executed by the annotations of the data. Fluent API and data annotations could be used together, but more preference is given by the Code.
- First to the Fluent API, then data annotations and finally to the default conventions. Fluent API is a way for configuring the domain classes.
- The Fluent API of the Code First is accessed with the help of overriding the OnModelCreating method of the derived DbContext. Fluent API in the MVC is that which offers more configuration functionality than the DataAnnotations. Fluent API allows the user to configure the properties of the entities.

</blockquote>

</details>

---

25. How to turn off lazy loading in entity framework?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Lazy loading in the entity framework is the loading that can be turned off for a particular context or an entity. To turn off the lazy loading for a specific property, one must not convert it to the virtual. For disabling the lazy loading for the entire entities in a context, the configuration property must be set to false. Now let us see the ways for turning off the lazy loading.

Context.configuration.ProxyCreationEnabled should be true. Context.Configuration.LazyLoadingEnabled should be made true.
Navigation property is the property that should not be defined as virtual and public. The context will be doing the lazy loading if the property is defined as the virtual.

</blockquote>

</details>

---

26. Will there be any issues adding a table without primary keys to a Data Model?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Every entity must be having a key, even in case where the entity maps to a view. When you are using the Entity Designer for creating or updating a model, the classes that are generated inherit from EntityObject which requires EntityKey. So, we need to have a primary key in the table for adding it to the data model.

</blockquote>

</details>

---

27. Mention in what all scenarios Entity Framework can be applicable?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Entity Framework can be applicable in three scenarios

- If you have an existing database already or you want to build your database first then other parts of the application.
- If your prime focus is your domain classes and then create the database from your domain classes.
- If you want to design your database schema on the visual designer and create the classes and database.

</blockquote>

</details>

---

28. How can you enhance the performance of Entity Framework?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

For enhancing the performance of Entity Framework, one must have to follow the following steps:

- Try to avoid to put all the DB objects into one single entity model.
- Disable change tracking for entities if not needed.
- Reduce response time for the first request by using pre-generating Views.
- If not required try to avoid fetching all the fields.
- For data manipulation select appropriate collection.
- Wherever needed use a compiled query.
- Avoid using Views and Contains.
- While binding data to grid or paging, retrieve only required no of records.
- Debug and Optimize LINQ query

</blockquote>

</details>

---

29. In what way did the Entity Framework affect the LINQ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

LINQ (Language Integrated Query) is defined as a component of Entity Framework which actually helps the programmers for querying the database without creating any stored procedures using a language which is similar to SQL.

</blockquote>

</details>

---

