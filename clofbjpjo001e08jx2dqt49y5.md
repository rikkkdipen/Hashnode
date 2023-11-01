---
title: "Day 8: DevOps Engineers' Guide to Git and GitHub: Enhance Collaboration and Efficiency"
seoTitle: "Mastering Git and GitHub for DevOps Engineers: Elevate Collaboration a"
seoDescription: "Git is a vital tool in modern software development, offering developers the power to track and manage changes to their code efficiently..."
datePublished: Wed Nov 01 2023 05:30:10 GMT+0000 (Coordinated Universal Time)
cuid: clofbjpjo001e08jx2dqt49y5
slug: day-8-devops-engineers-guide-to-git-and-github-enhance-collaboration-and-efficiency
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698749965558/8999e689-efcd-4b48-aeb5-01c1d3f0159e.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698758302834/73cfdf10-6bc3-48e1-bc38-f060cd6545f1.png
tags: github, git, 90daysofdevops, wemakedevs, trainwithshubham

---

### What is Git?

Git is a vital tool in modern software development, offering developers the power to track and manage changes to their code efficiently. Created by Linus Torvalds, Git ensures the integrity of software projects and allows for seamless collaboration. It's a distributed version control system (DVCS) that provides a historical record of all code changes, empowers developers to work offline, and simplifies the process of merging code contributions from various team members. Git's speed, security, and open-source nature make it a cornerstone of DevOps and software development, with platforms like GitHub enhancing collaboration and enabling continuous integration and deployment.

### Aspects of Git

1. **Version Control:** Git tracks changes to files over time, allowing developers to see the entire history of modifications to a project. This makes it easy to revert to previous states, track who made changes, and understand when and why changes were made.
    
2. **Distributed:** Git is distributed, meaning that each developer working on a project has a complete copy of the repository. This allows them to work offline, make changes, and then synchronize (push/pull) their changes with other team members' copies.
    
3. **Branching:** Git makes it simple to create branches or divergent lines of development. Developers can work on new features, bug fixes, or experiments in isolated branches, which can later be merged into the main project when they are ready.
    
4. **Collaboration:** Git facilitates collaboration among multiple developers. They can work on different branches and merge their changes into the main project. Git hosting platforms like GitHub, GitLab, and Bitbucket offer tools for code review, issue tracking, and collaboration.
    
5. **Speed and Efficiency:** Git is designed to be fast and efficient. It only tracks changes, not entire files, and it uses a snapshot-based approach, making operations like branching and merging quick.
    
6. **Security:** Git employs cryptographic hashing to ensure the integrity of data. Each commit is identified by a unique hash, and changes to the codebase can be verified using these hashes.
    
7. **Open Source:** Git is open source, which means it is freely available and has a large community of users and contributors. It is widely adopted and supported on various operating systems.
    

To summarize it in short we can say that With Git, you can keep a record of who made changes to what part of a file, and you can revert to earlier versions of the file if needed. Git also makes it easy to collaborate with others, as you can share changes and merge the changes made by different people into a single version of a file.

### What is GitHub?

GitHub is an essential web-based platform for developers, offering a collaborative space to efficiently manage software projects. Leveraging the powerful Git version control system, it supplements Git's capabilities with an intuitive web interface and robust collaboration tools. Explore the key features of GitHub below:

1. **Git Hosting:** GitHub is where you can store and share your code, making it accessible from anywhere.
    
2. **Web Interface:** GitHub provides an easy-to-use website for managing your code, eliminating the need for complex Git commands.
    
3. **Collaboration:** It allows multiple people to work together on a project, sharing their changes and ideas.
    
4. **Issue Tracking:** GitHub's built-in system helps you keep track of tasks, bugs, and feature requests.
    
5. **Code Review:** You can propose and review code changes before merging them into the main project.
    
6. **Continuous Integration:** GitHub integrates with testing and deployment tools for automated code testing.
    
7. **Community:** GitHub is a hub for developers to follow, contribute, and collaborate on various projects.
    
8. **Documentation:** You can document your project and create wikis to share information easily.
    

### What is Version Control?

Version control is like a time machine for your files. It keeps track of changes you make to your work, so you can go back in time if something goes wrong. It's really helpful when many people are working on the same project.

There are 2 types of version control that are mainly used they are

* Centralized version Control (CVS)
    
* Decentralized Version Control (DVCS)
    

### **Centralized Version Control:**

Centralized version control is like having a single, central hub where all your project's files and their histories are stored. Imagine a library where everyone borrows and returns books from the same place. Here's how it works:

1. **Central Repository:** There is a central server where all project files and their versions are kept. It's like the main library where all the books are stored.
    
2. **Checkout:** When a team member wants to work on a project, they "check out" a copy of the files from the central repository. It's like taking a book out of the library.
    
3. **Editing:** They can edit these files on their computer and save their changes.
    
4. **Commit:** Once they are done, they "commit" their changes back to the central repository. It's like returning the book to the library.
    
5. **Conflict:** If two people make changes to the same file at the same time, there can be conflicts that need to be resolved.
    

