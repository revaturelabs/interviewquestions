1. What is containerization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Containerization is a process of packaging an application code along with its required libraries, frameworks, and configuration files so that it can be run efficiently and seamlessly in any environment.

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

Docker is a very popular containerization platform which packages our application along with its dependencies in the form of containers so that our application can work seamlessly in any environment, be it development , test, or production.

</blockquote>
</details>

---

4. What is Docker Registry?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- It's a remote repository where docker images can be stored.
- Two types of registry are there: public e.g., Docker hub , private

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

No, we can pull the images from the Docker hub without login. But to push the images to Docker hub then login is needed.

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

- A Docker image is a read-only template that contains source code, libraries, dependencies, and a set of instructions for creating a container.
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
- On the other hand, Docker container has dependency on Docker image. Let's suppose we need to run Tomcat Docker container , for that we need to pull Tomcat Docker image without that image we cannot run the container.

</blockquote>
</details>

---

11. Consider a host server that has 2 GB space and your image size is 500 MB, then is it possible to run more than 4 containers of this image on the host?

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
- Command to check Docker version is `docker -v`.

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

15. If an **alpine-git** image needs to be pulled and **alpine** image is already installed then will Docker download a full or partial **alpine-git** image?

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
- Frequent cleanup of these images is very important to keep our disk space free.
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

24. 10+ containers are running on a host server. All these containers stop on server reboot or docker engine restart which requires a manual container start. Is there any way to auto restart the containers in this scenario?

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

27. A GitHub repo needs to be cloned, but the git utility is not installed in the system, although docker is running in the system and git image is also available, how can the repo be cloned?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can make use of available git image along with bind mount to mount host directory inside a container and run `git clone` command on container start to clone the data in mounted directory.

</blockquote>
</details>

---

28. Is there an alternate way to copy token/config file inside a container without using Docker command?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker shares resources from out host for running a container. So whatever changes are happening inside our Docker container are actually written somewhere on a host machine. So, we have to find that folder location and copy the content over there. Then it will automatically get visible in the Docker container.

</blockquote>
</details>

---

29. An app and a db container are running on the same host, how can these containers talk to each other?

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

35. Differentiate Virtualization and Containerization?

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

40. What is Docker compose?

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

42. What is the difference between a container and a virtual machine?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Containers and virtual machines (VMs) both provide isolation, but they work differently. A container shares the host operating system's kernel and resources, allowing for faster startup and more efficient resource utilization. In contrast, a VM runs a separate operating system on top of a hypervisor and requires more resources.

</blockquote>
</details>

---

43. What are the benefits of using Docker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker offers several benefits, including:

1. Portability: Docker containers can run on any system that supports Docker, making it easy to deploy applications across different environments.
2. Scalability: Docker enables horizontal scaling, allowing you to replicate containers to handle increased workloads.
3. Isolation: Containers provide process-level isolation, ensuring that applications and their dependencies are encapsulated and don't interfere with each other.
4. Reproducibility: Docker containers encapsulate the entire application stack, making it easier to reproduce the same environment across different machines.
5. Continuous Integration and Deployment (CI/CD): Docker simplifies the process of building, testing, and deploying applications, making it a popular choice for CI/CD pipelines.

</blockquote>
</details>

---

44. How do you install Docker?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker provides installation instructions for various operating systems on their website. You can visit https://www.docker.com/get-started to find the installation steps for your specific platform.

</blockquote>
</details>

---


45. How do you create a Docker image with Dockerfile?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker images are created using a Dockerfile, which is a plain text file that contains a set of instructions to build the image. You can use the `docker build` command with the appropriate options to build an image based on the Dockerfile.

</blockquote>
</details>

---

46. How do you run a Docker container?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can run a Docker container using the `docker run` command followed by the name or ID of the Docker image you want to run. You can also specify additional options, such as port mappings or environment variables, to customize the container's behavior.

</blockquote>
</details>

---

47. How can containers communicate with each other?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker provides networking capabilities that allow containers to communicate with each other. By default, containers can communicate with each other on the same Docker network using their container names as hostnames. You can also expose and publish ports to allow external access to specific containers.

</blockquote>
</details>

---

48. Can Docker be used for both development and production environments?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, Docker is commonly used in both development and production environments. It provides consistency between development, testing, and production by ensuring that the same containerized environment is used throughout the software lifecycle.

</blockquote>
</details>

---

49. What is a Dockerfile, and how does it work?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A Dockerfile is a text file that contains a set of instructions for building a Docker image. It provides a declarative syntax for specifying the image's base, dependencies, environment variables, volume mounts, network settings, and more. When you run the `docker build` command with a Dockerfile, Docker reads the file and executes the instructions step-by-step to create the image.

</blockquote>
</details>

---

50. What are the techniques used to optimize the size of Docker images?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To optimize the size of Docker images, you can consider the following techniques:

1. Use lightweight base images: Start your Docker image with a minimal and specialized base image rather than a general-purpose operating system.
2. Minimize layers: Combine multiple RUN instructions into a single instruction to reduce the number of layers in the image.
3. Remove unnecessary dependencies and files: Clean up temporary files, unused dependencies, and artifacts in the same layer where they were created.
4. Use .dockerignore: Create a .dockerignore file in your build context to exclude unnecessary files and directories from being added to the image.
5. Use multi-stage builds: Utilize multi-stage builds to build artifacts in one stage and copy only the necessary artifacts to the final image.

</blockquote>
</details>

---

51. What are the ways to scale Docker containers?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker provides several mechanisms to scale containers:

1. Manual scaling: You can manually start multiple instances of a container using the `docker run` command with appropriate options and different container names.
2. Docker Compose scaling: If you're using Docker Compose, you can define the desired number of container replicas for a service in the Compose file and use the `docker-compose up --scale <service-name>=<replica-count>` command to scale the service.
3. Orchestration platforms: Docker can integrate with container orchestration platforms like Docker Swarm or Kubernetes, which provide built-in mechanisms for scaling containers based on defined rules and policies.

</blockquote>
</details>

---

52. How can you manage persistent data with Docker?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker offers several options for managing persistent data:

1. Volumes: Docker volumes are the recommended way to manage persistent data. They can be attached to containers, allowing data to be stored and shared independently of the container's lifecycle. Volumes can be created manually or defined in a Docker Compose file.
2. Bind mounts: Bind mounts map a host file or directory to a container, allowing you to access and modify the host's filesystem from within the container. Bind mounts provide direct access to the host's file system and can be useful for development or when you need to share data between the host and the container.
3. Docker plugins: Docker plugins like Docker Volume Plugins (DVP) or third-party storage plugins allow you to integrate external storage systems with Docker to manage persistent data.

</blockquote>
</details>

---

53. How Docker Swarm differs from Kubernetes?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Docker Swarm is Docker's native clustering and orchestration solution for managing a cluster of Docker nodes. It provides features for service discovery, load balancing, scaling, and high availability. Docker Swarm is simpler to set up and has a smaller learning curve compared to Kubernetes, making it a good choice for smaller deployments or when you want to stick with the Docker ecosystem.

Kubernetes, on the other hand, is a popular and highly flexible container orchestration platform that can manage containers from various sources, not just Docker. It offers a more extensive set of features and is suitable for large-scale, complex deployments with advanced requirements.

</blockquote>
</details>

---