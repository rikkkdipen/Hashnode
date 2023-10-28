---
title: "Day 3: Essential Linux Commands Every DevOps Engineer Should Master"
seoTitle: "Day 3: Essential Linux Commands Every DevOps Engineer Should Master"
seoDescription: "In the previous article, we learned about what is Linux and what are some of the basic commands of the Linux Operating System.

In this article, we are ...."
datePublished: Fri Oct 27 2023 11:12:53 GMT+0000 (Coordinated Universal Time)
cuid: clo8il6ok000c09l1ebhpgw90
slug: day-3-essential-linux-commands-every-devops-engineer-should-master
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698399413354/9774b4d1-4c0a-4150-909a-cc7a3a2c0e93.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698405129084/7dd053ac-f6bc-4c4b-99c4-0243b1d7a06e.png
tags: devops, hashnode, 90daysofdevops, wemakedevs, trainwithshubham

---

> Day 3 of #90daysofdevops

In the [previous](https://dipen.hashnode.dev/day-2-exploring-linux-an-open-source-os-powering-supercomputers) article, we learned about what is Linux and what are some of the basic commands of the Linux Operating System.

In this article, we are going to see what are some of the commands of Linux that DevOps engineers use in day-to-day life.

## 1\. ls Command

> `ls` command is used to list the contents of a directory.

```bash
ls
```

* if you use `ls -l` it will show the permissions, owner, size, and last modified date for each file in the directory.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698402891703/f5819e1b-214b-48f3-8679-2e45ff40d94a.png align="center")

# 2\. sudo Command

> `sudo` command executes commands that run only with superuser privilege.

```bash
sudo apt update
```

* if you use just `apt update` to update your system it won't work but when you use `sudo apt update` will update your entire system.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698402949255/175bd56f-4002-44ed-a520-b45ab0f25264.png align="center")

## 3\. pwd Command

> `pwd` command will show you the current working directory in which you are working.

```bash
pwd
```

* if you use the `pwd` command in the shell will show you which directory you are currently in.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403003485/947e27cf-eeb2-4aa2-b400-597d0e347a58.png align="center")

## 4\. cat Command

> `cat` command is used to concatenate and display files and contents on the terminal but it can also be used to modify existing contents.

```bash
cat dipen.txt
```

* if you use `cat` command with a filename.txt it will show you the contents of filename.txt
    

`cat -b`: This adds line numbers to non-blank lines

`cat -n`: This adds line numbers to all lines

`cat -s`: This squeezes blank lines into one line

`cat –E`: This shows $ at the end of the line

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403191955/a60ff5c1-6228-4203-a2a5-4b2af1e81052.png align="center")

## 5\. Vim Command

> `vim` is the text editor used in the Linux Operating System. `Vim` stands for Vi Improved. It uses different modes to operate on files.

```bash
vim dipen.txt
```

* Normal mode: This is the default mode in which Vim starts. In normal mode, you can use various commands to navigate and edit the text.
    
* Insert mode: In insert mode, you can type text into the file. To enter insert mode, press the "i" key. To exit insert mode and return to normal mode, press the "Esc" key.
    
* Command mode: In command mode, you can enter commands to perform various actions, such as saving the file or quitting vim. To enter command mode, press the ":" key.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403340951/795c3aeb-d564-44d5-92f0-610b6a34783b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403460115/a28a37aa-c428-484c-9096-626c0f747049.png align="center")

## 6\. grep Command

> `grep` command is used to find the particular strings/word in a txt file. This is very similar to `Ctrl + F` button but this command is executed via CLI.

```bash
vim this dipen.txt
```

* This would print all of the lines in “dipen.txt” that contain the word “hashnode".
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403606240/71524c13-13d3-400e-a121-02cdbfb556e2.png align="center")

## 7\. sort Command

> `sort` command is used to `sort` the results of the search either alphabetically or numerically. `sort` can also sort files and directories.

```bash
sort dipen.txt
```

*there are 3 modes in sort command.*

* `sort -r`***:*** the flag returns the results in reverse order.
    
* `sort -f`***:*** the flag does case-insensitive sorting.
    
* `sort -n`***:*** the flag returns the results as per numerical order.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403653290/a4e9f1e0-93cc-4a58-8ad7-b0606f111d32.png align="center")

## 8\. tail Command

> `tail` command prints the last N number of data of the given output.

* By default, `tail` command prints 10 lines but with commands, you can change it to any number.
    

```bash
tail dipen.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403698989/d7a2fe04-8409-423a-98f2-fa515a477f81.png align="center")

## 9\. chmod Command

> `chmod` command is used to change the access permissions of files and directories.

* `chmod` can change the permission to read-write.
    

```bash
chmod u+wrx dipen.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403754921/68259b3f-ea13-4345-8a0a-10201a37501f.png align="center")

## 10\. chown Command

> `chown` command is used to change the file owner or group.

* `chown` command can permit to read write and execute a file.
    

```bash
sudo chown root dipen.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403790945/f9568378-c314-4f04-9451-2a899a8d1f00.png align="center")

## 11\. ping Command

> `ping` command is used to ping a host and check if it is responding

* It is used to check `ping` response of the system
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403824988/536d917d-61ec-4765-a75b-73bb5bec65e3.png align="center")

## 12\. lsof Command

> `losf` command is used to display all open files on the Linux system

* if you use this command it will show you all the open files/services in Linux system.
    

```bash
sudo lsof -u root
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698403925263/902cbac7-d873-461a-b7f7-250461a72e6f.png align="center")

## 13\. diff Command

> `diff` command is used to show the difference between two files

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698404564686/be56018b-a745-48c3-b18d-458c95e2e711.png align="center")

These are some of the commands that DevOps engineers use in their day-to-day life while working.

Happy learning💡

~Dipen : )