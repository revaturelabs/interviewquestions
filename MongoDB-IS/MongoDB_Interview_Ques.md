
# MongoDB Interview Questions

1. Does `MongoDB` support primary-key and foreign-key relationship? If yes, then how?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> `MongoDB`,  by-default, does not support primary and foreign key relationship. But we can achieve it by embedding one document inside another one. For example, embedding 'city' document inside 'address' document. 
</details>

---

2. Using the Aggregate function `$avg` write a MongoDB query.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> `db.student.aggregate([{$group : {_id:null, Average_marks : {$avg : "marks"}}}])`. Here we are getting average of the marks field in student collection.
</details>

---

3. Use the Aggregate function `$sum` to write a MongoDB query. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> `db.student.aggregate([{$group : {_id:null, Total_marks : {$sum : "marks"}}}])`. Here we are getting sum of the marks field in student collection.
  </details>
 
 ---
 
4. In a find() query like `db.collection_name.find({ "school.student": "Jack"})` , what could be school and what could be a student?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> In `db.collection_name.find({ "school.student": "Jack"})` query, "school" is a outer document field and "student" is a inner document field.  

</details>

---

5. When creating a database in MongoDB, if you are getting "could not connect to the server" error, then what steps you will follow to resolve that error. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> To resolve the "could not connect to the server" error, we can take few measures like:
> 1. We must ensure that we put correct hostname and port number. 
> 2. If any firewall is blocking your port connection, uninstall that firewall or try to connect from different server.
> 3. Must ensure that your MongoDB instance is running in the background.
> 4. If server is shutdown then i will start the server again.
</details>
 
---

6. Suppose you are collaborating with your team on “ABC” database which have some data inside it. How can you make sure that if someone by mistake deletes the “ABC” database, you can still have a backup of that database. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> To make sure that we have a backup of our database, we can use the `mongodump` command that will store our data in a backup file. For that, we just have to write `mongodump --db database_name -- collection collection_name`.  
   
To import again the backup file in Mongodb we can use the mongorestore command:     
`mongorestore --db database_name path_of_file`  


</details>

---

7.  What `insert()` method returns after successfully inserting a document into a collection.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> It returns an object that contains the information about the operation. It returns a `WriteResult` object when we insert a single document and `BulkWriteResult` object when we insert more than one document in a single insert query.
</details>

---

8.  When a person inserts a document into collection, MongoDB automatically creates an `_id` field which acts as a primary key for that data, then how can we set one of our fields as primary key in MongoDB if we want? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> The `_id` field is the default primary key in `MongoDB` and it is reserved , we cannot create any other primary key but, we can put the data that we want to be unique into the `_id` field of the document like `{"_id" : 01}`. 
</details>

--- 

9. Create a “Company” database and make a collection as “Department” in it. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>
  
```
use Company;
db.createCollection("Department");
```
</details>

---

10. Imagine you have an “employee” database and “emp” collection. Write a query to update salary of an employee by 1000 where name ="Jack".

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
 
```
use employee;
db.emp.update({"name": "Jack"}, {$inc: {"salary": 1000}});
```
</details>

--- 

11. Tell the difference between `update()` and `save()` method in MongoDB.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> The `update()` method is used to update the existing document values in MongoDB without creating a new document. Whereas, `save()` method is used to replace the existing document with the document passed in the `save()` method. 
</details>

---

12.  Write a single query that will perform update operation if document is present in the collection and if not, then it performs insert operation. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> To perform both update and insert operations in a single query by making "upsert" option to "true" inside the `update()` method.  
  
```
db.collection_name.update({name:"Henry"}, {$set: {dept: "HR"}},{upsert:true});
```
</details>

---

13. Imagine you have added 5 documents into a collection named as “emp” and suddenly there is a need to add one common field into all the five documents then what query you will write for the same purpose? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
  db.emp.update({}, 
  {$set: 
  {address: 1}}, 
  {multi: true});
```
Here address is the field that has to be added in all the documents.  
</details>
  
--- 

14. Suppose a document have five fields as “name”, “age”, “salary”, “dept”, “address” and if you want to remove the “age” field from the document of “emp” collection, then what query you will provide to remove only “age” field?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.emp.update({}, 
  {$unset: 
  {"age": 1}}, 
  {multi: true});
```
</details>

---

15. How do you fetch the employees, from “emp” collection, whose name starts with ‘A’. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
 
>
```
db.emp.find({name: /A/});
```
</details>

