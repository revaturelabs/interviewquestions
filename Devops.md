1. What does CICD mean and stand for?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

CICD stands for Continuous Integration and Continuous Delivery (or Deployment).

- **Continuous Integration (CI):** It is a software development practice in which developers regularly integrate their code changes into a shared repository. With CI, developers can quickly identify and fix integration issues and ensure that the code is always in a stable state. CI tools automate the building and testing of code changes, which helps catch errors earlier in the development process.

- **Continuous Delivery (CD):** It is the process of automatically deploying code changes to production or staging environments after they have passed the necessary tests. CD ensures that the code is always ready for deployment and reduces the risk of introducing errors into the production environment. CD tools automate the deployment of code changes, which helps reduce the time and effort required to release new features and updates.

Together, CI and CD make up the CICD pipeline, which is a set of processes and tools that automate the building, testing, and deployment of software changes. CICD is a key part of modern software development practices and is critical for teams looking to release software quickly and reliably.

- Jenkis, Github Actions, GitLabs and Codebuild and CodeDeploy in AWS are few CI/CD tools.
  
</blockquote>

</details>

2. Do you know DevOps?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

DevOps as name implies is combining the development and operations processes. Traditionally the development and opertions teams are soiled but in DevOps the barriers are removed which will result in faster development cycles, more frequent releases and better collaboration between development, operations and sometimes even security and quality assurance teams. The DevOps process includes the developemnet, testing and deployment phases.

</blockquote>

</details>

3. What do you understand by CI/ CD pipe line?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

- The CI/CD stands for continious integration and continious deployment. The changes made to the codebase are merged to a centralised repository which trigges a build lifecycle which will build, test and deploy the application to production enviorment. 
- The CI/CD pipeleine can be built using github actions, gitlabs, jenkins, AWS code pipeline and AzureDevops.


</blockquote>

</details>
 


4. How much do you know/understand about the docker architecture?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

Docker architecture is a client server architecture, with Dokcer client and Docker daemon. Docker client can communicate with one or more deamons and Docker daemon is responsible for managing the dokcer objects like images, containers, networks and volumes.

</blockquote>

</details>
 


5. Where is the docker image stored when it is being built?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

When a docker image is being built, it is stored in the local Docker host machine's storage. During the building process, Docker creates a new image for every instruction in the docker file which run as isolated namespaces. and each new layer in the image is cached in local machine.
</blockquote>

</details>
 


6. Explain Jenkins

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

Jenkins is an opensource source automation server. It is use to automate the tasks like building, testing, and deploying the application.

</blockquote>

</details>

7. What are the services you used and how do they fit into the context of a CI/CD pipeline.

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

The CI/CD pipeline starts with a codebase repository like GitHub.For example

1. GitHub: Whenever there is commit or push in repostory the build process is triggered. 
2. Jenkins: Jenkins application has a job and the build will triggered with a webhook in GitHub. The Jenkinsfile in the repository contains the commands to build test, containerize and deploy the application.

The above process can also be achieved using other tools like GitHub actions, GitLabs CI/CD, AWS CodePipeline and AzureDevops CI/CD.

3. Docker: Docker is used to containerize or build an image of the project which can be run.

</blockquote>

</details>

8. Differences between Jenkins and CodePipeline?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

Jenkins and AWS CodePipeline are both popular CI/CD tools used to automate the software delivery process, but they have some differences:

**Jenkins:**

- Open-source and can be installed on-premises or in the cloud.
- Supports a wide range of plugins and integrations with other tools.
- Highly customizable and flexible in terms of workflow and pipeline design.
- Requires more manual configuration and maintenance.

**AWS CodePipeline:**

- Cloud-based service provided by Amazon Web Services (AWS).
- Built-in integration with other AWS services like CodeCommit, CodeBuild, and CodeDeploy.
- Scalable and reliable with high availability and fault tolerance.
- Provides a simplified and streamlined pipeline creation and management process.
- Less flexible compared to Jenkins in terms of customization and plugin support.

</blockquote>

