---
title: "Day 7: Unlocking System Efficiency: Mastering Package Manager & Systemctl"
seoTitle: "Unlocking System Efficiency: Mastering Package Manager & Systemctl"
seoDescription: "Learn how to harness the power of Package Managers and Systemctl for streamlined operations and optimized productivity."
datePublished: Sat Mar 16 2024 06:46:18 GMT+0000 (Coordinated Universal Time)
cuid: clttq5gvv000309l59k8s0gni
slug: day-7-unlocking-system-efficiency-mastering-package-manager-systemctl
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1710569433599/db7f5e83-2221-43f1-ac86-2d0fd0d6e70c.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1710571461617/4e206cab-e490-441d-b9fd-e29904bd712c.png
tags: linux, github, web-development, opensource, git, devops, hashnode, package-manager, systemd, linux-for-beginners, kunalkushwaha, systemctl, 90daysofdevops, wemakedevs, trainwithshubham

---

### Package Manager in Linux

In Linux, a package manager is like a smart shopping assistant for your computer. Just as you'd go to a store to buy groceries, your computer needs certain software tools and programs to function smoothly.

The package manager helps you find, download, install, and manage these software packages effortlessly. It's like browsing through aisles in a supermarket, where each package is a different product.

With a package manager, you can easily search for the software you need, install it with just a few clicks, and even keep it updated automatically. It saves you time and effort by handling all the technical details behind the scenes, ensuring that your system stays organized and up-to-date with the latest software.

### What is Package in Linux?

In Linux, a package is like a neatly wrapped gift containing software programs, libraries, configuration files, and other necessary components. Just as you might receive a gift box with various items inside, a package bundles together everything needed to install and run a particular piece of software on your computer.

Each package comes with its own set of instructions on how to install it, where to put its files, and how it interacts with other software on your system. This makes it easy for your computer to manage and organize different software applications.

When you want to install new software or update existing ones, you can use a package manager to handle everything for you. It's like having a helpful assistant who knows exactly how to unwrap and set up each package, making the process smooth and hassle-free.

### Different Kinds of Package Managers

In Linux, there are different kinds of package managers, each with its own way of handling software packages. Think of them like different brands of stores, each with its own unique layout and style.

1. **APT (Advanced Package Tool)**: APT is like a well-organized supermarket. It's commonly used in Debian-based distributions like Ubuntu. With APT, you can easily search for, install, and update software packages using simple commands like `apt-get` or `apt`.
    
2. **YUM (Yellowdog Updater Modified)**: YUM is similar to APT but used in Red Hat-based distributions like Fedora and CentOS. It's like a reliable grocery store where you can find everything you need. You can use commands like `yum install` or `yum update` to manage packages.
    
3. **DNF (Dandified YUM)**: DNF is the next generation of YUM and offers improved performance and features. It's like an upgraded version of your favorite grocery store, making it easier and faster to find and install software packages.
    
4. **Pacman**: Pacman is the package manager used in Arch Linux and its derivatives. It's like a boutique store with a curated selection of high-quality products. Pacman uses commands like `pacman -S` to install packages and `pacman -Syu` to update the entire system.
    
5. **Snap**: Snap is a universal package manager that works across different Linux distributions. It's like a one-stop shop where you can find a wide range of software packages. With Snap, you can install software with a single command and ensure it runs smoothly on any Linux system.
    
6. **Flatpak**: Flatpak is another universal package manager that focuses on sandboxing applications for improved security. It's like a modern convenience store where you can quickly grab and install software without worrying about compatibility issues.
    

Each package manager has its own strengths and weaknesses, but they all make it easy to find, install, and manage software packages on your Linux system.

## Tasks

### Install Docker and Jenkins in your system from your terminal using package managers

