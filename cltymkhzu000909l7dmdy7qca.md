---
title: "Day 9: Git & GitHub Mastery: Navigating the Depths for DevOps Engineers"
seoTitle: "Git & GitHub Mastery: Navigating the Depths for DevOps Engineers"
seoDescription: "Dive into Git & GitHub for DevOps. Master version control, collaboration, and automation. Boost productivity today"
datePublished: Tue Mar 19 2024 17:04:51 GMT+0000 (Coordinated Universal Time)
cuid: cltymkhzu000909l7dmdy7qca
slug: day-9-git-github-mastery-navigating-the-depths-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1710867732275/3e0cd041-eeca-4f51-abb5-fd67d0b45085.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1710867830487/afd955f6-a7ba-4553-941e-b118cea7d8a0.png
tags: docker, github, python, web-development, git, developer, devops, hashnode, jenkins, devops-articles, devops-journey, 90daysofdevops, wemakedevs, trainwithshubham

---

## What is Git and why it is Important?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867591141/6e8ead48-e386-4855-bef5-3c120e6f23ba.png align="center")

Git is a tool that helps people work together on projects, especially when they're writing code for software. Think of it like a super organized and smart version of Google Docs, but for programming.

Here's why Git is important:

1. **Version Control**: Git keeps track of all the changes you make to your project. This means if something goes wrong, you can always go back to an earlier version, like a time machine for your code. No more worrying about accidentally deleting something important!
    
2. **Collaboration**: Git allows multiple people to work on the same project at the same time. It helps you avoid conflicts when two people try to change the same part of the project. You can work on your part without interfering with others, and then easily combine everyone's work together.
    
3. **Backup**: Git acts as a backup system for your project. Instead of relying on one person's computer to store everything, Git stores copies of your project on multiple computers, making sure your hard work is safe even if your computer crashes.
    
4. **Branching**: Git lets you experiment with new ideas without messing up the main project. You can create a "branch," which is like a separate copy of your project, try out new things, and then merge your changes back into the main project when you're ready.
    

## Difference between Main branch and Master Branch

1. **Master Branch**: In the past, "master" was the default name for the main branch in Git. It's like the trunk of a tree, where all the main work happens. When you start a project, you usually begin with the master branch. It holds the most stable and polished version of your project.
    
2. **Main Branch**: Over time, some people realized that the term "master" might have negative connotations, so they started using "main" instead. The main branch serves the same purpose as the master branch—it's where all the important and finalized changes are stored.
    

So, in essence, both "main" and "master" branches serve as the primary branch in your project, where the most up-to-date and stable version of your work resides. They're just named differently, but their function remains the same

## Difference between Git and Github

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867555715/75cd0c2b-be3e-49a0-8eea-e78ce538c45f.png align="center")

1. **Git**: Git is like the tool you use to track changes in your project. It's like having a magic notebook where you write down every change you make to your project. This helps you keep track of what you've done, go back to previous versions if needed, and work with others without messing things up.
    
2. **GitHub**: GitHub is like a big online community center for Git projects. It's a website where you can store your Git projects and collaborate with others. Imagine it as a huge library where people can share their notebooks (Git projects) and work on them together. You can see other people's projects, contribute to them, or even start your own.
    

In short, Git is the tool you use on your computer to manage your project, while GitHub is the online platform where you can store and share your Git projects with others.

## What is difference between local and remote repository? How to connect local to remote?

1. **Local Repository**: Think of this as your personal workspace on your computer. It's like your desk where you do all your work. The local repository stores all the files and changes you make to your project on your own computer.
    
2. **Remote Repository**: This is like a backup or a shared space where you can store your project online. It's like having a copy of your work stored on the internet. Remote repositories, such as those on platforms like GitHub or GitLab, allow you to collaborate with others and keep your project safe.
    

To connect your local repository to a remote one:

1. **Set Up Remote Repository**: First, you need to have a remote repository set up on a platform like GitHub. It's like renting a storage space online for your project.
    
2. **Link Local to Remote**: You tell Git where your remote repository is located by adding a link to it. This is done using a command like `git remote add origin <remote_repository_URL>`. This command tells Git that your remote repository is called "origin" (a common name for the default remote repository) and specifies its URL.
    
3. **Push Changes**: Once you've linked your local repository to the remote one, you can push your changes from your local repository to the remote repository using `git push`. It's like sending your updated files to your online storage space so others can see and work with them.
    

## Tasks

### How to setup username and email address

Setting up your username and email address in Git is important because it associates your commits (changes) with your identity. Here's how you can do it:

1. **Open Git Bash (Windows) or Terminal (Mac/Linux)**: This is where you'll enter the commands.
    
