1. What is containerization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Containerization is a process of packaging an application code along with its required libraries, frameworks and configuration files so that it can be run efficiently and seamlessly in any environment.

</blockquote>
</details>

---

2. What are the advantages of containerization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Quick software development
- Easy software delivery

</blockquote>
</details>

---

3. What is Docker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker is a very popular containerization platform which packages our application along with its dependencies in the form of containers so that our application can work seamlessly in any environment, be it development , test or production.

</blockquote>
</details>

---

4. Can u tell me about Docker Registry?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

-It's a remote repository where docker images can be stored.
-Two types of registry are there: public e.g.,Docker hub , private

</blockquote>
</details>

---

5. How to access public registry?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using the command `docker login`.
- We need to use Docker login to access public registry. Before that we need to create an account at **http://hub.docker.com** so that we will get username and password. we can use that to access .

</blockquote>
</details>

---

6. Do you need to login to public registry to pull the images?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

No,we can pull the images from the Docker hub without login. But to push the images to Docker hub then login is needed.

</blockquote>
</details>

---

7. How to access private registry?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using the command `docker login <Private Registry URL>`.

</blockquote>
</details>

---

8. What is Docker image?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A Docker image is a read-only template that contains source code, libraries, dependencies and a set of instructions for creating a container.
- Also Docker image is an immutable.


</blockquote>
</details>

---

9. What is Docker Container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Container is a running instance of the image.
- Every time we start a new container an extra writeable layer is created for it.

</blockquote>
</details>

---

10. Is there any dependency between Docker image and container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Docker image has no dependency on Docker container. Because we can install Docker image and it is okay if we do not run a container from it.
- On the other hand, Docker container has depency on Docker image. Let's suppose we need to run Tomcat Docker container , for that we need to pull Tomcat Docker image without that image we cannot run the container.

</blockquote>
</details>

---

11. Suppose host server has 2 GB space and your image size is 500 MB, then is it possible to run more than 4 containers of this image on the host?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, we can create multiple containers from the same image. As the image is made up of Read-only layers , none of the container can modify it. But each container has got the writable layer, where container specific changes can be stored.

</blockquote>
</details>

---

12. In which language Docker is written and how to check Docker version?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Docker is written in Golang.
-Command to check Docker version is `docker -v`.

</blockquote>
</details>

---

13. What are the different ways to create Docker images?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are two ways to create Docker images

   - Manually from running Docker container.
   - Automatically by writing instructions in Docker file.

</Blockquote>
</details>

---

14. How to search and pull any Docker image in local system ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In two ways we can do it.

  - Go to `https://hub.docker.com/` in our web browser and search.
  - Use `docker search<ImageName>` in our linux server.

</blockquote>
</details>

---

15. Suppose i want to pull a **alpine-git** image and **alpine** image is already installed then will Docker download a full or partial **alpine-git** image?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker will not download any already available layer of **alpine-git**.

</blockquote>
</details>

---

16. How to check details about each layer in a Docker image like size, task done, timestamp?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The command to get the required details about each layer is `docker history <ImageName/Id>`.

</blockquotes>
</details>

---

17. How to remove dangling images and why is it useful ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Dangling images are those unused images which are not associated with any of the container.
- Frequent clean up of these images is very important to keep our disk space free.
- command to remove the dangling image is `docker image prune -a`.

</blockquote>
</details>

---

18. How to run a container in interactive and daemon mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The command is `docker run -itd --name test<ImageName>`.
  - -it for interactive mode.
  - -d for daemon mode.

</blockquote>
</details>

---

19. How to check the details about a container ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The command is `docker inspect <ContainerName/Id>`.

</blockquote>
</details>

---

20. Is it possible to create container's writable layer without running a docker container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes, using docker create command.
- For e.g., **docker create -it --name test1 image**


</blockquote>
</details>

---

21. How to find size of any container's writable layer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

-Using the command is `docker ps -as`.

</blockquote>
</details>

---

22. How to check logs of a container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

-Using the command `docker logs<ContainerName/Id>`.

</blockquote>
</details>

---

23. Are the container logs stored inside a container or in a host server? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Container logs are stored in host server. 

</blockquote>
</details>

---

24. 10+ containers are running on my host server. All these containers stop on server reboot or docker engine restart which requires a manually container start. Is there any way to auto restart the containers in this scenario?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

