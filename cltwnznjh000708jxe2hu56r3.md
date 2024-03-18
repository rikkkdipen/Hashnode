---
title: "Day 8: Mastering GitHub: Essential Toolkit for DevOps Wizards"
seoTitle: "Mastering GitHub: Essential Toolkit for DevOps Wizards"
seoDescription: "Maximize GitHub with 'Mastering GitHub: Essential Toolkit for DevOps'. From version control to collaboration, this guide boosts efficiency. Get started toda"
datePublished: Mon Mar 18 2024 08:09:06 GMT+0000 (Coordinated Universal Time)
cuid: cltwnznjh000708jxe2hu56r3
slug: day-8-mastering-github-essential-toolkit-for-devops-wizards
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1710743332068/f2cc0ad6-c9bc-484d-ab30-6df7e644711a.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1710749255825/11f6d239-0845-417d-af71-8f09b037d2f1.png
tags: linux, aws, github, opensource, git, devops, hashnode, terraform, 90daysofdevops, wemakedevs, trainwithshubham

---

## What is Git?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710749009139/1cf00d3f-2003-409b-8ccf-9445b02ec7e7.png align="center")

Imagine you have a magical notebook where you write down all your ideas, stories, and changes you make to them. This notebook not only keeps track of what you write but also remembers every version of your stories, almost like having a time machine for your writing.

Git is like that magical notebook, but for computer programmers. Instead of stories, programmers write code, and Git helps them keep track of all the changes they make to that code over time. So, if they want to go back to a previous version of their code or see who made what changes, Git makes it easy. It's like having a super organized and efficient way to manage all your coding projects.

## What is Github?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710749125375/f004b59d-3326-4f04-acd1-95c79c7b778e.png align="center")

Imagine you have a box of LEGO bricks. Each brick represents a piece of code or a project you're working on. Now, GitHub is like a huge playground where you can share your LEGO creations with others and collaborate on building even cooler things together.

It's not just about sharing your LEGO creations, though. GitHub also provides tools to help you and your friends work on projects together efficiently. For example, you can suggest changes to someone else's LEGO creation, and they can decide whether to accept or reject your suggestions.

In simpler terms, GitHub is a platform where programmers can store and share their code, work on projects together, and keep track of changes they make along the way. It's like a big virtual space where people can collaborate and build amazing things with their code, just like playing with LEGO bricks in a giant playground.

## What is Version Control System (VCS)?. How many types of version controls we have?

Version control is like having a time machine for your work. It's a system that keeps track of changes you make to files over time. Imagine you're writing a story on your computer. Version control would help you see all the different drafts you've written, and if you don't like the latest version, you can go back in time to an earlier one.

There are mainly two types of version control systems:

1. **Centralized Version Control Systems (CVCS)**: In this system, there's a central server that stores all the files and their versions. When you want to make changes, you check out a copy of the files from the server, make your edits, and then check them back in. Examples include Subversion (SVN) and Perforce.
    
2. **Distributed Version Control Systems (DVCS)**: Here, every user has their own copy of the entire project and its history on their computer. This means you can work offline and still have access to the full history of the project. When you're ready, you can synchronize your changes with others. Git and Mercurial are examples of distributed version control systems.
    

Both types have their advantages and are used in different scenarios, but they both serve the same purpose: to keep track of changes and make collaboration easier.

## Why we use Distributed Version Control over Centralized Version Control?

Centralized version control is like having one big master copy of your project stored in a central location. When you want to make changes, you have to connect to that central location to get the latest version and then save your changes back there. It's like everyone working on a single document together.

Distributed version control, on the other hand, is like giving everyone their own copy of the project. Each person can make changes to their own copy whenever they want, without needing to connect to a central server. They can then share those changes with others whenever they're ready. It's like everyone having their own copy of the document, making edits, and then merging those edits together later.

There are a few reasons why distributed version control is often preferred:

1. **Flexibility and Independence**: With distributed version control, you're not reliant on a central server. If the server goes down, or if you're not connected to the internet, you can still work on your own copy of the project and make changes.
    
2. **Offline Work**: Since everyone has their own copy of the project, you can work offline. You don't need to be constantly connected to a central server to make changes.
    
3. **Collaboration**: Distributed version control makes it easier for multiple people to work on the same project at the same time. Each person can work on their own copy of the project and then merge their changes together later.
    
4. **Branching and Merging**: Branching and merging, which are essential for managing complex changes and features, are typically easier and more powerful in distributed version control systems. This allows for more flexibility and experimentation without disrupting the main project.
    

Overall, distributed version control offers more flexibility, independence, and collaboration capabilities compared to centralized version control systems.

## Tasks:

### Install Git on your Computer

* Use the following command to install git on your Linux Operating System
    

```bash
sudo apt -y install git
```

* To check if git is installed on your system use the command below
    

