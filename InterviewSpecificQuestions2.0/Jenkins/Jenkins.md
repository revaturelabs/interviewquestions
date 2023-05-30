1. What is Jenkins?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins is a self-contained, open-source automation server, which can be used to automate the building, testing and deployment of software.

</blockquote> 

</details>

---

2. Why Jenkins pipeline is used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins Pipeline (or simply Pipeline with a capital P) is a suite of plugins that supports implementing and integrating continuous delivery pipelines into Jenkins. 
- This allows us to automate the process of getting software from version control to our users and customers.

</blockquote> 

</details>

---

3. What are two types of Jenkins Pipeline syntax?

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

4. What do you mean by environment variable in Jenkins?

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

5. What is the purpose of SonarLint?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- SonarLint is a free, open-source linting tool. 
- A linting tool/linter is a software tool which, when integrated with an IDE, can provide increased code quality feedback to the developer.
- SonarLint is an IDE extension that helps detect and fix quality issues as we write code. 
- For Eclipse, you can get it directly from the Eclipse Marketplace, and it will then detect new bugs and quality issues as we code (in Java, JavaScript, PHP, SQL, and Python).

</blockquote> 

</details>

---

6. What is the use of Sonar Cloud?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Sonar Cloud is a cloud-based code review solution which can be configured to review code within a cloud repository, such as GitHub.

</blockquote> 

</details>

---

7. What is Sonar Qube?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- SonarQube is a Code Quality Assurance tool built to work on a centralized server or integrated into a development pipeline that collects and analyzes source code and provides reports for the code quality of our project. 
- SonarQube is an open-source platform developed by SonarSource for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells on 29 programming languages and enables quality to be measured continually over time.

</blockquote> 

</details>

---

8. How is Jenkins installed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Jenkins is usually shipped as war file which can be run in servlet containers such as Apache Tomcat or GlassFish.
- Docker image of Jenkins is also available, which can be run in Docker as container.

</blockquote> 

</details>

---

9. What are the different types of Jenkins jobs?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The different types of Jenkins jobs are:

1. Freestyle Jobs: Freestyle jobs are the most flexible type of Jenkins job. They allow you to configure custom build steps, execute shell commands, trigger other jobs, and perform various actions based on your requirements.

2. Pipeline Jobs: Pipeline jobs, also known as Jenkins Pipeline, allow you to define your build process as a code script using the Jenkinsfile. The Jenkinsfile can be written in either the Declarative or Scripted syntax, and it provides powerful capabilities for defining complex build pipelines and managing the entire software delivery process.

3. Maven Jobs: Maven jobs are specifically designed for building Maven-based projects. They automatically configure the Maven environment and provide options to specify the Maven goals, profiles, and other parameters for building and testing the project.

4. Multibranch Pipeline Jobs: Multibranch pipeline jobs are used when you have multiple branches in your version control system (such as Git or SVN), and you want to create separate build pipelines for each branch. This allows you to build, test, and deploy each branch independently.

5. GitHub Organization Jobs: GitHub Organization jobs are used to automatically create Jenkins pipelines for multiple repositories within a GitHub organization. It scans the organization's repositories and creates separate pipeline jobs for each repository, enabling continuous integration and delivery for all projects in the organization.

6. Parameterized Jobs: Parameterized jobs allow you to define parameters that can be passed to the job at runtime. These parameters can be used to customize the build process or provide user inputs during job execution.


</blockquote> 

</details>

---

10. How do you create a Jenkins job?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To create a Jenkins job, you can follow these steps:

1. Log in to your Jenkins server and navigate to the Jenkins dashboard.

2. Click on "New Item" or "Create new jobs" to create a new Jenkins job.

3. Enter a name for your job and select the type of job you want to create (e.g., Freestyle project, Pipeline, Maven project, etc.).

4. Configure the job settings based on your requirements. This may include specifying the source code repository, build triggers, build steps, post-build actions, and other job-specific settings.

5. Save the job configuration.

6. Once the job is created, you can manually trigger the build by clicking on the "Build Now" or "Build" button. Alternatively, you can set up triggers such as polling the repository for changes or triggering the build based on specific events.

7. Monitor the build status and view the console output to track the progress and any errors or warnings during the build process.

8. Customize the job further by adding additional build steps, integrating with external tools or plugins, setting up parameters, or configuring build artifacts and notifications.

9. Save and update the job configuration as needed.


</blockquote> 

</details>

---

