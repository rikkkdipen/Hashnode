---
title: "Day 4: DevOps Engineers' Guide to Linux Shell Scripting"
seoTitle: "Mastering Linux Shell Scripting: A Step Towards DevOps Excellence"
seoDescription: "Discover the essential concepts of Linux shell scripting, from understanding the Kernel to exploring different types of shells. Dive into the world of ....."
datePublished: Sat Oct 28 2023 14:09:55 GMT+0000 (Coordinated Universal Time)
cuid: cloa4cptm00090al8ckvkbhzm
slug: day-4-devops-engineers-guide-to-linux-shell-scripting
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698480830158/df861306-9651-402f-93ab-3f1ca56968f1.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698502095801/8914e6bb-8d2f-4e2c-8aa8-d14b123983e5.png
tags: linux, devops, 90daysofdevops, wemakedevs, trainwithshubham

---

In the [previous](https://dipen.hashnode.dev/day-3-essential-linux-commands-every-devops-engineer-should-master) article we learned about the Essential commands in the Linux operating system, if you haven't checked that article please go through that article once. Now in today's article, we are going to learn about Shell Scripting in Linux and why it is important.

But before going on SSH and SCP let's see some basic concepts like What is Kernel? and What is Shell? etc.

To understand the concepts properly refer to the diagram below:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698482541186/598b39b2-a89f-45ca-bf59-64eb6c561736.png align="center")

### What is Kernel?

The kernel is the most crucial component of the Linux Operating System which is located at the core of the Linux architecture between the computer hardware and its various processes.

It is named Kernel because if you look at the Linux architecture the kernel looks like a seed in the hard shell of the Linux OS. The kernel exists like a seed within the OS and controls all the major functions of the hardware.

The kernel manages these resources

* File management
    
* Process management
    
* I/O management
    
* Memory management
    
* Device management etc.
    

Now you know what kernel is. so let's move on to what a shell is.

### What is Shell?

A shell is a special program of the Linux OS that provides a CLI-like interface to the user to control every aspect of the OS. Shell accepts human-readable commands from a user and converts them into something that the kernel can understand. It is a command language interpreter that executes commands read from input devices such as keyboards or from files.

Shell is also divided into 2 types:

* Command Line Shell
    
* Graphical shell
    

### Command Line Shell

Using a command line can be tricky for beginners because there are lots of commands to remember. But it's super powerful. You can save commands in a file and run them together. This makes it easy to do the same tasks over and over. In Windows, these files are called batch files, and in Linux/macOS, they're called Shell Scripts.

### Graphical Shell

Graphical shells make it easy to control programs using pictures and buttons. They let you do things like open, close, move, and change the size of windows on your computer. It's like what you see in Windows or Ubuntu, where you use your mouse to click on things. You don't have to type commands for everything.

The shell gets started when the user logs in or starts the terminal.

### Different Types of Shells

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698501629328/eee6e8d8-a0f3-4976-a62e-fedb5c2a5eb7.png align="center")

There are several shells are available for Linux systems like –

* BASH (Bourne Again SHell) – It is the most widely used shell in Linux systems. It is used as the default login shell in Linux systems and macOS. It can also be installed on Windows OS.
    
* CSH (C SHell) – The C shell’s syntax and its usage are very similar to the C programming language.
    
* KSH (Korn SHell) – The Korn Shell was also the base for the POSIX Shell standard specifications etc.
    
* ZSH (Z SHell) - It is a Unix shell that can be used as an interactive login shell and as a command interpreter for shell scripting. Zsh is an extended Bourne shell with many improvements, including some features of Bash, ksh, and tcsh.
    

Now that you know the basic terminologies let's move on to SSH.

### What is SSH?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698501738787/8ed2b677-eeb1-43bf-814e-214f2fe97f91.png align="center")

SSH also called Secured Shell is a protocol used to securely access the remote computer by using a command line interface. SSH is the most common way to access remote Linux and Unix-like servers

