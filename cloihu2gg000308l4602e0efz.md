---
title: "Day 10: Mastering Git and GitHub for DevOps Engineers: An Advanced Guide (Part 1)"
seoTitle: "Mastering Git and GitHub for DevOps Engineers: An Advanced Guide (Part"
seoDescription: "GitHub is the main focus for many big companies and open-source project maintainers and contributors to showcase their contributions. Many people think..."
datePublished: Fri Nov 03 2023 10:49:29 GMT+0000 (Coordinated Universal Time)
cuid: cloihu2gg000308l4602e0efz
slug: day-10-mastering-git-and-github-for-devops-engineers-an-advanced-guide-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699008511264/b5ae2a2c-3b9a-4c84-a2a9-98a4e6205714.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699008536095/5ba83092-414e-4445-aa25-936fac065ec9.png
tags: linux, github, devops, wemakedevs, trainwithshubham

---

GitHub is the main focus for many big companies and open-source project maintainers and contributors to showcase their contributions. Many people think Github is more of pulling requests and merging codes.

But that's not the case Github is more advanced than many people think. Today let's learn about a few more advanced concepts of GitHub such as

* Branching
    
* Revert & Reset
    
* Rebase & Merge
    

### What is Git Branching?

Think of Git as a tool that helps you keep track of changes in your code, like a time machine for your code. Branching is like creating a separate copy of your code that you can work on without affecting the original or main code.

Here's how it works:

1. **Main Branch (Master/Branch):** This is your main code, the one that's already working and stable. It's like the main story in a book.
    
2. **Creating a Branch:** When you want to work on a new feature, bug fix, or experiment with your code, you create a new branch. It's like writing a side story in the book, separate from the main story.
    
3. **Working in Your Branch:** You make changes in your branch, like adding new features or fixing a bug. These changes won't affect the main code because you're in your own branch.
    
4. **Switching Branches:** You can switch back and forth between the main branch and your branch, just like reading different parts of the book.
    
5. **Merging:** When you're happy with the changes you made in your branch and want to include them in the main code, you merge your branch back into the main branch. It's like adding your side story to the main story in the book.
    
6. **Conflict Resolution:** Sometimes, when merging, there might be conflicts if both the main branch and your branch have changed the same part of the code. You need to resolve these conflicts, just like editing a book to make sure everything flows smoothly.
    
7. **Deleting Branch:** After merging, you can delete your branch because it served its purpose, and its changes are now part of the main code. It's like removing the side story from the book since it's now part of the main story.
    

So, Git branching is like having multiple storylines in a book (your code) without messing up the main storyline. It helps you experiment and work on different things separately, and when they're ready, you can combine them into one cohesive story.

### What is Git Revert & Reset?

1. **Git Revert**:
    
    * Imagine you're working on a project and you make a mistake by committing some changes that you want to undo.
        
    * Git revert is like using an eraser on your changes. It creates a new commit that undoes the changes from a previous commit, but it doesn't remove the commit itself.
        
    * It's like saying, "I made a mistake, and I want to go back in time to fix it by creating a new change that cancels out the old one."
        
    * Other people working on the project won't be disrupted because the old commits still exist.
        
2. **Git Reset**:
    
    * Suppose you realize you made a mistake, and you want to completely remove a commit from the project's history.
        
    * Git reset is like a time machine that lets you go back and rewrite history. It erases commits and moves your branch pointer to a different point in the project's history.
        
    * It's like saying, "I want to pretend this mistake never happened, and I'm going to change the project's history to make it look like that."
        
    * Be careful with Git reset because it can disrupt collaboration if other people are also working on the project.
        

In simple language, Git revert is a way to undo a commit by creating a new one that cancels out the changes, while Git reset is a more powerful tool that lets you change the project's history by removing commits. Use Git revert for safer and collaborative undoing, and use Git reset with caution when you want to rewrite history.

### What is Git merge and rebase?

Git rebase and merge are two different ways to integrate changes from one branch into another in Git. Let me explain them in simple terms:

