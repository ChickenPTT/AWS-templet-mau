---
title: "Blogs Posted"
date: 2026-07-13
weight: 3
chapter: false
pre: " <b> 3. </b> "
---



This section lists and introduces the blogs you have posted to [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

###  [Blog 1 - S3 INTELLIGENT-TIERING – WHEN STORAGE "KNOWS" WHERE IT SHOULD LIVE](3.1-Blog1/index.md)
This blog introduces S3 Intelligent-Tiering, a storage class that automatically observes each object's access behavior and places it in the appropriate cost tier without human intervention. It features 3 fully automatic access tiers (Frequent Access, Infrequent Access, Archive Instant Access) and 2 additional archive tiers for deeper savings, making it ideal for data lakes with diverse data sources where predicting access patterns is nearly impossible.

###  [Blog 2 - HOW SAMSUNG ACHIEVED REAL-TIME PRICING WITH AWS LAMBDA RESPONSE STREAMING](3.1-Blog2/_index.md)
This blog explains how Samsung leveraged AWS Lambda Response Streaming to eliminate the latency challenge in their global e-commerce system. By removing intermediate caching layers and querying the Pricing Engine directly in real time, they achieved a 98% reduction in P90 latency (from 4,500ms to 50ms) and dramatically reduced infrastructure costs from over 100 auto-scaled instances to just 5–10 Lambda functions.

###  [Blog 3 - ENSURING FAIR PLAY BY DETECTING AND PREVENTING PROFILE ALTERATIONS WITH AMAZON TEXTRACT](3.1-Blog3/index.md)
This blog presents a Serverless architecture using Amazon Textract to automatically detect and blur text in gaming profile pictures to prevent collusion and cheating. The solution processes images uploaded to S3, extracts text coordinates with Textract, applies Gaussian Blur to sensitive information areas, and sends alerts via SNS. This approach provides high AI accuracy, automatic scaling, and cost optimization without managing any servers.