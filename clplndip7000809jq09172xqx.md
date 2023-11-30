---
title: "Day 19: Docker for DevOps Engineers (Part 2)"
seoTitle: "Day 19: Docker for DevOps Engineers (Part 2)"
seoDescription: "Imagine Docker containers as lightweight, portable units that can run applications and their dependencies. Now, these containers are like small, self..."
datePublished: Thu Nov 30 2023 20:27:36 GMT+0000 (Coordinated Universal Time)
cuid: clplndip7000809jq09172xqx
slug: day-19-docker-for-devops-engineers-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1701268425231/a0a036cc-c990-468d-9806-d6bc91c103df.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1701376031835/e539b8b5-4a20-4f6c-ad23-865aa860df99.png
tags: linux, docker, github, kubernetes, git, devops, docker-images, docker-network, 90daysofdevops, trainwithshubham

---

### What is Docker Volume?

Imagine Docker containers as lightweight, portable units that can run applications and their dependencies. Now, these containers are like small, self-contained worlds. They have their own file system, isolated from the host machine.

But what if you want some data to persist even if the container is stopped or removed? That's where Docker volumes come in.

A Docker volume is like a shared folder between your host machine and the Docker container. It's a way for the container to store and retrieve data that persists beyond the container's life. So, if you have a database running in a Docker container and you want the database files to stick around even if you stop or remove the container, you'd use a Docker volume.

Docker allows you to create something called volumes. Volumes are like separate storage areas that can be accessed by containers. They allow you to store data, like a database, outside the container, so it doesn't get deleted when the container is deleted. You can also mount from the same volume and create more containers having same data. [reference](https://docs.docker.com/storage/volumes/)

In simpler terms, a Docker volume is a bridge that lets your container and your computer talk to each other, sharing and preserving data. It's a handy tool to ensure that your important information doesn't vanish when your container takes a break.

### What is Docker Network?

Think of Docker containers like individual computers running different applications. Now, for these containers to communicate with each other, you need a way for them to be on the same network, just like computers in a home or office are connected to the same Wi-Fi or local network.

In Docker, a network is like a virtual space that allows containers to talk to each other. It's a way for them to share information and services. There are different types of networks in Docker, like a bridge network (default for containers on the same host), an overlay network (for containers across multiple hosts), and more.

So, if you have a web server in one Docker container and a database in another, you'd put them on the same Docker network. This way, they can easily exchange data without any hassle, just like devices on the same Wi-Fi network can communicate with each other.

Docker allows you to create virtual spaces called networks, where you can connect multiple containers (small packages that hold all the necessary files for a specific application to run) together. This way, the containers can communicate with each other and with the host machine (the computer on which the Docker is installed). When we run a container, it has its own storage space that is only accessible by that specific container. If we want to share that storage space with other containers, we can't do that. [reference](https://docs.docker.com/network/)

Let's move on to the tasks of the day

### Task 1: Multi container docker compose file

* Create a multi-container docker-compose file which will bring *UP* and bring *DOWN* containers in a single shot ( Example - Create application and database container )
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701272334836/0260b3bf-bcf2-4e44-ba1c-e97d0bab5560.png align="center")

Use the `docker-compose up` command with the `-d` flag to start a multi-container application in detached mode.

```bash
#To start the multi-container
docker-compose up -d
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701272394323/35367b9f-efd2-4a46-b84f-1d51b5efd053.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701272452323/a5b59568-5a16-4262-8976-9cfb1d063f16.png align="center")

Use the `docker-compose ps` command to view the status of all containers, and `docker-compose logs` to view the logs of a specific service.

```bash
#To stop the container
docker-compose down
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701272526130/85125d77-6410-410a-8180-19f5a4d280d2.png align="center")

### Task 2: Docker Volumes

* Learn how to use Docker Volumes and Named Volumes to share files and directories between multiple containers.
    

```bash
#To create docker volume
docker volume create --name django-todo-volume --opt type=none --opt device=/home/sh/Desktop/DevOps/projects/volumes/django-app --opt o=bind
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701367871136/b82f1f13-26f5-4519-90bb-4ef5829e26e5.png align="center")

* Create two or more containers that read and write data to the same volume using the `docker run --mount` command.
    

```bash
#mount
docker run -d -p 8000:8000 --mount source=django-todo-volume,target=/data django-todo-app:latest
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701274829439/f2f7699e-7911-4ec2-bf87-022e6d52adac.png align="center")

* Verify that the data is the same in all containers by using the `docker exec` command to run commands inside each container.
    

```bash
#Docker exec -it <container-id> bash
docker exec -it 76250168a0c9 bash
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701375409056/5f1b9a27-4065-4084-bc62-c822189b2ecb.png align="center")

* Use the docker volume ls command to list all volumes and the docker volume rm command to remove the volume when you're done.
    
* I already deleted and removed the container images which i forgot to take screenshot of so here is the next step
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701375802025/3114318f-0b5d-4b1a-9ff4-6e273847ec13.png align="center")

n conclusion, Docker volumes play a crucial role in managing data persistence and sharing between containers, especially in multi-container and multi-stage setups. Volumes provide a mechanism to decouple data storage from the container lifecycle, ensuring data integrity, scalability, and easy container management.

For multi-container applications orchestrated with tools like Docker Compose, volumes enable seamless data sharing between different services, allowing them to collaborate without the constraints of container boundaries. This promotes modularization, enhances security, and simplifies data management.

Stay in the loop and connect with me on socials:

Linkedin: [https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)  
Twitter: [https://twitter.com/dipenr06](https://twitter.com/dipenr06)  
Github: [https://github.com/dipen006](https://github.com/dipen006)

Thank you for reading! Your support means the world to me. Let's keep learning, growing, and making a positive impact in the tech world together.

~Dipen : )