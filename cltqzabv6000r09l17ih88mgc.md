---
title: "Day 5: Advanced Linux Shell Scripting: DevOps Mastery with User Management"
seoTitle: "Advanced Linux Shell Scripting: DevOps Mastery with User Management"
seoDescription: "Unlock the power of Advanced Linux Shell Scripting! Elevate your DevOps skills with expert techniques in user management."
datePublished: Thu Mar 14 2024 08:38:42 GMT+0000 (Coordinated Universal Time)
cuid: cltqzabv6000r09l17ih88mgc
slug: day-5-advanced-linux-shell-scripting-devops-mastery-with-user-management
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1710392983161/35ea19c0-6e79-4440-a173-ab132c044108.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1710405415400/526fdbb2-c086-460f-8910-77e022cb3993.png
tags: linux, terminal, bash, devops, hashnode, terraform, linux-for-beginners, devops-articles, devops-journey, 90daysofdevops, wemakedevs, day5, trainwithshubham

---

## Introduction

Welcome to the world of Advanced Linux Shell Scripting and User Control! In this exciting journey, we'll delve into the depths of Linux command-line magic, empowering you to take control of your system like never before.

Shell scripting is like wielding a powerful wand in the world of Linux. With it, you can automate tasks, streamline processes, and unleash the full potential of your operating system. But we're not stopping at the basics. We're diving into the advanced realm, where complex tasks become simple and efficiency reigns supreme.

One of the key aspects we'll explore is user control. Managing users in Linux is crucial for system security, access control, and resource management. Whether you're a DevOps engineer, a system administrator, or an enthusiast looking to level up your skills, understanding advanced user management techniques will open doors to new possibilities.

## Tasks

### Write a bash script create directories.sh that when the script is executed with three given arguments to create directories

```bash
#!/bin/bash

# Check if three arguments are provided
if [ "$#" -ne 3 ]; then
    echo "Usage: $0 <directory_name> <start_number> <end_number>"
    exit 1
fi

# Assigning arguments to variables
directory_name=$1
start_number=$2
end_number=$3

# Loop through the range of directories
for ((i=start_number; i<=end_number; i++)); do
    # Creating the directory with dynamic name
    mkdir -p "${directory_name}${i}"
    echo "Directory ${directory_name}${i} created."
done

echo "Directories created successfully."
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710393443623/3f986b1b-e108-4ff4-ae78-9d51a36e4878.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710393462148/aad36ac8-1442-4af8-b5cd-b7ccba43c781.png align="center")

### Create a Script to backup all your work done till now

```bash
#!/bin/bash

# Define backup directory name with timestamp
backup_dir="/home/sh"
timestamp=$(date +"%Y%m%d_%H%M%S")

# Define backup destination
backup_dest="$backup_dir/backup_$timestamp"
mkdir -p "$backup_dest"

cp -R * "$backup_dest"

if [ $? -eq 0 ]; then

        echo "Backup Completed Successfully"
else
        echo "backup Failed"
fi
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710396583281/72914ba8-f0d5-4760-b2a2-c00e60994e15.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710396608176/f791860f-6fa6-4f24-973f-4b8da1dc09a9.png align="center")

### Read about cron and crontab to Automate Backup Script

cron is like a scheduling assistant for your computer. It's a tool used in Unix-like operating systems (such as Linux) to automate tasks at specific times or intervals.

Here's how it works:

1. **Setting a Schedule**: With cron, you can tell your computer to do something (like run a script or command) at a particular time, on a specific day, or at regular intervals (like every hour or every day).
    
2. **Using the crontab**: The schedule for these tasks is stored in a file called the "crontab" (short for "cron table"). Each user on the system can have their own crontab, which lists the tasks they want to run and when.
    
3. **Syntax**: In the crontab, you specify when you want a task to run using a specific syntax. This syntax includes fields for minutes, hours, days of the month, months, and days of the week. You also specify the command or script you want to run.
    
4. **Automation**: Once you set up a task in the crontab, cron takes care of the rest. It'll execute the specified command or script according to the schedule you've defined, without you needing to do anything manually.
    

In essence, cron is like having a personal assistant that remembers to do certain tasks for you at the times you specify, making it a handy tool for automating repetitive or scheduled tasks on your computer.

* **Commands for the Corntab are as follows:**
    

1. **crontab -e** = To select an editor and open corntabEdits a copy of the user's crontab file.
    
2. **crontab -l** \\= Lists the user's crontab file.
    
3. **crontab -r** = Removes the user's crontab file from the crontab directory.
    

### To automate backup script using crontab

Open Terminal and enter the command below

```bash
crontab -e
```

Enter the following in the bottom

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710397382438/390ae33b-6b3e-4e96-8b57-67fb695ecff0.png align="center")

replace 06 06 with \* \* to automate this backup for every minute and every hour.

### User Management in Linux

User management in Linux is the process of controlling who can access the system and what they can do once they're logged in. Here's a simple breakdown:

1. **User Accounts**: Each person who uses a Linux system has their own user account. This account includes a username and password, which they use to log in.
    
2. **User Groups**: Users can be organized into groups, which helps manage permissions more efficiently. For example, all users who need access to administrative tasks might be in the "sudo" group.
    
3. **Permissions**: Linux systems use permissions to determine what users and groups can do with files and directories. These permissions include read, write, and execute access for the owner of the file, the group associated with the file, and all other users.
    
4. **User Management Tools**: Linux provides various tools for managing users and groups. For example, the `useradd` command is used to add new users, `passwd` is used to change passwords, and `usermod` is used to modify user attributes.
    
5. **System Accounts**: Some user accounts are used by the system itself, rather than by individual users. These accounts typically have restricted permissions and are used to perform specific system tasks.
    

Overall, user management in Linux is about controlling access to the system, organizing users into groups, and setting permissions to ensure that users can only access the resources they need. It's a fundamental aspect of system administration and security on Linux systems.

### Create 2 users and just display their usernames

```bash
#To add new user
useradd username
#To check user configuration File
cat/etc/passwd
#To print all the user in linux
awk -F ':' '{print $1}' /etc/passwd
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710405160099/00bf438b-1e9c-4105-9143-9e7d49633560.png align="center")

## Summary

User management in Linux is about controlling who can use the computer and what they can do. Each person has their own account with a username and password. Accounts can be grouped together for easier management. You can set rules to determine who can access files and programs. There are tools to add, modify, and remove user accounts. It's important for keeping the system secure and organized.

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )