---
title: "Day 18: Docker Mastery for DevOps Pros"
seoTitle: "Day 18: Docker Mastery for DevOps Pros"
seoDescription: "Master Docker for DevOps Pros in just 18 days! Dive deep into containerization, Docker Compose, orchestration, and more."
datePublished: Tue Apr 30 2024 15:36:17 GMT+0000 (Coordinated Universal Time)
cuid: clvmjwdv4000309jvekeo16s8
slug: day-18-docker-mastery-for-devops-pros
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1714459785388/45c1b999-6b94-4d7e-9fd1-ba1b670a22ea.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1714459948345/c79ccbb7-3f45-4c53-ac87-b8f9ce488fe7.png
tags: blogging, linux, docker, web-development, mongodb, kubernetes, developer, devops, hashnode, blockchain, devops-articles, devops-journey, wemakedevs, trainwithshubham

---

## 🔷 What is Docker Compose?

Imagine you're throwing a big party and you need to organize everything from the venue to the music to the food. Instead of handling each task separately, Docker Compose is like your party planner. It helps you manage all the different things you need for your party, like setting up the venue (containers), coordinating the music (services), and arranging the food (networking) – all in one go! It simplifies the process of running multiple Docker containers together, making it easier for you to focus on having a great party (or in this case, running your applications smoothly).

1. **Container Coordination:** Docker Compose lets you manage multiple Docker containers as a single application, defining how they interact and work together.
    
2. **Simplified Configuration:** With a simple YAML file, you can specify all the services, networks, and volumes needed for your application, streamlining setup and deployment.
    
3. **Efficient Development:** It speeds up the development process by allowing you to define your application environment once and easily replicate it across different machines, ensuring consistency and reliability.
    

## 🔷 What is YAML?

YAML (YAML Ain't Markup Language) is like a special code that's super easy for both computers and humans to read. It's used to organize and structure information in a way that's clean and understandable. Imagine it's like writing a recipe or making a to-do list – you list items and their properties in a clear and organized manner using simple rules, making it easy for both you and your computer to understand what needs to be done.

* YAML is a data serialization language that is often used for writing configuration files. Depending on whom you ask, YAML stands for yet another markup language or YAML ain’t markup language (a recursive acronym), which emphasizes that YAML is for data, not documents.
    
* YAML is a popular programming language because it is human-readable and easy to understand.
    
* YAML files use a .yml or .yaml extension.
    

## Tasks

### 🔷 Task 1

Learn how to use the docker-compose.yml file, to set up the environment, configure the services and links between different containers, and also to use environment variables in the docker-compose.yml file.

A docker-compose.yml file is like a blueprint for your multi-container Docker application. It's written in a format called YAML, which is easy to read and write. This file helps Docker Compose understand how your application should be set up and managed.

Here's what you can include in this file:

1. **Services**: Each service is like a separate container in your application. You can say what image to use, which ports to open, and other settings for each service.
    
2. **Networks**: You can create custom networks to connect your services. This helps them talk to each other securely.
    
3. **Volumes**: These are places where your data is stored. You can set up volumes to keep your data safe, even if containers are restarted.
    
4. **Environment Variables**: These are settings you can pass to your services to customize how they work.
    
5. **Dependencies**: You can specify if one service needs another to be running before it can start.
    
6. **Scaling**: You can say how many copies of each service you want to run, depending on how much demand your application has.
    
7. **Resource Limits**: You can set boundaries on how much CPU or memory each service can use.
    

By writing a docker-compose.yml file, you're basically telling Docker Compose how your application should be built and run. It helps you manage your application's complexity and ensures it runs consistently across different environments.

[Sample docker-compose.yaml file](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day18/docker-compose.yaml)

### 🔷 Task 2

Pull a pre-existing Docker image from a public repository (e.g. Docker Hub) and run it on your local machine. Run the container as a non-root user (Hint- Use `usermod` command to give user permission to docker). Make sure you reboot instance after giving permission to user.

```bash
#To pull a pre-existing Docker images
docker pull rikkkdipen/django-todo-cicd:tagname
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714455265817/d1b2f3a8-8c99-4321-9b20-c964a9f3af3f.png align="center")

* Inspect the container's running processes and exposed ports using the docker inspect command.
    

```bash
#To run docker
docker run rikkkdipen/django-todo-cicd:latest
#To check docker process status
docker ps
docker images
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714455386960/6dfc5ab9-2730-436a-9ef1-af51b74c21a4.png align="center")

* docker inspect
    

```bash
docker inspect <image-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714455469230/d17024a3-f161-4852-9c5b-1fd9e14d6115.png align="center")

* Use the docker logs command to view the container's log output.
    

```bash
docker logs <container-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714455576742/62028fa0-e524-4eb7-b98f-05f0fce7e338.png align="center")

* Use the docker stop and docker start commands to stop and start the container.
    

```bash
#To stop docker container
docker kill <container-id>
#To start docker container
docker start <container-id>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714455830404/f9354ffe-ee76-4f7f-9c6c-21911941ef06.png align="center")

## 🔷 How to run Docker Commands without sudo?

1. First, make sure Docker is installed and your system is up to date. You can check if Docker is installed by typing "docker --version" in your terminal.
    
2. Then, add yourself to the Docker group with the command "sudo usermod -a -G docker $USER".
    
    ```bash
    sudo usermod -a -G docker $USER
    ```
    
3. After that, reboot your computer to make sure all changes take effect.
    

In summary, Docker Compose makes it easy to manage applications that require multiple containers. With a single file called docker-compose.yml, you can set up different services, networks, and storage volumes without hassle.

In conclusion, Docker and Docker Hub make a great combo for containerizing and deploying applications. Dockerfiles are like instruction manuals for building Docker images, and Docker Hub is a handy place to store, share, and find these images.

~Dipen : )