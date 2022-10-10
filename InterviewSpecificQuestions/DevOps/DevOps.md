## Technical

1. What is `DevOps`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Software Development (Dev) Operations (Ops) are a set of practices and methodologies designed to combine the development (production/writing of code), deployment and maintenance of code into a streamlined process. 

</blockquote> 

</details>

---

2. What is goal of `DevOps`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The primary goal of DevOps is to expedite the lifecycle of application development, particularly through the automation of tasks.

</blockquote> 

</details>

---

3. What do you understand by Continuous Integration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The process of regularly and consistently merging code into a central repository and reviewing new code to ensure that it integrates well within the previously established code base.

</blockquote> 

</details>

---

4. What tools are used for Continuous Integration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- GitHub
- GitLab

</blockquote> 

</details>

---

5. What are the common steps in DevOps?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The steps or phases for DevOps refers to the creation, testing, and deployment of an application.
    - Source code Control: Producing (writing) code and pushing to a repository
    - Building and Testing Automation: Test basic functionality of code (Generally unit testing) and create a new, working build
    - Deploying to Staging: Deployment of working build to a temporary environment
    - Acceptance Testing: Undergo other more complex tests (systems, integration) within temporary environment
    - Deployment of Build: Migrate working build to Production environment accessible by end users

</blockquote> 

</details>

---

6. What do you understand by Continuous Delivery?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Development principle which focuses on the automation of the DevOps pipeline to the extent that human intervention is not required. 
- Generally, source code control, building and testing, and deployment to staging are automated.
- While acceptance testing and if necessary deployment to production environment may be handled by a Human or requires manual approval.

</blockquote> 

</details>

---

7. What do you understand by Continuous Deployment?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Continuous deployment automates releasing an application to production. 
- There is no manual gate at the stage of the pipeline before production (like Continuous Delivery).
- Any code commit that passes the automated testing phase is automatically released into the production.

</blockquote> 

</details>

---

8. State True or False. 

Due to Continuous Integration code can be tested easily by creating separate, test or development branches based on the mainline code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- True

</blockquote> 

</details>

---

9. State True or False. 

Continuous Integration establishes the foundation for an automated DevOps pipeline & ensures the entire team works on the most up to date code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- True

</blockquote> 

</details>

---

10. What is Jenkins?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins is a self-contained, open-source automation server, which can be used to automate the building, testing and deployment of software.

</blockquote> 

</details>

---

11. Why Jenkins pipeline is used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins Pipeline (or simply Pipeline with a capital P) is a suite of plugins that supports implementing and integrating continuous delivery pipelines into Jenkins. 
- This allows us to automate the process of getting software from version control to our users and customers.

</blockquote> 

</details>

---

12. What are two types of Jenkins Pipeline syntax?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A Jenkinsfile can be written using two types of syntax - Declarative and Scripted. 
- Declarative and Scripted Pipelines are constructed fundamentally differently. 
- Declarative Pipeline is a more recent feature of Jenkins Pipeline which:
    - provides richer syntactical features over Scripted Pipeline syntax, and
    - is designed to make writing and reading Pipeline code easier.

</blockquote> 

</details>

---

13. What do you mean by environment variable in Jenkins?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins Pipeline exposes environment variables via the global variable `env`, which is available from anywhere within a `Jenkinsfile`. 
- Few variables listed below-
  - `BUILD_NUMBER`: The current build number, such as "153".
  - `JOB_NAME`: Name of the project of this build, such as "foo" or "foo/bar".
  - `WORKSPACE`: The absolute path of the workspace.

</blockquote> 

</details>

---

14. What is the purpose of SonarLint?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- SonarLint is a free, open-source linting tool. 
- A linting tool/linter is a software tool which, when integrated with an IDE, can provide increased code quality feedback to the developer.
- SonarLint is an IDE extension that helps detect and fix quality issues as we write code. 
- For Eclipse, you can get it directly from the Eclipse Marketplace, and it will then detect new bugs and quality issues as we code (in Java, JavaScript, PHP, SQL and Python).

</blockquote> 

</details>

---

15. What is the use of Sonar Cloud?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Sonar Cloud is a cloud-based code review solution which can be configured to review code within a cloud repository, such as GitHub.

</blockquote> 

</details>

---

16. What is Sonar Qube?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- SonarQube is a Code Quality Assurance tool built to work on a centralized server or integrated into a development pipeline that collects and analyzes source code and provides reports for the code quality of our project. 
- SonarQube is an open-source platform developed by SonarSource for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells on 29 programming languages and enables quality to be measured continually over time.

</blockquote> 

</details>

---

17. How is Jenkins installed?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins is usually shipped as war file which can be run in servlet containers such as Apache Tomcat or GlassFish.
- Docker image of Jenkins is also available, which can be run in Docker as container.

</blockquote> 

</details>

---

