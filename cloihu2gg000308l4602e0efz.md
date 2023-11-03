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

If you find my blog valuable, I invite you to like and share. Your feedback is precious as it fuels continuous improvement. Let's embark on this transformative DevOps adventure together!🚀🚀