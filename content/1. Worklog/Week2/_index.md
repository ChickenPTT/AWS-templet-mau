---
title: "Worklog Week 2"
date: 2026-05-11
weight: 1
chapter: false
pre: ""
---

### Week 2 Objectives:

- Master fundamental knowledge about Amazon EC2 and basic features such as Instance types, AMI, Snapshots
- Practice deploying Node.js applications on EC2 instances running Amazon Linux and Windows
- Understand how to manage access permissions and limit resource usage with AWS IAM
- Get familiar with AWS Cloud9 IDE for direct cloud application development
- Master basic static website hosting on Amazon S3 with advanced features
- Optimize website performance using CloudFront CDN
- Manage object versioning and perform data replication across regions on S3

### Work Tasks to be Completed This Week:

| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Start Date | End Date   | Resources                                                                                                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | ---------- | ---------------------------------------------------------------------------------------------------------------- |
| 2   | **Lab Practice: Getting Started and Deploying Applications on Amazon Compute Cloud (Amazon EC2)** <br>&emsp; + Introduction to AWS (Amazon Elastic Compute Cloud) - EC2 <br>&emsp;&emsp; • Instance type <br>&emsp;&emsp; • AMI/BackUp/Keypair <br>&emsp; + Preparation steps: <br>&emsp;&emsp; • Create VPC Linux/Window <br>&emsp;&emsp; • Security group Linux/Window <br>&emsp; + Initialize Window/Linux instance <br>&emsp; + EC2 Basics: <br>&emsp;&emsp; • Change EC2 configuration <br>&emsp;&emsp; • Create snapshot <br>&emsp;&emsp; • Custom AMI <br>&emsp;&emsp; • Create instance from Custom AMI <br>&emsp;&emsp; • Access EC2 when losing keypair Linux and Window <br>&emsp;&emsp; • Configure desktop interface for EC2-ubuntu 22.04 <br>&emsp;&emsp; • Amazon EBS Snapshot archive                                                                                                                                                                                                                                                                                                                                                                          | 11/05/2026 | 12/05/2026 | <https://000004.awsstudygroup.com/vi/5-amazonec2basic/>                                                          |
| 3   | **Continue Completing EC2 Lab Practice** <br>&emsp; + Deploy Node.js app on Amazon Linux: <br>&emsp;&emsp; • Download LAMP web server <br>&emsp;&emsp; • Prepare LAMP <br>&emsp;&emsp; • Configure and install phpMyAdmin <br>&emsp;&emsp; • Install Node.js on Linux <br>&emsp;&emsp; • Deploy app on Linux instance <br>&emsp; + Deploy Node.js app on Amazon Window: <br>&emsp;&emsp; • Install XAMPP on Window instance <br>&emsp;&emsp; • Install Node.js on Window instance <br>&emsp;&emsp; • Deploy on Window instance <br>&emsp; + Limit resource usage with IAM service <br>&emsp;&emsp; • Allow usage by specific Region <br>&emsp;&emsp; • Limit EC2 by instance family <br>&emsp;&emsp; • Limit EC2 by instance type <br>&emsp;&emsp; • Limit EBS volume <br>&emsp;&emsp; • Limit resource deletion permissions <br>&emsp;&emsp; • Limit resource deletion by time range <br> **Lab Practice: Grant application permissions to access AWS services with IAM Role** <br>&emsp; + Create EC2 instance <br>&emsp; + Create S3 bucket <br>&emsp; + Use access key: Create IAM user, access key, use access key <br>&emsp; + Create IAM role <br>&emsp; + Use IAM role | 12/05/2026 | 12/05/2026 | <https://000048.awsstudygroup.com/vi/3-iamroleec2/> <br> <https://000004.awsstudygroup.com/vi/5-amazonec2basic/> |
| 4   | **Lab Practice: Using Cloud IDE in Browser with AWS Cloud9** <br>&emsp; + Overview of AWS Cloud9 <br>&emsp; + Create Cloud9 instance <br>&emsp; + Basic features: <br>&emsp;&emsp; • Use command line <br>&emsp;&emsp; • Work with text files <br>&emsp;&emsp; • Dashboard interface <br>&emsp; + Use AWS CLI <br> **Lab Practice: Hosting Static Website with Amazon S3** <br>&emsp; + Overview theory introduction <br>&emsp; + Create S3 bucket <br>&emsp; + Upload data <br>&emsp; + Enable static website feature <br>&emsp; + Configure Block Public Access <br>&emsp; + Configure public object <br>&emsp; + Check Website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | 13/05/2026 | 14/05/2026 | <https://000057.awsstudygroup.com/vi/1-introduce/> <br> <https://000049.awsstudygroup.com/vi/>                   |
| 5   | **Lab Practice: Hosting Static Website with Amazon S3 (Continued)** <br>&emsp; + Speed up static website with CloudFront <br>&emsp; + Block public access to S3 <br>&emsp; + Configure Amazon CloudFront <br>&emsp; + Check Amazon CloudFront <br>&emsp; + Bucket versioning: <br>&emsp;&emsp; • Introduction <br>&emsp;&emsp; • How it works <br>&emsp;&emsp; • Implementation guide <br>&emsp; + Move Object <br>&emsp; + Copy S3 Object to another region                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 14/05/2026 | 14/05/2026 | <https://000057.awsstudygroup.com/vi/1-introduce/>                                                               |

### Achievements for Week 2

**EC2 Core Knowledge:**

- Mastered EC2 concepts:
  <br> + Instance types
  <br> + AMI, Backup, Keypair
  <br> + Security Groups and VPC configuration
  <br> + Snapshots and Custom AMI
  <br> + Handling lost keypairs for both Linux and Windows
  <br> + Desktop GUI setup for EC2-ubuntu 22.04
  <br> + Amazon EBS Snapshot archive

- Node.js application deployment:
  <br> + LAMP stack setup on Amazon Linux
  <br> + phpMyAdmin configuration
  <br> + Node.js installation on Linux instance
  <br> + Node.js app deployment on Linux
  <br> + XAMPP setup on Windows instance
  <br> + Node.js installation on Windows instance
  <br> + Node.js app deployment on Windows

**IAM Resource Control:**

- Limited resource usage with IAM policies:
  <br> + Region-specific access control
  <br> + Instance family restrictions
  <br> + Instance type limitations
  <br> + EBS volume quotas
  <br> + Resource deletion permissions
  <br> + Time-based resource deletion policies

**IAM Role Practice:**

- Practiced granting permissions with IAM Roles:
  <br> + EC2 instance creation and configuration
  <br> + S3 bucket setup
  <br> + IAM user and access key management
  <br> + IAM role creation and usage
  <br> + Application access to AWS services

**AWS Cloud9 IDE:**

- Mastered AWS Cloud9 concepts:
  <br> + Cloud IDE overview
  <br> + Cloud9 instance creation
  <br> + Command line usage
  <br> + Text file editing
  <br> + Dashboard interface
  <br> + AWS CLI integration

**Amazon S3 Static Website Hosting:**

- Static website hosting on S3:
  <br> + S3 bucket creation
  <br> + Data upload
  <br> + Static website hosting configuration
  <br> + Block Public Access settings
  <br> + Public object configuration
  <br> + Website testing

- CloudFront CDN optimization:
  <br> + CloudFront distribution creation
  <br> + Public S3 access blocking
  <br> + CloudFront configuration
  <br> + CloudFront verification

- S3 Advanced Features:
  <br> + Bucket versioning setup and management
  <br> + Object movement between buckets
  <br> + Object replication to different regions
