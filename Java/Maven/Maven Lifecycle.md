## Technical

1.  List the valid lifecycle goals in maven?

<details><summary><b> Show Answer </b></summary>

Here are some of the most important phases in the default build lifecycle:
 
  - `validate`: check if all information necessary for the build is available
  - `compile`: compile the source code
  - `test-compile`: compile the test source code
  - `test`: run unit tests
  - `package`: package compiled source code into the distributable format (jar, war, …)
  - `integration-test`: process and deploy the package if needed to run integration tests
  - `install`: install the package to a local repository
  - `deploy`: copy the package to the remote repository

</details>

---

2. Mention the three standard lifecycle followed in maven.

<details><summary><b> Show Answer</b></summary>

- clean
- default(or build)
- site

</details>

---

3. How does the order of execution is decided in maven?

<details><summary><b> Show Answer</b></summary>

- It depends on the order of which goals and phases invoked.
- Here clean and package are arguments of build phase , others are termed ad goals.
- **Example** : ` mvn clean dependency:copy-dependencies package`.
- Clean will be executed first then dependency and finally package will be executed.

</details>

---

4. Which command is used to invoke clean lifecycle?

<details><summary><b> Show Answer</b></summary>

- Clean lifecycle can be executed by running the command `mvn post-clean`.
- Which can be of following phases
    - `pre - clean`
    - `clean`
    - `post - clean`

</details>

---

5. Mention some commands used in maven project.

<details><summary><b> Show Answer</b></summary>

- `mvn compile`: used to compile the project’s source code.
- `mvn clean`: used to clean or remove all previous-build files generated.
- `mvn test`:used to run project testing steps.
- `mvn test-compile`:used to compile the code from the test source.
- `mvn install`:used to deploy the packaged WAR/JAR files storing them as classes in the local repository.
- `mvn package`:used to create packages or a project WAR or JAR file to be able to use a distributable format.
- `mvn deploy`:used after compilation, running project tests and project building.

</details>

---

6. List the phases used in site lifecycle.

<details><summary><b> Show Answer</b></summary>

- Pre site:process before generating the actual project site;
- Site: generate the site document of the project;
- Post site:the process required to complete site generation;
- Site deploy :deploy the generated site documents to the specified web server.

</details>

---

7. List the type of maven build profiles.

<details><summary><b> Show Answer</b></summary>

- `Per-User`:described in Maven settings.xml file.
- `Per Project`:described in pom.xml of the project.
- `Global`:described in the global Maven settings.xml file.

</details>

---

8. List the phases used in default lifecycle.

<details><summary><b> Show Answer</b></summary>

- Setup 
- Compilation 
- Testing
- Packaging 
- Integration Test 
- Release

</details>

---

9. Explain Archetype.

<details><summary><b> Show Answer</b></summary>

- It is a Maven plugin used to create a project structure as per its template.
- This command is used ` mvn archetype:generate ` to create a new project based on Archetype.

</details>

---

10. What command will be used to package the Maven project?

<details><summary><b> Show Answer</b></summary>
 
- `mvn - package` is used to package the project.

</details>

---