2. **Type the Following Commands, Replacing the Placeholder Text**:
    
    * For setting up your username:
        
        ```bash
        git config --global user.name "Your Name"
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710865491319/0e19dd72-720e-457c-ace8-60c2a7e7f194.png align="center")
        
        Replace `"Your Name"` with your actual name.
        
    * For setting up your email address:
        
        ```bash
        git config --global user.email "your_email@example.com"
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710865524330/98a70602-45c8-4475-9854-02071fe71b08.png align="center")
        
        Replace `"`[`your_email@example.com`](mailto:your_email@example.com)`"` with your actual email address.
        
3. **Verify Your Configuration**: You can check if your username and email are correctly set up by using the following commands:
    
    * To check your username:
        
        ```bash
        git config --global user.name
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710865432885/f7a7ea17-b71a-4206-b1cf-b3f0df555082.png align="center")
        
    * To check your email:
        
        ```bash
        git config --global user.email
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710865455433/13811115-e45a-4973-9fc6-f776a5a03782.png align="center")
        

That's it! You've now set up your username and email address in Git. These details will be associated with your commits when you make changes to your projects.

### Create a repository named Devops on Github

Creating a repository named "Devops" on GitHub is like making a new folder for your project on the GitHub website. Here's how you can do it:

1. **Go to GitHub**: Open your web browser and go to [GitHub.com](http://GitHub.com).
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866085107/1a035926-51b7-4944-a2c8-7380ffc849e2.png align="center")
    
2. **Sign In or Sign Up**: If you don't have an account, you'll need to sign up. If you have one, sign in.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866112892/b51f92c7-ed54-42ed-883b-4de0c1ca4fd0.png align="center")
    
3. **Click on the "New" Icon**: At the top right corner of the page, you'll see a "New" icon. Click on it.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866152597/be5c5892-5341-4354-b7d7-23966c53a9b8.png align="center")
    
4. **Name Your Repository**: In the "Repository name" field, type "Devops."
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866225820/9c4f8293-34bc-4c2f-9470-fa375069767a.png align="center")
    
5. **Optional: Add Description**: You can add a description if you want, to briefly explain what your project is about.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866256767/ac929482-991b-4168-91a9-5dcfef46609b.png align="center")
    
6. **Choose Visibility**: You can choose whether you want your repository to be public (visible to everyone) or private (visible only to you and the people you give access to). For simplicity, you can keep it public.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866275917/c12da810-b102-4d12-bf1e-8a3bbf87be14.png align="center")
    
7. **Initialize with a README**: Check the box that says "Initialize this repository with a README." This will create a README file in your repository, which is like the first page of your project where you can write information about it.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866294032/44a10b9a-3da0-4491-860a-a4ffcdef62b5.png align="center")
    
8. **Click "Create repository"**: Once you've filled in the necessary details, click the green button that says "Create repository."
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866311080/64e641a1-bc6a-4397-a288-0e6e7adc6856.png align="center")
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866339539/cfc31046-4af8-4e97-829c-7b5e11749ee7.png align="center")

That's it! You've now created a repository named "Devops" on GitHub. You can now start adding files, writing code, and collaborating with others on your project.

### Connect your local repository to the repository on Github

To connect your local repository to the repository on GitHub, you need to follow these steps:

1. **Copy the Repository URL from GitHub**:
    
    * Go to your repository on GitHub (in this case, "Devops").
        
    * Click the green "Code" button.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866825661/ab62d32b-45d4-4d47-af7f-22bf88ee2462.png align="center")
        
    * Copy the URL provided. It should look something like: [`https://github.com/your-username/Devops.git`](https://github.com/your-username/Devops.git).
        
2. **Open Terminal or Command Prompt**:
    
    * Navigate to the directory where your local repository is located. You can use the `cd` command to change directories.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866888980/6d0b300b-935a-4b29-92f3-7b9f98271d26.png align="center")
        
3. **Initialize Git (If Not Already Done)**:
    
    * If your local directory isn't a Git repository yet, you'll need to initialize it. You can do this with the command: `git init`.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866915047/7dcafcbf-d3ed-42e1-869b-eb5d6ab940eb.png align="center")
        
4. **Link Your Local Repository to GitHub**:
    
    * Use the following command to add a remote named "origin" (though you can name it anything you like) and provide the GitHub repository URL you copied earlier:
        
        ```bash
        git remote add origin https://github.com/your-username/Devops.git
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866965824/db73c35b-736f-478a-9f26-ab536f97a835.png align="center")
        
    * Replace [`https://github.com/your-username/Devops.git`](https://github.com/your-username/Devops.git) with the URL you copied from GitHub.
        
