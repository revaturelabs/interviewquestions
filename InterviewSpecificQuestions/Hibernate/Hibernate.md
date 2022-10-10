1. What is an ORM? Explain a bit about it.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Hibernate ORM stands for Object Relational Mapping. This is a mapping tool pattern mainly used for converting data stored in a relational database to an object used in object-oriented programming constructs. This tool also helps greatly in simplifying data 	retrieval, creation, and manipulation.
	
![Hibernate](https://user-images.githubusercontent.com/106813140/192742158-93dfe2ff-6019-4a5b-9b63-8223a3485a10.png)


</blockquote>

</details>

------

2. Have you used Hibernate? If yes, tell me what problem it solves in your project.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Hibernate ORM stands for Object Relational Mapping. This is a mapping tool pattern mainly used for converting data stored in a relational database to an object used in object-oriented programming constructs. This tool also helps greatly in simplifying data 	retrieval, creation, and manipulation.

</blockquote>

</details>

------


3. What is Persistence?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Data Persistence is a means for an application to persist and retrieve information from a non-volatile storage system. 
- Persistence is vital to enterprise applications because of the required access to relational databases.

</blockquote>

</details>

------


4. Any idea about O-R (Object relational) impedance mismatch? Talk about it if you have an idea.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Impedance mismatch is the term used to refer to the problems that occurs due to differences between the database model and the programming language model. 
- The practical relational model has 3 components these are:
  - Attributes and their data types
  - Tuples
  - Tables
- Problems:Following problems may occur due to the impedance mismatch:
  - The first problem that may occur is that is data type mismatch means the programming language attribute data type may differ from the attribute data type in the data model.Hence it is quite necessary to have a binding for each host programming language that specifies for each attribute type the compatible programming language types. It is necessary to have different data types, for example, we have different data types available in different programming languages such as data types in C are different from Java and both differ from SQL data types.
  - The second problem that may occur is because the results of most queries are sets or multisets of tuples and each tuple is formed of a sequence of attribute values. In the program, it is necessary to access the individual data values within individual tuples for printing or processing.Hence there is a need for binding to map the query result data structure which is a table to an appropriate data structure in the programming language. A mechanism is needed to loop over the tuples in a query result in order to access a single tuple at a time and to extract individual values from the tuple.The extracted values are typically copied to appropriate program variables for further processing by the program.A cursor or iterator is a variable which is used for looping over the tuples in a query result. Individual values within each 	tuple are extracted into different or unique program variables of the appropriate datatype.
  - Impedance mismatch is less of a problem when a special database programming language is designed that uses the same data model and data type as a database model for example Oracles’sPL/SQL.

</blockquote>

</details>

------


1. Can we use Hibernate in. standalone (or console based) applications?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Yes we can use.

</blockquote>

</details>

------


6.	What is lazy initialization in the Java Persistence?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Lazy Loading is a design pattern that we use to defer initialization of an object as long as it's possible.
- Let's see how this works.
- First, we'll look at the UserLazy class:

```java
@Entity
@Table(name = "USER")
public class UserLazy implements Serializable {
    @Id
    @GeneratedValue
    @Column(name = "USER_ID")
    private Long userId;

    @OneToMany(fetch = FetchType.LAZY, mappedBy = "user")
    private Set<OrderDetail> orderDetail = new HashSet();

    // standard setters and getters
    // also override equals and hashcode
}
```
- Next, we'll see the OrderDetail class:

```java
@Entity
@Table (name = "USER_ORDER")
public class OrderDetail implements Serializable {
    @Id
    @GeneratedValue
    @Column(name="ORDER_ID")
    private Long orderId;
    
    @ManyToOne(fetch = FetchType.LAZY)
    @JoinColumn(name="USER_ID")
    private UserLazy user;

    // standard setters and getters
    // also override equals and hashcode
}
```
- One User can have multiple OrderDetails. In eager loading strategy, if we load the User data, it will also load up all orders associated with it and will store it in a memory.
- But when we enable lazy loading, if we pull up a UserLazy, OrderDetail data won't be initialized and loaded into a memory until we make an explicit call to it.

</blockquote>

</details>

------

7. If you are a developer and want to develop database application using Java, will you opt-in for JDBC or Hibernate (or any other JPA framework)? Justify your choice.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- I will opt hibernate because using this we can persist entity class object into database and can retrieve data from database in form of entity object. So performance of project will increase . 

</blockquote>

</details>

------


8. Can we use SQL inside the Hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Yes we can use using native query as below:
  
```sql
	
    @Query( value = "SELECT * FROM Users u WHERE u.status = ?1", nativeQuery = true) User 	findUserByStatusNati(Integer status);

```

</blockquote>

</details>

------

1. Can you talk about dialect in the context of Hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- A database dialect is a configuration setting for platform independent software (JPA, Hibernate, etc) which allows such software to translate its generic SQL statements into vendor specific DDL, DML.

</blockquote>

</details>

------


10.	Can you talk about dialect in the context of Hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- A database dialect is a configuration setting for platform independent software (JPA, Hibernate, etc) which allows such software to translate its generic SQL statements into vendor specific DDL, DML.

</blockquote>

</details>

------


11.	What are all the JDBC information that you need to configure in the hibernate configuration file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- We configure database driver,url,username,password,dialect,connection pool,entity information as below

```xml
<hibernate-configuration>
<session-factory>
      <property name="hibernate.connection.driver_class">com.mysql.jdbc.Driver</property>
      <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/mydatabase</property>
      <property name="hibernate.connection.username">root</property>
      <property name="hibernate.connection.password">rajesh</property>
      
      <property name="hibernate.connection.pool_size">10</property>
      <property name="show_sql">true</property>
      <property name="dialect">org.hibernate.dialect.MySQL8Dialect</property>
      <property name="hibernate.hbm2ddl.auto">update</property>
      
     
      <mapping class="com.facebook.entity.FacebookUser"/>
      <mapping class="com.facebook.entity.Trainer"/>
      <mapping class="com.facebook.entity.Trainees"/>
</session-factory>
</hibernate-configuration>
```

</blockquote>

</details>

------


12.	Can you change the hibernate configuration file name to a different file name from its default name? If so, how your application knows the non-default file name?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Yes we can change suppose my file name is revature.cfg.xml then our application will load it as 
SessionFactory sf=new Configuration().configure(“revature.cfg.xml”).buildSessionFactory().

</blockquote>

</details>

------


13.	What should I do to automatically create the database schemas from configuration file or annotation information in Hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- We have to set following properties

```xml
    <property name="hibernate.hbm2ddl.auto">update</property>
```

</blockquote>

</details>

------


14.	Can we have an entity bean in Hibernate without default or no-argument constructor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Default constructor automatically comes in class so not necessary to mention it explicitly.

</blockquote>

</details>

------


15. Can you talk about the .hbm file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- HBM is a short name for Hibernate Mapping. It is an xml file in which we define the mapping between pojo class to database table 	and pojo class variables to table columns.

</blockquote>

</details>

------


16.	In the hibernate mapping file, can we skip the column property of <property> element?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- No we can skip because it map entity class variable to database table column.

</blockquote>

</details>

------


17.	What are all the hibernate mapping types? Why they exist?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- It is class and file. Using class we can map entity class as below:
``` xml
   <mapping class=”entity class qualified name” />
```

- Using file we can map .hbm file as below

```xml    
  <mapping file=”a.hbm.xml” />
```

</blockquote>

</details>

------


18.	How Java reflection is used in hibernate mapping?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Unlike some frameworks, you do not need to do anything special to your objects to allow them to persist via Hibernate. 
- They can be Plain Old Java Objects (or POJO) objects. These objects can follow the JavaBeans conventions and provide setters and getters.
- Hibernate will then use reflection to obtain the data required to persist the object. Example is below

```
Class Cls = ... ;
cls.getField("xyz").getAnnotation(ManyToMany.class).mappedBy
```

</blockquote>

</details>

------


19.	If we want to increase the hibernate start-up performance

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Map the hibernate types explicitly in the mapping file
  Let the hibernate identifies the type automatically
- Map the hibernate types explicitly in the mapping file

</blockquote>

</details>

------


20.	How SessionFactory gets the hibernate metadata?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

```java
SessionFactory sf=new Configuration().configure(“revature.cfg.xml”).buildSessionFactory().
```

</blockquote>

</details>

------


21.	SessionFactory is a thread-safe object? Can you explain what it is?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Yes because all the methods of SessionFactory is synchronized so at a time it will allow only one task.

</blockquote>

</details>

------


22.	What is session in hibernate and how it is created?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- A Session is used to get a physical connection with a database. The Session object is lightweight and designed to be instantiated each time an interaction is needed with the database. Persistent objects are saved and retrieved through a Session object.
- The session objects should not be kept open for a long time because they are not usually thread safe and they should be created and destroyed them as needed.


</blockquote>

</details>

------


23.	Write the code snippet that creates a hibernate session and stores an object to the database. Assume that the SessionFactory object is available with the variable sessionFactory.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

```java
Session session=sessionFactory.openSession();
EntityTransaction et=session.getTransaction();
et.begin();
session.save(entity class object);
      		et.commit();

```

</blockquote>

</details>

------


24.	Do you see any advantage of using annotations in hibernate rather than mapping file? Brief about it.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

What advantages I see in using @Annotations:
•	compiler-safe
•	based on @Entity you can easily distinguish entity from no-entity
•	with packagesToScan Spring's feature entites are easily scannable
•	moving entites from packages to packages or class renaming is easy

</blockquote>

</details>

------


25.	Can we use JPA syntax / annotation in hibernate? If not why and if so why?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

Yes we can use because JPA is a specification. So we can use all its annotation with hibernate.

</blockquote>

</details>

------


26.	Its advised to create only one SessionFactory object for a database in hibernate, why?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Assume the scenario that you are using one database called mysql in your application then following is the way to create the SessionFactory object :

```java
Configuration cfg=new Configuration(); // Empty object will be created.
cfg=cfg.configure();
```

- Here when you called configure() method It looks for hibernate-cfg.xml and for Hibernate mapping file filled with all the properties defined in the configuration documents and mapping documents.

SessionFactory sc=cfg.buildSessionFactory();
• SessionFactory object will be created once and will be used by multiple users for long time.  Because it is a thread safe class. 
• Session Factory object is the factory for session objects.

</blockquote>

</details>

------

27.	What are first-level cache and second-level cache in hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- First level cache is a session level cache and it is always associated with session level object. 
- Second level cache is session factory level cache and it is available across all sessions.

</blockquote>

</details>

------


28.	Why hibernate class or attributes are recommended to be non-final members or class? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The class must not be declared final. No methods or persistent instance variables must be declared final. 
- JPA implementations use proxies in front of your entities to manage for example: Lazy loading. As a final class cannot be extended, a proxy cannot be built.
- The class must have a public or protected, no-argument constructor.
- These kind of frameworks and others in order to create new objects use that is the reason why a no arg constructor is needed.

```java
Class.newInstance()
``` 

- Persistent instance variables must be declared private, protected, or package-private.
Being only accesible through accessor or business methods allow interception in proxies.

</blockquote>

</details>

------


29.	What is field based access and property based access of table fields?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Access strategies
    As a JPA provider, Hibernate can introspect both the entity attributes (instance fields) or the accessors (instance properties). By default, the placement of the @Id annotation gives the default access strategy. When placed on a field, Hibernate will assume field-based access. Place on the identifier getter, Hibernate will use property-based access.

- Field-based access
Example 1. Field-based access
```java
@Entitypublic class Simple {

    @Id
    private Integer id;

    public Integer getId() {
        return id;
    }

    public void setId( Integer id ) {
        this.id = id;
    }}
```

- When using field-based access, adding other entity-level methods is much more flexible because Hibernate won’t consider those part of the persistence state. To exclude a field from being part of the entity persistent state, the field must be marked with the @Transient annotation.

- Another advantage of using field-based access is that some entity attributes can be hidden from outside the entity. An example of such attribute is the entity @Version field, which must not be manipulated by the data access layer. With field-based access, we can simply omit the getter and the setter for this version field, and Hibernate can still leverage the optimistic concurrency control mechanism.

Property-based access

Example 2. Property-based access

```java
@Entitypublic class Simple {

    private Integer id;

    @Id
    public Integer getId() {
        return id;
    }

    public void setId( Integer id ) {
        this.id = id;
    }}
```
When using property-based access, Hibernate uses the accessors for both reading and writing the entity state. Every other method that will be added to the entity (e.g. helper methods for synchronizing both ends of a bidirectional one-to-many association) will have to be marked with the @Transient annotation.

</blockquote>

</details>

------


30.	Which relationship annotation is direct equivalent to foreign key relationship in tables?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- @ForeignKey and @Relations

</blockquote>

</details>

------


31.	Give an example of unidirectional @OneToMany relationship

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Lookup.java

```java
@Entity@Table(name = "DATREG")public class Lookup implements PersistableEntity {

    @Id
    @Column(name = "DATREG_META_CODE")
    private String metaCode;

    @OneToMany
    @JoinTable(name="TXT", 
            joinColumns=@JoinColumn(name="DATREG_META_CODE", referencedColumnName="TXTHEAD_CODE"),
            inverseJoinColumns=@JoinColumn(name="DATREG_META_CODE"))
    private List<Text> text;

Text.java
@Entity@Table(name = "TXT")public class Text {

    @Id
    @Column(name = "TXT_ID")
    private Long id;

    @Column(name = "TXTHEAD_CODE")
    private String code;
```

</blockquote>

</details>

------


32.	How to map collection of values to an entity, in hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- Event Class:

```java
@MappedSuperclass@Inheritance(strategy = InheritanceType.TABLE_PER_CLASS)

public abstract class Event {

   @Column(name="title")
   private String title;

   @Column(name="location")
   private String location;

   @Column(name="date")
   private String date;
CorporateEvent Class:
@Entity@Table(name="corporate_event")

public class CorporateEvent extends Event {

    @Id
    @GeneratedValue(strategy = GenerationType.SEQUENCE, generator = "id_generator")
    @SequenceGenerator(name = "id_generator", sequenceName = "corporate_event_id_seq", allocationSize = 1)
    @Column(name = "id", updatable = false, nullable = false)
    private int id;

    @ElementCollection
    private ArrayList<Task> tasks;

    @Column(name="expenses")
    private String expenses;
```     
Task Class:

```java
@Entity@Table(name="task")

public class Task {

  @Id
  @GeneratedValue(strategy = GenerationType.SEQUENCE, generator = "id_generator")
  @SequenceGenerator(name="id_generator", sequenceName = "task_task_id_seq", allocationSize=1)
  @Column(name="task_id", updatable = false, nullable = false)
  private int id;

  @Column(name="name")
  private String taskName;

  @Column(name="description")
  private String description;
```

</blockquote>

</details>

------


33.	Can you elaborate the states of persistent context?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

![hiber2](https://user-images.githubusercontent.com/106813140/192742500-013b5b25-9fe1-4f96-914e-5dfbe77a800a.png)

</blockquote>

</details>

------


34.	HQL vs SQL – brief about them.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- HQL is similar to SQL and is also case insensitive.
- HQL and SQL both fire queries in a database. In the case of HQL, the queries are in
the form of objects that are translated to SQL queries in the target database.
- SQL works with tables and columns to manipulate the data stored in it.
- HQL works with classes and their properties to finally be mapped to a table structure
in a database.
- HQL supports concepts like polymorphism, inheritance, association, etc. It is a
powerful and easy-to-learn language that makes SQL object oriented.
- SQL lets you modify the data through insert, update, and delete queries. You can add
tables, procedures, or views to your database. The permissions on these added objects
can be changed.

</blockquote>

</details>

------


35.	What is transaction and how it is achieved in hibernate?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- A transaction simply represents a unit of work. In such case, if one step fails, the whole transaction fails (which is termed as atomicity). 		A transaction can be described by ACID properties (Atomicity, Consistency, Isolation and Durability).

- Transaction Interface in Hibernate:
    In hibernate framework, we have Transaction interface that defines the unit of work. It maintains abstraction from the transaction implementation (JTA,JDBC).

    A transaction is associated with Session and instantiated by calling session.beginTransaction().

    The methods of Transaction interface are as follows:

    1.	void begin() starts a new transaction.
    2.	void commit() ends the unit of work unless we are in FlushMode.NEVER.
    3.	void rollback() forces this transaction to rollback.
    4.	void setTimeout(int seconds) it sets a transaction timeout for any transaction started by a subsequent call to begin on this instance.
    5.	boolean isAlive() checks if the transaction is still alive.
    6.	void registerSynchronization(Synchronization s) registers a user synchronization callback for this transaction.
    7.	boolean wasCommited() checks if the transaction is commited successfully.
    8.	boolean wasRolledBack() checks if the transaction is rolledback successfully.

- Example of Transaction Management in Hibernate:

    In hibernate, it is better to rollback the transaction if any exception occurs, so that resources can be free. Let's see the example of transaction management in hibernate.

```java
    	Session session = null;  
    	Transaction tx = null;  
    	try {  
    	session = sessionFactory.openSession();  
    	tx = session.beginTransaction();  
    	//some action	  
    	tx.commit();  
    	}catch (Exception ex) {  
    	ex.printStackTrace();  
    	tx.rollback();  
    	}  
    	finally {session.close();}  
```

![hiber1](https://user-images.githubusercontent.com/106813140/192742423-e0cc47ea-7fe2-44d0-b9b2-d02aa7553cf7.jpg)

</blockquote>

</details>

------


36.	Hibernate Criteria query, have you used it? If so, explain about it.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary> <b>Show Answer</b> </summary>

<blockquote>

- The Hibernate Session interface provides createCriteria() method, which can be used to create a Criteria object that returns instances of 	the persistence object's class when your application executes a criteria query.
Following is the simplest example of a criteria query is one, which will simply return every object that corresponds to the Employee class.

```java
Criteria cr = session.createCriteria(Employee.class);List results = cr.list();
```


</blockquote>

</details>

------
