---
title: "Day 25: Jenkins CI/CD Project Documentation"
seoTitle: "Day 25: Jenkins CI/CD Project Documentation"
seoDescription: "Day 25: Jenkins CI/CD Project Documentation"
datePublished: Tue May 28 2024 03:36:55 GMT+0000 (Coordinated Universal Time)
cuid: clwpuj4b3000009jxfciaalu5
slug: day-25-jenkins-cicd-project-documentation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716725011197/11e9a540-c528-42bf-9b05-40ffc099ebf6.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1716725150892/e2e3c123-56f3-4f9b-97d8-8179870e0579.png
tags: linux, docker, development, web-development, bash, webdev, developer, devops, jenkins, web3, devops-articles, 90daysofdevops, wemakedevs, trainwithshubham

---

## Introduction

This documentation provides a comprehensive guide for setting up a Jenkins CI/CD pipeline using the "node-todo-cicd" project. Available on GitHub at [node-todo-cicd](https://github.com/LondheShubham153/node-todo-cicd), this project demonstrates the automation of building, testing, and deploying a Node.js application utilizing CI/CD principles.

## Prerequisites

Before starting, ensure you have the following:

* An open AWS account with an instance launched.
    
* SSH access to your terminal.
    
* Jenkins installed and configured on your server or cloud platform.
    

### Install and Configure Jenkins

#### Step 1: Install Java

Update your system and install Java:

```sh
sudo apt update
sudo apt install openjdk-11-jre
java -version
```

The version output should resemble:

```bash
openjdk version "11.0.12" 2021-07-20
OpenJDK Runtime Environment (build 11.0.12+7-post-Debian-2)
OpenJDK 64-Bit Server VM (build 11.0.12+7-post-Debian-2, mixed mode, sharing)
```

#### Step 2: Install Jenkins

Run the following commands to install Jenkins:

```sh
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-202.. | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

#### Step 3: Start Jenkins

Enable and start Jenkins:

```sh
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```

#### Step 4: Unlock Jenkins

Retrieve the initial admin password:

```sh
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

## Jenkins Job Configuration

### Creating a Jenkins Job

1. Fork the repository: [node-todo-cicd](https://github.com/LondheShubham153/node-todo-cicd.git).
    
2. Create a new Jenkins job:
    
    * Navigate to Jenkins dashboard.
        
    * Click on "New Item".
        
    * Enter a job name and select "Freestyle project".
        
    * Click "OK".
        

### Integrate Source Code

1. In Jenkins, go to the job configuration.
    
2. Under "Source Code Management", select "Git".
    
3. Add the repository URL from your forked repository.
    

### GitHub Integration

1. Go to your GitHub repository settings &gt; Webhooks.
    
2. Click "Add Webhook".
    
3. Enter the payload URL (your Jenkins URL followed by `/github-webhook/`).
    
4. Set the content type to `application/json`.
    
5. Select events that should trigger the webhook.
    
6. Save the webhook configuration.
    

## Build Stage Configuration

1. In Jenkins job configuration, under "Build", add a build step "Execute shell".
    
2. Write your build script using Groovy syntax:
    

```sh
# Example build script
npm install
npm run build
```

3. Ensure the build script works by triggering a build.
    

## Test Stage Configuration

Integrate automated tests to ensure code quality:

1. Add another "Execute shell" build step for running tests:
    

```sh
# Example test script
npm test
```

2. Ensure tests are executed successfully during the build.
    

## Deployment Configuration

Deploy your application to the target environment:

1. Add another "Execute shell" build step for deployment:
    

```sh
# Example deployment script
npm run deploy
```

2. Configure the target environment settings in the script.
    

## Troubleshooting

### Common Issues and Solutions

* **Jenkins not accessible**: Ensure your security group inbound rules allow traffic on ports 8080 (Jenkins) and 8000 (application).
    
* **Build failures**: Check console output for errors and verify script syntax.
    

## Conclusion

By following this guide, you can set up a complete Jenkins CI/CD pipeline to automate the process from source code management to deployment, ensuring consistent and reliable software delivery. Jenkins orchestrates these steps based on defined triggers, providing an efficient workflow for development and deployment.

### Stay Connected

Keep up with the latest insights on cloud and DevOps by following me on:

* [Hashnode](https://hashnode.com/rikkkdipen)
    
* [LinkedIn](https://www.linkedin.com/in/rikkkdipen)
    
* [GitHub](https://github.com/rikkkdipen)
    

Thank you for reading! Let's continue learning, growing, and making a positive impact in the tech world together.

%%[buymeacoffeebutton]