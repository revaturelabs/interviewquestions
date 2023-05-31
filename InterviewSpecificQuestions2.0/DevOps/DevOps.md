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

3. What is Continuous Integration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The process of regularly and consistently merging code into a central repository and reviewing new code to ensure that it integrates well within the previously established code base.

</blockquote> 

</details>

---

4. List the tools used for Continuous Integration?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- GitHub
- GitLab
- Jenkins
- Azure DevOps (formerly known as Visual Studio Team Services)
- Bamboo

</blockquote> 

</details>

---

5. What are the common steps involved in DevOps?

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

6. Explain Continuous Delivery?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Development principle which focuses on the automation of the DevOps pipeline to the extent that human intervention is not required. 
- Generally, source code control, building and testing, and deployment to staging are automated.
- While acceptance testing and if necessary, deployment to production environment may be handled by a Human or requires manual approval.

</blockquote> 

</details>

---

7. What is Continuous Deployment?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Continuous deployment automates releasing an application to production. 
- There is no manual gate at the stage of the pipeline before production (like Continuous Delivery).
- Any code commit that passes the automated testing phase is automatically released into the production.

</blockquote> 

</details>

---

8. What are the advantages of implementing DevOps in an organization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Implementing DevOps in an organization offers the following advantages:

1. DevOps enables faster delivery of software, reducing the time it takes to bring new features or products to market.
2. With DevOps, organizations can automate build, test, and deployment processes, ensuring a continuous flow of software releases and updates.
3. Improved collaboration and communication between teams.
4. Increased operational efficiency and resource optimization.
5. Enhanced software quality and early issue detection.
6. Agility and adaptability to changing needs.
7. Improved reliability and system stability.
8. Scalability and flexibility to accommodate growth.
9. Cost savings through optimized processes.
10. Cultivates a culture of innovation and experimentation.


</blockquote> 

</details>

---

9.  How does DevOps help in achieving faster and more frequent software releases?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- DevOps achieves faster and more frequent software releases through automation of tasks like build, testing, and deployment.
-  Continuous integration and deployment ensure incremental updates and quick feedback. Collaboration and communication enhance issue resolution. 
- Infrastructure as Code enables consistent and fast environment setup. 
- Agile practices break work into smaller cycles, facilitating frequent releases. 
- Continuous monitoring provides real-time feedback on performance and errors, enabling prompt resolution. 
- Together, these practices streamline the release process, allowing organizations to deliver updates quickly and frequently.

</blockquote> 

</details>

---

10. What is a DevOps pipeline? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A DevOps pipeline, also known as a CI/CD pipeline (Continuous Integration/Continuous Deployment pipeline), is an automated workflow that facilitates the development, testing, and deployment of software applications. It is a fundamental concept in DevOps that enables organizations to deliver software rapidly, consistently, and with high quality.

</blockquote> 

</details>

---

11. what is monitoring and logging in devops ?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- In DevOps, monitoring refers to the process of observing and measuring the performance, availability, and health of software applications and infrastructure. It involves collecting and analyzing data such as system metrics, application metrics, logs, and events in real-time to gain insights into the system's behavior and identify potential issues or bottlenecks.

- Logging, on the other hand, involves capturing and recording important events, messages, errors, and other relevant information generated by applications and systems. Logs serve as a record of activities and can be used for troubleshooting, debugging, and auditing purposes. They provide a detailed account of what happened within the system, allowing DevOps teams to understand the sequence of events and diagnose issues effectively.

</blockquote> 

</details>

---

12. Why is monitoring and logging important for DevOps?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Monitoring:

It is important to monitor our pipelines and various services for any downtime and other unexpected service disruptions that may happen

- Logging:

Logging is important because we can trace back and look through the log file to figure out where went wrong and at what time for better traceability

</blockquote> 

</details>

---

13. Explain CI/CD.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- CI/CD stands for Continuous Integration and Continuous Deployment. 
- It is a software development approach that involves automating the process of integrating code changes, running tests, and deploying applications.
-  Continuous Integration focuses on merging code changes frequently and automatically testing them to catch integration issues early. - Continuous Deployment focuses on automating the release and deployment of code changes to production environments, ensuring fast and frequent delivery of software updates. 
- Together, CI/CD enables teams to deliver software more rapidly, reliably, and with reduced manual effort.

</blockquote> 

</details>

---

