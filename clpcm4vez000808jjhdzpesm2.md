---
title: "Day 17: "Mastering Docker: A Beginner's Guide to Creating, Building, and Sharing Web Apps Hassle-Free!""
seoTitle: "A Beginner Guide to Creating, Building, and Sharing Web without hassle"
seoDescription: "A Dockerfile is like a cooking recipe for your computer programs. Instead of telling you how to cook a meal, it gives instructions on how to set up and run."
datePublished: Fri Nov 24 2023 12:42:57 GMT+0000 (Coordinated Universal Time)
cuid: clpcm4vez000808jjhdzpesm2
slug: day-17-mastering-docker-a-beginners-guide-to-creating-building-and-sharing-web-apps-hassle-free
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700829690177/14034b3c-378d-4418-91bd-0d1a22819349.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700829743019/dbd1ad8a-9adb-4926-8cfa-3fbdfc77f9ad.png
tags: linux, docker, github, devops, 90daysofdevops

---

### **What is a Dockerfile?**

A Dockerfile is like a cooking recipe for your computer programs. Instead of telling you how to cook a meal, it gives instructions on how to set up and run a software application. This helps make sure that your program works the same way on any computer, solving the problem of different computer setups. It's a handy tool for packaging and sharing software, ensuring consistency and making it easy for others to use your applications.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700829319348/4eb341e6-6519-445b-972a-94354fa25327.png align="center")

### **Why is it needed?**

Imagine you have a fantastic software application that works perfectly on your computer. You want to share it with others, but they might have different setups on their machines. This can lead to compatibility issues. A Dockerfile helps solve this problem by providing a consistent way to package and distribute your software, ensuring that it runs the same way on any machine.

let's now move on to today's tasks

### Task 1: Create a Dockerfile for a simple web application (e.g. a Node.js or Python app)

```bash
# Use an official Python runtime as the base image
FROM python:3

WORKDIR /app

# Copy the rest of the application code
COPY . /app

RUN pip install django==3.2

# Install the required packages
RUN python manage.py migrate

# Define the command to run the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828501587/938dee70-1fad-4c14-bcf8-e3856410bafc.png align="center")

### Task 2: Build the image using the Dockerfile and run the container

```bash
#To build the image
docker build . -t todo-app
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828593064/a3d491c1-83d6-4eaf-8a45-95dc728d417b.png align="center")

```bash
# To run the container
docker run -d -p 8001:8001 todo-app
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828702588/10760508-c517-4d0f-b41a-54acb99769d9.png align="center")

### Task 3: Verify that the application is working as expected by accessing it in a web browser

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828758580/146df183-8816-4bdf-9b1c-b3c5fc1cc834.png align="center")

### Task 4: Push the image to a public or private repository (e.g. Docker Hub )

```bash
#docker tag old-tag new-tag
docker tag todo-app dipen06/todo-app
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828836871/3c8ddb1b-aab4-4fe3-b8f0-3cff3fb8b6b8.png align="center")

```bash
#To login docker hub
docker login
#to push docker image
sudo docker push imagename
```

I already used these commands before so you will have a little difference in the outputs

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828953058/734965b3-76d7-41ec-b296-2e0d6c3a1cc9.png align="center")

### Docker Image Pushed

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700828997168/d96dd951-52c8-481c-9cf5-98fc756e0583.png align="center")

In conclusion, a Dockerfile serves as the recipe for constructing a consistent and reproducible software environment. Just as a recipe guides the creation of a dish, a Dockerfile provides step-by-step instructions to set up and package a software application. Its necessity becomes apparent when sharing software across diverse computing environments, where differences in setups can lead to compatibility issues. With a Dockerfile, developers ensure that their applications run uniformly on any machine, fostering seamless deployment and collaboration.

## Follow me on socials and stay in loop😉:

Github: [https://github.com/dipen006](https://github.com/dipen006)  
Twitter: [https://twitter.com/dipenr06](https://twitter.com/dipenr06)  
LinkedIN: [https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)