### **Distributed Version Control:**

Distributed version control is like having your copy of the entire library and being able to make changes. Each person has a library with all the books. Here's how it works:

1. **Local Copies:** Everyone has a complete copy of the project's files and their history on their computer. It's like having your library at home.
    
2. **Commit:** Every Team member can make changes and "commit" them to their local copy. It's like making notes or highlighting in your books.
    
3. **Push and Pull:** They can share their changes with others by "pushing" and "pulling" from each other's libraries. It's like sharing your book annotations with friends and borrowing their notes.
    
4. **Conflict Resolution:** If there are conflicts between changes, they can be resolved by merging the different versions.
    
5. **Backup:** Since everyone has a copy, there's a backup if the central repository or someone's computer crashes. It's like having copies of the books at different places.
    

Distributed version control gives each team member more independence and flexibility, while centralized control relies on a central hub for coordination.

### Why do we use a Distributed Version Control System over a Centralized Version Control System?

We use a Distributed Version Control System (DVCS) over a Centralized Version Control System (CVCS) for several reasons:

1. **Work Anywhere:** With DVCS, you can work on your code even without the internet, while CVCS often needs an internet connection.
    
2. **Speed:** DVCS is usually faster for common tasks like saving your changes, making new branches, and combining changes. CVCS can be slower because it relies on a central server.
    
3. **Backup:** In DVCS, everyone has a full copy of the project, so it's like having multiple backups. In CVCS, if the central server has problems, the project could be in trouble.
    
4. **Flexible Teamwork:** DVCS lets team members work on their own without causing trouble for others. You can even experiment with your code separately. CVCS requires more coordination to avoid conflicts.
    
5. **Branching and Merging:** DVCS makes it easier to create different versions of your code and merge changes. CVCS can be more complicated in this regard.
    
6. **Large Teams and Long Distances:** DVCS is better for big teams and when team members are far apart because everyone has their complete copy of the project.
    
7. **Security:** Even if the central server is hacked in DVCS, your work is safe on your computer. In CVCS, if the central server is compromised, it's riskier.
    

In summary, while both DVCS and CVCS have their use cases, DVCS provides more flexibility, resilience, and efficiency, making it a preferred choice for many modern software development teams, particularly those working on large and distributed projects.

### How to Install Git?

In Ubuntu, we use an apt package manager to install any software package we want to use, to install git on your system enter the following command:

```bash
sudo apt install git -y
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698752209134/d8e9e604-e4d6-4b38-8a93-551ef2acaa95.png align="center")

Now Git is easily installed on your system. Let's perform the following tasks

* Sign up on GitHub
    
* Create a new repository in GitHub
    
* Clone a new repository on your local system
    
* Make some changes to a file in the repository and commit them to the repository using Git.
    
* Push the changes back to the repository on GitHub
    

### How to Sign up on Git Hub?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753365529/1fc56965-4491-413a-9bc1-ec46eb804302.png align="center")

Click on the Sign-up button on the top right tab to sign up to GitHub,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753438559/d79c412a-8f28-48b0-9219-b1b87092678f.png align="center")

Enter your email id and click continue.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753469139/8dd4c6d7-f426-4efd-b025-21240d6945b9.png align="center")

Enter whatever password you want and remember to take note of it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753523772/e12b594a-8f09-4b98-845a-5c275b18ba22.png align="center")

Enter your username. enter whatever name you prefer and click continue. make sure the name is professional and suits your profession.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753610066/cdcdd5ea-7aef-4314-9a06-c6e2904bfc4f.png align="center")

Type "Y" or "N" according to your preference and solve the captcha. Then click on Submit. and then click on Create Account.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753680908/b9014ed1-13a9-43c6-bd99-8b97c5923f85.png align="center")

Enter the code you receive on your email and you'll be redirected to your GitHub account.

### How to do a basic git setup?

open your terminal and paste the following commands

```bash
git config --global user.name "your username"
git config --global user.email "your email"
```

### How to Create a New Repository in GitHub?

* Go to your profile
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753835801/9167ba87-e7a9-40fb-b749-e2af912225b6.png align="center")
    
    Click on repositories and click on New
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753889102/0796befd-77d0-4aed-9311-7e7e1ebf8cf0.png align="center")
    
    Enter the name you want to give to your repository
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753963941/a904e576-de67-486a-807d-e09975f05a94.png align="center")
    
    scroll down and click on create repository
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698753999088/8a7424ca-1489-4694-a908-b283d4ccb3c5.png align="center")
    
    Congratulations you're repository has been created
    

### How to clone a repository locally?

To clone a repository on your local system. Go to the repository you want to clone to your system.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754223140/cb29e485-44f5-44fe-b46c-a0ed75177293.png align="center")

Copy the highlighted https link

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754280400/401dd3c5-32c7-456a-a78b-f9306e1fe031.png align="center")

Open your terminal, paste the link in it and click enter.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754347157/6caa7a58-3a41-4849-88a2-f53282820376.png align="center")

Note: if you click on add a readme.md file then you're repository won't be empty

Great now you have cloned your repository on your local system. Now let's move on to the next task.

### Make some changes to a file in the repository and commit them to the repository using Git

* Open the repo that you have cloned on your system in the terminal.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754579460/590b995c-6bc7-4140-936f-54d755f3869e.png align="center")
    
    currently, the repo is empty. Now let's add something to the repo. To demonstrate this I'm gonna add a script directory to the repo
    
* To make a directory and enter into that directory enter the code below
    

```bash
mkdir script && cd script
```

This will create a script directory and will take you inside the directory

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754737522/38c6328a-e6f8-4dcd-b2c8-7cd26af6af62.png align="center")

Now let's create a simple update script with Bash.

### How to create a simple update script with bash

In the directory open the terminal and enter the command vim directoryname.sh

```bash
vim update.sh

