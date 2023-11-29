---
title: "Day 18: Docker for DevOps Engineers (part 1)"
seoTitle: "Day 18: Docker for DevOps Engineers"
seoDescription: "In the world of software magic, Docker Compose is like a wizard that makes managing multiple containers feel like a breeze. Imagine having a ....."
datePublished: Sat Nov 25 2023 09:50:12 GMT+0000 (Coordinated Universal Time)
cuid: clpdvekdr000009js28iah646
slug: day-18-docker-for-devops-engineers-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700905621042/2c165f62-391b-4ed9-b5cd-89086f882443.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700905749108/0a93e3c2-717e-4075-8d3a-9b5988a680f6.png
tags: linux, docker, devops, linux-for-beginners, devops-articles, 90daysofdevops, trainwithshubham

---

In the world of software magic, Docker Compose is like a wizard that makes managing multiple containers feel like a breeze. Imagine having a recipe (docker-compose.yml) that tells your computer how to run not just one, but a whole team of software services together. This blog post is your guide into this world, where we'll chat about containers (those lightweight, standalone packages of magic), the harmony of multi-container applications, and the secret language called YAML that helps us talk to Docker Compose. We'll sprinkle in some handy commands to make your apps dance to your tune. Get ready for a hands-on journey where we'll pull and run Docker images, and by the end, you'll be orchestrating your software like a tech wizard! 🚀

### What is Docker Compose?

