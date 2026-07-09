---
title: "Worklog Week 8"
date: 2026-06-22
weight: 1
chapter: false
pre: ""
---

### Week 8 Objectives:

- Create project structure/architecture design within 2 days.
- Finalize architecture diagrams for proposal and workshop.
- Practice main workshop content.
- Begin converting workshop content into clear report files.

### Tasks for This Week:

| Day | Task | Start Date | End Date | Resource |
| --- | --- | --- | --- | --- |
| 2 | **Draw Project Structure - Day 1** <br>&emsp; + Identify architecture layers: Frontend/Auth, Storage, Backend/AI-ML, Monitoring/Security <br>&emsp; + Sketch the processing flow from image upload to result storage <br>&emsp; + Select appropriate AWS services for each layer | 22/06/2026 | 22/06/2026 | [Proposal](/Content/2.%20Proposal/_proposal.md) |
| 3 | **Draw Project Structure - Day 2** <br>&emsp; + Complete architecture diagram <br>&emsp; + Verify the flow S3 -> SQS -> Lambda -> Rekognition/Textract -> DynamoDB <br>&emsp; + Add CloudWatch and IAM to the diagram | 23/06/2026 | 23/06/2026 | [DiagramStructure](/Content/2.%20Proposal/image/DiagramStructure.png) |
| 4 | **Practice Workshop Content** <br>&emsp; + Prepare IAM Role for Lambda <br>&emsp; + Create SQS queue to receive image processing events <br>&emsp; + Configure S3 bucket and event notification | 24/06/2026 | 24/06/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |
| 5 | **Edit Workshop Report** <br>&emsp; + Review overview, IAM, SQS, and S3 sections <br>&emsp; + Standardize descriptions for each practice step <br>&emsp; + Add illustrative images and verification results | 25/06/2026 | 25/06/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |

### Results Achieved in Week 8

**Architecture Design:**

- Completed the overall project structure:
  <br> + Frontend/Auth using Amplify, Cognito, API Gateway
  <br> + Storage using Amazon S3
  <br> + Backend processing using SQS and Lambda
  <br> + AI/ML using Rekognition and Textract
  <br> + Data layer using DynamoDB
  <br> + Monitoring/Security using CloudWatch and IAM

**Workshop Practice:**

- Practiced fundamental workshop steps:
  <br> + Created IAM Role
  <br> + Created SQS queue
  <br> + Configured S3
  <br> + Prepared Lambda function

- Began converting practice content into a structured workshop report.
