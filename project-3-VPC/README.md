<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** khalidogidan202@gmail.com  
**Email:** khalidogidan202@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

This project consists of a virtual private cloud equipped with a subnet and an internet gateway.

### What is Amazon VPC?

Amazon VPC stands for Virtual Private Cloud and it is useful because it allows for keeping resources private and organised.

In today's project, I used Amazon VPC to create a subnet and an internet gateway that allowed me to publicise my resources on the Internet.

### Personal reflection

This project took me about 1 hour and 45 minutes to complete.

One thing I didn't expect in this project was how straightforward it was when it came to setting up and attaching the internet gateway, I thought it would be a complicated process.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access the VPC console in AWS and then create a VPC.

### How VPCs work

VPCs are subsections of the cloud that allow resources to be private preventing public access. VPCs allow users to organise their private resources and facilitates communication and integration between those resources without the public internet.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This was the reason why i was able to launch resources like EC2 and connect services from Day 1 of using AWS.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I needed to define an IPV4 CIDR block. CIDR stands for Classless Inter-Domain Routing and it is a way to assign a whole block of IPV4 addresses.

---

## Subnets

### What I did in this step

In this step, I will launch a subnet inside my VPC.

### Creating and configuring subnets

Subnets are used to group resources with similar access rules and restrictions. There are already subnets existing in my account, one for every availability zone.

### Public vs private subnets

The difference between public and private subnets is that public subnets are connected to the internet while private subnets do not have direct internet access. For a subnet to be considered public, it has to be connected to an intenet gateway.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPV4 addresses. This setting makes sure that any EC2 instance launched in that subnet will instantly get a public IP address in order to access the internet or be accessible from the internet.

---

## Internet gateways

### What I did in this step

In this step, I will connect my VPC to the internet using a internet gateway.

### Setting up internet gateways

Internet gateways are a bridge that connect a VPC to the public through the Internet. Internet gateways are key to making applications available on the internet.

Attaching an internet gateway to a VPC means resources in my VPC can now access the Internet. If I missed this step, the resources in my VPC will remain private.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-networks-vpc_4ae90410)

---
