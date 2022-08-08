## Technical

1. What is POM?

<details><summary><b> Show Answer </b></summary>

- Project Object Model -Which is a fundamental unit of work in maven.
- Which resides in the base directory of the project as pom.xml file.

</details>

---

2. What will be stored in pom.xml file?

<details><summary><b> Show Answer </b></summary>

- pom.xml file will store the project structure and instructtions for maven to build the project such as dependencies, source code,plugins, goals 
  etc.
- It contains the information about the project and to instruct the maven too build the project.

</details>

---


3. List the most common terms encountered while using Maven.

<details> <summary> <b> Show Answer </b> </summary>

- groupId - which is a domain ID, identifies the project uniquely.
- artifactId - It is the name of the jar without version.
- version - It creates a version of the project
- Local repository - downloads all required dependencies and stores in this repository.

</details>

---

4. What is the commanly used requirement of a POM?

<details><summary><b> Show Answer </b></summary>

- Project root
- Model version
- groupId
- artifactId
- version

</details>

---

5. Explain about super POM.

<details><summary><b> Show Answer </b></summary>

- It is the maven's default POM.All POMs inherited from base or parent POM called Super POM.
- Which contains values inherited by default.

</details>

---

6. How to view the default configuration of super POM?

<details><summary><b> Show Answer </b></summary>

- By running the command ` mvn help:effective-pom ` we can view the default configuration of super POM.

</details>

---

7. How does a basic POM look like?

<details><summary><b> Show Answer </b></summary>


``` java
<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.mycompany.app</groupId>
  <artifactId>my-app</artifactId>
  <version>1</version>
</project>
```

</details>

---

8. Where does pom.xml file resides?

<details><summary><b> Show Answer </b></summary>

- pom.xml file resides in `projects root-folder`.

</details>

---

9. How can you run a pom.xml file manually?

<details><summary><b> Show Answer </b></summary>

- to run a pom.xml file `right-click the pom. xml file and select Run As Maven build`.

</details>

---

10. What is maven dependency?

<details><summary><b> Show Answer </b></summary>

- A project should have dependency to compile, build, test and run , which is collectively present in pom.xml file.

</details>

---

11. Explain about Maven plugins.

<details><summary><b> Show Answer </b></summary>
  
  - Any action performed on a project is implemented as a maven plugin.
  - whcih is used to create jar files, create war files, compile code, unit test code, create project documentation etc.
  
</details>

---

12. What is a Mojo?

<details><summary><b> Show Answer </b></summary>
  
  - A mojo is a Maven plain Old Java Object. Each mojo is an executable goal in Maven, and a plugin is a distribution of one or more related mojos.
 - It is a goal in maven, a plug-in can have any number of goals.
 - Which specifies the metadata about the goal. The goal name, which phase of lifecycle it fits in and parameters its excepcting.
 
</details>

---

13. Explain about Snapshot.

<details><summary><b> Show Answer </b></summary>

-It is a special version of a Maven package that refers to the latest production branch code. It is a development version that precedes the final release version. 
- We can identify a snapshot version of a Maven package by the suffix SNAPSHOT that is appended to the package version.

</details>

---

14. List the type of plug-ins used in maven.

<details><summary><b> Show Answer </b></summary>
  
- **Build plugins**-which is executed during the build and they should be configured in the <build/> elements from the POM.
- **Reporting plugins**-which is executed during the site generation and they should be configured in the <reporting/> elements from the POM.
- **Core plugins **- where the Plugins corresponding to default core phases (ie. clean, compile). They may have multiple goals as well.
- **Packaging types/tools -** which relates to packaging respective artifact types.
- **Tools**-which are miscellaneous tools available through Maven by default.
  
 </details>
 
 ---
  
  





