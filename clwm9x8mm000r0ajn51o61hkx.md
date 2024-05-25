---
title: "Day 22: Getting Started with Jenkins: Automate Your Software Development with a Freestyle Pipeline"
seoTitle: "Getting Started with Jenkins: Automate Your Software Development"
seoDescription: "Learn how to automate software development with Jenkins. Explore key features like automation, continuous integration, and pipelines."
datePublished: Sat May 25 2024 15:36:44 GMT+0000 (Coordinated Universal Time)
cuid: clwm9x8mm000r0ajn51o61hkx
slug: day-22-getting-started-with-jenkins-automate-your-software-development-with-a-freestyle-pipeline
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716631815807/c799fa8e-736d-4bac-943e-bbdbf332ca8a.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1716631908925/1d76fa8e-ed5f-47be-9263-c699d003b608.png
tags: linux, docker, github, web-development, opensource, git, developer, devops, beginners, blockchain, jenkins, devops-articles, 90daysofdevops, trainwithshubham

---

## What is Jenkins?

Jenkins is a tool that helps software developers and IT teams to automate parts of the software development process. Imagine you're building a house. Instead of manually laying every brick and hammering every nail yourself, you use machines to do some of the repetitive tasks, making the construction faster and more efficient. Jenkins acts like those machines but for building software.

Here’s how Jenkins works in simple terms:

1. **Automation**: Jenkins automates repetitive tasks. For example, every time you make changes to your code, Jenkins can automatically check if your changes break anything by running tests. It can also build your application and deploy it to a server without you having to do it manually.
    
2. **Continuous Integration**: This means Jenkins helps in merging code changes from multiple contributors into a shared project frequently, often several times a day. This helps to detect problems early.
    
3. **Plugins**: Jenkins is highly flexible because it has a lot of plugins. Think of plugins like apps on your smartphone. They add new features or integrate with other tools. For example, there are plugins to work with different code repositories, testing tools, and deployment platforms.
    
4. **Pipelines**: Jenkins allows you to create pipelines, which are sequences of automated steps that take your code from development to production. For instance, a pipeline might include steps to fetch the latest code, build it, run tests, and then deploy it to a live server if all tests pass.
    

In summary, Jenkins is like a helper robot for developers. It takes care of the tedious and repetitive parts of software development, making the process faster, more reliable, and less prone to human error.

## Tasks

1. ### **What is Jenkins in own language?**
    

Jenkins is a tool that automates parts of the software development process. It helps us make sure our code works correctly and gets deployed smoothly.

**Key Points:**

1. **Automation**: Jenkins can automatically run tests and build our software every time we make changes, saving us from doing these tasks manually.
    
2. **Continuous Integration**: It helps us merge changes from multiple developers frequently, which makes it easier to catch and fix problems early.
    
3. **Plugins**: Jenkins has many plugins, like apps on a phone, which add extra features and allow it to work with other tools we use.
    
4. **Pipelines**: We can set up pipelines in Jenkins to define a series of steps (like testing and deployment) that our code goes through automatically.
    

**In a nutshell**: Jenkins is like an assistant that handles repetitive and error-prone tasks in software development, making our workflow faster and more reliable.

2. ### Create a Freestyle Pipeline to print "Hello world!"
    

To create a freestyle pipeline in Jenkins. Open your Jenkins server on `:8080` port. Below screen will appear

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716630851720/275824b7-e427-4f46-acdc-473a9d50a7b6.png align="center")

sign in with your username and password. When you first time start the Jenkins server it will ask you to get the password from this location

```plaintext
/home/sh/.jenkins/secrets/initialAdminPassword
```

then reset the password.

after resetting put the username and password to login into the server then below screen will appear

* Click on create a job
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631014067/2a8a1555-2d35-41cf-9e45-efc7171e48d1.png align="center")

* Enter the name and click on Freestyle project
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631068678/fdd2dc57-cfbf-4fc1-a4b5-9f1d0477d0df.png align="center")

* Give the description as you need
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631154058/5ed44475-e612-4bc3-82fa-6b53bdef20f6.png align="center")

* after that scroll down and click on `add build step` in the Build Step section.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631226447/4514c86a-64b1-4596-bdd3-00ee294793ae.png align="center")

* A drop down menu will appear. Click on execute shell
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631259129/77e3ba24-ffd7-489d-a50f-11713705aa9c.png align="center")

* Write the syntax in bash format as
    

```bash
echo "Hello World!"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631335827/ca802cea-dc2e-4a2b-ba0b-d0ad3591a34a.png align="center")

and click on the save button at the bottom.

After you click on save the below screen will appear

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631438614/86dd2162-80c6-44ce-84ae-65479e397a41.png align="center")

* Click on Build Now button the left side
    
* Your build will happen below
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631513879/e8d225ee-9c76-4feb-9f78-388f766106d1.png align="center")

* Click on #1 to see all the logs and configurations
    
* click on console output on the left to see the result
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631597530/ac7500d8-9b50-4710-a413-d6e4c5807010.png align="center")

As you can see the project is properly built and we got the proper output

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716631677782/b06ab485-2b57-4113-bcb3-9e61df35b4e3.png align="center")

~Dipen : )