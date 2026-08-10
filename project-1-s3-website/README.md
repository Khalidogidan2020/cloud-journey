<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Khalid Ogidan  
**Email:** khalidogidan202@gmail.com

---

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will host a static website using Amazon S3.

### Tools and concepts

Services I used were Amazon S3 bucket and the Key concepts I learnt include ACL which taught me about who has access to certain sites and bucket website endpoint URL which allows users to view your bucket's files.

### Time, challenges, and wins

This project took me approximately 25 minutes to complete.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create a storage space for my website's files. 

### How long it took to create the bucket

Creating an S3 bucket took me less than 5 minutes.

### Region selection

The Region I picked for my S3 bucket was Europe-Ireland because that is the closest region.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means that no other AWS account in the world can use my bucket name unless I delete it.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will get the resources i need for my website and upload them to my S3 bucket

### Files I uploaded

I uploaded two files to my S3 bucket - they were index.html which is the website page itself and the other upload was the folder containing all the images for the site.

### How the files work together

Both files are necessary for this project as they directly compliment each other. One is for the base structure and the other is for filling up the structure and making it look presentable and attractive.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure my S3 bucket for static website hosting and visit the link to make sure that it is functional.

### Understanding website hosting

Website hosting means to publicise your website to be viewed by anyone on the internet.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I configured the following settings: 
Static web hosting- Enabled
Hosting type- Chose Host a static website
Index document- Entered "index.html"

### Access Control Lists (ACLs)

An ACL stands for Access Control List which is a set of rules that decides who can get access to a resource. I enabled it becuase i want my website to be viewed by anyone in the public.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL which is similar to a regular URL and allows people to visit my S3 bucket's files as a website.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an error 403 Forbidden due to the contents of the site still being private.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make my site publicly acessible and live on the Internet

### How I resolved the 403 error

To resolve this 403 Forbidden error, I selected the objects tab on my buckets page and then selected the actions dropdown menu and then I selected the "make public using ACL" option.

![Image](http://learn.nextwork.org/thankful_silver_mysterious_mulberry/uploads/aws-host-a-website-on-s3_5d4474f9)

---
