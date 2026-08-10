<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Set Up a Web App in the Cloud

**Project Link:** [View Project](http://nextwork.ai/projects/aws-devops-vscode)

**Author:** khalidogidan202@gmail.com  
**Email:** khalidogidan202@gmail.com

---

## Set Up a Web App Using AWS and VS Code

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_7a1de541)

---

## Introducing Today's Project!

In this project, I will set up a Web App using AWS and VS Code. I am doing this project to learn how to use VS Code to set up a remote SSH connection to an EC2 instance and use Maven and Java to generate a basic web app.

This project is part one of a series of DevOps projects where I'm building a CI/CD pipeline! 

I did this project because I am on Day one of my journey in learning the foundation of Devops.

### Key tools and concepts

Services I used were Amazon EC2, Maven,Java and VS Code. The key concepts I learnt include: SSH, Amazon Coretto 8, how to install Apache Maven and Java through the Terminal and created the web app.

### Project reflection

This project took me approximately 3 hours. The most challenging part was typing in the long commands accurately It was most rewarding when I ran the code and it worked flawlessly.

One thing I didn't expect in this project was how quick and seamless the installation of Java and Maven was and I also did not expect it to be done entirely through the terminal.

---

## Launching an EC2 instance

### What I did in this step

In this step, I will launch a new EC2 instance, set up a key pair for secure access and set up network settings for my instance.

I started this project by launching an EC2 instance because it allows  me to customise a virtual computer to fit what I need for this project.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_7852fbf3)

### I also enabled SSH

SSH stands for Secure Shell and it is a protocol used to ensure only authorized users can access a remote server. I enabled SSH so that when I connect to my EC2 instance, it will set up a secure connection and then all data transferred gets encrypted.

### Key pairs

A key pair is like the keys to a virtual computer and it lets me securely access my EC2 instance. It is made up of a public and private key. The private key is what verifies that I am the one allowed to access that specific virtual machine, keeping everything secure.

### Downloaded key pair file

Once I set up my key pair, AWS automatically downloaded the private key.

---

## Set up VS Code

### What I did in this step

In this step, I will use VS Code to connect with my instance so that I can create and edit my web app's code.

### What is VS Code?

VS Code is an integrated development environment used for editing source code.

I installed VS Code to help build up my Web App.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_53d05e68)

---

## My first terminal commands

A terminal is where you send instructions to your computer using texts instead of clicks. The first command I ran for this project is "cd ~\Desktop\DevOps" which navigates my terminal to my DevOps folder in my desktop.

### Updating file permissions

I also updated my private key's permissions by typing commands with these keywords:
1. "/reset" removes all existing permissions making it a clean slate
2. "/grant:r "khali:R"" gives only my user account read access to the file
3. "/inheritance:r" stops the file from inheriting permissions from its parent folder, keeping it locked down.


![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_9328ada1)

---

## SSH connection to EC2 instance

### What I did in this step

In this step, I will set up a connection to my EC2 instance so that I can set up the web app.

### Connecting to EC2

To connect to my EC2 instance, I ran the command:
ssh -i [[inserted .pem file path here]] ec2-user@[[inserted EC2 IPDNS here]]

### This command required an IPv4 address

A server's IPV4 DNS (Domain Name System) is the public address for the server that the internet uses to find and connect to it.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_e3069dca)

---

## Maven & Java

### What I did in this step

In this step, I will install Apache Maven on my EC2 instance and install Amazon Coretto 8 to help with building my web app.

### Why I'm using Maven

Apache Maven is a tool that helps developers build and organize Java software projects.

Maven is required in this project because it's really useful for kick-starting web projects. It uses something called archetypes, which are like templates to lay out the foundations for different types of projects like web apps.

### Why I'm using Java

Java is a popular programming language used to build different types of applications, from mobile apps to large enterprise systems.

Java is required in this project because Maven is a tool that needs Java to operate, without Java I would not be able to use Maven to generate the web app.

---

## Create the Application

### What I did in this step

In this step, I will generate the web app using Maven and Java.

### Creating the Java web app

I generated a Java web app using the command:
mvn archetype:generate -DgroupId=com.nextwork.app -DartifactId=nextwork-web-project -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false




### Installing Remote - SSH

I installed Remote - SSH, which lets me connect directly via SSH to another computer securely over the internet. This lets me use VS Code to work on files or run programs on that server as if I were doing it on my own computer, which will come in handy when I edit the web app in my EC2 instance!

### SSH configuration details

Configuration details required to set up a remote connection include:
1. Host
2. Host Name
3. Identity File
4. User

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_2939cf01)

---

## Create the Application

### Exploring the project structure

Using VS Code's file explorer, I could see all the files and subfolders that are a part of my web app.

Two of the project folders created by Maven are src and webapp. src is the source folder which holds all the source code files that define how my web app looks and works.
webapp contains all the web app's files.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_45f91fd7)

---

## Using Remote - SSH

### What I did in this step

In this step, I will connect VS Code to my EC2 instance through the use of an extension. This is different to the already established connection through SSH because SSH only connects tot the terminal but the extension unlock's VS Code's IDE features directly on my EC2 instance making it easier to edit and manage my webapp.

### Updating the web app

The index.jsp is  a file used in Java web apps. It's similar to an HTML file because it contains markup to display web pages.

I edited index.jsp by typing in what I want to display on my web app and then clciking the Ctrl + S Command to save my changes.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-vscode_7a1de541)

---
