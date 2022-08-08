## Technical

1. What is POM?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- Project Object Model -Which is a fundamental unit of work in maven.
- Which resides in the base directory of the project as pom.xml file.

</details>

---

2. What will be stored in pom.xml file?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- pom.xml file will store the project structure and instructtions for maven to build the project such as dependencies, source code,plugins, goals etc.

</details>

3. What are the attributes used to uniquely identify the project in repository?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- The project group(groupId), name(artifactId) and its version- these attributes need to decided before creating a POM to identify the project.

</details>

---

4. What is the Minimal requirement for a POM?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- Project root
- Model version
- groupId
- artifactId
- version

</details>

---

5. Explain about super POM.

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- It is the maven's default POM.All POMs inherited from base or parent POM called Super POM.
- Which contains values inherited by default.

</details>

---

6. How to view the default configuration of super POM?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- By running the command ` mvn help:effective-pom ` we can view the default configuration of super POM.

</details>

---

7. How does a POM look like?

<details> <summary> <b> Show Answer </b> </summary> </deatils>


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

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- pom.xml file resides in `projects root-folder`.

</details>

9. How to run a pom.xml file?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- to run a pom.xml file `right-click the pom. xml file and select Run As Maven build`.

</details>

---

10. What is maven dependency?

<details> <summary> <b> Show Answer </b> </summary> </deatils>

- A project should have dependency to compile, build, test and run , which is collectively present in pom.xml file.

</details>

---


