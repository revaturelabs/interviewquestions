## Technical

1. What is maven  Repository?

<details> <summary> <b> Show Answer </b> </summary>

- A Maven Repository is a location, generally on a filesystem (either remote or local), where maven artifacts are stored and managed.
- In Maven terminology, a repository is a directory where all the project jars, library jar, plugins or any other project specific artifacts are  
  stored and can be used by Maven easily.

</details>

---

2. List the types of repositories used in maven.

<details> <summary> <b> Show Answer </b> </summary>

- Local repository - present in developer's machine.
- Remote repository - hosted on intranet web server to be used by companies in their own primies.
- Central repository - present in maven community.

</details>

---

3. Explain about Local repository.

<details> <summary> <b> Show Answer </b> </summary>

- Maven stores all the project jar files or dependencies, by default the folder name is .m2. Which refers to developer mchine. All the materials related to project will be stored in this repository.

</details>

---

4. Explain about Remote repository.

<details> <summary> <b> Show Answer </b> </summary>

- Which refers to the repository hosted on intranet web server to be used by companies in their own primies. Used when maven needs to download the   dependencies.
- Remote repository work exactly same way as maven’s central repository. Whenever an artifact is needed, it is downloaded to developer’s local    
  repository and then it is used.

</details>

---

5. Explain about central repository.

<details> <summary> <b> Show Answer </b> </summary>

- It was used to downlaod the dependencies, When there is a need and which was not there in local reposirory.  
- It is the default location for maven to download all the project dependency libraries.

</details>

---

6. How dependencies will be mentioned in pom.xml file?

<details> <summary> <b> Show Answer </b> </summary>

<code>

	<dependency>
	<groupId>com.baeldung</groupId>
	<artifactId>custom-project</artifactId>
	<version>1.3.2</version>
	<type>pom</type>
	<scope>import</scope>
	</dependency>

</code>

</details>

--- 

7. How can we change the location of maven local repository?

<details> <summary> <b> Show Answer </b> </summary>

- We can change the location of maven local repository by changing the settings.xml file.

</details>

---

8. In which order does maven searches for the dependencies?

<details> <summary> <b> Show Answer </b> </summary>

local repository  ->  central repository -> remote repository

</details>

---

9. What will happen if dependency is not found in all three repositories?

<details> <summary> <b> Show Answer </b> </summary>

- If the dependencies are not found, maven stops processing and thrwos an error. 

</details>

---

10. How to install jar files in local repository?

<details> <summary> <b> Show Answer </b> </summary>

- Jar files will be installed in local repository by using the command <code> mvn install </code>.
- Manually also it can be installed by using the plugin `install-file-Dfile =<file path> `.

</details>

---
