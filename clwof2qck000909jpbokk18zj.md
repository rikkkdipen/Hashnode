---
title: "Day 24: Complete Jenkins CI/CD Project"
seoTitle: "Day 24: Complete Jenkins CI/CD Project"
seoDescription: "Day 24: Complete Jenkins CI/CD Project"
datePublished: Mon May 27 2024 03:36:30 GMT+0000 (Coordinated Universal Time)
cuid: clwof2qck000909jpbokk18zj
slug: day-24-complete-jenkins-cicd-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716724454363/7d76a894-dd55-4bff-84bb-9b6e93d8779d.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1716724520361/3f398cc0-f524-49b3-a63c-84650368c20d.png
tags: docker, web-development, machine-learning, kubernetes, webdev, developer, devops, jenkins, cicd-cjy1vtdk2005kjjs17n8couc3, devops-articles, 90daysofdevops, wemakedevs, trainwithshubham

---

## Task 1:

* Fork [**https://github.com/LondheShubham153/node-todo-cicd.git**](https://github.com/LondheShubham153/node-todo-cicd.git) repository.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716325042/29c7f85d-14e0-4fd6-b640-9b0fc6f638d9.png align="center")

Create a connection to your Jenkins job and your GitHub Repository via GitHub Integration.  
To generate the SHH key for integration use the `shh-keygen` command for public and private keys.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716376370/25a62bc0-d9da-4754-ba9d-40157b3862e7.png align="center")

To create a Public key we have to use `cat /home/ubuntu/.ssh/id_`[`rsa.pub`](http://rsa.pub)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716433141/e89bdf64-1ba8-4c1a-a85b-d324bfafdcdf.png align="center")

To configure the GitHub Goto account setting &lt; SHH and GPG keys and paste the ssh-rsa key here.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716487712/06a8bf69-2b3d-4b84-a777-f51bc5870b1f.png align="center")

Click on New SSH keys

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716546955/a9b326c5-4a5a-4721-9928-9fceb789ff50.png align="center")

Give the desired name and paste the public keys

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716654402/60f8657b-f9e2-4337-8753-aedbe2bf1f31.png align="center")

Click on Add SSH key and Save

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716708017/af752f12-3d6f-460b-89e6-7dc2b7b09f36.png align="center")

Now your SSH keys has been added

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716716759019/3860e976-9343-4591-9b3d-1a4533cbf21a.png align="center")

Read About [**GitHub WebHooks** and make sure](https://betterprogramming.pub/how-too-add-github-webhook-to-a-jenkins-pipeline-62b0be84e006) you have a CICD setup.

For setting up a github webhook go to github [repo's setting](https://betterprogramming.pub/how-too-add-github-webhook-to-a-jenkins-pipeline-62b0be84e006) &lt; Webhooks and add webhook

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716717127060/e7e479fd-a15a-4c65-be81-72d585d867fb.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716717142620/d0573ec5-70ea-4471-9fac-80c147b2a58e.png align="center")

Click on Add Webhook

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716717167590/ee8f623f-44a5-414d-932c-2400c55993c3.png align="center")

In the payload URL enter your Jenkins URL and after / write github-webhook

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718550685/5b792cf4-6377-4c18-9c89-dd1bc63be01c.png align="center")

also change the content type to `application.json` and click on add webhook

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718538354/2413b279-b9ed-4672-ac6b-5512b4b56812.png align="center")

Note: Localhost URL will not work do create an ec2 instance and after that try to put the payload URL

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718770224/f62c7670-dfa0-402a-b071-b8b365167c90.png align="center")

To install GitHub integration plugins go to the Jenkins dashboard &gt; Manage Jenkins &gt; Plugins

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718803735/f8d8617b-f14a-4365-bfb7-80a53452f5b0.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718819366/8c7720b1-6677-4e42-be71-f9f1617923c4.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718834506/029abba5-239f-4df2-8cec-f4dc8fbf2ff7.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718855093/b5cef8c2-2e59-4496-853b-49fa9a935b44.png align="center")

Install the selected plugin

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718895458/de1dee65-2ed6-4af7-a97d-b8428a102139.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716718906277/ac60bc70-8dba-411d-8202-a6eaa791e050.png align="center")

Do wait for sometime till jenkins restart

Once Jenkins is restarted. Create a new project with freestyle pipeline

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719020376/7e930e82-ad93-47c4-9531-dd0d20109595.png align="center")

add git repo for clone [https://github.com/rikkkdipen/node-todo-cicd.git](https://github.com/rikkkdipen/node-todo-cicd.git)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719084256/dd7b4597-9e93-4f14-9a82-4b9f08fd3055.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719107926/5365cb4a-2b00-494d-9613-c54bd1941f5b.png align="center")

click on add credentials and add

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719199028/eb088d7d-2975-4ed4-bfc8-971cc243b353.png align="center")

In the kind section select SSH Username with private key

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719241064/2410e909-8897-4b41-a239-b121f21b3c0b.png align="center")

Enter your Hostname and add the private key from .ssh folder on your instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719318821/d3ce2ada-2b12-4493-bfce-85ea4effd796.png align="center")

After that scroll down to build trigger section and select Git Hook trigger for SCM polling

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719378897/7b554437-50ad-4cc4-929d-14739a15c918.png align="center")

and click save

# **Task 2:**

* In the Execute shell run the application using Docker compose
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719625423/9b12c583-2dc0-452f-adfe-ce559dc758d9.png align="center")

* You will have to make a Docker Compose file for this Project
    
* Run the project and give yourself a treat
    

### Troubleshooting

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719681375/704fdb64-61af-48a3-b609-9fff086fbe8c.png align="center")

It says docker-compose not found. Since I created this new instance only for demo purpose so i didn't install docker-compose in it

we can install docker-compose with a short and simple command in the instance

```bash
sudo apt -y install docker-compose
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716719767990/533f2069-10f6-4f85-88e6-5153e59af976.png align="center")

since docker-compose is now installed on the EC2 instance. Let's try and build the project again

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716724026731/3d5cfcfe-fc2a-42dd-b967-2b052a64a62f.png align="center")

In brief, the GitHub-Jenkins webhook integration for CI/CD synergizes version control and automation, expediting development cycles and elevating code quality. This fusion enhances collaboration, delivering efficient and reliable application deployment. Leveraging this integration is pivotal for modern software development, enabling agile and effective practices.