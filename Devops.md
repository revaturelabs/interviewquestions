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

**Jenkins:** Jenkins is an open-source 

**AWS:**

</blockquote>

</details>

9.  What do you prefer, Jenkins or aws?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

</blockquote>

</details>

10.   How does this code pipeline trigger?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

</blockquote>

</details>

11.  What is Docker, and how does it compare to virtual machines

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

</blockquote>

</details>

12.  How have you set up a CI/CD pipe?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

</blockquote>

</details>

13. What are the steps to create a CI/CD pipeline in Jenkins?

<details> <summary><b>Show Answer</b></summary>
 
<blockquote>

</blockquote>

</details>


