---
title: "Day 12: Git & GitHub Cheatsheet"
seoTitle: "Git and Github Cheatsheet"
datePublished: Mon Apr 01 2024 09:22:17 GMT+0000 (Coordinated Universal Time)
cuid: clugqrpna000508kydz2ugjnq
slug: day-12-git-github-cheatsheet
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1711963133765/a4386dee-1790-4138-94f6-94f833ef913a.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1711963311849/4a24ce9d-2b68-4907-a504-e9694b792231.png
tags: linux, github, web-development, git, developer, devops, cheatsheet, linux-for-beginners, devops-articles, 90daysofdevops, wemakedevs, trainwithshubham

---

**Git Basics:**

1. **Initialize a Repository:**
    
    ```bash
    git init
    ```
    
2. **Clone a Repository:**
    
    ```bash
    git clone <repository-url>
    ```
    
3. **Check Status:**
    
    ```bash
    git status
    ```
    
4. **Stage Changes:**
    
    ```bash
    git add <file>
    git add .       # Stage all changes
    ```
    
5. **Commit Changes:**
    
    ```bash
    git commit -m "Commit message"
    ```
    
6. **View Commit History:**
    
    ```bash
    git log
    ```
    
7. **Create a New Branch:**
    
    ```bash
    git branch <branch-name>
    ```
    
8. **Switch Branches:**
    
    ```bash
    git checkout <branch-name>
    ```
    
9. **Merge Branches:**
    
    ```bash
    git merge <branch-name>
    ```
    
10. **Undo Changes (Unstaged):**
    
    ```bash
    git checkout -- <file>
    ```
    
11. **Undo Changes (Staged):**
    
    ```bash
    git reset HEAD <file>
    ```
    
12. **Undo Last Commit (Keep Changes):**
    
    ```bash
    git reset --soft HEAD~1
    ```
    
13. **Undo Last Commit (Discard Changes):**
    
    ```bash
    git reset --hard HEAD~1
    ```
    

**GitHub Basics:**

1. **Push Changes to Remote Repository:**
    
    ```bash
    git push origin <branch-name>
    ```
    
2. **Pull Changes from Remote Repository:**
    
    ```bash
    git pull origin <branch-name>
    ```
    
3. **Add Remote Repository:**
    
    ```bash
    git remote add origin <repository-url>
    ```
    
4. **View Remote Repositories:**
    
    ```bash
    git remote -v
    ```
    
5. **Create Pull Request:**
    
    1. Push changes to GitHub.
        
    2. Go to the repository on GitHub.
        
    3. Click on "Pull Requests".
        
    4. Click on "New Pull Request".
        
    5. Select the branches to compare.
        
6. **Merge Pull Request:**
    
    1. Go to the Pull Request on GitHub.
        
    2. Review changes.
        
    3. Click on "Merge Pull Request".
        
    4. Confirm merge.
        
7. **Fetch Changes from Remote:**
    
    ```bash
    git fetch origin
    ```
    
8. **View Branches:**
    
    ```bash
    git branch -a
    ```
    
9. **Remove Remote Repository:**
    
    ```bash
    git remote remove <repository-name>
    ```
    
10. **Sync Forked Repository:**
    
    1. Add upstream repository:
        
        ```bash
        git remote add upstream <upstream-repo-url>
        ```
        
    2. Fetch changes:
        
        ```bash
        git fetch upstream
        ```
        
    3. Merge changes into local branch:
        
        ```bash
        git merge upstream/<branch-name>
        ```
        
11. **Create and Apply Gitignore:**
    
    1. Create `.gitignore` file in root directory.
        
    2. Add files or patterns to ignore.
        
    3. Save changes and commit.
        
12. **View Gitignore Status:**
    
    ```bash
    git status --ignored
    ```
    

**Advanced Git:**

1. **Rebase Branch:**
    
    ```bash
    git rebase <base-branch>
    ```
    
2. **Interactive Rebase:**
    
    ```bash
    git rebase -i <base-branch>
    ```
    
3. **Cherry-Pick a Commit:**
    
    ```bash
    git cherry-pick <commit-hash>
    ```
    
4. **Stash Changes:**
    
    ```bash
    git stash
    ```
    
5. **Apply Stashed Changes:**
    
    ```bash
    git stash apply
    ```
    
6. **View Stash List:**
    
    ```bash
    git stash list
    ```
    
7. **Drop Specific Stash:**
    
    ```bash
    git stash drop <stash-index>
    ```
    
8. **Clean Untracked Files:**
    
    ```bash
    git clean -fd
    ```
    
9. **View Differences Between Branches:**
    
    ```bash
    git diff <source-branch> <target-branch>
    ```
    
10. **Resolve Merge Conflicts:**
    
    1. Open the conflicted file.
        
    2. Manually resolve conflicts.
        
    3. Add resolved files.
        
    4. Commit changes.
        

This cheat sheet covers essential Git and GitHub commands for beginners and more advanced users. Use it as a quick reference guide to streamline your workflow and collaboration processes.

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )