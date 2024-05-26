---
title: "Day 23:  Streamline Your DevOps Workflow: Mastering Jenkins Freestyle Projects and CI/CD Pipelines"
seoTitle: "Mastering Jenkins Freestyle Projects and CI/CD Pipelines"
seoDescription: "Master Jenkins Freestyle Projects and CI/CD pipelines to streamline your DevOps workflow. Automate and enhance your software development "
datePublished: Sun May 26 2024 03:36:51 GMT+0000 (Coordinated Universal Time)
cuid: clwmznbxc000l09l99izb1ixw
slug: day-23-streamline-your-devops-workflow-mastering-jenkins-freestyle-projects-and-cicd-pipelines
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716658894470/98415522-d20e-4115-9115-1bc6e6988e30.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1716658995293/393e26c8-d762-4659-8487-861a2187bc01.png
tags: artificial-intelligence, linux, docker, python, web-development, kubernetes, developer, devops, beginners, jenkins, cicd-cjy1vtdk2005kjjs17n8couc3, docker-images, devops-articles, 90daysofdevops, trainwithshubham

---

### What is CI/CD?

CI/CD stands for Continuous Integration and Continuous Deployment (or Continuous Delivery). It's a process used in software development to make things easier and more efficient.

### Continuous Integration (CI)

Think of Continuous Integration like a big group project in school where everyone is working on the same document. Every time someone makes changes, those changes are saved to the main document right away. In software development, CI means that every time a developer makes changes to the code, those changes are automatically tested and merged into the main codebase. This helps catch problems early and ensures that everyone's code works well together.

### Continuous Deployment (CD)

Continuous Deployment takes it a step further. Imagine after updating the group project document, it's automatically printed and handed in to the teacher without any extra steps. In software development, CD means that once the code is tested and merged, it’s automatically deployed to the live environment where users can access it. This ensures that new features and fixes are delivered to users quickly.

### Benefits of CI/CD

1. **Faster Development**: Code changes are tested and deployed quickly.
    
2. **Fewer Bugs**: Automated testing catches issues early.
    
3. **Team Collaboration**: Developers can work together more easily since their changes are integrated continuously.
    

### Simple Example

Let's say you're working on a web app with a team. With CI/CD:

1. **CI**: You write a new feature and push your code. Jenkins (a CI tool) automatically runs tests to make sure your code doesn’t break anything and merges it with the main project.
    
2. **CD**: Once the tests pass, the new version of your app is automatically deployed to the server where users can start using the new feature right away.
    

In summary, CI/CD helps automate and streamline the process of integrating and deploying code changes, making software development faster and more reliable.

### What is a Build Job?

A build job automates the process of creating a software application. It takes different pieces of code and combines them to make a working application.

### Key Points

1. **Automation**: Compiles and assembles the code automatically.
    
2. **Tools**: Uses tools like Jenkins.
    
3. **Steps**: Includes steps like compiling code, running tests, and packaging the application.
    

### Example in Simple Terms

1. **Ingredients**: You have pieces of code.
    
2. **Steps**:
    
    * Compile the code.
        
    * Run tests to ensure everything works.
        
    * Package the application.
        

### Why It’s Important

1. **Consistency**: Builds the application the same way every time.
    
2. **Efficiency**: Saves time by automating tasks.
    
3. **Quality**: Catches errors early through automated testing.
    

### How It Works in Jenkins

1. **Create a Job**: Name it “demoApp Build”.
    
2. **Add Steps**: Define steps like compiling, testing, and packaging.
    
3. **Run the Job**: Jenkins runs these steps automatically.
    

In summary, a build job automates creating and testing software, ensuring it works correctly before release.

Sure, here's a shorter version:

### What is a Freestyle Pipeline?

A freestyle pipeline in Jenkins automates software tasks like compiling, testing, and deploying. It's flexible, customizable, and easy to use.

### Key Points

1. **Flexibility**: Customize tasks for your project.
    
2. **Automation**: Automate compiling, testing, and deployment.
    
3. **Ease of Use**: Managed through Jenkins.
    

### Example

Like a recipe:

1. **Ingredients**: Your code.
    
2. **Steps**:
    
    * Compile.
        
    * Test.
        
    * Deploy.
        

### Benefits

1. **Efficiency**: Saves time.
    
2. **Consistency**: Tasks are done the same way.
    
3. **Integration**: Works with other tools.
    

### How to Use

1. **Create a Job**: Set up a freestyle project.
    
2. **Define Steps**: Configure tasks.
    
3. **Run**: Trigger the pipeline.
    

In short, a freestyle pipeline automates software tasks, speeding up development.

## Task 1:

* Create an agent for your job
    
* create a new jenkins freestyle project for your job
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716638352853/3e48f8c4-7318-49b6-8a73-fe512ff7783b.png align="center")

I have cloned the github repo [https://github.com/LondheShubham153/django-todo-cicd.git](https://github.com/LondheShubham153/django-todo-cicd.git)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716638506584/58a817e2-fdaa-465a-8d7a-b4f1032427d6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716638903105/34b70003-80c4-4fda-9833-fcfd0d9a6238.png align="center")

gave branch name develop as repos was the default branch name develop.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716638964898/e289d37a-97b3-4578-8d65-cc298cfe5509.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716638992251/8bfe2582-8a1c-4e84-85d4-27599aef0300.png align="center")

In the Build Section of the project add a build step to run the "docker build" command to build the image for the container.

Click on save and then click the Build Now Button

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716639129234/b936e0c6-57a2-4fa8-a088-5892f9ab32e9.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716639193448/0761f5a1-0318-4173-9fff-aea55a29e586.png align="center")

As you can see the Job ran successfully

and you can successfully check the job build in the following directory

`sudo ls /var/lib/jenkins/workspace/`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716639400017/f12d105a-4d3a-4414-ad76-770df76cb5d1.png align="center")

Add a second step to run the "docker run" command to start a container using the image created in step 3.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657117661/e54e39fd-543d-4a98-836d-76d34891eaba.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657238731/25085c98-616d-4a6e-9b8d-416a4a0a4728.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657674812/be801d54-dfeb-4e94-9a3a-482a1c3060f8.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657682802/41a7ddf8-6c12-49a1-98a4-ee4353dd8c6c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657704667/ee1a8f48-fb8f-4e27-9378-bec191b397a6.png align="center")

To check the port number where the container is running use `docker ps`  
Please add a rule in your instance security group port number.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657741602/2995c892-bd29-416c-903d-8b1445988460.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657785148/36d9a7d9-c592-4534-bf00-8150ee72b359.png align="center")

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Task 2:

* Create Jenkins project to run the "docker-compose up -d" command to start the multiple containers defined in the compose file (Hint- use day-19 Application & Database docker-compose file)
    
* Set up a cleanup step in the Jenkins project to run the "docker-compose down" command to stop and remove the containers defined in the compose file.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658291649/0ede9b7e-a6da-455c-a611-b94745c4dffc.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658343109/aeb39559-2991-4ff3-83a7-56748936acb4.png align="center")

we have stop the previous container by `docker kill container-id` and `docker rm container-id`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658415551/e29bf6a5-4e92-4c14-9304-73b4a0b4caec.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658510124/4d9d0e73-49f8-4ff3-bc83-cf313d7d3be4.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658518973/66a0d217-5b66-4d9a-a18f-61b56770a0a6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658528122/14127efb-b0c6-4029-919e-fb088d9169e5.png align="center")

we can also check if the pipeline has worked or not through the `docker ps` command

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658584520/e248d6ea-5bb4-4ec7-a06f-725560aa6fee.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716658616021/be96f136-ecb6-4a0c-a5da-cfd305ff0077.png align="center")

In conclusion, the Jenkins Freestyle Project empowers DevOps engineers to automate, integrate, and enhance software development. Its versatility, efficiency, and collaborative features contribute to streamlined workflows and improved software quality. Embracing this tool is crucial for modern DevOps practices, enabling agile and effective development lifecycles.

~Dipen : )