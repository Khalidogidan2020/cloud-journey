<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Create S3 Buckets with Terraform

**Project Link:** [View Project](http://nextwork.ai/projects/aws-devops-terraform1)

**Author:** Khalid Ogidan  
**Email:** khalidogidan202@gmail.com

---

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_9i0j1k2l)

---

## Introducing Today's Project!

In this project, I will create S3 buckets using Terraform. The goal is for me to learn how to use Terraform to automate the deployment of an S3 bucket.

### Tools and concepts

The Key services I used were Terraform, AWS CLI, and  AWS IAM . Key concepts I learnt include infrastructure as code, Terrafrom Init, Terraform plan and Terraform Apply.

### Project reflection

This project took me approximately three and a half hours to complete. The most challenging part was determining where AWS CLI had been installed because it stopped me from progressing for a little while. It was most rewarding to finally figure out that I was simply in the wrong directory and I just had to navigate to where AWS CLI was accessible.

I chose to do this project today because learning how Terraform functions and how to use it is such an improtant aspect of working in the cloud and helps with not relying too much on the AWS console.

---

## Introducing Terraform

Terraform is a tool that will help me to build and manage cloud infrastructure using code. If I want cloud infrastructure like databases or servers, I just write a script and Terraform automatically builds it all for me using the script as a blueprint. 



Infrastructure as code (IaC) is the practice of describing your cloud setup (like your servers, storage, networks) in plain text files instead of clicking through a web console. Terraform is a popular IaC tool because it understands all the big cloud providers: AWS, Azure, and Google Cloud.

Terraform uses configuration files to define and manage infrastructure. main.tf is a central configuration file in a Terraform project, it is where I will write down what I would want my cloud infrastructure to look like using Terraform's language.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_9i0j1k2l)

---

## Configuration files

The configuration is structured under three blocks of code with headings as follows:
1. Provider "aws" {}
2. Resource "aws_s3_bucket" "my_bucket" {}
3. Resource "aws_s3_bucket_public_access_block" "my_bucket_public_access_block" {}


### My main.tf configuration has three blocks

The first block tells Terraform to use AWS. A "provider" is a plugin that lets Terraform work with a specific cloud service. The provider turns my configuration into API calls that create and manage my infrastructure.

The second block creates an S3 bucket. "my_bucket" is an internal name that other blocks of code in "main.tf" will use to reference my bucket.

The third block manages who can access my S3 bucket. All the settings like block_public_acls, ignore_public_acls, block_public_policy, and restrict_public_buckets are set to true to prevent public access to my bucket and its contents.


![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_ljvh9876)

---

## Customizing my S3 Bucket

---

## Terraform commands

I ran 'terraform init' to set up my project by doing the following things:
1. Downloads necessary plugins
2. Setting up the backend: to keep its own record of my infrastructure
3. Preparing modules: If my setup uses reusable code blocks (called modules) this is where the code is downloaded from their source to replace placeholders in my code.
4. Creating a lock file: This file keeps track of the versions of everything Terraform is using.

Next, I ran 'terraform plan' to create an execution plan, which shows me what changes Terraform will make to my infrastructure based on my configuration files (like main.tf).

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_3g4h5i6j)

---

## AWS CLI and Access Keys

When I tried to plan my Terraform configuration, I received an error message that says "No valid credential source found". This was because Terraform didn't have the necessary credentials to access my AWS account. 

To resolve my error, first I installed AWS CLI, which is a powerful tool that lets me manage AWS services from my terminal instead of having to use the AWS Management Console, I can now run text commands from my local machine.

I set up AWS access keys to log in via the command line interface.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_7j8k9l0m)

---

## Lanching the S3 Bucket

I ran 'terraform apply' to apply the changes I have written in my terraform configuration. Running 'terraform apply' will affect my AWS account by creating the S3 bucket.

The sequence of running terraform init, plan, and apply is crucial because If I ran terraform apply before terraform init, I would've run into an error because terraform init needs to set up my project first by downloading the necessary plugins and setting up the state file, which is the file terraform uses to track the current state of my infrastructure.

![Image](http://nextwork.ai/thankful_silver_mysterious_mulberry/uploads/aws-devops-terraform1_1q2w3e4r)
