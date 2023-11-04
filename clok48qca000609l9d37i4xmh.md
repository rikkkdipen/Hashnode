---
title: "Day 11: Mastering Git and GitHub for DevOps Engineers: An Advanced Guide (Part 2)"
seoTitle: "Mastering Git and GitHub for DevOps Engineers: An Advanced Guide"
seoDescription: "Git stash is a command that allows developers to temporarily save changes that have not been committed to a branch..."
datePublished: Sat Nov 04 2023 14:04:31 GMT+0000 (Coordinated Universal Time)
cuid: clok48qca000609l9d37i4xmh
slug: day-11-mastering-git-and-github-for-devops-engineers-an-advanced-guide-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699106605122/7a78d5d5-d486-4976-a067-b47a28a3a032.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699106636969/3d315743-3887-4a66-834c-1646ef2f4aaa.png
tags: linux, github, git, devops, trainwithshubham

---

In part 1 we have covered with few concepts such as Git branching, Git revert, Git reset and many other concepts. Today let us see some more advanced concepts such as stash and resolving conflicts etc.

### What is Git Stash?

Git stash is a command that allows developers to temporarily save changes that have not been committed to a branch. It's particularly useful when you're working on a specific task but need to switch to another branch to address an urgent bug or tackle a different feature. Stashing your changes allows you to switch branches without committing to half-finished work.

To use Git stash, you first create a new branch and make some changes to it. Then you can use the command git stash to save those changes. This will remove the changes from your working directory and record them in a new stash. You can apply these changes later. git stash list command shows the list of stashed changes.

You can also use git stash drop to delete a stash and git stash clear to delete all the stashes.

### How to Use Git Stash:

Using Git stash is straightforward. Here's a step-by-step guide to get you started:

1. Make sure your current branch is clean (no uncommitted changes).
    
2. Use the command: `git stash` to save your current changes.
    
3. You can stash multiple times, creating a stack of stashes.
    
4. After stashing, your working directory is clean, and you can switch branches or perform other tasks.
    
5. To retrieve your stashed changes, use `git stash apply` followed by the stash reference (e.g., `git stash apply stash@{0}`).
    
6. Optionally, you can use `git stash pop` to retrieve the changes and remove the stash from the stack.
    

### Cherry-pick

Cherry-pick is a Git feature that allows you to choose and apply specific commits from one branch to another. This feature can be particularly useful when you need to pull in changes or fixes from another branch or repository without merging the entire branch.

### How to Cherry-Pick a Commit in GitHub:

Using cherry-pick in GitHub is straightforward. Here's a step-by-step guide:

1. First, ensure you are on the branch where you want to apply the cherry-picked commit.
    
2. Navigate to the repository on GitHub.
    
3. Locate the commit you want to cherry-pick and click on it to view the commit details.
    
4. Click on the "Copy SHA" button to copy the commit's unique identifier.
    
5. Return to your local repository and run the following command:
    

```bash
shellCopy codegit cherry-pick <commit-SHA>
```

Replace `<commit-SHA>` with the SHA-1 hash of the commit you copied.

1. Git will attempt to apply the changes from the selected commit to your current branch. If there are any conflicts, you'll need to resolve them manually.
    
2. After resolving conflicts, commit the changes.
    
3. Finally, push the updated branch to your remote repository on GitHub.
    

### Resolving Conflicts

Conflicts can occur when you merge or rebase branches that have diverged, and you need to manually resolve the conflicts before git can proceed with the merge/rebase. git status command shows the files that have conflicts, git diff command shows the difference between the conflicting versions and git add command is used to add the resolved files.

### Task 1

* Create a new branch and make some changes to it.
    
    ```bash
      git checkout -b feature
      git branch
      vim version01.txt
      git add .
    ```
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699105381945/2a1c3c5e-5685-453f-aa44-d26dd1c72ac1.png align="center")
    
* Use git stash to save the changes without committing them.
    
    ```bash
      git stash
      git status
    ```
    
* Switch to a different branch, make some changes and commit them.
    
    ```bash
      git checkout -b development
      vim version01.txt
      git add .
      git commit -m "New version file commited"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699105472552/cd6af205-c863-42d3-903a-52ec34ea0a35.png align="left")
    
* Use git stash pop to bring the changes back and apply them on top of the new commits.
    
    ```bash
      git stash list
      git stash pop
      git add .
      git commit -m "git stash file commited"
      git log --oneline
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699105573554/8d43445e-57e4-43e6-aef6-5db7d2eab979.png align="left")
    

# 🔶 Task-02

* In version01.txt of the development branch add the below lines after “This is the bug fix in the development branch” that you added in Day10 and reverted to this commit.
    
    ```bash
      git checkout dev
      vim version01.txt
      cat version01.txt
      git add version01.txt
      git commit -m "New commited file on dev"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699105693732/5845c5fc-d260-47a1-aa31-f3548ffe08ef.png align="left")
    
* Line2&gt;&gt; After bug fixing, this is the new feature with minor alterations”
    
    Commit this with the message “ Added feature2.1 in development branch”
    
    ```bash
      vim version01.txt
      git add version01.txt
      git commit -m "Added feature 2.1 in development branch"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699105945964/0c9aab65-304a-41f7-a793-3444a343699d.png align="left")
    
* Line3&gt;&gt; This is the advancement of the previous feature
    
    Commit this with the message “ Added feature2.2 in development branch”
    
    ```bash
      vim version01.txt
      git add version01.txt
      git commit -m "Added feature 2.2 in development branch"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699106024022/4ce516c4-c092-495a-b7fc-9c4311d83592.png align="left")
    
* Line4&gt;&gt; Feature 2 is completed and ready for release
    
    Commit this with the message “ Feature2 completed”
    
    ```bash
      vim version01.txt
      git add version01.txt
      git commit -m "Feature2 completed"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699106140331/e8183af5-6181-49e6-83ad-610bb675be6a.png align="left")
    
* All these commit messages should be reflected in the Production branch too which will come out from the Master branch (Hint: try rebase).
    
    ```bash
      git checkout -b prod
      git rebase dev
      git log --oneline
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699106276973/775f270b-8af2-404f-bb24-73e218e387bf.png align="left")
    

# 🔶 Task-03

* In the Production branch Cherry picked Commit “Added feature2.2 in development branch” and added the below lines in it.
    
    ```bash
      git cherry-pick fad8512
    ```
    
* The line to be added after Line3&gt;&gt; This is the advancement of the previous feature
    
    ```bash
      vim version01.txt "This is the advancement of previous feature"
      git add version01.txt
      git commit -m "Advancement feature"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699106427006/eb91d9b2-37a0-4537-9c02-5339c6796d98.png align="left")
    
* Line 4&gt;&gt;Added a few more changes to make it more optimized.
    
* Commit: Optimized the feature
    
    ```bash
      vim version01.txt "Added few more changes to make it more optimized"
      git add version01.txt
      git commit -m "Optimized the Feature"
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699106487097/636ebc91-85fa-49e6-997f-44901feca408.png align="left")
    

Stay in the loop with my latest insights and articles on cloud ☁️ and DevOps ♾️ by following me on Hashnode, LinkedIn ([https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)), and GitHub ([https://github.com/dipen006](https://github.com/dipen006)).

Thank you for reading! Your support means the world to me. Let's keep learning, growing, and making a positive impact in the tech world together.