5. **Verify the Connection**:
    
    * To ensure that your local repository is now connected to the GitHub repository, you can run the command:
        
        ```bash
        git remote -v
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710866989786/0b5c1e2d-ab92-4a08-be48-60c199308fee.png align="center")
        
    * This command will list the remote URLs associated with your repository.
        
6. **Push Your Changes to GitHub**:
    
    * After connecting your local repository to GitHub, you can push your changes to the GitHub repository using the command:
        
        ```bash
        git push -u origin master
        ```
        
    * This command pushes your local changes to the "master" branch of the remote repository named "origin". If your main branch is named differently (e.g., "main"), replace "master" with the appropriate branch name.
        

That's it! Your local repository is now connected to the repository on GitHub, and you can start syncing changes between them.

### Create a new file in Devops/Git/Day-02.txt & add some content to it

To create a new file named "Day-02.txt" in the "Devops/Git" directory and add some content to it, you can follow these steps:

1. **Navigate to Your Local Repository Directory**: Open your Terminal or Command Prompt and navigate to the directory where your local repository ("Devops") is located.
    
2. **Create the Directory and File**: If the "Git" directory doesn't exist yet, create it using the following command:
    
    ```bash
    mkdir -p Devops/Git
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867057858/f4aeba1c-8906-48e3-8975-92ea64975a41.png align="center")
    
    This command creates the "Git" directory inside the "Devops" directory. If the "Git" directory already exists, you can skip this step.
    
3. **Navigate to the "Git" Directory**:
    
    ```bash
    cd Devops/Git
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867078405/5d1d4543-f25b-4385-ba0a-d51c61cbd5b8.png align="center")
    
4. **Create the New File**: Use your preferred text editor to create the "Day-02.txt" file and add some content. If you're using command-line editors like Vim or Nano, you can create and open the file with:
    
    ```bash
    nano Day-02.txt
    ```
    
    This will open the Nano text editor. Enter your desired content in the file.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867111925/273b7bd8-8d4f-4405-81fe-75776d7fadb6.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867149925/a092bf11-41ab-419a-8bd5-c112bfdc31fd.png align="center")
    
5. **Save and Exit the Editor**: After adding your content, save the changes and exit the editor. For Nano, you can do this by pressing `Ctrl` + `X`, then confirming to save the changes.
    
6. **Check Git Status**:
    
    ```bash
    git status
    ```
    
    This command will show you the status of your repository and indicate that there are untracked files.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867204324/4f174ef6-6b18-46bf-8fa1-411a74c43896.png align="center")
    
7. **Add the New File to Git**:
    
    ```bash
    git add Day-02.txt
    ```
    
    This command stages the new file for commit.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867244604/0800db79-4cec-49d4-b048-c6b381d804d0.png align="center")
    
8. **Commit the Changes**:
    
    ```bash
    git commit -m "Add Day-02.txt with some content"
    ```
    
    This command commits the changes you've made with a brief message describing what you did.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867277709/23d87251-95e4-4dc0-9af5-748f5dbbaf11.png align="center")
    
9. **Push the Changes to GitHub**:
    
    ```bash
    git push origin master
    ```
    
    This command pushes your committed changes to the remote repository on GitHub.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867325031/36d9cf10-c148-43e6-b58a-f688e6f79d0d.png align="center")
    

That's it! You've created a new file named "Day-02.txt" in the "Devops/Git" directory, added some content to it, and pushed the changes to GitHub.

### Push your local commits to the repository on Github

To push your local commits to the repository on GitHub, you can follow these steps:

1. **Navigate to Your Local Repository Directory**: Open your Terminal or Command Prompt and navigate to the directory where your local repository ("Devops") is located.
    
2. **Check Git Status (Optional)**: It's good practice to check the status of your repository before pushing any changes to ensure everything is in order. You can do this with:
    
    ```bash
    git status
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867357336/cc4884ac-51f5-45f3-85af-f161dd40b6fb.png align="center")
    
3. **Add Any Untracked Files (Optional)**: If you have any untracked files that you want to include in your commit, you need to add them to the staging area. You can do this with:
    
    ```bash
    git add .
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867377383/2d43f6fd-8ffe-4c92-aef2-ad706a27d1e2.png align="center")
    
    This command adds all untracked files to the staging area. Replace `.` with specific file names if you only want to add certain files.
    
4. **Commit Your Changes**:
    
    ```bash
    git commit -m "Your commit message here"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867405914/981d1c98-c1d7-49fb-9712-c692e544b960.png align="center")
    
    Replace `"Your commit message here"` with a brief description of the changes you're committing.
    
5. **Push Your Commits to GitHub**:
    
    ```bash
    git push origin master
    ```
    
    This command pushes your local commits to the remote repository on GitHub. If your main branch is named differently (e.g., "main"), replace "master" with the appropriate branch name.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710867450656/1df28fa8-1aed-4c79-95e9-c23282470b79.png align="center")
    
6. **Enter Your GitHub Credentials (If Prompted)**: If this is your first time pushing to the repository or if you haven't authenticated recently, Git may prompt you to enter your GitHub username and password.
    
7. **Wait for the Push to Complete**: Git will upload your commits to GitHub. Depending on the size of your changes and your internet connection speed, this may take a moment.
    
8. **Check GitHub**: After the push is complete, you can go to your GitHub repository in a web browser and verify that your changes have been successfully pushed.
    

That's it! Your local commits have been pushed to the repository on GitHub.

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )