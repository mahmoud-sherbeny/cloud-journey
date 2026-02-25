<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="250" />

# ☁️ Hosting a Static Website on Amazon S3

**Project Link:** http://learn.nextwork.org/projects/aws-host-a-website-on-s3  
**Author:** Mahmoud ElSherbeny  
**Duration:** ~1.5 hours

---

## 📌 Project Overview

In this project, I deployed a static website using **Amazon S3**.  
The goal was to understand how cloud storage services can also function as web hosting platforms and how access permissions affect website availability.

This project helped me learn how AWS stores objects in the cloud and how static websites are served directly from S3 buckets.

---

## 🧰 Services & Concepts Used

**AWS Services**
- Amazon S3

**Key Concepts Learned**
- S3 Buckets
- Static Website Hosting
- Bucket Policies
- Access Control Lists (ACLs)
- Public Access Configuration
- Bucket Endpoint URLs

---

## ⏱️ Time, Challenges & Wins

- **Project duration:** approximately 1 hour 30 minutes
- **Main challenge:** resolving the `403 Forbidden` error
- **Biggest win:** successfully making the website publicly accessible

---

## 🪣 Creating the S3 Bucket

I created an S3 bucket to store the website files.

### Region Selection
I selected the **Frankfurt (eu-central-1)** region because it is geographically closer to Egypt, which helps reduce latency.

### Bucket Name Uniqueness
S3 bucket names must be globally unique across all AWS accounts worldwide.

![Bucket Creation](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## 📤 Uploading Website Files

I uploaded the website files into the bucket:

- `index.html`
- image/assets folder

The HTML file defines the page structure, while the assets provide visual content required for the website.

Without uploaded files, the bucket cannot serve a website.

![Upload Files](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_a265af88)

---

## 🌐 Enabling Static Website Hosting

Static website hosting was enabled from the **Properties** tab of the bucket.

I configured:
- Index document: `index.html`

This step converts the bucket from simple storage into a web-hosting endpoint.

![Static Hosting](http://learn.nextwork.org/courageous_orange_kind_chameleon/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## 🔗 Bucket Endpoint & 403 Error

After enabling hosting, AWS generated a **bucket endpoint URL**.

Initially, visiting the endpoint resulted in a:
