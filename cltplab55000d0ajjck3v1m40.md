---
title: "Day 4: Mastering Linux Shell Scripting: Essential Skills for DevOps Success"
seoTitle: "Mastering Linux Shell Scripting: Essential Skills for DevOps Success"
seoDescription: ""Unlock the power of Linux Shell Scripting with our comprehensive guide. Master essential skills tailored for DevOps success."
datePublished: Wed Mar 13 2024 09:19:01 GMT+0000 (Coordinated Universal Time)
cuid: cltplab55000d0ajjck3v1m40
slug: day-4-mastering-linux-shell-scripting-essential-skills-for-devops-success
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1710317165544/6bf152bd-0bde-423f-8ff9-9c4cdb7014f3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1710321403241/9de11a3a-3fdf-445b-a6ad-9e73e575e40d.png
tags: linux, github, bash, shell, hashnode, scripting, linux-for-beginners, 90daysofdevops, wemakedevs, trainwithshubham

---

### Introduction

Welcome to the world of Linux Shell Scripting! As a DevOps engineer, you're about to embark on a journey that will empower you to automate tasks, streamline processes, and enhance efficiency in your operations.

Linux Shell Scripting is a fundamental skill in the toolkit of any DevOps professional. At its core, it involves writing scripts using the command-line interface (CLI) of Linux operating systems. These scripts enable you to automate repetitive tasks, manage system configurations, and interact with various components of your infrastructure programmatically.

Whether you're provisioning servers, configuring applications, or orchestrating complex workflows, mastering Linux Shell Scripting will significantly boost your productivity and effectiveness as a DevOps engineer.

### What is Kernel?

Imagine your computer as a city. In this city, the kernel is like the mayor. It's the core part of the operating system, which is the software that manages everything on your computer.

The kernel acts as a bridge between the hardware (like your computer's processor, memory, and devices) and the software (like the programs you use). It handles tasks such as managing memory, handling input and output from devices like keyboards and screens, and coordinating between different programs that are running.

Just like a mayor keeps the city running smoothly by making decisions and managing resources, the kernel keeps your computer running smoothly by making sure everything works together efficiently. Without the kernel, your computer wouldn't be able to function properly.

### What is Shell?

Think of your computer as a house. The shell is like the front door. It's the interface that lets you communicate with the operating system—the software that runs your computer.

When you open the front door (the shell), you can talk to your computer by typing commands. These commands tell the computer what to do, like opening a program, copying files, or checking the weather.

Just like your front door lets you access your house, the shell lets you access and control your computer. It's your gateway to getting things done!

In technical language A shell is special user program which provide an interface to user to use operating system services. Shell accept human readable commands from user and convert them into something which kernel can understand. It is a command language interpreter that execute commands read from input devices such as keyboards or from files. The shell gets started when the user logs in or start the terminal.

### What is Linux Shell Scripting?

Imagine you have a bunch of tasks you do on your computer every day, like organizing files, running programs, or setting up your system. Linux Shell scripting is like creating a set of instructions for your computer to follow automatically.

Here's how it works:

1. **Writing Instructions**: You write these instructions using commands in a special language called a "script." It's a bit like writing a recipe for your computer.
    
2. **Automation**: Once you've written your script, you can run it whenever you want your computer to perform those tasks. It's like pressing a button and watching your computer do all the work for you.
    
3. **Efficiency and Consistency**: By using shell scripting, you can save time and ensure that tasks are done consistently every time you run the script. No more repeating the same steps over and over again!
    

In simple terms, Linux Shell scripting is a way to automate tasks on your computer by writing a set of instructions in a special language. It's like having a helpful assistant that follows your commands to get things done quickly and efficiently.

## Tasks

### Explain in your own words and examples, what is Shell Scripting for DevOps?

Shell scripting for DevOps is the practice of using scripting languages, typically within the command-line interface (CLI) or shell environment of a Linux or Unix-based operating system, to automate tasks related to the deployment, management, and maintenance of software systems and infrastructure.

### What is `#!/bin/bash?` can we write `#!/bin/sh` as well?

The line `#!/bin/bash` is known as a "shebang" or "hashbang." It's a special instruction at the beginning of a script file in Unix-like operating systems (including Linux) that tells the system which interpreter should be used to execute the script.

In this case, `#!/bin/bash` specifies that the Bash (Bourne Again Shell) interpreter should be used to execute the script. Bash is a popular shell with powerful scripting capabilities and is commonly used in Linux environments.

However, you can also use `#!/bin/sh` in your script. This specifies that the script should be executed using the system's default shell, which may or may not be Bash. `sh` typically refers to the Bourne Shell or a compatible shell, which is a simpler and more basic shell compared to Bash.

### Write a Shell Script which prints "I will complete #90daysofdevops challenge"

```bash
#!/bin/bash

echo "I will complete #90daysofdevops challenge"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710320015789/e2b687a3-40f6-4ca2-9add-2190c962b0a6.png align="center")

### Write a Shell Script to take user input, input from arguments and print the variables

```bash
#!/bin/bash

# Taking input from the user
echo "Enter your name:"
read userName


# Printing the variables
echo "Hello it is very nice to meet you $userName"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710320785046/d9014ff1-99e3-4525-b288-7913bc3925bd.png align="center")

### Write an example of an if else shell scripting by comparing 2 numbers

```bash
#!/bin/bash

# Define two numbers
number1=10
number2=20

# Compare the numbers
if [ $number1 -gt $number2 ]; then
    echo "$number1 is greater than $number2"
elif [ $number1 -lt $number2 ]; then
    echo "$number1 is less than $number2"
else
    echo "$number1 is equal to $number2"
fi
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710321223099/6837dcb7-c7ce-467f-abc4-66ea6a12dae6.png align="center")

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )