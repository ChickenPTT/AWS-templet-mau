---
title: "Create and Code an AWS Lambda Function"
date: 2026-06-21
weight: 5
chapter: false
pre: ""
---

# Step 4: Create and Code an AWS Lambda Function

### Objective

In this step, you will create a Lambda Function that receives messages from Amazon SQS, reads information about images uploaded to Amazon S3, and calls AI services such as Amazon Rekognition and Amazon Textract to analyze the images.

---

### 4.1 - Create a Lambda Function

1. Open **AWS Lambda** and choose **Create function**.

![Open AWS Lambda](/images/5-Workshop/5.5-Policy/image1.png)

2. Select **Author from scratch**.

![Select Author from scratch](/images/5-Workshop/5.5-Policy/image2.png)

![Create Lambda function](/images/5-Workshop/5.5-Policy/image3.png)

3. Configure the Lambda Function.

![Configure Lambda function](/images/5-Workshop/5.5-Policy/image4.png)

![Select runtime and role](/images/5-Workshop/5.5-Policy/image5.png)

Suggested configuration:

- Function name: **image-quality-processor**
- Runtime: **Python 3.x**
- Execution role: select the IAM Role **Lambda-ImageProcessing-Role** created in Step 1

4. Choose **Create function**.

![Create function](/images/5-Workshop/5.5-Policy/image6.png)

5. Open the **Configuration** tab, choose **General configuration**, then choose **Edit**.

![Open General configuration](/images/5-Workshop/5.5-Policy/image7.png)

6. Set **Timeout = 60 seconds**, then save the configuration.

![Set Lambda timeout](/images/5-Workshop/5.5-Policy/image8.png)

---

### 4.2 - Attach SQS as a Trigger

1. On the Lambda Function page, choose **Add trigger**.

![Add trigger to Lambda](/images/5-Workshop/5.5-Policy/image9.png)

2. Select **SQS** as the source.

![Select SQS trigger](/images/5-Workshop/5.5-Policy/image10.png)

3. Select the **image-processing-queue** queue.

4. Configure **Batch size = 1**.

A batch size of 1 lets Lambda process one message at a time, which is suitable for this lab because it makes logs easier to observe and debug.

5. Choose **Add**.

![Configure SQS trigger](/images/5-Workshop/5.5-Policy/image11.png)

---

### 4.3 - Write Python Code

1. Open the **Code** tab.

2. Remove the sample code, paste the following Python code that processes SQS messages, then choose **Deploy** to save the code.

![Write Lambda code and deploy](/images/5-Workshop/5.5-Policy/image12.png)

Sample code:

```python
import json
import urllib.parse

import boto3

s3 = boto3.client("s3")
rekognition = boto3.client("rekognition")
textract = boto3.client("textract")


def lambda_handler(event, context):
    for record in event["Records"]:
        body = json.loads(record["body"])

        for s3_record in body.get("Records", []):
            bucket = s3_record["s3"]["bucket"]["name"]
            key = urllib.parse.unquote_plus(s3_record["s3"]["object"]["key"])

            print(f"Processing image: s3://{bucket}/{key}")

            labels = rekognition.detect_labels(
                Image={
                    "S3Object": {
                        "Bucket": bucket,
                        "Name": key
                    }
                },
                MaxLabels=10,
                MinConfidence=70
            )

            print("Rekognition labels:")
            for label in labels["Labels"]:
                print(f"- {label['Name']}: {label['Confidence']:.2f}%")

            text_result = textract.detect_document_text(
                Document={
                    "S3Object": {
                        "Bucket": bucket,
                        "Name": key
                    }
                }
            )

            print("Textract text:")
            for block in text_result["Blocks"]:
                if block["BlockType"] == "LINE":
                    print(block["Text"])

    return {
        "statusCode": 200,
        "body": "Processed SQS messages successfully"
    }
```
