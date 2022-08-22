
# MongoDB Interview Questions

1. Does `MongoDB` support primary-key and foreign-key relationship? If yes, then how?

<details><summary> <b>Show Answer</b> </summary> 
  
`MongoDB`,  by-default, does not support primary and foreign key relationship. But we can achieve it by embedding one document inside another one. For example, embedding 'city' document inside 'address' document. 
</details>

---

2. Using the Aggregate function ‘$avg’ write a MongoDB query.
<details><summary> <b>Show Answer</b> </summary> 
 
`db.student.aggregate([{$group : {_id:null, Average_marks : {$avg : "marks"}}}])`. Here we are getting average of the marks field in student collection.
</details>

---

3. Use the Aggregate function ‘$sum’ to write a MongoDB query. 

<details><summary> <b>Show Answer</b> </summary> 

`db.student.aggregate([{$group : {_id:null, Average_marks : {$sum : "marks"}}}])`. Here we are getting sum of the marks field in student collection.
  </details>
 
 ---
 
4. In a find() query like `db.collection_name.find({ "school.student": "Jack"})` , what could be school and what could be a student?

<details><summary> <b>Show Answer</b> </summary> 

In `db.collection_name.find({ "school.student": "Jack"})` query, "school" is a outer document field and "student" is a inner document field.  

</details>

---

5. When creating a database in MongoDB, if you are getting "could not connect to the server" error, then what steps you will follow to resolve that error. 
<details><summary> <b>Show Answer</b> </summary> 

To resolve the "could not connect to the server" error, we can take few measures like:
1. We must ensure that we put correct hostname and port number. 
2. If any firewall is blocking your port connection, uninstall that firewall or try to connect from different server.
3. Must ensure that your MongoDB instance is running in the background.
4. If server is shutdown then i will start the server again.
</details>
 
---

6. Suppose you are collaborating with your team on “ABC” database which have some data inside it. How can you make sure that if someone by mistake deletes the “ABC” database, you can still have a backup of that database. 
<details><summary> <b>Show Answer</b> </summary> 

To make sure that we have a backup of our database, we can use the `mongodump` command that will store our data in a backup file. For that, we just have to write `mongodump --db database_name -- collection collection_name`.    
To import again the backup file in Mongodb we can use the mongorestore command:     
`mongorestore --db database_name path_of_file`  


</details>

---

7.  What insert() method returns after successfully inserting a document into a collection.

<details><summary> <b>Show Answer</b> </summary> 
  
It returns an object that contains the information about the operation. It returns a `WriteResult` object when we insert a single document and `BulkWriteResult` object when we insert more than one document in a single insert query.
</details>

---

8.  When a person inserts a document into collection, MongoDB automatically creates an `_id` field which acts as a primary key for that data, then how can we set one of our fields as primary key in MongoDB if we want? 
<details><summary> <b>Show Answer</b> </summary> 

The `_id` field is the default primary key in `MongoDB` and it is reserved , we cannot create any other primary key but, we can put the data that we want to be unique into the `_id` field of the document. 
</details>

--- 

9. Create a “Company” database and make a collection as “Department” in it. 

<details><summary> <b>Show Answer</b> </summary>
  
```
use Company;
db.createCollection("Department");
```
</details>

---

10. Imagine you have an “employee” database and “emp” collection. Write a query to update salary of an employee by 1000 where name =”Jack”.

<details><summary> <b>Show Answer</b> </summary> 
 
