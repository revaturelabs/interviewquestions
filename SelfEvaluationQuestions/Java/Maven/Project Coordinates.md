## Technical 

1. Explain about Maven Coordinates.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary> <b> Show Answer </b></summary>
	
<blockquote markdown="1">
	
-  Maven coordinates helps us to uniquely identify a project, a dependency or a plugin defined in `pom.xml` file. Based on the combination of a group identifier, an artifact and the version of project.
-  **For example:** If you want to include any library dependency in `pom.xml` file, you have to define the _Maven coordinates_. i.e., - `groupId` , `artifactId` and `version` of that dependency. Below, we have `mysql-connector-java` dependency with Maven coordinates.
```xml
<!-- MySQL database driver -->
<dependency>
	<groupId>mysql</groupId>
	<artifactId>mysql-connector-java</artifactId>
	<version>5.1.9</version>
</dependency>
```
</blockquote>
	
</details>

---

2. List and explain the main coordinates used in Maven.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<blockquote markdown="1">

<details markdown="1"><summary> <b> Show Answer </b></summary>

- `groupId`- Is the way of grouping different Maven artifacts.
- `artifactId` - Is the way of identifying the artifact.(Like JAR, WAR)
- `version` - Particular release of the project, denotes different versions in same artifacts and same repository.
- <b>Example</b> for the coordinates explained above	
	<img width="930" alt="Capture" src="https://user-images.githubusercontent.com/92523245/183573496-fe0e3b37-7998-4fe1-a8f2-296a64c98e7a.PNG">

</blockquote>

</details>

---

3. What will a valid POM file have?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary> <b> Show Answer </b></summary>
	
<blockquote markdown="1">

- A valid POM file should have groupId, artifactId and version. groupId and version can also be inherited from parent POM file.

</blockquote>

</details>

---

4. What are the additional coordinates used in POM?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b> Show Answer </b></summary>
	
<blockquote markdown="1">

- There are two additional coordinates used in Maven but not to uniquely identify the project.
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
	
</blockquote>

</details>

---

5. What is the difference between JAR and WAR files?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"><summary> <b> Show Answer </b></summary>
	
<blockquote markdown="1">
	
- JAR is a file format, used for java archive files.
- JAR files are the only archive format that works across several platforms, which means that any JAR file on your 
	desktop will be atomatically executed with the Java JAR. 
	
- WAR is a file format, used for web application archive files. 
- The benefit of utilizing a WAR file is to consolidate all of the files into a single unit, to reduces the amount of time it takes for the serve to move a file from one client to another client.


</blockquote>
	
</details>

---

6. How can we define Maven coordinates?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary> <b> Show Answer </b></summary>
	
<blockquote markdown="1">

`groupId:artifactId:packaging:version` - through which will express the dependencies of a project in POM file.
	
<b>Example</b> `MySQL:MYSQL-Connector:jar: 6.0`

</blockquote>

</details>

---