---

16. State the difference between update() and findAndModify() method in MongoDB.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> - The update() method can update the multiple documents at a time, whereas the findAndModify() method, by default, can update the single document at a time.   
  
> - The update() method does not return any document after updation, whereas the findAndModify() method returns the pre-modified document.
</details>

---

17. Suppose you have a “Company” database and “emp” collection inside that database then how do you find the records of top 5 employees based on salary field?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> To find the top 5 records, we can use the sort() and limit() method along with find().  
   
```
db.emp.find({})
  .sort({"salary":-1})
  .limit(5)
```

</details>

---

18. Write a query to get all the records of employee whose “age” is greater than 25 and “experience” greater or equal to 3 years. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 
  
> 
```
db.collection_name.find({ 
  $and: [
  {"age": {$gt: 25}}, 
  {"experience": {$gte: 3}}
  ]
  });
```
</details>

---
19. What is the difference between findOneAndReplace() and findOneAndUpdate() in MongoDB?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> The `findOneAndUpdate()` will update the fields of the document that are passed in the query. whereas the `findOneAndReplace()` will not only update the fields of the document that are passed in the query but also replaces or deletes the fields of the documents that are not passed to it in query.
 
</details>

---
20. Differentiate between `findOneAndReplace()` and `replaceOne() in MongoDB?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Both `findOneAndReplace()` and `replaceOne()` in MongoDB is used to replace the document's fields based on filter criteria, but the main difference between both is that `findOneAndReplace()` returns a pre-modified document by default whereas `replaceOne()` doesn't return any document. 
</details>

---

21. Imagine you are working on “Company” database having “Dept” as collection and inside your collection there are millions of documents and your boss is asking for some data from it, then what sort of practice you will do to increase the query performance and fast retrieval of data. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> There are few practices that one can follow to increase the query performance and fast retrieval of data:  
> 1. We can create and use the indexes on the fields that are frequently being a part of query.   
> 2. While doing the find(), we can use projection to select only those fields that are required in the result.   
> 3. We can also use the limit() method to limit the data that we want in our result.   

</details>

---
22. Consider your documents have some array fields and you want to create an index on it. Is it possible in MongoDB? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
 
> Yes, it is possible to create index on an array field. MongoDB automatically creates the multikey index for each value of an array.  For example, let’s take an array field which holds the values as address : [ "NY", "MIAMI","TEXAS"], we can create an index on that field by writing:    
`db.collection_name.createIndex({“address” : 1})`

</details>

---
23. What sort of practice you will take as a developer to increase the availability of data in MongoDB when there is a routine maintenance check or system failure?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> As a developer we must make sure that all the data are not present in one single server or machine.   
> -	We can distribute the data into different systems , so that if one system fails, we can get the data from other systems.   
> -	We can also distribute the data into multiple servers of one system, so that we can get the easily use the other server in case of downtime of one server.   

</details>

---

24. What query do you write to get employee details in “emp” collection where “job_role” matches “Technical Specialist” and  “emp_age” is between 22 and 28? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.emp.find({
  $and: [
  {"job_role":"Technical Specialist"}, 
  {"emp_age": {$gte: 22 , $lte: 28}}
  ]
  });
```
</details>

---

25. An intern in your company is asking for your help to fetch the records of “department” that belongs to “product”, but “type” should not equal to “A” and whenever the “type” is equal to “A”, the “department” should not equal to “product”. Here is the collection he is using to fetch the data:  
```
{ "department" : "product", "type" : "A" }  
{ "department " : "training", "type" : "A" }  
{ “department " : "product", "type" : "B" }  
{ "department " : "finance", "type" : "C" }  
```
Help him to write a query that will produce the output as:   
```
{ "department " : "training", "type" : "A" }  
{ “department " : "product", "type" : "B" }
{ "department " : "finance", "type" : "C" }
```

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.collection_name.find({
    "$or": [
    {"department": {"$ne": "product"}},
    {"type": {"$ne": "A"}}
  ]
})
```
</details>

---

26. Give me the query that will fetch only “name” and “age” field from the collection “emp”, that having the “DOB” between 01/03/1990 to 31/12/1999 and “salary”  greater than “50k”. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
  
> 
```
db.emp.find({
  "$and: [
  {"DOB":{$gte: ISODate("1990-03-01"), $lte: ISODate("1999-12-31")}},
  {"salary":{$gt: 50000}}
  ]},
  {_id:0, name:1, age: 1}
  );
