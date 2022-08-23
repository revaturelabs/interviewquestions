## Technical 
1.What is Maven?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- Maven is a tool used in Java to build a project and to handle dependency and documentation.
>- It is based on POM. (Project Object Model) : which is an XML file, contains information to project a configuration information to build the project.

</details>

---

2.List the uses of Maven.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- Maven is a building tool used for creating projects , build reports , integerating , deals with dependency and documentation.
>- It has made the life of develeoper easier, by making the process of building projects simple.
>- It increases the reusability.

</details>

---

3. Does maven need jdk to execute various goals?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>Yes

<details> <summary> <b> Explanation </b> </summary>

>- We need compatible version of jdk to execute Maven. jdk should be installed & JAVA_HOME environment variable should be set properly. 
>- We need Java to execute Maven. Java should be installed to set <code> JAVA_HOME environment varaiable </code> to point to a valid Java SDK(Like Java 8).

</details>

</details>

---
4. Which is the most fundamental unit of Maven system?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>POM (Project Object Model)- which is an XML file having the details of project  structure and contents termed as pom.xml file.

</details>

---

5. What does a build tool has to manage?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- Generate source code.
>- Create documentation from the source code generated.
>- Compiles the source code.
>- Packages the compiled code into JAR, WAR, EAR file.
>- Install the packaged code into Local, Remote repository.
 
</details>

---

6. What is the command used to create a simple project using Maven?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
 
 <blockquote>

 We can create a simple project in Maven using <code> archetype:generate </code> in command promt using Maven.
 Syntax to generate a project architecture.
  
 </blockquote>
  
<blockquote>
  
<code>

mvn archetype:generate -DgroupId=groupid -DartifactId=artifactid -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=booleanValue

</code>
  
</blockquote>

</details>

---

7. How to compile the Maven project?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

 >- To compile go to the project directory.(like: C:\Users\IT\SQUARECALCULATOR) and write the follwoing command `mvn clean compile` and When you check your project directory, target directory will be craeted.

</details>

---

8. How to run the Maven project?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

 >- To run the project, go to the project directory\target\classes.(like: C:\Users\IT\SQUARECALCULATOR\target\classes) and write the follwoing command `java com.javatpoint.App ` .

</details>

---

9.  Why do we use build tools or build automation?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- In small projects, developers will often manually invoke the build process. This is not practical for larger projects, where it is very hard to keep track of what needs to be built, in what sequence and what dependencies there are in the building process. Using an automation tool allows the build process to be more consistent.

 >Various build tools available(Naming only few):
   >- For java - Ant,Maven,Gradle.
   >- For .NET framework - NAnt
   >- C# - MsBuild
 
</details>

---


10. When a jar file will be craeted in the project?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- Jar file will be created inside the project/target directory, When you execute the command <code> mvn package </code> in the command prompt to package the Maven project.

</details>

---  

11. List some scenarios where the Maven should be used in the project.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- If the project needs to have quick documentation, compiling and packaging of source coide into JAR/ZIP files.
>- If the project requires a huge amount of dependencies.
>- If the version of dependecies requires a frequent up-gradation.

</details>

---

12. In which repository does the dependencies will be loaded?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

>- The dependencies will be loaded in  the Local repository.

</details>

---

13. Define Build tool.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
 
 <blockquote>

- Build tools are programs that automate the creation of executable applications from source code (e.g., .apk for an Android app, jar war for java apps). Building incorporates compiling,linking and packaging the code into a usable or executable form.
  
  
 </blockquote>
 
 <blockquote>
 
- Basically build automation is the act of scripting or automating a wide variety of tasks that software developers do in their day-to-day activities like:
  1. Downloading dependencies.
  2. Compiling source code into binary code.
  3. Packaging that binary code.
  4. Running tests.
  5. Deployment to production systems.

  
 </blockquote>
 
 </details>

---








