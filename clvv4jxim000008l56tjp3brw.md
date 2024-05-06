---
title: "Day 19: Maximizing Docker Efficiency: Harnessing Volumes and Networks in DevOps"
seoTitle: "Maximizing Docker Efficiency: Harnessing Volumes and Networks"
seoDescription: ""Optimize Docker efficiency in DevOps with strategic use of volumes and networks. Maximize resource utilization and streamline development workflows.""
datePublished: Mon May 06 2024 15:36:38 GMT+0000 (Coordinated Universal Time)
cuid: clvv4jxim000008l56tjp3brw
slug: day-19-maximizing-docker-efficiency-harnessing-volumes-and-networks-in-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1715000642060/02a6a190-20fa-4054-882c-ba556a009add.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1715000839829/7c543f9a-4908-4ef5-9612-220c29690f44.png
tags: cloud, blogging, docker, aws, python, development, developer, devops, hashnode, blockchain, docker-images, devops-articles, 90daysofdevops, wemakedevs, trainwithshubham

---

### 🔷 Docker Volume

Think of a Docker volume as a special folder that Docker containers can share and access. It's a way for containers to store and retrieve data separately from the container itself. Imagine you have a group project where everyone needs to access the same set of files. Instead of each person keeping a copy on their own laptop, you all work from a shared folder stored in a central location. Docker volumes work in a similar way, allowing containers to easily access and share data, making it handy for tasks like database storage, file sharing, or configuration files.

Docker allows you to create something called volumes. Volumes are like separate storage areas that can be accessed by containers. They allow you to store data, like a database, outside the container, so it doesn't get deleted when the container is deleted. You can also mount from the same volume and create more containers having the same data. [**reference**](https://docs.docker.com/storage/volumes/)

### 🔷 Docker Network

Picture a Docker network as a digital highway that allows different containers to communicate with each other. Just like cars on a highway can travel to different destinations and interact with each other, containers on a Docker network can send data and messages to one another. This network helps containers talk to each other, share information, and work together smoothly, making it easier for your applications to function effectively in a Docker environment.

Docker allows you to create virtual spaces called networks, where you can connect multiple containers (small packages that hold all the necessary files for a specific application to run). This way, the containers can communicate with each other and with the host machine (the computer on which the Docker is installed). When we run a container, it has its own storage space that is only accessible by that specific container. If we want to share that storage space with other containers, we can't do that. [**reference**](https://docs.docker.com/network/)

### 🔷 Task 1

Create a multi-container docker-compose file which will bring *UP* and bring *DOWN* containers in a single shot.

* git clone from
    

I have already cloned the file from git so it'll just say the file already exists

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714654694734/7aa733e1-bd5e-417f-a482-52c6384f9148.png align="center")

Use the `docker-compose up` command with the `-d` flag to start a multi-container application in detached mode.

```bash
#To start the multi-container
docker-compose up -d
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714654817439/3ebfc130-5d5d-426b-a420-33e59dfba733.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714654851751/ab350592-7f54-428e-ac23-20b4503376b3.png align="center")

Use the `docker-compose ps` command to view the status of all containers, and `docker-compose logs` to view the logs of a specific service.

```bash
#To view the status
docker-compose ps
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714654896633/47b0e6f1-dcad-44e8-a4ba-cac755c29c0e.png align="center")

Use the `docker-compose down` command to stop and remove all containers, networks, and volumes associated with the application

```bash
#To stop the container
docker-compose down
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714654935784/22d76ecf-5e11-405c-90db-cb421a2ac5e2.png align="center")

### 🔷 Task 2

* Learn how to use Docker Volumes and Named Volumes to share files and directories between multiple containers.
    

```bash
#To create docker volume
docker volume create --name django_todo_volume --opt type=none --opt device=/home/sh/Desktop/90daysofdevops/projects/django-todo-cicd/volume --opt o=bind
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714655085730/50c481a4-3915-46e5-98fb-6bfb791483bf.png align="center")

* Create two or more containers that read and write data to the same volume using the `docker run --mount` command.
    

```bash
#mount
docker run -d --mount source=django_todo_volume,target=/data -p 8000:8000 django-todo-cicd:latest
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714655225768/650d89fc-d406-45a6-9372-aa727d45c5ed.png align="center")

* Verify that the data is the same in all containers by using the `docker exec` command to run commands inside each container.
    

```bash
#Docker exec -it <container-id> bash
docker exec -it 23e4f8de944c bash
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701375409056/5f1b9a27-4065-4084-bc62-c822189b2ecb.png?auto=compress,format&format=webp align="left")

* Use the docker volume ls command to list all volumes and the docker volume rm command to remove the volume when you're done.
    
* I already deleted and removed the container images which i forgot to take screenshot of so here is the next step
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701375802025/3114318f-0b5d-4b1a-9ff4-6e273847ec13.png?auto=compress,format&format=webp align="left")

In conclusion, Docker volumes play a crucial role in managing data persistence and sharing between containers, especially in multi-container and multi-stage setups. Volumes provide a mechanism to decouple data storage from the container lifecycle, ensuring data integrity, scalability, and easy container management.

For multi-container applications orchestrated with tools like Docker Compose, volumes enable seamless data sharing between different services, allowing them to collaborate without the constraints of container boundaries. This promotes modularization, enhances security, and simplifies data management.

~Dipen : )