```
</details>
  
---

27. Write the single query that will give the sorted result based on “dob” field that satisfies the following condition:
i) Where “name” starts with “s” alphabet and “salary” in between 40k to 70k 
ii) Where “department” not equal to “product”. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
 
> 
```
db.collection_name.find({
  $and: [
  {"name": /s/},
  {"salary": { $gte: 40000, $lte: 70000}},
  {"department": { $ne: product}}
  ]})
  .sort({"dob": 1}); 
```
</details>

---

28. Jack is trying to fetch all the records, from a collection called “people”, without including the `_id` field. When he wrote the query as `db.people.find({} { _id: 0})`, he was getting syntax error message stating “unexpected { ”. What he needs to change in his query to get the desired output. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> The only problem in the `db.people.find({} { _id: 0})` is missing comma after empty {} inside find() method. To resolve this error,jack has to write the query as `db.people.find({}, { _id: 0});`. 
</details>

---

29.  Write a query that will fetch the top 20 records from “student” collection of those students who are from 8th, 9th and 10th “class” having “marks” greater or equal to 70 in science and math subject.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.student.find({
      $and: [
      {"class": {$in: ["8th", "9th", "10th"]}},
      {"marks.science": {$gte: 70}},
      {"marks.math": {$gte: 70}}
      ]})
      .limit(20);

```
</details>

---

30. A developer doesn’t want to see the first 10 documents of “dept” collection and doesn’t have the permission to delete any document from the collection as well, so what query he must write to see the rest of the documents after 10 documents without deleting any document?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Using skip() method, we can skips the number of documents based on our need.
```
db.dept.find({}).skip(10);
```
</details>

---

31. Write a query to get the number of employees whose “address” is “New York” having “age” less than equal to 40  and earning salary greater than 50K. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.collection_name.find({
      "$and: [
      {"address": "New York"},
      {"age": {$lt: 40}},
      {"salary": {$gt: 50000}}
      ]})
      .count();
      
```
</details>

---

32. As 1 and -1 are used to represent  ascending and descending order respectively in sort() method, then what will happen if we use -2 or 2 instead in sort(). 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> If we use -2 or 2 with the fields inside sort() method instead of using -1 or 1, MongoDB will throw an error for that. Only 1 can be used with the fields that we want to sort in ascending order and -1 can be used with the fields that we want to sort in descending order. 
</details>

---

33. In a document having 5 fields “name”, “age”, “score”, “subject” and “address”, when your friend is trying to fetch only “name” and “address” field using the following query “db.collection.find({}, {_id: 0, name: 1, age: 0, score: 0, subject: 0, address: 1})” , he is getting an error message in output screen. What need to be changed in the above query to make it run and produce the desired output. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> In the projection query, we cannot use combination of 0 and 1. It should be either all 1 or all 0, except _id field value. So to get rid of that error we can re-write the query as:  
`db.collection.find({}, {_id: 0, name: 1, address: 1});`   
Here we are selecting only name and address fields from the data.
</details>

---

34. How to check if the field is present or not in a collection in MongoDB.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 
 
> To check if the field is present or not in the mongodb we can use $ne operator in the `find()` method query.  
```
db.collection.find({
          "Field_value": {
           $ne: null}
           });
```
</details>

---

35. A boss has given a task to you to give the “name” and “department” of those employees who do not work on Monday and Tuesday of every “week” and having “experience” less than 5. What sort of query you will write for the same purpose. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```
db.collection_name.find({
       $and : [
       {"week": {$nin : [ "Monday", "Tuesday"]}},
       {"experience" : {%lt : 5}}
       ]},
       {"_id": 0, "name" : 1, "department" : 1}
       );
```
</details>

---

36. As we know MongoDB is a Document oriented Database. What are the benefits document database gives over others?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> There are many advantages document database gives over Relational or other databases:    
> 1. They are schema less. They doesn't have any structure.  
> 2. No need to have same number of fields in all the documents. Some may have > 4 fields while others may have 3 or 5 fields.
> 3. They have replica set that contains duplicate data in it. So if one server fails we can still recover the data from other servers.   
> 4. All the documents can be independent of one another as they don't have foreign keys concept.  
</details>

---

37. Does MongoDB writes the data to the disk immediately or not?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> No, MongoDB doesn't write the data to the disk immediately. Firstly, it pushes the write to the journals and from journal it pushes the data to the disk. Therefore it is not an immediate action. 
</details>

---

38. What are your thoughts, when anyone says durability is one of the best features of MongoDB? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Yes, it is correct that durablity is one of the best features of MongoDB.  
Whenever there is a server failure or system crashes, we can still recover the data from the journal nodes as well as we can get the data from different replica sets.   
</details>

---
39. Is creating Indexes in MongoDB always helpful?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> We cannot deny the fact that using indexes efficiently in MongoDB can increase query performance, But there are some disadvantages of indexes as well like:  
> - Each index that we create takes around 8 kB of space in memory. So, if we have many indexes that are not in use frequently will drain our resources. 
> - Whenever we update or delete the documents, the indexes that are associated with that document also be updated. And these indexe updates hinder the write performance badly.
</details>

---

40. A primary key also known as object-id in MongoDB contains what?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> An object-id in MongoDB also refers as primary key consists of 12-byte BSON type. Out of those 12 bytes:  
> - 4 byte represents the time in seconds, when it is created.
> - 5 byte represents the Unique-id of the system and that is unique to the machine and process. 
> - 3 byte increment represents the increment counter generated randomly. 
</details>

---

41. Suppose I have an “address” field in “student” collection and if I removes it from the database, will it also remove it from the disk too?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Yes, one we remove any field or fields from the document or a whole document, it will also be removed from the disk too.
</details>

---

42. Does MongoDB creates any Index by default, when we create any new collection?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Yes, MongoDB creates an Object-Id that is `_id`, which also works as an Index by default.   
</details>

---

43. Give the steps to connect MongoDB with Python?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> - To connect MongoDB with Python application we first have to install and import the `pymongo` Module. 
> - Then from pymongo import the MongoClient, that will help in putting the connection string.
> - Then we have to pass the hostname and port number as an parameter to MongoClient instance and our connect will be ready.
> - At last, after doing all the opertions, close the connection using close() method.
  
</details>

---

44. How will you insert more than one document at a time without using default `insert()` method?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> To insert multiple documents thorugh a single query we can use the insertMany() command. for example,   
``` 
db.collection.insertMany([{name: "Jack", dept: "training"},
                          {name: "Henry", dept: "finance"},
                          {name: "Tom", dept: "product"}]);