* To install docker in ubuntu, you can use the following commands
    
    ```bash
    # To install docker
    sudo apt -y install docker.io
    
    # To install docker-compose
    sudo apt -y install docker-compose
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710569984303/49666fd0-e6d7-4a27-9d50-9cf231b01c62.png align="center")
    
    I have combined both the commands and wrote it as one. And since I have docker already installed on my system it is showing that it's already installed on the system.
    

### To install Jenkins

When installling Jenkins, it is of utmost importance that you should have java installed on your system which has to be of proper version

* To install Java you can use the following commands
    
    ```bash
    sudo apt update
    sudo apt install fontconfig openjdk-17-jre
    java -version
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710570678139/c2846b64-9a70-4c5b-a9ee-19df10599ebe.png align="center")
    
* The first line will update your system and the 2nd line will actually install the java on your system
    
    Also you can check the version of java with the 3rd commands which is `java --version`
    
* To install Jenkins
    
    ```bash
    sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
      https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
      https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
      /etc/apt/sources.list.d/jenkins.list > /dev/null
    sudo apt-get update
    sudo apt-get install jenkins
    ```
    
    The above commands will install jenkins properly on your system
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710570745304/7524033e-36fa-4341-a8f9-05c212a1fcc4.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710570762411/6b68cef1-8031-484c-9e9b-b6df6748d735.png align="center")
    
    Now Jenkins has been properly installed on your ubuntu system.
    

## Systemctl and Systemd : )

In simple terms, systemctl and systemd are like the boss and the playbook for managing everything that happens when your computer starts up and runs.

1. **systemctl**: Think of systemctl as the boss. It's a command-line tool that lets you control and monitor different services and processes on your computer. Just like a boss manages employees, systemctl manages everything that's running on your system, from web servers to printers.
    
2. **systemd**: Now, systemd is like the playbook or rulebook that the boss follows. It's a system and service manager that coordinates all the tasks needed to start and run your computer. It ensures that everything starts up in the right order and runs smoothly, like making sure each employee knows their role and follows the company's procedures.
    

So, when you use systemctl, you're basically telling the boss what you want to happen—whether it's starting a service, stopping it, or checking its status. And systemd makes sure that everything happens according to the plan laid out in the playbook, keeping your computer running smoothly and efficiently.

In short systemctl is used to examine and control the state of “systemd” system and service manager. systemd is system and service manager for Unix like operating systems(most of the distributions, not all).

### Tasks

### Check the status of docker service in your system

* To check the status of docker service you can use this command
    
    ```bash
    systemctl status docker
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710570954646/1e6a9e83-fea8-4bdc-aba4-8dd2ba1f0508.png align="center")

### Stop the service jenkins and post before and after screenshots

* To stop the jenkins service you can use this command
    
    ```bash
    sudo systemctl stop jenkins
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710571147337/5e8302f1-0f3f-4e19-b42b-bbca06c09828.png align="center")
    
    In the above Image you can easily see that how the service of jenkins has been stopped with a mere command.
    
* To restart it you can use the following commands
    
    ```bash
    sudo systemctl start jenkins
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1710571256101/0e47a5f1-2569-474e-99ad-d1753c048ad4.png align="center")
    
    And the service has been started again just like before
    

This is how you can start and stop a service with the use of terminal in your linux operating system.

### Read about the commands systemctl vs service

In simple terms, both `systemctl` and `service` are tools in Linux used to manage services - the programs that run in the background to keep your system running smoothly.

1. `systemctl`: This is like the master tool. It's more modern and powerful, allowing you to control and manage services, as well as other aspects of system management. It's like having a control panel for your system where you can start, stop, restart, enable, or disable services, and also check their status.
    
2. `service`: Think of this as the old-school way of doing things. It's simpler and more straightforward, mainly used to start, stop, and restart services. It's like flipping a switch to turn a light on or off. While it's still widely used and works well for basic tasks, `systemctl` offers more advanced features and flexibility.
    

So, if you just need to quickly start or stop a service, `service` is like the easy button. But if you want more control and options, `systemctl` is the tool you'll want to use.

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )