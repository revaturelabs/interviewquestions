## Technical 

1. Explain about Maven Coordinates.

<details><summary> <b> Show Answer </b></summary>

-  Maven coordinates helps us to uniquely identify a project, a dependency or a plugin defined in `pom.xml` file. Based on the combination of a group identifier, an artifact and the version of project.
-  **For example:** If you want to include any library dependency in `pom.xml` file, you have to define the _Maven coordinates_. i.e., - `groupId` , `artifactId` and `version` of that dependency. Below, we have `mysql-connector-java` dependency with maven coordinates.
```xml
<!-- MySQL database driver -->
<dependency>
	<groupId>mysql</groupId>
	<artifactId>mysql-connector-java</artifactId>
	<version>5.1.9</version>
</dependency>
```
</details>

---

2. List and explain the main coordinates used in maven.

<details><summary> <b> Show Answer </b></summary>

- `groupId`- Is the way of grouping different maven artifacts.
- `artifactId` - Is the way of identifying the artifact.(Like JAR, WAR)
- `version` - Particular release of the project, denotes different versions in same artifacts and same repository.
- <b>Example</b> for the coordinates explained above	
	<img width="930" alt="Capture" src="https://user-images.githubusercontent.com/92523245/183573496-fe0e3b37-7998-4fe1-a8f2-296a64c98e7a.PNG">


</details>

---

3. What does a valid POM file should have?

<details><summary> <b> Show Answer </b></summary>

- A valid POM file should have group identifier, artifact and version. Group id and version can also be inherited from parent POM file.

</details>

---

4. What are the additional coordinates used in POM?

<details><summary> <b> Show Answer </b></summary>

- There are two additional coordinates used in maven but not to uniquely identify the project.
	- **Packaging** - Which defines the project type (WAR,JAR).
	- **Classifiers** - Which is used to distinguish between the artifacts created for two versions.
- **Example** for these coordinates.
``` java
	  <dependency>
	  <groupId>com.javatpoint.application1</groupId>  
 	  <artifactId>my-application1</artifactId>  
 	  <version>1.0</version>  
  	  <packaging>jar</packaging>  
	  <classifier>sources</classifier>
          </dependency>
```
	
</details>

---

5. What is the difference between JAR and WAR files?

<details><summary> <b> Show Answer </b></summary>
	
- JAR is a file format, used for java archive files.
	- JAR files are the only archive format that works across several platforms, which means that any JAR file on your desktop will be 
	  automatically executed with the Java JAR. 
	
- WAR is a file format, used for web application archive files. 
	- The benefit of utilizing a WAR file is to consolidate all of the files into a single unit, to reduces the amount of time it takes for the  		user to move a file from one client to another client.


</details>

---

6. How can we define maven coordinates?

<details><summary> <b> Show Answer </b></summary>

`groupId:artifactId:packaging:version` - through which will express the dependencies of a project in POM file.
	
<b>Example</b> `MySQL:MYSQL-Connector:jar: 6.0'

</details>

---