```
use employee;
db.emp.update({"name": "Jack"}, {$inc: {"salary": 1000}});
</details>

--- 

11. Tell the difference between `update()` and `save()` method in MongoDB.

<details><summary> <b>Show Answer</b> </summary> 

The `update()` method is used to update the existing document values in MongoDB without creating a new document. Whereas, `save()` method is used to replace the existing document with the document passed in the `save()` method. 
</details>

---

12.  Write a single query that will perform update operation if document is present in the collection and if not, then it performs insert operation. 

<details><summary> <b>Show Answer</b> </summary> 

  
</details>

---

13. Imagine you have added 5 documents into a collection named as “emp” and suddenly there is a need to add one common field into all the five documents then what query you will write for the same purpose? 
<details><summary> <b>Show Answer</b> </summary> 

</details>
  
--- 

24. Suppose a document have five fields as “name”, “age”, “salary”, “dept”, “address” and if you want to remove the “age” field from the document of “emp” collection, then what query you will provide to remove only “age” field?

<details><summary> <b>Show Answer</b> </summary> 

</details>

---

26. How do you find the employees, from “emp” collection, whose name starts with ‘A’. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

28. State the difference between update() and findAndModify() method in MongoDB.
<details><summary> <b>Show Answer</b> </summary> 
  
  </details>

---

30. Suppose you have a “Company” database and “emp” collection inside that database then how do you find the records of top 5 employees based on salary field?
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

32. Write a query to get all the records of employee whose “age” is greater than 25 and “experience” greater or equal to 3 years. [collection name is “emp”]. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---
34. What is the difference between findOneAndReplace() and findOneAndUpdate() in MongoDB?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---
36. Differentiate between findOneAndReplace() and replaceOne() in MongoDB?

<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

38. Imagine you are working on “Company” database having “Dept” as collection and inside your collection there are millions of documents and your boss is asking for some data from it, then what sort of practice you will do to increase the query performance and fast retrieval of data. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---
40. Consider your documents have some array fields and you want to create an index on it. Is it possible in MongoDB? 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---
42. What sort of practice you will take as a developer to increase the availability of data in MongoDB when there is a routine maintenance check or system failure?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

44. What query do you write to get employee details in “emp” collection where “job_role” matches “Technical Specialist” and  “emp_age” is between 22 and 28? 

<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

46. An intern in your company is asking for your help to fetch the records of “department” that belongs to “product”, but “type” should not equal to “A” and whenever the “type” is equal to “A”, the “department” should not equal to “product”. Here is the collection he is using to fetch the data:
{ "department" : "product", "type" : "A" }
{ "department " : "training", "type" : "A" }
{ “department " : "product", "type" : "B" }
{ "department " : "finance", "type" : "C" }	
Help him to write a query that will produce the output as: 
{ "department " : "training", "type" : "A" }
{ “department " : "product", "type" : "B" } 

<details><summary> <b>Show Answer</b> </summary> 
 
</details>

---

26. Give me the query that will fetch only “name” and “age” field from the collection “emp”, that having the “DOB” between 01/03/1990 to 31/12/1999 and “salary”  greater than “50k”. 

<details><summary> <b>Show Answer</b> </summary> 
  
  </details>
  
---

28. Write the single query that will give the sorted result based on “dob” field that satisfies the following condition:
i) Where “name” starts with “s” alphabet and “salary” in between 40k to 70k 
ii) Where “department” not equal to “product”. 

<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

28. Jack is trying to fetch all the records, from a collection called “people”, without including the “_id” field. When he wrote the query as “db.people.find({} { _id: 0})”, he was getting syntax error message stating “unexpected { ”. What he needs to change in his query to get the desired output. 
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

30.  Write a query that will fetch the top 20 records from “student” collection of those students who are from 8th, 9th and 10th “class” having “marks” greater or equal to 70 in science and math “subject”.
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

32. A developer doesn’t want to see the first 10 documents of “dept” collection and doesn’t have the permission to delete any document from the collection as well, so what query he must write to see the rest of the documents after 10 documents without deleting any. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

34. Write a query to get the number of employees whose “address” is “New York” having “age” less than equal to 40  and earning salary greater than 50K. 
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

36. As 1 and -1 are used to represent  ascending and descending order respectively in sort() method, then what will happen if we use -2 or 2 instead in sort(). 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

38. In a document having 5 fields “name”, “age”, “score”, “subject” and “address”, when your friend is trying to fetch only “name” and “address” field using the following query “db.collection.find({}, {_id: 0, name: 1, age: 0, score: 0, subject: 0, address: 1})” , he is getting an error message in output screen. What need to be changed in the above query to make it run and produce the desired output. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

40. How to check if the field is present or not in a collection in MongoDB. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

42. A boss has given a task to you to give the “name” and “department” of those employees who do not work on Monday and Tuesday of every “week” and having “experience” less than 5. What sort of query you will write for the same purpose. 
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

44. As we know MongoDB is a Document oriented Database. What are the benefits document database gives over others?

<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

46. Does MongoDB writes the data to the disk immediately or not?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

48. What are your thoughts, when anyone says durability is one of the best features of MongoDB?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---
50. Is creating Indexes in MongoDB always helpful?
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---

52. A primary key also known as object-id in MongoDB contains what?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

54. Suppose I have an “address” field in “student” collection and if I removes it from the database, will it also remove it from the disk too?
<details><summary> <b>Show Answer</b> </summary> 

</details>

---

56. Does MongoDB creates any Index by default, when we create any new collection?
<details><summary> <b>Show Answer</b> </summary> 
  
</details>

---
