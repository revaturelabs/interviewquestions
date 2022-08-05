## Technical 
1.What is maven?

<details> <summary> <b> Show Answer </b> </summary>

- Maven is a tool used in Java to build a project and to handle dependency and documentation.
- It is based on POM. (Project Object Model) : which is an XML file, contains information to project a configuration information to build the project.

</details>

---

2.List the uses of Maven.

<details> <summary> <b> Show Answer </b> </summary>

- Maven is a building tool used for creating projects , build reports , integerating , deals with dependency and documentation.
- It has made the life of develeoper easier, by making the process of building projects simple.
- It increases the reusability.

</details>

---

3. Does maven need Java to be executed?

<details> <summary> <b> Show Answer </b> </summary>

Yes

<details> <summary> <b> Explanation </b> </summary>

- We need Java to execute maven. Java should be installed to set <code> JAVA_HOME environment varaiable </code> to point to a valid Java SDK(Like Java 8)

</details>

</details>

---
4. Which is the most fundamental unit of maven system?

<details> <summary> <b> Show Answer </b> </summary>

- POM (Project Object Model)- which is an XML file having the details of project  strccture and contents termed as pom.xml file.

</details>

---

5. What does a build tool has to manage?

<details> <summary> <b> Show Answer </b> </summary>

- Generate source code
- Create documentation from the source code generated.
- Compiles the source code
- Packages the compiled code into JAR of ZIP file.
- Install the packaged code into Local repository, Server repository and Central repository.

</details>

---

6. What is the command used to create a simple projet using Maven?

<details> <summary> <b> Show Answer </b> </summary>

- We can create a simple project in maven using <code> archetype:generate </code> in command promt using maven.
- Syntax to generate a project architecture

<code>

mvn archetype:generate -DgroupId=groupid -DartifactId=artifactid   
-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=booleanValue

</code>

</details>

---

7. How to compile the maven project?

<details> <summary> <b> Show Answer </b> </summary>


 - To compile go to the project directory.(like: C:\Users\IT\SQUARECALCULATOR) and write the follwoing command 

<code>

mvn clean compile  

</code>

- When you check your project directory, target directory will be craeted.

</details>

---

8. How to run the maven project?

<details> <summary> <b> Show Answer </b> </summary>

 - To run the project, go to the project directory\target\classes.(like: C:\Users\IT\SQUARECALCULATOR\target\classes) and write the follwoing command 

<code>

java com.javatpoint.App  

</code>

</details>

---

9. How to package a maven project?

<details> <summary> <b> Show Answer </b> </summary>

- mvn package command completes the maven lifecycle as
    1. validate
    2. compile
    3. test
    4. package
    5. integration
    6. verify
    7. install
    8. deploy

</details>

---


10. When a jar file will be craeted in the project?

<details> <summary> <b> Show Answer </b> </summary>


- Jar file will be created inside the project/target directory, When you execute the command <code> mvn package </code> in the command prompt to package the maven project.

</details>

---  

11. List some scenarios where the maven should be used in the project.

<details> <summary> <b> Show Answer </b> </summary>

- If the project needs to have quick documentation, compiling and packaging of source coide into JAR/ZIP files.
- If the project requires a huge amount of dependencies.
- If the version of dependecies requires a frequent up-gradation.

</details>

---

12. In which repository does the dependencies will be loaded?

<details> <summary> <b> Show Answer </b> </summary>

- The dependencies will be loaded in  the Local repository

</details>

---

13. What will be stored in pom.xml file?

<details> <summary> <b> Show Answer </b> </summary>

- It contains the information about the project and to instruct the maven too build the project.

</details>

---

14. Define Build tool.

<details> <summary> <b> Show Answer </b> </summary>

- It is to set up all the requirements to run a java program independently. Which generates source code, compile and package the code into JAR file.

</details>

---

15. List some general phrases used in Maven.

<details> <summary> <b> Show Answer </b> </summary>

- groupId - which is a domain ID, identifies the project uniquely.
- artifactId - It is the name of the jar without version.
- version - It creates a version of the project
- Local repository - downloads all required dependencies and stores in this repository.

</details>

---