```
> It will inserts 3 documents at a time.
  
</details>

---

45. How will you delete only first document having "name" equal to "Tom"?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> To remove only one document without effecting any other document, we can use the `remove()` method with 'justOne' parameter set as 1.      
```
db.collection_name.remove({"name" : "Tom"},1);
```
  
</details>

---

46. Is `remove()` and `deleteMany()` methods in MongoDB are same?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> Both the methods in MongoDB is used to delete documents. The only difference between both is the value return after deletion operation.  
> - The `remove()` method return a WriteResult object.
> - The `deleteMany()` method returns a document conatining acknowledged value and deleted count. 
  
</details>

---

47. What is the use of `pretty()` method in MongoDB?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> `pretty()` when applied with the `find()` method, it will display output documents in an easy to read format. Without `pretty()` if the documents have so many fields and we fetched all the documents fields through `find()` then it is very difficult to read values from each document as it will show one document in one line only.
  
</details>

---

48. Tell me what do you understand by vertical scaling and horizontal scaling?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> - Vertical scaling refers to adding additional resouces in a single system to increase it performace such as ram, cpu, etc. 
> - Horizontal scaling refers to adding multiple servers to a single server and partitioning the dataset over those server.
  
</details>

---

49. Which method can be used to see the results in a formatted way?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
  
> We can use the `pretty()` method to format the resulted documents.
  
</details>

---

50. Explain about sharding in MongoDB?

<details><summary> <b>Show Answer</b> </summary> 
  
> It is the process of adding data across multiple servers so that if one server is down we can still utilize the data from other servers. MongoDB supports sharding by breaking the larger datasets into smaller data sets and sending it to other servers. It increases the redundancy of data and provides durability in times of failure.
  
</details>

---

51. Explain the work of primary and secondary replica sets in MongoDB?

<details><summary> <b>Show Answer</b> </summary> 

> - The primary replica set is a master replica that receives the write operations, on the other hand secondary replica set is used only for read operations. 
> -  The primary replica set will always be one in the count, whereas secondary replica sets can be one or more than one. 
> - Both primary and secondary replica sets provides the redundancy of data and at the time of failure of primary replica, one of the nearest secondary replica becomes the primary replica set and process remains uneffected. 
> - After the write operation by primary replica node, the secondary replicas will replicate the data from primary through log files.

</details>

---

52. How will you say MongoDB doesn't have schema?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 

> In MongoDB, one document can have 4 fields while other documents can have same or more or less fields. There is no restriction of having same number of fields in all the documents inside collection, which makes it schemaless. 

</details>

---

53. Does MongoDB stores it data to RAM or Disk?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 

> MongoDB stores it data to RAM first but later on all the RAM data has been stored into Disk, so that at the time of failure the MongoDB will gets it data from disk without any loss. 

</details>

---

54. Stating MongoDB as one of the best NoSQL database is always true, but at what time it is not prefered?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 
> There are few limitations that MongoDB have such as:  
> - There are no joins that we can use with MongoDB.
> - Document size is limited to only 16mb.
> - MongoDB doesn't have support of transaction by default.
> - One MongoDB collection cannot have more than 64 indexes. 

</details>

---

55. Does MongoDB stores data in JSON format or BSON format? And what is the difference between both, if any?

<details><summary> <b>Show Answer</b> </summary> 

> MongoDB stores the data in BSON format. Although both JSON and BSON looks same still there is one difference between them:     
> - JSON is a text based format which stores the data in key-value pairs, on the other hand BSON is a binary format of JSON that provides efficient space in memory to store large data as well as it optimizes the speed to fetch the data from Memory.   
> Because of this only it becomes the ideal choice to store the data in BSON format.

</details>

---

56. Tell me the types of indexes in MongoDB?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 

> - We have deafult index in MongoDB as '_id'
> - Single field indexes are also there, which uses single fields.
> - Compound Indexes are used to combine multiple fields of a document.
> - Multi-key indexes are used for array fields.

</details>

---

57. After starting the MongoDB daemon how can we see the number of connected devices?

<details><summary> <b>Show Answer</b> </summary> 

> Using `db.serverStatus()` method we can see the information about number of connections as well as the available connections. For that we have to write ` db.serverStatus().connections`.

</details>

---

58. At a time, how many connections a MongoDB can handle?

<details><summary> <b>Show Answer</b> </summary> 

> By default MongoDB can handle 64k connections. But it can be changed by going into the configuration file of MongoDB.

</details>

---

59. In MongoDB, how do we see the connections utilized?

<details><summary> <b>Show Answer</b> </summary> 

> Using `db_adminCommand("connPoolStats")` we can see the connections utilized by MongoDB.

</details>

---

60. Tell me the basic CRUD operations of MongoDB?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary> 

> To perform the basic CRUD opertions we can use the following methods:
> - `insert()` method for entering documents into collections.
> - `find()` method for reading documents values.
> - `update()` method to change the values of a document.
> - `remove()` method to delete any document from the collection.

</details>

---

61. Give the query that will find the count of number of resturants that are present in texas, florida and alaska state.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.resturants.find(
        {"state": { 
        $in : [ "texas", "florida", "alaska"]}
        }).count();
```

</details>

---

62. From "revature" company collection fetch the name and experience of those employees who are not working in night shift.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.revature.find({"shift": {
                 $ne: "night"}},
                 {_id:0, name:1, experience: 1});
```

</details>

---

63. Give a query in MongoDB that will tell whether all the "address" contain "NY" or not in "emp" collection. 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.emp.find({
             "address.NY":
             { $exists : true}
             });
```

</details>

---

64. Your boss is asking you to give the emp_id, name and dept of those employees who works from everywhere except Florida and NY. What query you will write to complete that task?  

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.collection_name.find({
                   $and : [
                   {"state" : {$ne : "Florida"}},
                   {"state" : {$ne : "NY"}}
                   ]},
                   {"empid" : 1, "name" : 1, "dept" : 1}
                   );
```

</details>

---

65. Suppose you are having a collection as "company" and you want to fetch the deatils of those employees whose are from "training" department based on their experience in the industry. What query you will write to get what you want.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.company.find({
               "department" : "training"}
               )
               .sort("experience" : -1);
```
</details>

---

66. In MongoDB, write a query that will give details of all the employees based on their "DOJ"(data of joining) in ascending order and  "salary" in descending order.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

>
```
db.collection_name.find()
                   .sort(
                   {"DOJ" : 1,"salary" : -1}
                   );
```

</details>

---