Before SSH we used to use Telnet for accessing the remote servers through the command line interface but due to various security reasons telnet got outdated and today we use SSH or Secured Shell instead of Telnet.

By Default SSH or Secured Shell uses port no 22. So if anyone asks you which port SSH uses?. Then 22 is the answer to that question.

## #Day 4 Tasks:

While learning something it is very much important that you do some tasks yourself. Like, suppose you're learning something you should explain it to yourself and ask different questions like Can we do this or that etc. So today we are going to do just that.

### 1\. What is Linux Shell Scripting for DevOps?

A shell script is like a little computer program made to work with a Linux command line. Think of it as a set of instructions you can give your computer. These scripts are often seen as scripting languages. What they do is handle tasks like moving files, running programs, and showing text on the screen.

### 2\. What is #!/bin/bash? can we write #!bin/sh as well?

The line "`#!/bin/bash`" is called a shebang or hashbang. It's a special code that tells the computer which program to use when running the script.

In this case, "`/bin/bash`" says to use the Bash shell. Bash is a popular choice for scripting on Linux and Unix systems.

You can also use "`#!/bin/sh`" in the shebang. This tells the computer to use the Bourne shell, which is an older and simpler shell. It's not as powerful as Bash, but it's still found on many systems and can handle basic tasks.

The cool thing is that Bash understands the Bourne shell's language, so most Bourne shell scripts work in Bash without changes. So, unless you have a specific reason to use the Bourne shell, it's usually a good idea to stick with Bash for your scripting needs.

### 3\. Shell Script for message printing

* Write a shell script that prints "I will complete 90 days of DevOps Challenge"
    

```bash
#!/bin/bash
echo "I will complete #90daysofdevops challenge"
```

The Shell Script mentioned above uses the "bash" as the interpreter and uses the "echo" command to print the output on the terminal screen.

To run the above script save it to a file with "name.sh". or (.sh extension) In this way the Linux or the OS will understand that it is a Shell script after that the command "chmod +x" to make the file executable and after that execute the file with ./ command or by specifying the complete path

```bash
sudo ./message.sh

sudo /home/sh/Desktop/message.sh
```

### 4\. **Write a Shell Script to take user input from arguments and print the variables.**

```bash
#!/bin/bash
# Take user input
echo "Enter your name: "
read name

#Take input from 2 arguments
arg1=$1
arg2=$2

#print the name
echo "your name is $name"
echo "Argument 1 is $arg1"
echo "Argument 2 is $arg2"
```

The script written above prompts the user to enter the name and then take the arguments that we provided while initializing the script and then prints the output on the screen.

To run the script

1. Save the script in a file and give it a ".sh" extension. This tells your computer it's a shell script.
    
2. Next, make the file executable by running the command "chmod +x" followed by the name of your file.
    
3. After making it executable, you can run the script by typing "./" and then the name of the file. You can also specify the full path to the file if it's not in your current folder you can also refer to the above example.
    

### 5\. **Write an Example of If else in Shell Scripting by comparing 2 numbers.**

```bash
#!/bin/bash

echo "Enter the 1st number"
read number1

echo "Enter the 2nd number"
read number2

if [ $number1 -gt $number2 ]
then
 echo "$number1 is greater than $number2"
elif [ $number1 -lt $number2 ]
 then echo "$number1 is less than $number2"
else
 echo "$number1 is equal to $number2"
fi
```

The above script will take 2 numbers as user input and then compare those two numbers with each other to print which one of the numbers is the greater number.

it works like

1. We start by checking if "num1" is bigger than "num2" using \[ $num1 -gt $num2\]. If it's true, we say "$num1 is greater than $num2."
    
2. If the first check is false, we move to the next one using "elif \[ $num1 -lt $num2\]." If this is true, we say "$num1 is less than $num2."
    
3. If neither of the above is true, we go to the "else" part, which happens when "num1" is the same as "num2." In this case, we say "$num1 is equal to $num2."
    

That was all about today's.

Happy Learning 💡

~Dipen : )