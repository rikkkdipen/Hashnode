---
title: "Day 5: "Mastering Linux Scripting: Creating Directories and Backups with Bash""
seoTitle: "Mastering Linux Scripting: Creating Directories and Backups with Bash"
seoDescription: ""Unlock the power of Linux scripting with our step-by-step guide. Learn how to automate directory creation and backups using Bash scripts, making your ...."
datePublished: Sun Oct 29 2023 11:11:21 GMT+0000 (Coordinated Universal Time)
cuid: clobdexkq000509mj863s2imu
slug: day-5-mastering-linux-scripting-creating-directories-and-backups-with-bash
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698568167422/e1ef5804-d397-4106-8d63-c2706ee40c96.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698577754787/de6c1959-6632-421a-a30c-a16e69c10ad0.png
tags: linux, devops, 90daysofdevops, wemakedevs, trainwithshubham

---

In the ever-evolving landscape of DevOps and automation. scripting has become an indispensable tool for streamlining tasks, boosting productivity, and ensuring consistency. Among the many scripting languages available we focused on bash scripting for Linux. Till now we have covered the Basics of Bash with theory and some practicals.

Today let's cover the advance of shell scripting with some hands-on practicals.

For hands-on practicals, we will do some tasks with the bash script. Tasks which include:

* Creating multiple directories with the bash script
    
* Create a backup script of all the work done till now
    

Previously, we have seen that we can create directories in Linux with the mkdir command which was a very simple and easy way to do it

### 2 Ways to Create Multiple Directories in Linux

```bash
mkdir directory_name
```

This is the way we used to create directories before. But this way is not efficient when we want to create multiple directories to use

There is another command we can use to create multiple directories in Linux the command can be written as:

```bash
mkdir directory_name{start_num..end_num}
```

This is an efficient way but still not that efficient. who wants to write all this stuff when you can just automate the work of creating directories in the Linux Operating System

### Bash Script Automation

Bash script automation is like teaching your computer to do boring, repetitive tasks all by itself. It's like a super-smart assistant that follows your instructions. This means you can make your computer automatically do things like making copies of important stuff, keeping your computer healthy, and handling complicated data work. By using these automated scripts, people who manage computers can spend their time on more interesting and important jobs. It's like having a reliable helper that ensures things get done correctly, which is super helpful in the fast-paced world of technology.

### Bash Script to Create Multiple Directories

```bash
#!/bin/bash

# take the user input
echo "Enter the base name of the directory"
read name
echo "Enter the starting number"
read start
echo "Enter the ending number"
read end

# for loop for automation
for(( i=start; i<=end; i++ ))
do
{
mkdir $name$i
}
done

# print the message
echo "Directories has been created..."
```

with the above Bash script, you can easily automate the work of creating directories in Linux.

Now, let's see how this script works. To run this Bash script you have to give it executable permission.

### Why give executable permission to Bash Scripts?

When we create Bash scripts in Linux they come by default with just read and write permission. To make them executable as well, we have to use a certain command to them permission to become executable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698569940737/8cf73444-f2ce-44d8-96bb-6d7049f8e7c4.png align="center")

As you can see the in image above the mkdirectories.sh is in white color which means that it is not an executable file

### How to make the Bash Script executable?

making the bash script executable is simple you just have to use the chmod command and write the permission for the file.

```bash
chmod 777 mkdirectories.sh
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698570062106/016ca725-ad18-4db7-8cbc-1d5814de6b3b.png align="center")

Now you can see that after using the chmod command the color of the shell script has changed to a different color which means that the script can be executed now.

here, 777 has its significance too. We will learn that in the upcoming posts.

Now that you have made the script executable. you can run it easily with the shell or the terminal of your Linux Operating System.

To run the script you can use

```bash
./mkdirectories.sh
```

This will execute the script and ask you for the inputs.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698570240232/892809cd-c2ea-43a4-a3be-4e009c7ff298.png align="center")

You can see that the script has been executed. Now let's see if the script worked or not.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698570280850/b2907455-5046-4551-98f2-51d036875bd3.png align="center")

This Bash script is designed to create a series of directories with names based on user input. Let's break down the code step by step:

1. `# take the user input`: This is a comment indicating the purpose of the following code.
    
2. `echo "Enter the base name of the directory"`: This line displays a message asking the user to input the base name for the directories they want to create.
    
3. `read name`: The `read` command is used to capture the user's input and store it in a variable called `name`. This variable will be used as the base name for the directories.
    
4. `echo "Enter the starting number"`: This line asks the user to input the starting number for the series of directories.
    
5. `read start`: Similar to the previous step, the `read` command captures the user's input and stores it in a variable called `start`.
    
6. `echo "Enter the ending number"`: This line prompts the user to input the ending number for the series of directories.
    
7. `read end`: Again, the `read` command captures the user's input and stores it in a variable called `end`.
    
8. `# for loop for automation`: This comment explains the purpose of the upcoming for loop.
    
9. `for(( i=start; i<=end; i++ ))`: This is the beginning of a for loop that iterates from the `start` number to the `end` number. It will create directories with names based on the user's input.
    
10. `{`: The curly brace `{` denotes the start of a block of commands that will be executed for each iteration of the loop.
    
11. `mkdir $name$i`: This command creates a directory with a name composed of the base name (`$name`) and the current value of `i`. For example, if the user input "mydir" as the base name, and the loop is currently at `i=1`, it will create a directory named "mydir1."
    
12. `}`: The closing curly brace `}` marks the end of the block of commands executed for each iteration of the loop.
    
13. `done`: This signals the end of the for loop.
    
14. `echo "Directories have been created..."`: Finally, this line prints a message indicating that the directories have been successfully created.
    

In summary, this script takes user input for a base directory name, a starting number, and an ending number. It then uses a for loop to create a series of directories with names based on the user's input.

Now that we have completed the first task let's move to the other task which is to write a bash script to take a backup of the progress we have made till now.

### Why Taking Backup is Important in Linux

Linux backup is like making a copy of your important stuff on your computer. It's important because if something goes wrong, like your computer breaks or you accidentally delete something, you can get your stuff back from the copy. It's like a safety net for your computer so you don't lose your important things.

### Bash Script to take Backup

```bash
#!/bin/bash

# Backup Directory

Backup_dir="/home/sh/Desktop/Devops"

# where to backup

Backup="/home/sh/Desktop/Backup"

# date of the backup

date=$(date + "%d-%b-%y")
cp -r $Backup_dir $Backup/$date

echo "Backup created in $Backup/$date"
```

This Bash script is designed to create a backup of a directory. Let's break down the code step by step:

1. `#!/bin/bash`: This is called a shebang, and it indicates that the script should be interpreted by the Bash shell.
    
2. `Backup_dir="/home/sh/Desktop/Devops"`: This line defines the source directory that you want to back up. In this case, it's "/home/sh/Desktop/Devops."
    
3. `Backup="/home/sh/Desktop/Backup"`: This line specifies the destination directory where the backup will be stored. It's "/home/sh/Desktop/Backup" in this script.
    
4. `date=$(date + "%d-%b-%y")`: This line uses the `date` command to obtain the current date and store it in a variable called `date`. The format for the date is set to day-month-year, such as "29-Oct-23."
    
5. `cp -r $Backup_dir $Backup/$date`: This is the command that creates the backup. It uses the `cp` command with the `-r` flag to copy the contents of the source directory (`$Backup_dir`) to the destination directory (`$Backup`) and appends the current date to the destination path, creating a folder with the backup date.
    
6. `echo "Backup created in $Backup/$date"`: Finally, this line simply prints a message indicating where the backup was created, using the values of the variables for the source directory, destination directory, and the current date.
    

So, in summary, this script makes a backup of the "Devops" directory on the user's desktop and stores it in a "Backup" directory with the current date as a subfolder within "Backup."

### Summary

In the world of technology, Bash scripting is like having a smart assistant for your computer. It helps you automate repetitive tasks, making your work more efficient and error-free. We've started with the basics and now we're diving into more advanced scripting.

One cool thing we can do with Bash scripts is create a bunch of folders without clicking around. You just tell the script a few things, like what to name the folders and how many you want, and it does the work for you. This is super helpful, especially when you have a lot of folders to create.

Another important thing we've learned is how to take a backup. Think of it like making a copy of your important files, so if something bad happens, you can get them back. It's like a safety net for your computer.

In the end, Bash scripting and automation are like having a handy assistant who does tasks for you, making your work easier and more reliable in the fast-paced world of tech.