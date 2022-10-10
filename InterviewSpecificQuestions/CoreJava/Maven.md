1. What is Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Maven is an automation and management tool developed by Apache Software Foundation.
- It allows us to create projects, dependency, and documentation using Project Object Model and plugins. 
- It can also build any number of projects into desired output such as jar, war, metadata.

</blockquote>
</details>

---

2. Do you know in which language Maven was written?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Maven is a build automation tool used primarily for Java projects. 
- Maven can also be used to build and manage projects written in C#, Ruby, Scala, and other languages.

</blockquote>
</details>

---

3. How do you think Maven helps the developer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- It actually helps the developer to create the Java project in a easy way.
-  Accessibility of new feature created or added in Maven can be easily added to a project in Maven configuration that will increases the performance of project and building process.
- Apart from all these the main feature of Maven is that it can download the project dependency libraries automatically.

</blockquote>
</details>

---

4. Can you list out the processes which can be managed using Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Builds, Documentation, Reporting, Dependencies, SCMs, Releases, Distribution, mailing list

</blockquote>
</details>

---

5. Can u explain a bit about how to use Maven?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- To configure the Maven in Java, you need to use Project Object Model, which is stored in a pom.xml-file.
- POM includes all the configuration setting related to Maven. Plugins can be configured and edit in the  `<plugins>` tag of a pom.xml file and developer can use any plugin without much detail of each plugin.
- When user start working on Maven Project, it provides default setting of configuration, so the user does not need to add every configuration in pom.xml.

</blockquote>
</details>

---

6. What is your understanding about the saying Maven uses Convention over Configuration?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Maven uses Convention over Configuration which means developers are not required to create build process themselves. and they dont have to mention each and every configuration details.

</blockquote>
</details>

---

7. What is Maven Build Lifecycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A Build lifecycle is a well-defined sequence of phases that outline the order in which the goals are to be executed. Here phase represents a stage in the life cycle.

</blockquote>
</details>

---

8. Can you tell me the build lifecycle of Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The three build lifecycles are:
 - Clean: cleans up artifacts created by previous builds.
 - Default (or build): this can be accustomed to build the appliance.
 - Site: generates site documentation for the project.

 </blockquote>
 </details>

 ---

9. Could you tell me a little bit about the Maven artifact? 


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- An artifact is a file, usually a JAR that gets deployed to a Maven repository. A Maven build produces one or more artifacts, such as a compiled JAR and a `sources` JAR.
- Each artifact has a group ID, an artifact ID , and a version string. The three together uniquely identify the artifact. A project's dependencies are specified as artifacts.

</blockquote>
</details>

---

10. What are the phases of a Maven build lifecycle?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- validate :  the project is correct and all necessary information is available.
- compile :  compile the source code of the project.
- test : test the compiled source code with a suitable unit testing framework. These tests should not require the code be packaged or deployed.
- package : take the compiled code and package it in its distributable format, such as a JAR.
- integration-test : process and deploy the package if necessary into an environment where integration tests can be run.
- verify :  run any checks to verify whether the package is valid and meets quality criteria.
- install : install the package into the local repository, for use as a dependency in other projects locally.
- deploy : done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.

</blockquote>
</details>

---

11.  What phases does a clean lifecycle consist of?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The clean lifecycle consists of the following phases:
  - pre-clean.
  - clean.
  - post-clean.

</blockquote>
</details>

---

12. What phases does a site lifecycle consist of?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The phases in site lifecycle are:
  - pre-site
  - site
  - post-site
  - site-deploy

</blockquote>
</details>

---

13. What are the two setting files called in Maven called and what are their locations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Maven, the setting files are called settings.xml, and the two setting files are located at:
- Maven installation directory: $M2_Home/conf/settings.xml
- User’s home directory: ${ user.home }/ .m2 / settings.xml

</blockquote>
</details>

---

14. Can you tell what the "jar: jar" goal would do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`jar: jar` will not recompile sources; it will imply just create a JAR from the target/classes directory considering that everything else has been done.

</blockquote>
</details>

---

15. Can you list out what the Maven’s order of inheritance is?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The maven’s order of inheritance is
  - Parent Pom
  - Project Pom
  - Settings
  - CLI parameters

</blockquote>
</details>

---

16. Do you know how to run test classes in Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To run test classes in Maven, we need surefire plugin and we need to check and configure our settings in setting.xml and pom.xml for a property named `test.`

</blockquote>
</details>

---

17.  How to install Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Make sure JDK is installed, and `JAVA_HOME`  the variable is added as a Windows environment variable.
Add both `M2_HOME` and `MAVEN_HOME` variable in the Windows environment, and point it to your Maven folder.

</blockquote>
</details>

---

18. What are the archetype goals?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Four goals associated with archetype plugin:
   - Create : creates using a quick-start template.
   - Generate : provide a menu of templates.
   - Create-from-project : creates an archetype from an existing project.
   - Crawl : searches the repository for archetype and updates catalog.

</blockquote>
</details>

---

19. Do you know about Parent POM's?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Basically, these are parent projects without code used by companies to define the set of libraries/versions, plugins they want their teams using.It can have dependencies, build plugins, variables definitions, and even their own parent POM, forming a chain.
- A great example is Spring Boot. You can extract it to create production-grade web services crazily fast. 

</blockquote>
</details>

---

20. What is a system dependency?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Dependency with reach system is always accessible and is not looked up in the repository. They are regularly used to tell Maven about dependencies that are provided by the JDK. So, system dependencies are mainly useful for resolving dependencies on artefacts that JDK usually provides.

</blockquote>
</details>

---

21. How does Maven looks for a dependency or resource ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It refers to the settings.xml to look for the repositories to look for the resource. It first looks into the configured local repository, then it looks into the configured remote repositories. If the resource is still not found , it looks it within maven repository central i.e repo1.maven.org. If its still not found, it throws the exception saying `Unable to find resource in repository central`.

</blockquote>
</details>

22. How can we look into the Dependencies for the project and where they are defined ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Using mvn dependency:tree

</blockquote>
</details>

---

23. What are the different types of Maven Repositories?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are three types of Maven repositories:

1. Local Repository: 
    - Local repository refers to the machine of the developer where all the project material is saved.The local repository contains all the dependency jars.
2. Remote Repository:
    - The remote repository refers to the repository present on a server usually in company intranet to download dependencies.
    - The advantage of remote repository is that it can have all publically available depdendencies as well as private dependencies used only in intranet by employees of the enterprise.
3. Central Repository:
    - Central repository refers to the Maven community that comes into action when there is a need for dependencies, and those dependencies cannot be found in the local repository.
    - Maven downloads the dependencies from here in the local repository whenever needed.

</blockquote>
</details>

---

24. What are the types of Maven Plugins?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are two types of Maven Plugins:

- **Build plugins** : These plugins are executed during the build and are configured in the `<build/>` element of pom.xml
- **Reporting plugins** : These plugins are executed during the stage generation and are configured in the `<reporting/>` element of the pom.xml.

</blockquote>
</details>

---

25. What is meant by the term **Dependencies and Repositories** in Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Dependencies refer to the Java libraries that are needed for the project. Repositories refer to the directories of packaged JAR files.
If the dependencies are not present in your local repository; then Maven downloads them from a central repository and stores them in the local repository.

</blockquote>
</details>

---

26. Why do we need **Optional dependecies**?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Optional dependencies are used to decrease the transitive burden of some libraries.
- These dependencies are used when it is not feasible to divide a project into sub-modules.
- Some dependencies are only used for a specific feature in the project, and if that feature is not there, then that dependency will not be used.

</blockquote>
</details>

---

27. Do you know where the Maven dependencies got stored?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- All the JARS, dependency files, etc. that are downloaded by Maven are saved in the Maven local repository.
- The Maven local repository is a folder location on the local system where all the artifacts are locally stored.

</blockquote>
</details>

---

28. How will you install JAR files in the Local Repository? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`mvn install` is used to install JAR files in the local repository.
To install the JAR manually into the local Maven repository, the following plugin is used: `mvn install:install-file-Dfile=<path to file>.`

</blockquote>
</details>

---

29. How will you create a new project based on an archetype?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Creating a project from an archetype consists of four steps:
- Refer to the repository.
- selecting an archetype.
- the configuration of that archetype.
- the project’s efficient creation based on the data collected.

</blockquote>
</details>

---

30. Can u explain a bit about **Snapshot** in Maven?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Snapshot refers to the version available in the Maven remote repository. It signals the latest development copy. Maven inspects for a new version of Snapshot in the remote repository, for every new build.The snapshot is updated by the data service team with an updated source code every time to the repository for each Maven build.

</blockquote>
</details>

---