#enter the following in bash script

sudo apt update && sudo apt upgrade -y
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698754905282/08388751-312e-4ddd-8c27-1fb4d0e22123.png align="center")

Now we have made the changes in the repo, now let's push this changes to Git.

### How to push changes to Git?

1. Initialize Git with the git init command
    

```bash
git init
# enter this is the directory you want to push to git
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698755192770/0b6d9150-eea4-40ff-abb7-7fab2353ea24.png align="center")

1. After initializing Git use the git status command to check the status of Git in the repo.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698755268809/1b87ff90-67b7-4155-b747-f6ce500d8fe0.png align="center")

* git status shows the files which are yet to be pushed into the main repo
    

1. To push the remaining folders to the git use the git add command
    

```bash
git add *

# using * at the end will add everything to the stack to push to main repo
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698755395334/e26b7171-d652-4e8a-8de0-e63c6e7cff5f.png align="center")

you can see the status changes before and after using the git add command

1. Once the files turn green you can use the git commit command to commit the files to GitHub with the message
    

```bash
git commit -m "Enter your message here"
```

where -m represents the message that you can add when you commit the files to git.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698755575719/c626d268-4aeb-42fd-a658-5fd9a63692f1.png align="center")

type a simple message for the viewers to understand what you committed with files and what changes you have made

1. Once you have commit the files to the github then you can easily use the git push command to push your changes to the main repository.
    

* Connect git remotely to the terminal with the following command
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698755858129/d3e1d057-19fc-4e3b-b7bb-afd2a2940469.png align="center")
    
    you might face an error like this
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756285521/f7c473a5-f79a-4ea8-99f2-c8ee4114783e.png align="center")
    
    to solve the error do the following
    

### How to connect git remotely to your system?

* click on your profile and click on your settings
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756375159/8a98e577-57db-4549-9b7d-566b6121632b.png align="center")
    
    after that click on developer settings at the deep bottom.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756456894/8dd2754c-0d69-4842-bba1-51e916e3fde5.png align="center")
    
    click on the personal access token and then click on the Tokens (classic)
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756519456/0959e837-fccb-4d40-a22c-f8362b2d7468.png align="center")
    
    click on Generate a new token
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756567300/abe962a0-3eb4-4837-9743-95c6ccdc76f7.png align="center")
    
    Name the token and set the expiration to your preference
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698756677499/a3eb2a78-e777-4b83-bbb6-77cf2b119897.png align="center")
    
    check all the checkboxes so you can perform every task without any issues.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698757057145/386133a3-920c-4e15-8aab-70c35104e922.png align="center")
    

click on generate a token. make you sure you copy the code to some file safe because this code won't be visible after this.

now use the git push command and enter the token into the password

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698757512915/d6e010e1-cd8a-401c-85dd-bd181cf23565.png align="center")

Enter the token as a password and press enter

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698757561345/cec1f9ec-61a0-4aef-9286-faa6b6dc6c77.png align="center")

Now you are set with the local remote setup now you can use the push command directly and push the changes to the main repo

```bash
git push origin main
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698757637726/b88c251f-b74a-4d70-8dc0-7f38f7e3753e.png align="center")

and you're done. now everything is set and you've pushed your changes to the main branch directly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698757711825/ac3e71b0-ea1b-4adc-b2f3-d3b258c0ce2b.png align="center")

you can see the script folder has been added to the repo

congratulations you now know how to remotely connect GitHub to your local computer

### Summary

In summary, Git is a vital version control system that empowers developers to efficiently manage code changes, with aspects like version control, distributed collaboration, branching, and more. GitHub complements Git, providing a web-based platform for collaborative software project management.

Version control, which acts as a time machine for files, can be centralized or distributed. DVCS, like Git, offers benefits like working offline, speed, flexibility, security, and more.

Installing Git on Ubuntu is simple with the `apt` package manager. To use Git effectively:

1. Sign up on GitHub.
    
2. Create a GitHub repository.
    
3. Clone the repository to your local system.
    
4. Make changes and commit them to Git.
    
5. Push the changes back to GitHub.
    
6. Configure Git and secure the connection with a personal access token.
    

This guide helps you understand Git, GitHub, version control, and how to perform essential tasks in a straightforward and practical manner.