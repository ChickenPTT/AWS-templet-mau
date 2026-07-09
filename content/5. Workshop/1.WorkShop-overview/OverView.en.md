---
title: "Workshop Overview"
date: 2026-06-21
weight: 2
chapter: false
pre: ""
---

# Build an Asynchronous Image Processing Flow with Amazon S3, SQS, and AWS Lambda

### Workshop Summary

This workshop guides you through building an asynchronous image processing flow using an event-driven architecture on AWS. The goal is to handle the case where many users upload images at the same time while keeping the system stable, scalable, and cost-aware.

---

### Main Objectives

- Design an **S3 -> SQS -> Lambda** architecture to process images through a queue, preventing Lambda from being invoked too aggressively when many uploads happen at the same time.
- Write a Lambda function in Python to:
  - Receive messages from SQS that contain S3 events.
  - Download images from S3.
  - Call Amazon Rekognition to detect labels or identify package conditions, such as damaged parcels.
  - Call Amazon Textract to extract text from package labels, such as tracking codes, route information, phone numbers, and other details.
  - Write processing results to CloudWatch Logs for observation and testing.

### What You Will Learn

- Why SQS is needed as a buffer between S3 and Lambda in high-load systems.
- How to configure an IAM Role using the least privilege principle.
- How to create and configure:
  - An S3 bucket and Event Notification.
  - An SQS Standard Queue with important settings such as Visibility Timeout and retention.
  - A Lambda trigger from SQS with a small batch size for easier observation.
- How to run end-to-end testing and validation.
- How to clean up resources to avoid unnecessary costs.
