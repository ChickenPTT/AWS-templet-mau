---
title: "Clean Up Resources"
date: 2026-06-21
weight: 7
chapter: false
pre: ""
---

# Step 6: Clean Up Resources

### Objective

After completing the workshop, delete the resources you created to avoid unnecessary charges.

---

### 1. Delete the SQS Queue

1. Open **Amazon SQS**.

2. Select the queue created in the workshop, then choose **Delete**.

![Delete SQS queue](/images/5-Workshop/5.7-CleanUp/image1.png)

3. Enter **Confirm** to confirm the queue deletion.

![Confirm SQS queue deletion](/images/5-Workshop/5.7-CleanUp/image2.png)

---

### 2. Delete the Lambda Function

1. Open **AWS Lambda**.

2. Select the function created in the workshop, then choose **Delete**.

![Delete Lambda function](/images/5-Workshop/5.7-CleanUp/image3.png)

3. Enter the confirmation text to delete the function.

![Confirm Lambda function deletion](/images/5-Workshop/5.7-CleanUp/image4.png)

---

### 3. Delete the S3 Bucket

1. Open **Amazon S3**.

2. Open the bucket created in the workshop.

3. Select the bucket to delete, then choose **Delete**.

Note: The S3 bucket must be empty before deletion. If the bucket still contains objects, delete all objects in the bucket first.

![Delete S3 bucket](/images/5-Workshop/5.7-CleanUp/image5.png)

---

### 4. Delete the IAM Role

1. Open **IAM**.

2. Select **Roles**.

3. Select the IAM Role **Lambda-ImageProcessing-Role** created in the workshop, then delete the role.

![Delete IAM Role](/images/5-Workshop/5.7-CleanUp/image6.png)