</details>

9.  What do you prefer, Jenkins or aws?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

The choice between Jenkins and AWS CodePipeline would depend on the specific needs and requirements of the project. Jenkins is a popular open-source tool that offers a high level of customization and flexibility, while AWS CodePipeline is a fully managed service that is tightly integrated with other AWS services. Ultimately, the choice would depend on factors such as the complexity of the project, the need for customizability, and the available resources and expertise of the team.

</blockquote>

</details>

10.   How does this code pipeline trigger?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

A code pipeline can be triggered in different ways depending on how it's configured. Here are some common triggers:

1. **Code commit:** The pipeline is triggered when changes are pushed to a version control system like Git.

2. **Schedule:** The pipeline is triggered on a set schedule, such as daily or weekly.

3. **Manual:** The pipeline is triggered manually by a user, either through a web interface or a command-line tool.

4. **Webhooks:** The pipeline is triggered when a specific event occurs on a web service, such as a new release being deployed to a server.

5. **Continuous integration:** The pipeline is triggered automatically when a new build is ready to be tested.


</blockquote>

</details>

11.   What is Docker, and how does it compare to virtual machines?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

| Docker Container                                            | Virtual Machine                                                                                  |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| Lightweight                                                 | Heavyweight                                                                                      |
| Shares the host OS kernel                                   | Has its own OS kernel                                                                            |
| Runs on a single server and shares resources                | Runs as a separate server                                                                        |
| Starts up quickly                                           | Takes longer to start up                                                                         |
| More flexible and easier to manage                          | More complex and difficult to manage                                                             |
| More suitable for microservices architecture                | More suitable for monolithic applications                                                        |
| Requires less storage space                                 | Requires more storage space                                                                      |
| Provides better performance                                 | Provides lower performance                                                                       |
| Suitable for running multiple applications on a single host | Suitable for running single applications or multiple applications with different OS requirements |
| Supports horizontal scaling                                 | Supports vertical scaling                                                                        |

</blockquote>

</details>

12.  How have you set up a CI/CD pipe?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

**Steps to set up a CI/CD pipeline:**

1. **Choose a CI/CD tool:** Select a CI/CD tool that suits your project requirements. Some popular options include Jenkins, Travis CI, CircleCI, and GitLab CI/CD.

2. **Create a repository:** Create a repository for your project and connect it to your chosen CI/CD tool.

3. **Configure your pipeline:** Define the steps that your pipeline should execute, such as building the project, running tests, and deploying to a production environment. This configuration can be done either through a configuration file or via the CI/CD tool's web interface.

4. **Set up automated triggers:** Configure triggers to automatically start the pipeline whenever changes are pushed to the repository.

5. **Test the pipeline:** Run the pipeline manually to ensure that it runs successfully and performs the expected actions.

6. **Monitor and optimize the pipeline:** Keep an eye on your pipeline to identify any issues and optimize its performance. This could involve monitoring build times, identifying and resolving failed builds, and tweaking the pipeline configuration to improve efficiency.

7. **Continuously improve:** Continuously improve your pipeline by incorporating feedback and new ideas from your team and other stakeholders.


</blockquote>

</details>

13.  What are the steps to create a CI/CD pipeline in Jenkins?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

Creating a CI/CD pipeline in Jenkins typically involves several steps:

1. **Setup:** Install and configure Jenkins on a server or cloud platform of your choice.
2. **Code Repository:** Connect Jenkins to your code repository, such as GitHub or Bitbucket.
3. **Build:** Define a build process, which includes compiling the code, running tests, and packaging the code.
4. **Integration:** Connect Jenkins to other tools in your stack, such as JIRA for issue tracking or Slack for notifications.
5. **Deployment:** Define deployment scripts and configurations to deploy the code to production or staging environments.
6. **Automation:** Automate the pipeline to trigger a build when changes are made to the code repository and deploy the code when the build is successful.
7. **Monitoring:** Set up monitoring and logging tools to track performance and identify issues in real-time.


</blockquote>

</details>