One should enable auto restart policy to handle above scenario. Restart supports the policies like 
   - on-failure.
   - always.
   - unless-stopped. 

</blockquote>
</details>

---

25. Developers create multiple test containers in dev server in a day which consumes lot of disk space and manual cleanup is required. Is there any way to automate this cleanup?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

we should use -rm flag while starting a container to auto remove the container on its exit.

</blockquote>
</details>

---

26. Is it possible to use restart policy and -rm flag together when starting a container?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

No, restart and rm cannot be used together. restart will try to start the container as soon as it stops and rm will try to remove the container as soon as it stops. 

</blockquote>
</details>

---

27. I want to clone a github repo but i don't have git utility installed in my system, although docker is running in my system and git image is also available. So considering the scenario, how can i clone the repo now?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can make use of available git image along with bind mount to mount host directory inside a container and run `git clone` command on container start to clone the data in mounted directory.

</blockquote>
</details>

---

28. I have a requirement to copy token/config file inside a container but can't use Docker command for that. Is there any alternate way to achieve it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker shares resources from out host for running a container.So whatever changes are happening inside our Docker container are actually written somewhere on a host machine.So we have to find that folder location and copy the content over there.Then it will automatically gets visible in the Docker container.

</blockquote>
</details>

---

29. I have an app and a db container running on a same host? How can these two containers talk to each other?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using link flag in case of default bridge.
- user defined bridge.

</blockquote>
</details>

---

30. What are the most common instructions you used while writing a dockerfile?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- FROM
- ARG
- LABEL
- ENV
- WORKDIR
- RUN
- COPY
- ADD
- Expose
- CMD and ENTRYPOINT

</blockquote>
</details>

---

31. Differentiate between COPY and ADD commands that are used in a DockerFile?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**COPY** provides just the basic support of copying local files into the container whereas **ADD** provides additional features like remote URL and tar extraction support.

</blockquote>
</details>

---

32. What is the benefit of using a Docker over a Hypervisor?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A hypervisor is required to host and maintain virtual machines; a system administrator needs to maintain the hypervisor itself. However, the Docker engine is a lightweight container virtualization technology that runs on the host operating system, and Docker containers can be started very quickly.

</blockquote>
</details>

---

33. Is it necessary to monitor a Docker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, active monitoring ensures higher productivity and better outcomes. Docker monitoring also notifies about any default in the system.

</blockquote>
</details>

---

34. Name the three main Docker components?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Docker Client**. Performs Docker build pull and run operations to open up communication with the Docker Host. The Docker command then employs Docker API to call any queries to run.
**Docker Host**. Contains Docker daemon, containers, and associated images. The Docker daemon establishes a connection with the Registry. The stored images are the type of metadata dedicated to containerized applications.
**Registry**.  Docker images are stored here. There are two of them, a public registry and a private one. Docker Hub and Docker Cloud are two public registries available for use by anyone.

</blockquote>
</details>

---

35. Differentiate Virtalization and Containerization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Virtualization is an abstract version of a physical machine, while containerization is the abstract version of an application.

</blockquote>
</details>

---

36. What is Docker hub?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker Hub is a service provided by Docker for finding and sharing container images with your team. It provides two repositories: Push and pull container images.

</blockquote>
</details>

---

37. How Docker client and Docker daemon communicate with each other?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker client and Docker Daemon communication happen with the combination of Rest API, socket.IO, and TCP.

</blockquote>
</details>

---

38. What are Docker Namespaces?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Docker uses a technology called namespaces to provide the isolated workspace called the container. When we run a container, Docker creates a set of namespaces for that container.
- These namespaces provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

</blockquote>
</details>

---

39.  What is Docker Swarm?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

 A Docker Swarm is a group of either physical or virtual machines that are running the Docker application and that have been configured to join together in a cluster. Once a group of machines have been clustered together, we can still run the Docker commands that we're used to, but they will now be carried out by the machines in our cluster. The activities of the cluster are controlled by a swarm manager, and machines that have joined the cluster are referred to as nodes.

</blockquote>
</details>

---

40. Can u tell me something about Docker compose?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker Compose is a tool that was developed to help define and share multi-container applications. With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down.

</blockquote>
</details>

---

41. How to start, stop and kill a container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To start the following command is used:
`$ docker start <container_id>`.
The command used for stopping a running container:
`$ docker stop <container_id>`.
The command to kill a container:
`$ docker kill <container_id>`.

</blockquote>
</details>

---