67. Imagine you are a Food Investigator Specialist and you are checking the database of a company having collection as "food" that is used by the company to store the food items details. Your task is to fetch the details of those food "items" that having a "grade" as "A+" and having "MD" (manufacturing date) on those items as "2022-08-25".



<details><summary> <b>Show Answer</b> </summary>

>
```
db.food.find(
            { "items.grade" : "A+" ,
             "MD" : ISODate("2022-08-25")
            });
```     
             

</details>

---

68. As a food investigation specialist your task is to fetch the details of those restaurants "name" and "address" who are using "palm oil"  as a "food_oil" in making of their dishes. You have to send the report to the higher authorities, so that they can take actions on those resturants.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.resturants.find(
                  { "food_oil" : "palm oil"},
                  {"_id": 0, "name" : 1, "address" : 1}
                  );
```  

</details>

---

69. For storing documents and doing opertaions on those data requires MongoDB to use lot of RAM?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> No, MongoDB doesn't requires lot of RAM to store those documents and doing operations on those documents because it automatically allocates and deallocates the RAM based on the operations requirements.  

</details>

--- 

70. In MongoDB, what do you understand by covered query?

<details><summary> <b>Show Answer</b> </summary>

> A covered query is the one whose fields in the query are the part of indexes as well as the returned output fields also contains those same index.

</details>

---
71. If an index is not fit into the RAM then what will happen in MongoDB at that point?

<details><summary> <b>Show Answer</b> </summary>

> If RAM has no space to fit the indexes in it, then MongoDB takes the data from the disk which is relatively slow compared to taking data from the RAM.

</details>

---

72. How you will check how many indexes your teammate created on the "school" collection?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> By using `getIndexes()` method, we can check the list of indexes in MongoDB.  
```
db.school.getIndexes()
```

</details>

---

73. In MongoDB, by-default locking and transcations are not suppoted, then is there any way to achieve those concepts?

<details><summary> <b>Show Answer</b> </summary>

> yes, we can achieve the concepts of locking and transcations by putting one document inside another document also called as nested documents. By this way, MongoDB supports atomic operations.

</details>

---

74. Can we say that MongoDB reads and writes data from both primary and secondary replica set? 

<details><summary> <b>Show Answer</b> </summary>

> No, In MongoDB, only primary replica set has the right to do the write operations but not secondary replica set. 
  
</details>

---

75. Is embedding one document inside another document gives some benifit in MongoDB?

<details><summary> <b>Show Answer</b> </summary>

> We can consider embedding documents when:  
> - We need to attain primary-forign key relationship.
> - We want to do atmoic transaction opertaions on the document.
> - We need to attain one-to-many relationship between fields.
  
</details>

---

76. Why the newer versions of MongoDB are not preferred for 32-bit systems?


<details><summary> <b>Show Answer</b> </summary>

> While storing Data and indexes in MongoDB we cannot predict how much total space the server will requries for storing all these things. And as the total storage space in 32-bit systems are fixed to 2 gigabytes only, which is not suitable for production scenarios. therefore, 64-bit systems are preferred over 32-bit systems, that have unlimited server space for storage virtually.
  
</details>

---

77. While working on a system how will you check whether you are working on the master server?

<details><summary> <b>Show Answer</b> </summary>

> We can check by using `db.isMaster()` command, that returns a document containing the status of a replica set. and also tells whether it is a part of primary replica or secondary replica set.
  
</details>

---

78. Give the query that will display the number of employees from "emp" collection who have achieved "H1" reward in january and feburary month.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.emp.find({
             "award" : "H1" ,
             "month" : {$in : ["january", "feburary"]}
             })
             .count();
```
  
</details>

---

79. You are a headmaster of a school and you want to check the details of those students who have got marks less than 33 in chemistry and physics subjects and are from 11th and 12th class. Your school is maintaining one school database having students as a collection in MongoDB.

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.students.find({
                 $and : [
                 {"marks" : {$lt : 33}},
                 {"subjects" : {$in : ["chemistry", "physics"]}},
                 {"class" : {$in : [ "11th" , "12th"]}}
                 ]});
```

</details>

---

80. As a flying investigating officer you are managing a Database in MongoDB about the flights. And now you are trying to get the details of those flights who are flying over texas, florida and alaska states based on their "departure" time in ascending order.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary> <b>Show Answer</b> </summary>

> 
```
db.flights.find({
                "states" : { $in : [ "texax", "florida", "alaska"]}
                })
                .sort( "departure" : 1);
```
                
</details>

---




