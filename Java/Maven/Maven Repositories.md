## Technical

1. What is Maven  Repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
	
- A Maven Repository is a location, generally on a filesystem (either remote or local), where Maven artifacts are stored and managed.
- In Maven terminology, a repository is a directory where all the project jars, library jar, plugins or any other project specific artifacts are stored and can be used by Maven easily.
	
</blockquote> 

</details>

---

2. List the types of repositories used in Maven.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Local repository - present in developer's machine.
- Remote repository - hosted on intranet web server to be used by companies in their own premises.
- Central repository - present in Maven community.

</details>
	
</blockquote> 

---

3. Explain about Local repository.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Maven stores all the project jar files or dependencies, by default the folder name is .m2. Which refers to developer machine. All the materials related to project will be stored in this repository.

</blockquote> 
	
</details>

---

4. Explain about Remote repository.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Which refers to the repository hosted on intranet web server to be used by companies in their own premises. Used when Maven needs to download the dependencies.
- Remote repository work exactly same way as Maven’s central repository. Whenever an artifact is needed, it is downloaded to developer’s local repository and then it is used.
	
</blockquote> 

</details>

---

5. Explain about central repository.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
<blockquote> 

- It was used to downlaod the dependencies, When there is a need and which was not there in local repository.  
- It is the default location for Maven to download all the project dependency libraries.
	
</blockquote> 

</details>

---

6. How dependencies will be mentioned in pom.xml file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
```java

	<dependency>
	<groupId>com.baeldung</groupId>
	<artifactId>custom-project</artifactId>
	<version>1.3.2</version>
	<type>pom</type>
	<scope>import</scope>
	</dependency>
```

</details>

--- 

7. How can we change the location of Maven local repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
<blockquote> 

We can change the location of Maven local repository by changing the settings.xml file.

</details>

</blockquote> 

---

8. In which order does Maven searches for the dependencies?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
<blockquote> 

local repository  ->  central repository -> remote repository

</blockquote> 

</details>

---

9. What will happen if dependency is not found in all three repositories?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
<blockquote> 

- If the dependencies are not found, Maven stops processing and thrwos an error. 
	
</blockquote> 

</details>

---

10. How to install jar files in local repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
	
<blockquote> 

- Jar files will be installed in local repository by using the command <code> mvn install </code>.
- Manually also it can be installed by using the plugin `install-file-Dfile =<file path> `.

</blockquote> 

</details>

---
