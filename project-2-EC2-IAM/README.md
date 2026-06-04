<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** khalidogidan202@gmail.com  
**Email:** khalidogidan202@gmail.com

---

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use the AWS Identity and Access Management (IAM) service to control who is authenticated (signed in) and how to grant other users temporary restricted access to my AWS account. The aim of this project is learn more about EC2 and IAM.

### Tools and concepts

The Services I used were Amazon EC2 and AWS IAM . The Key concepts I learnt include Instances, JSON Policy, AWS Account Alias and IAM Users and User groups.

### Project reflection

This project took me approximately 2 and a half hours The most challenging part was navigation and looking for the correct settings. The most rewarding part was figuring out how to successfully stop the development instance.

---

## Tags

### What I did in this step

In this step, I will launch two Amazon EC2 instances so that the computing power will be increased to match the amount of traffic flooding to the website.

### Understanding tags

Tags are like labels you can attach to AWS resources for organisation. They are useful for identifying all resources with the same tag at once by acting as filters when searching for something. They are also useful for cost allocation and applying policies based on environment types.

### My tag configuration

The tag I’ve used on my EC2 instances is called "Env" and the values I’ve assigned for my instances are "production" and "development".

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy that will give access to the development instance.

### Understanding IAM policies

IAM Policies are rules for who can do what with your AWS resources. It is all about giving permissions to IAM users, groups, or roles and saying what they can or can't do on certain resources.

### The policy I set up

For this project, I’ve set up a policy using the JSON method.

### Policy effect

I’ve created a policy that allows for actions like starting, stopping and describing EC2 instances for instances tagged with "Env = developement" while denying the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource

In a JSON policy, Effect can have two values- either Allow or Deny referring to either allowing or denying an action. Action refers to all actions that you could possibly take on EC2 instances are allowed. Lastly, specifying "*" means all resources within the defined scope that this policy applies to.

---

## My JSON Policy

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will simplify user login to my AWS account using an Account Alias to allow other users like interns access when needed.

### Understanding account aliases

An account alias is a friendly name for your AWS account that you can use instead of your account ID to sign in to the AWS Management Console.

### Setting up my account alias

Creating an account alias took me less than 2 minutes . Now, my new AWS console sign-in URL is https://nextwork-alias-khalidogidan.signin.aws.amazon.com/console

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will set up a dedicated IAM group for all NextWork interns, so that I can manage all interns' permissions from one place. Secondly, I will set up a dedicated IAM user for the new intern, so that they would have a way to log in.

### Understanding user groups

IAM user groups are a collection of IAM users. It allows you to manage permissions for all the users in your group at the same time by attaching policies to the group rather than individual users.

### Attaching policies to user groups

I attached the policy I created to this user group, which means that all users (in this case interns) will have the same permission settings.

### Understanding IAM users

IAM users are the people that will get access to your resources/AWS account.

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is by ticking the checkbox for "Provide user access to the AWS Management Console". The second way is by unticking the checkboxbox for "Users must create a new password at next sign-in".

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that some of my dashboard panels are showing access denied. This is due to the permission restrictions i laid out in the policy i set up earlier.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will log into AWS using the intern's IAM user and test the intern's access to my production and development instance.

### Testing policy actions

I tested my JSON IAM policy by attempting to stop both my production instance and development instance.

### Stopping the production instance

When I tried to stop the production instance, a big red banner appears and states that I am "not authorised to perform this operation". This is because this user does not have the permission to stop any instance with the production tag.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

When I tried to stop the development instance, it was successful unlike the production instance.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-security-iam_1811801c)
