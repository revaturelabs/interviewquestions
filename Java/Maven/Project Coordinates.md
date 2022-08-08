## Technical 

1. Explain about Maven Coordinates.

<details><summary> <b> Show Answer </b></summary>

- Which identifies uniquely a project, a dependency or a plugin defined in POM based on the combination of a group identifier, an artifact and the version of project.

</details>

---

2. List and explain the main coordinates used in maven.

<details><summary> <b> Show Answer </b></summary>

- Group identifier- Is the way of grouping different maven artifacts.
- Artifact - Is the way of identifying the artifact.(Like JAR, WAR)
- Version - Particular release of the project, denotes different versions in same artifacts and same repository.

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
        - Packaging - Which defines the project type (WAR,JAR).
        - Classifiers - Which is used to distinguish between the artifacts created for two versions.

</details>

---

5. What is the difference between JAR and WAR files?

<details><summary> <b> Show Answer </b></summary>

- A project with packaging set to JAR will give jar archive. (Java file).
- Whereas one with WAR produces a web application.

</details>

---

6. How can we define maven coordinates?

<details><summary> <b> Show Answer </b></summary>

` groupId:artifactId:packaging:version` - through which will express the dependencies of a project in POM file.

</details>

---