11. How do you schedule a Jenkins job to run at a specific time or interval?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To schedule a Jenkins job to run at a specific time or interval, you can use the built-in scheduling feature in Jenkins called "Build Triggers." Here's how you can do it:

1. Open the Jenkins job configuration page for the job you want to schedule.

2. Scroll down to the "Build Triggers" section.

3. Check the checkbox next to the trigger option that suits your scheduling needs. Some common options include:

   - **Build periodically**: This allows you to specify a cron-like schedule expression to run the job at specific times or intervals. For example, to run the job every day at 8:00 AM, you can use the expression `0 8 * * *`.

   - **Poll SCM**: This triggers the build when changes are detected in the source code repository. You can specify the polling interval to check for changes.

   - **Build after other projects are built**: This triggers the build when specific projects (defined by their names) have completed a build.

   - **GitHub hook trigger for GITScm polling**: This triggers the build when changes are pushed to the associated GitHub repository.

4. Configure the trigger settings based on your desired schedule or event.

5. Save the job configuration.

Once the job is configured with the appropriate trigger, Jenkins will automatically run the job according to the specified schedule or event.

</blockquote> 

</details>

---

12. How do you trigger a Jenkins job based on source code changes?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To trigger a Jenkins job based on source code changes, you can use the "Poll SCM" option in the job configuration. Here's how you can do it:

1. Open the Jenkins job configuration page for the job you want to trigger.

2. Scroll down to the "Build Triggers" section.

3. Check the checkbox for "Poll SCM."

4. Specify the polling schedule or interval in the "Schedule" field. For example, to check for changes every 5 minutes, you can use the expression `*/5 * * * *`.

5. Save the job configuration.



</blockquote> 

</details>

---

13. What is Jenkinsfile and how is it used?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The Jenkinsfile is a text file used to define the stages, steps, and flow of a CI/CD process in Jenkins. 
- It is stored alongside the project's source code and versioned with it. 
- The Jenkinsfile can be written in Declarative or Scripted Pipeline syntax and specifies the pipeline's stages, such as build, test, deploy, and custom stages, with their respective steps. Using a Jenkinsfile allows for version control, easy sharing, and repeatability of the CI/CD process. 
- It offers flexibility to define complex pipelines, including conditional logic and parallel execution.
-  Jenkins reads the Jenkinsfile during pipeline execution, following the defined stages and steps to build, test, and deploy the application.


</blockquote> 

</details>

---

14. How do you secure Jenkins and manage user access?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To secure Jenkins and manage user access, you can follow these steps:

1. Enable security: In the Jenkins global configuration, enable security to enforce authentication and authorization.

2. User creation: Create user accounts for each individual who needs access to Jenkins. Assign appropriate roles and permissions to each user.

3. Plugin installation: Install and configure relevant security plugins, such as the Role-based Authorization Strategy plugin, to enhance user access management.

4. Role-based access control: Define roles that represent different job functions or responsibilities within Jenkins. Assign permissions and access levels to each role.

5. Access control matrix: Configure the access control matrix to specify which users or groups have permissions for various Jenkins operations, such as job creation, configuration, and execution.

6. Securing sensitive information: Store sensitive information, such as API tokens or passwords, securely using credentials plugins or environment variables.

7. Single sign-on (SSO): Integrate Jenkins with existing authentication systems, such as LDAP or Active Directory, to enable single sign-on and streamline user management.

8. Audit trail: Enable auditing and logging to track user activities and monitor any unauthorized access attempts.


</blockquote> 

</details>

---

15. What is the role of Jenkins in continuous integration and continuous delivery (CI/CD)?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The role of Jenkins in continuous integration and continuous delivery (CI/CD) is to automate and streamline the software development and release processes.
- Jenkins acts as a central hub that facilitates the continuous integration of code changes, automated testing, and the deployment of applications. 
- It enables developers to merge their code changes into a shared repository, triggering the CI/CD pipeline.

</blockquote> 

</details>

---

16. What are Jenkins plugins and how do you install and use them?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Jenkins plugins are extensions that provide additional functionality to the Jenkins CI/CD platform. They allow users to enhance and customize Jenkins according to their specific requirements. 

To install a Jenkins plugin, you can follow these steps:

1. Access the Jenkins web interface and navigate to the "Manage Jenkins" section.
2. Select the "Manage Plugins" option, which will open the "Plugin Manager" page.
3. In the "Available" tab, you can browse the list of plugins available in the Jenkins plugin repository.
4. Search for the desired plugin using the search box or browse through different categories.
5. Once you find the plugin, select the checkbox next to its name.
6. Click the "Install without restart" button to install the plugin immediately. Alternatively, you can select the "Download now and install after restart" option if you want to install it during the next Jenkins restart.
7. Jenkins will download and install the selected plugin.


