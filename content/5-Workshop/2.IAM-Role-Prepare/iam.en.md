---
title: "Prepare IAM Role for Lambda"
date: 2026-06-21
weight: 2
chapter: false
pre: ""
---

# Step 1: Prepare an IAM Role for Lambda

### Introduction

An IAM Role defines the permissions that Lambda uses to access the AWS services required in this workshop, such as Amazon S3, Amazon SQS, Amazon Rekognition, and Amazon Textract.

In this step, you will create an IAM Role for Lambda and attach the required policies so Lambda can read data, receive messages, and write logs while processing images.

---

### Implementation Steps

1. Open the **AWS Console** and search for the **IAM** service.

![Search for IAM service](images/image1.png)

2. Select **Roles**, then choose **Create role**.

![Select Roles and Create role](images/image2.png)

3. In **Trusted entity type**, select **AWS service**.

4. In **Use case**, select **Lambda**, then choose **Next**.

![Select AWS service and Lambda](images/image3.png)

5. Search for and attach the required policies for Lambda.

![Search for Lambda policies](images/image4.png)

![Select Lambda policies](images/image5.png)

![Attach AWSLambdaBasicExecutionRole](images/image6.png)

![Attach AmazonS3ReadOnlyAccess](images/image7.png)

![Attach AmazonSQSFullAccess](images/image8.png)

![Attach Rekognition and Textract policies](images/image9.png)

6. Name the role **Lambda-ImageProcessing-Role**, then choose **Create role**.

![Name the IAM Role](images/image10.png)

![Create IAM Role](images/image11.png)

---

### Security Note

In a real production environment, instead of using broad AWS managed policies, you should write a **Custom Policy** that limits access to only the specific bucket, queue, and services required by the application.

This follows the **Least Privilege** security best practice: grant only the permissions that are necessary and avoid excessive access.

![Custom policy following least privilege](images/image12.png)