1. **Merge**:
    
    * Imagine you have a main road (main branch) and a side road (feature branch) that split from it.
        
    * When you want to bring the changes from the side road back onto the main road, you create a "merge." It's like adding a new lane to the main road that incorporates all the changes from the side road.
        
    * The side road still exists separately after the merge. It's like the side road is still there, but changes have been added to the main road.
        
    
    **Key Point**: Merge keeps a clear history of both the main and feature branches but adds a merge commit to the history.
    
2. **Rebase**:
    
    * Instead of adding a new lane (like in merge), think of rebase as picking up your entire side road and placing it on top of the main road.
        
    * This makes it look like all the changes from the side road were made directly on the main road one after the other, without any additional merge commits.
        
    * The side road effectively disappears after a successful rebase; its changes are now part of the main road.
        
    
    **Key Point**: Rebase creates a cleaner and linear history by "replaying" the changes on top of the main branch, but it can make the history less clear if used inappropriately.
    

In summary, merge preserves the history of both branches with a merge commit, while rebase creates a linear history by incorporating the changes from the feature branch onto the main branch as if they were made in sequence. The choice between them depends on your project's needs and your preference for how you want the history to look.

### Tasks

Add a text file called version01.txt inside the Devops/Git/ with “This is the first feature of our application” written inside. This should be in a branch coming from `master`, \[hint try `git checkout -b dev`\], switch to the `dev` branch ( Make sure your commit message will reflect as "Added new feature"). \[Hint use your knowledge of creating branches and Git commit command\]

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699089902015/81ecf106-4180-4b81-88c2-1fd5b5915029.png align="center")

A committed message with "Added new feature".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699089983494/795705d6-1c0b-4dc6-b15e-36842ecea33e.png align="center")

version01.txt should reflect at the local repo first followed by the Remote repo for review. \[Hint use your knowledge of Git push and Git pull commands here\]

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090056501/1febaf4e-8b25-4098-ad10-636cc2c41e94.png align="center")

Add a new commit in `dev` branch after adding the below-mentioned content in Devops/Git/version01.txt: While writing the file make sure you write these lines

* 1st line&gt;&gt; This is the bug fix in the development branch
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090141217/06ec29b0-86f1-474a-8700-0eedc7f1dedc.png align="center")

* Commit this with the message “ Added feature2 in development branch”
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090198688/d7e8de32-b283-4f20-8fb7-7b35195b3e18.png align="center")

* 2nd line&gt;&gt; This is gadbad code
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090257802/2aaad4b2-c55e-4d08-806f-52903dba1d75.png align="center")

* Commit this with the message “Added feature3 in the development branch"
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090348445/fffc2d7e-566d-4ab3-a9c9-fe81a4e36c79.png align="center")

* 3rd line&gt;&gt; This feature will gadbad everything from now.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090410767/cae8e2a6-9fa5-4e76-a5ce-348c176f4663.png align="center")

* Commit with the message “ Added feature4 in the development branch
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090455891/f42f9836-4440-4a6b-9063-d931fa49deb9.png align="center")

Restore the file to a previous version where the content should be “This is the bug fix in the development branch” \[Hint use git revert or reset according to your knowledge\]

use the git log to check the hash

```bash
git log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699090635966/671619f0-3e5c-4e87-ad3a-f57cd4ca07d1.png align="center")

use the git revert to return the to previous commit which you want

```bash
git revert #hash
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699091405188/25dd7ec0-238d-4b29-94e7-d56b6ba7d4d4.png align="center")

## **Task 2:**

* Demonstrate the concept of branches with 2 or more branches with a screenshot.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699091514671/d8014a35-446d-40f2-899f-dced25a06628.png align="center")

* add some changes to `dev` branch and merge that branch in `master`
    

I used the command before but forgot the screenshot that is why it'll show already up to date

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699091599617/39ff33c1-3eea-42a1-b63c-a85f98b4b087.png align="center")

Stay in the loop with my latest insights and articles on cloud ☁️ and DevOps ♾️ by following me on Hashnode, LinkedIn ([https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)), and GitHub ([https://github.com/dipen006](https://github.com/dipen006)).

If you find my blog valuable, I invite you to like and share. Your feedback is precious as it fuels continuous improvement. Let's embark on this transformative DevOps adventure together!🚀🚀