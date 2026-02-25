<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** mahmoud elsherbeny  
**Email:** mahmoudstudy4@gmail.com

---

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use S3 to host a static website I'm doing this project to learn about aws and how it can be use and how to host website with cloud services to sotre objects in the cloud and even host websites (how it works)

### Tools and concepts

Services I used were Amazon S3 Key concepts I learnt include  bucket policies , uploading static files (index.html),bucket endpoints URLs and ACLs and how they control access to our bucket's objects 

### Time, challenges, and wins

This project took me approximately 1 h30min including the demo time and quiz time The most challenging part was. resolving the 403 forbidden error  It was most rewarding to see the website load and be live 

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open up s3 service by aws and then create a storage space inside  it to store web files 

### How long it took to create the bucket

Creating an S3 bucket took me less than 10 minutes but i need to learn some new concepts like : (block public access , ACLs ) once i've learned about them i can create in even short time in the future 

### Region selection

The Region I picked for my S3 bucket was Frankfurt in Germany because it is the region  closest to my country Egypt so the latency will be more less than us east  , lower time to retrieve your things . 

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two aws buckets in the entire world can have the same name they had to be completely unique regardless the region or the account 


![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload website files into S3 bucket because no files = no website the bucket is empty 

### Files I uploaded

I uploaded two files to my S3 bucket - they were an index HTML this determines the structure i want it to goes inside and folder of images and assets this will fill in the website with images 

### How the files work together

Both files are necessary for this project as index HTML detriment the structure but the structure alone does not illustrate the contents of the website i.e if index html says insert image here it might not have the actual image to display i need to supply that image separately that's why i have multiple files uploaded the index html file to direct what is inside web page but also a bunch of assets like images that web is trying to display 

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make my website visible to the world this is called static website hosting its important  because our website files will stay just files without hosting without this step 

### Understanding website hosting

Website hosting means putting website files on a web server which is a computer designed to turn the files into a web page that people can visit 

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went to the properties section of the bucket and enable the static hosting and type the document name (index.html) as the index document this is the document i try to host

### Access Control Lists (ACLs)

An ACL is an Access Control List is a way to configure permission settings inside a bucket i've enabled it so that i can control access to website files later.

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is is a special web address (URL) that Amazon S3 provides when you configure an S3 bucket to host a static website. Think of it as the unique internet address for your website files stored in that specific S3 bucket. Instead of just being a storage location, this endpoint transforms your S3 bucket into a functional web server, allowing anyone with the URL to view your website directly in their browser.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw... The reason for this error was access denied code 403 Forbidden.
The reason of this error is the object in bucket is private by default even though I've switched off "Block all public access" the website files themselves are still completely private i need to mange their access settings separately  they need to be public files too for the public to see the website 

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will go into files i uploaded into the bucket  and make them public too because this will enable us to view the contents of the website 

### How I resolved the 403 error

To resolve this 403 Forbidden error, I have make the all objects of the bucket that designed for the website all of them public  using ACLs 

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to use bucket policies to control access to our bucket files  i'm doing this so that i can stop people from deleting the files inside the bucket 

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are. rules that determine who is allowed or not allowed to do something  The benefit of using bucket policies is that you can have even greater control of the actions that people are or aren't allow to do  while ACLs are useful for  controlling public access  into individual objects inside the bucket 

![Image](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy denied every ones from deleting the (index.html) in the bucket i tested this by trying to deleting the index file  and saw that permission is denied this means that my bucket policies works it successfully stoped me from deleting  the objects i want to protect 

---
