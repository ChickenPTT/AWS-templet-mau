---
title: "Test the System"
date: 2026-06-21
weight: 6
chapter: false
pre: ""
---

# Step 5: Test the System

### Objective

Confirm that the full **S3 -> SQS -> Lambda -> AI** flow works correctly.

In this step, you will upload images to S3, verify that Lambda processes messages from SQS, and review the analysis results in CloudWatch Logs.

---

### 5.1 - Prepare Test Images

Prepare at least two types of images:

- Images of dented or torn packages to test whether Amazon Rekognition detects the image content correctly.
- Images with clear shipping labels or tracking codes to test whether Amazon Textract extracts text correctly.

---

### 5.2 - Upload Images to S3

1. Open the S3 bucket **logistics-raw-images-&lt;your-name&gt;**, then choose **Upload**.

2. Upload about **5-10 images** at the same time to test parallel processing.

3. Choose **Upload** to start uploading the images.

![Upload images to S3](images/image13.png)

![Finish uploading images](images/image14.png)

---

### 5.3 - Check CloudWatch Logs

1. Open **CloudWatch** and choose **Log groups**.

2. Find the log group **/aws/lambda/image-quality-processor**.

3. Select the latest log stream and check the output from Lambda.

![Check CloudWatch Log groups](images/image15.png)

![Check Lambda output](images/image16.png)

---

### 5.4 - Check That SQS Has Been Fully Processed

1. Open the **SQS Console** and select **image-processing-queue**.

2. Choose **Send and receive messages**.

3. Choose **Poll for messages**.

If the queue is empty, Lambda has successfully processed all messages.

![Check messages in SQS](images/image17.png)