```bash
git --version
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710745694041/4fad9405-6eed-456d-a9ca-c50c6e6915f0.png align="center")

### Create a Github account if you don't have one

* if you don't have a Github account you can create one [here](https://github.com/join)
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710745782172/6108651e-6432-4731-9a74-5fc5e6ee2a05.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710745846459/8c4f13fe-094e-4721-874f-5fd3884719d1.png align="center")

As you can see I have my own github account. So I am not creating a new account but still if you want to create a new account you can watch the video below

%[https://www.youtube.com/watch?v=Gn3w1UvTx0A] 

### Basics of Git

1. **Version Control**: Git is a distributed version control system. It helps in tracking changes made to files over time. It allows multiple developers to collaborate on a project simultaneously.
    
2. **Repository (Repo)**: A Git repository is like a database for your project. It stores all the files, history, and metadata related to your project.
    
3. **Local and Remote Repositories**: There are typically two types of repositories: local and remote. The local repository is on your computer, while the remote repository is hosted on a server (like GitHub, GitLab, or Bitbucket).
    
4. **Commits**: Git works by creating snapshots of your files called "commits." Each commit represents a specific state of your project at a certain point in time. Commits include changes made to files along with a message describing the changes.
    
5. **Branches**: Git allows you to work on multiple versions of your project simultaneously through branches. A branch is like a parallel universe where you can make changes independently of the main project. This allows for experimentation without affecting the main codebase.
    
6. **Merge**: Merging is the process of combining changes from one branch into another. This is typically done when you've completed a feature or fixed a bug on a separate branch and want to incorporate those changes back into the main project.
    
7. **Pull and Push**: Pulling refers to fetching changes from a remote repository and merging them into your local repository. Pushing involves sending your local commits to the remote repository to share your changes with others.
    
8. **Clone**: Cloning creates a copy of a remote repository on your local machine. This allows you to work on the project locally and contribute to it without directly modifying the original repository.
    
9. **Pull Request (PR)**: A pull request is a way to propose changes to a repository hosted on a platform like GitHub. It allows others to review your changes before merging them into the main project.
    
10. **Conflict Resolution**: Sometimes, when merging branches or pulling changes, conflicts may arise if Git is unable to automatically reconcile differences between files. Conflict resolution involves manually resolving these conflicts by editing the affected files.
    

Overall, Git provides a robust framework for managing projects, tracking changes, and collaborating with others effectively. Mastering Git enables developers to work efficiently and maintain the integrity of their codebase.

## Exercises

### Create a new repository on github and clone it into your local machine

To create a new repository on Github. Click on Repositories

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710746550237/55ee7ae3-58f2-496c-9757-c6225aca62fa.png align="center")

Click on new

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710746590528/e5f73e79-da3e-447b-8e7d-bb9ec125bcae.png align="center")

Enter any name you want to give to your repo and check for its availability

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710746683083/4451f86f-2a09-4705-beb2-31c06203dedc.png align="center")

keep the repository public if you are the only individual using it or want other people to contribute it to.

keep the repository private If you are making the repo for a company or a particular group and you don't want any other person beside your team to contribute it to

Add a README.md file if you want to : ) (very important if you want to maintain a proper project)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710746859241/73722409-5336-45a9-a9f6-96b41e602f7d.png align="center")

and click on create repository.

Now you repository has been created and it will redirect you to this page

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710746959877/cc32c410-755c-4e83-9ec7-7c863e38efea.png align="center")

To Clone this Repository in yout local system

click on code

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747356591/073370e7-b6cf-4a06-bf63-7fc608d2df6c.png align="center")

copy the link

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747388424/fb5e9afb-f1e7-4c6e-a930-f274b0be7c6d.png align="center")

after you copied the link. open terminal in your local operatins sytem

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747446420/8fd8c11c-5362-4ac6-954f-3ed1ac982295.png align="center")

Now enter the following command

```bash
git clone <the link you copied>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747520253/1791710e-42f1-4bdf-a8d3-b18ddbe3e309.png align="center")

now the repository has been copied to your local system

you can check this by naviating to the path where you used git clone

for eg: I used git clone in my Desktop folder so to check that use the `ls` command

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747609669/2b6521bb-63cf-4905-80fc-d8128b46bd36.png align="center")

In above image you can see that the "demo" repository that we have created has been successfully cloned in your local repository

### Make some changes to the file in repository and commit them to repository using git

To make changes in your local repo. Open the repo with `cd` command

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747760922/f34c4c7e-5bad-44c6-8eca-f378c9fbef1c.png align="center")

To make changes in it

Now you can make any types of changes in your local repository but for the sake of this article I will just make few changes in my README.md file

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710747857323/2a6cbc49-d117-469c-978e-5c8d2fadeed2.png align="center")

I have made few changes in the README.md file for demonstration purpose

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710748124674/216ff562-77e3-492a-97bb-e1352c319d47.png align="center")

Now to commit the repository using Git

Open Terminal and navigate to the local repo

* To add changes you made in git use the following command
    

```bash
git add <file_name>
git add .
```

you can use either of commands to add the changes you made

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710748275290/c3118f26-3980-435f-b18f-62cee7714180.png align="center")

Now to commit the changes you made in the repo use the git commit command

```bash
git commit -m "your message"
```

* \-m in the command refers to the messge
    

you can use the git commit -m "Your message" to commit you changes with a message

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710748369663/080c9743-a7e8-4025-983a-a2fd85e96a71.png align="center")

The changes you made are now commited in the git repository

### Push the changes back to the repository on Github

* To push the changes back to repo you can use the `git push` command
    
    In the place of username put you github usename and in the password field put the token you have generated
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710748742428/9ba58bad-730f-4872-ac65-2b0f554c5b80.png align="center")

Now you can see that the changes you made have been properly pushed to your repository on Github

If you want to check whether your changes have been saved or not open the repository you have created in the Github website

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710748896566/922f8382-d947-4b96-b65b-05ece63b45e2.png align="center")

You can compare both before/after push command to notice the changes.

~Dipen : )