![Everything You Need to Know about Docker Compose](https://cdn.hashnode.com/res/hashnode/image/upload/v1662313547352/s0Uk-haLQ.jpg?w=1600&h=840&fit=crop&crop=entropy&auto=compress,format&format=webp align="left")

Docker Compose is a tool that helps you manage and run multi-container Docker applications. Let me break down the key concepts in simple language:

1. **Docker Containers:**
    
    * Think of a container as a lightweight, standalone, and executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and dependencies.
        
2. **Multi-Container Applications:**
    
    * Many applications are made up of multiple services or components (like a web server, a database, and so on), each running in its own container. Docker Compose helps you manage these multiple containers as a single application.
        
3. **Docker Compose File:**
    
    * Docker Compose uses a simple text file called a "docker-compose.yml" file to define how your multi-container application should behave. It's like a recipe for your application.
        
4. **Services:**
    
    * Each container in your application is defined as a service in the Docker Compose file. A service is essentially a container with its configuration.
        
5. **Configuration:**
    
    * You can specify various settings for each service in the Docker Compose file, such as which image to use, which ports to expose, and how containers should communicate with each other.
        
6. **Easy Management:**
    
    * With a single command, you can start, stop, and manage all the containers defined in your Docker Compose file. This makes it easy to deploy and scale your application.
        
7. **Isolation and Portability:**
    
    * Docker Compose helps maintain isolation between services, meaning changes to one service don't affect others. It also makes your application more portable, allowing you to run it on different environments without worrying about dependencies.
        
8. **Example:**
    
    * For instance, if you have a web application that uses both a web server and a database, you can use Docker Compose to define how these services should run together. Then, with a simple command like `docker-compose up`, Docker Compose will start both containers, and your application will be up and running.
        
9. if you want to learn more about docker-compose you can visit this [link](https://tecadmin.net/tutorial/docker/docker-compose/)
    

going ahead let's move on to some `docker-compose` commands:

### Docker-compose Commands:

1. `docker-compose up`**:**
    
    * This command brings your defined services (containers) to life. It reads your `docker-compose.yml` file, sets up the services according to the specifications, and starts them.
        
2. `docker-compose down`**:**
    
    * This is the opposite of `up`. It stops and removes all the containers defined in your `docker-compose.yml` file. It's like turning off and cleaning up your application.
        
3. `docker-compose ps`**:**
    
    * Shows the status of the services defined in your `docker-compose.yml` file. It tells you if they are running or stopped.
        
4. `docker-compose logs`**:**
    
    * Displays the logs of all the services. It's helpful for troubleshooting or checking what's happening inside your containers.
        
5. `docker-compose exec`**:**
    
    * Lets you run commands inside a running container. For example, `docker-compose exec webserver sh` would run the shell (`sh`) command inside the container named "webserver."
        
6. `docker-compose build`**:**
    
    * Builds or rebuilds the images specified in your `docker-compose.yml` file. This is useful when you make changes to your application and need to update the container images.
        
7. `docker-compose pull`**:**
    
    * Pulls the latest images for the services defined in your `docker-compose.yml` file from the Docker Hub or another registry. This ensures you have the most up-to-date versions.
        
8. `docker-compose restart`**:**
    
    * Restarts all the services. It's a quick way to apply changes to your configuration without bringing everything down and back up.
        
9. `docker-compose pause` **and** `docker-compose unpause`**:**
    
    * Pauses and unpauses services. When you pause a service, it stops its processes without actually stopping the container. Unpausing resumes the processes.
        
10. `docker-compose stop` **and** `docker-compose start`**:**
    
    * Stops and starts services individually. `docker-compose stop` halts the services, while `docker-compose start` resumes them.
        

### What is YAML?

**YAML is a readable way to write down information, like a list or settings for a program. It uses indentation to show the structure, and it's often used for easy-to-read configuration files in computer programs. No confusing symbols, just a clear way to write and understand data.**

* YAML is a data serialization language that is often used for writing configuration files. Depending on whom you ask, YAML stands for yet another markup language or YAML ain’t markup language (a recursive acronym), which emphasizes that YAML is for data, not documents.
    
* YAML is a popular programming language because it is human-readable and easy to understand.
    
* YAML files use a .yml or .yaml extension.
    
* Read more about it [here](https://www.redhat.com/en/topics/automation/what-is-yaml)
    

Now, it's time to do today's tasks

### Task 1:

Learn how to use the docker-compose.yml file, to set up the environment, configure the services and links between different containers, and also to use environment variables in the docker-compose.yml file.

`docker-compose.yml` is a configuration file used by Docker Compose to define and manage multi-container Docker applications. This YAML file allows you to specify various components of your application, such as services, networks, and volumes, along with their configurations and relationships.

Here's a breakdown of what you can define in a `docker-compose.yml` file:

1. **Services**: Each service represents a container in your application. You can specify the image to use, environment variables, ports, volumes, and other container-specific settings for each service.
    
2. **Networks**: You can define custom networks for your services to communicate with each other. This helps in isolating and securing communication between containers.
    
3. **Volumes**: Define persistent data storage locations (volumes) that can be mounted into containers. Volumes ensure that data is preserved even if containers are destroyed and recreated.
    
4. **Environment Variables**: Set environment variables for your services to configure their behavior.
    
5. **Dependencies**: You can define dependencies between services, ensuring that one service starts only after another service is up and running.
    
6. **Scaling**: You can specify the desired number of replicas for each service to scale horizontally based on demand.
    
7. **Resource Limits**: Configure resource limits for each service, such as CPU and memory limits.
    

By using a `docker-compose.yml` file, you can describe your entire application stack in a single document, making it easier to manage complex applications and their interdependencies. Docker Compose reads this configuration file and handles the orchestration of containers, networks, and volumes according to the defined specifications. This simplifies the deployment and management of multi-container applications while promoting consistency and reproducibility across different environments.

[**Sample docker-compose.yaml file**](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day18/docker-compose.yaml)

### Task 2:

* Pull a pre-existing Docker image from a public repository (e.g. Docker Hub) and run it on your local machine. Run the container as a non-root user (Hint- Use `usermod` command to give the user permission to docker). Make sure you reboot the instance after permitting the user.
    

```bash
#To pull a pre-existing Docker images
docker pull dipen06/todo-app:tagname
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700904782876/5b7d8797-f197-44f7-a035-1659ae84d6b4.png align="center")

* Inspect the container's running processes and exposed ports using the docker inspect command.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700904961600/5495f67c-dba2-4eb3-a7fc-8c05cce0dedf.png align="center")

docker inspect

```bash
#To inspect docker container's running processes
docker inspect <image-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700905033528/8cd0c904-6acc-4c65-98fb-4bd5b4af2ab7.png align="center")

* Use the docker logs command to view the container's log output. docker logs &lt;container-id&gt;
    

```bash
docker logs <container-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700905130078/e375c6d5-600a-43bc-8d1f-1102483db5ab.png align="center")

* Use the docker stop and docker start commands to stop and start the container.
    

```bash
#To stop docker container
docker kill <container-id>
#To start docker container
docker start <container-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700905204271/5cfc15d4-2a7a-4797-878c-6f56c905d516.png align="center")

* Use the docker rm command to remove the container when you're done.
    

```bash
#To remove container
docker rm <container-id>
```

It is very important to stop the container before removing it. Otherwise the commands won't work

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700905285648/cf7aacde-6dee-44f6-ba08-b0a43e8e67b4.png align="center")

## **How to run Docker commands without sudo?**

* Make sure docker is installed and the system is updated. To check docker install use `docker --version`
    
* `sudo usermod -a -G docker $USER`
    
* Reboot the machine.
    

In conclusion, Docker Compose offers a streamlined and efficient way to manage multi-container applications. By encapsulating the configuration of multiple services, networks, and volumes into a single docker-compose.yml file, developers and DevOps engineers can orchestrate complex application stacks with ease.

In conclusion, Docker and Docker Hub together provide a powerful ecosystem for containerization and application deployment. The Dockerfile serves as the blueprint for creating Docker images, while Docker Hub acts as a repository for storing, sharing, and distributing those images.

Stay in the loop with my latest insights and articles on cloud ☁️ and DevOps ♾️ by following me on my Socials:

Linkedin: [https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)  
Github: [https://github.com/dipen006](https://github.com/dipen006)  
DockerHub: [https://hub.docker.com/u/dipen06](https://hub.docker.com/u/dipen06)

DockerHub repo for above task 🐳: [https://hub.docker.com/repository/docker/dipen06/todo-app/general](https://hub.docker.com/repository/docker/dipen06/todo-app/general)

Thank you for reading! Your support means the world to me. Let's keep learning, growing, and making a positive impact in the tech world together.