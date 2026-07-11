---
title: "Workshop"
date: 2026-07-11
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Automated Goods Quality Monitoring Solution based on Serverless and AI/ML

#### Overview

This workshop guides you through building an automated goods quality monitoring system based on Serverless architecture and Artificial Intelligence (AI/ML) on AWS. The system allows delivery personnel or customers to take photos of damaged packages (torn, broken, dented, or damaged) and upload them directly to the system for automatic analysis.

The system uses Amazon Rekognition to analyze product images and detect damage signs, Amazon Textract to extract shipping information, store evidence, and send alerts to relevant departments. This reduces incident processing time from hours or days to just seconds.

#### Content

1. [Workshop Overview](1.WorkShop-overview/index.md)
2. [Prepare IAM Role](2.IAM-Role-Prepare/index.md)
3. [Create Chat Queue with AWS SQS](3.Create-Chat-Queue(AWS-SQS)/index.md)
4. [Configure S3 and Event Notification](4.Congif-Save-And-Event(AWS-S3)/index.md)
5. [Create and Code Lambda Function](5.CreateAndCode-LambdaFunction/index.md)
6. [Testing and Validation](6.Testing-Validation/index.md)
7. [Clean Up Resources](7.CleanUp/index.md)