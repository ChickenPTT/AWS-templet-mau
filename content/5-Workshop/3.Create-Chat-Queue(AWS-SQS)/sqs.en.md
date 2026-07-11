---
title: "Create an Amazon SQS Message Queue"
date: 2026-06-21
weight: 3
chapter: false
pre: ""
---

# Step 2: Create an Amazon SQS Message Queue

### Introduction

Amazon SQS acts as an intermediate message queue between Amazon S3 and AWS Lambda.

When a user uploads an image to S3, S3 sends a notification to SQS. Lambda then reads messages from SQS and processes them gradually, helping the system remain stable when many images are uploaded at the same time.

---

### Implementation Steps

1. Open the **AWS Console**, search for **Amazon SQS**, then choose **Create queue**.

![Search for Amazon SQS](images/image13.png)

2. Select **Standard Queue**.

Do not select **FIFO Queue** in this workshop because the goal is asynchronous image processing with high scalability. Strict ordering is not required.

![Select Standard Queue](images/image14.png)

3. Name the queue **image-processing-queue**.

![Name the SQS queue](images/image15.png)

4. Configure the important queue settings.

![Configure SQS settings](images/image16.png)

![Review SQS configuration](images/image17.png)

5. Choose **Create queue** to create the queue.

6. After the queue is created, copy its **ARN**. This ARN will be used in the S3 Event Notification configuration step.

![Copy the SQS queue ARN](images/image18.png)