</blockquote> 

</details>

---

17. How do you automate the deployment of Jenkins itself?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To automate the deployment of Jenkins itself, you can follow these general steps:

1. Set up an infrastructure provisioning tool: Use a tool like Ansible, Chef, or Terraform to automate the provisioning of the infrastructure where Jenkins will be deployed. This can include creating virtual machines, configuring networking, and installing the necessary dependencies.

2. Define the Jenkins configuration: Prepare a configuration file or script that defines the desired configuration of Jenkins, including plugins, security settings, system preferences, and other customizations. This configuration file can be in the form of a Jenkinsfile or a configuration management tool script.

3. Use configuration management tooling: Utilize a configuration management tool like Ansible, Chef, or Puppet to automate the installation and configuration of Jenkins on the provisioned infrastructure. The tool will execute the necessary commands to install Jenkins, apply the desired configuration, and ensure that Jenkins is running with the correct settings.

4. Implement version control for Jenkins configuration: Store the Jenkins configuration file or scripts in a version control system like Git. This allows you to track changes, collaborate with others, and easily roll back or revert to previous configurations if needed.

5. Set up continuous integration for Jenkins configuration: Implement a CI pipeline for the Jenkins configuration files themselves. This ensures that any changes to the configuration are automatically tested and validated before deployment. This can include running automated tests, syntax checks, and static code analysis on the configuration files.


</blockquote> 

</details>

---


18. What is the difference between a Jenkins Job and a Jenkins Pipeline?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A Jenkins job and a Jenkins pipeline are two different ways to define and manage automation in Jenkins:

1. **Jenkins Job:** A Jenkins job, also known as a freestyle job or a traditional job, is the basic unit of work in Jenkins. It allows you to define a series of build steps, such as compiling code, running tests, and deploying artifacts. A Jenkins job is typically configured using the Jenkins web interface and can be triggered manually or by various events, such as source code changes or a time-based schedule. Jenkins jobs are suitable for simple, linear workflows without complex dependencies or conditional logic.

2. **Jenkins Pipeline:** A Jenkins pipeline, also known as a Jenkinsfile pipeline or a scripted/declarative pipeline, is a more advanced and flexible way to define continuous integration and continuous delivery (CI/CD) processes in Jenkins. It allows you to define your entire build/test/deploy pipeline as code, using a domain-specific language (DSL). With a Jenkins pipeline, you can define complex workflows, including parallel execution, conditional logic, and integration with external tools. The pipeline is defined in a Jenkinsfile, which can be stored alongside the source code in a version control system. Jenkins pipelines provide better visibility, maintainability, and reusability compared to traditional Jenkins jobs.


</blockquote> 

</details>

---

19. How can we setup alerts in the Jenkins pipeline to alert us of the state of the pipeline?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- **Email notifications:** Jenkins has built-in support for email notifications. You can configure Jenkins to send email notifications when a build fails, succeeds, or when other specific conditions are met. You can specify the recipients, email content, and triggers for sending the email notifications.

</blockquote> 

</details>

---

20. How do you integrate Jenkins with version control systems like Git?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

To integrate Jenkins with version control systems like Git, you can use plugins and configure the Jenkins job to interact with the Git repository. Here's a general outline of the steps:

1. Install the Git Plugin: Install the "Git Plugin" in Jenkins from the Plugin Manager. This plugin provides the necessary functionality to interact with Git repositories.

2. Configure Git repository credentials: In the Jenkins job configuration, specify the Git repository URL and provide the appropriate credentials (username/password or SSH key) to access the repository.

3. Set up the branch to build: Specify the branch or branches you want Jenkins to monitor for changes. You can configure Jenkins to build automatically whenever changes are pushed to a specific branch or branches.

4. Define build triggers: Configure the build triggers based on your requirements. You can set up Jenkins to poll the Git repository at regular intervals to check for changes or configure it to trigger a build whenever a specific event occurs, such as a commit or a pull request.

5. Define build steps: Configure the build steps in your Jenkins job, such as compiling code, running tests, and deploying artifacts. You can use build tools like Maven, Gradle, or custom shell scripts to perform these tasks.

6. Set up post-build actions: Configure post-build actions, such as archiving artifacts, sending notifications, or triggering downstream jobs. You can specify actions to be performed after the build is completed, based on the build status or other criteria.


</blockquote> 

</details>

---
