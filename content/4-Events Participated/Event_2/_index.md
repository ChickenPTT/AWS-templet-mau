---
title: "AWS AI & Cloud Operations Workshop"
date: 2026-06-12
weight: 4
chapter: false
pre: " <b> 4.3. </b> "
---

# Reflection on "AWS AI & Cloud Operations Workshop"

### Event Objectives

- Update knowledge about AI Agent adoption in cloud operations, DevOps, and incident response.
- Explore real-world AI Voice challenges, including Vietnamese language handling, response latency, and natural conversation design.
- Understand how AI can support enterprise workflows such as recruiting, onboarding, candidate evaluation, and HR process optimization.
- Connect the event knowledge with the AWS cost estimation proposal for a serverless damaged-goods detection and processing system.

### Speakers

- **Truong Tran** - AI Solution Sales, Noventiq
- **Steve Tran** - CTO/Founder, CloudThinker
- **Trung Vu** - CEO, Revve AI
- **Anh Dang** - Solution Sales, Noventiq
- **Nghi Danh** - AI Engineer, Renova Cloud
- **Kiet Tran** - AI Engineer, AWS Student Builder Group
- **Bao Phan** - Cloud Engineer, Cloud Kinetics
- **Nguyen Nguyen** - Cloud Engineer, Cloud Kinetics
- **Toan Nguyen** - AWS Security Builder

---

### Key Highlights

#### AgenticOps for Your Cloud

**Steve Tran** shared the current challenges of operating complex microservices systems in the cloud. When logs, tracing, metrics, and alerts are scattered across multiple tools, engineers often spend significant time investigating the root cause of incidents.

- **Cloud operations reality**: Modern systems contain many independent components, making monitoring, troubleshooting, and incident response more difficult.
- **AgenticOps approach**: AI Agents can automate investigation steps, summarize operational data, and suggest response options, reducing analysis time from hours to minutes.
- **Operating workflow**:
  - **Classification**: Categorize incidents from alerts or direct requests.
  - **Investigation**: Analyze logs, metrics, topology, and possible root-cause hypotheses.
  - **Mitigation**: Suggest safe remediation options for engineers to review and apply.
  - **Optimization**: Recommend long-term improvements to prevent repeated issues.

#### AI Voice

The session by **Trung Vu**, **Nghi Danh**, and **Kiet Tran** focused on building low-latency voice conversation experiences that work well for Vietnamese users.

- **Latency requirement**: Natural voice interaction requires streaming across Speech-to-Text, LLM processing, and Text-to-Speech instead of waiting for a full sentence to complete.
- **Vietnamese language challenges**: AI needs to understand pronouns, gender references, context, and communication tone to avoid unnatural or disrespectful responses.
- **Regional accent handling**: Training data should include a reasonable amount of regional accents to improve recognition, while avoiding behavior where AI imitates a user's accent in an unprofessional way.

#### Technical and Practical Aspects of DevOps Agent

The speakers demonstrated a scenario where a website becomes slow or unstable due to a sudden increase in traffic. In a traditional setup, engineers must manually check several dashboards to collect logs, tracing, and metrics. With an AI Agent, that process can be automated in a controlled way.

- **Incident investigation**: AI Agent can summarize observable data, generate system topology, and propose hypotheses about the cause of an issue.
- **Extensibility**: The Agent can integrate with MCP (Model Context Protocol), Slack, ServiceNow, and other operations tools.
- **Security consideration**: The Agent should only access explicitly authorized data. If logs are not exported to CloudWatch or a central observability system, it should not automatically SSH into servers to collect data.
- **Live demo**: In a simulated DDoS case with 1,000 requests per second to an ALB, the AI Agent identified 10 spammed ECS Tasks and suggested commands to stop the affected tasks.

#### Real-World Case Studies

- **An online university**: Reduced MTTR from 2 hours to 28 minutes, around 77% faster.
- **Zenchef restaurant technology platform**: Detected a misconfiguration within about 20 minutes.

#### AI and Human Resources in Enterprise

The session by **Truong Tran** and **Anh Dang** discussed how AI can support HR teams in recruitment and workforce operations.

- **Talent retention**: Companies need to reduce the risk of losing employees after training and onboarding.
- **Candidate evaluation**: AI can compare CVs with job descriptions, analyze skills, evaluate experience, and estimate job fit.
- **Onboarding automation**: AI can shorten the time required for new employees to understand internal processes, documents, and systems.
- **No-code/low-code with Amazon Q**: HR users can build recruitment management or profile analysis applications without complex programming.
- **Live demo**: Amazon Q was used to generate a Junior Cloud Engineer job description, compare candidates by technical skills, problem solving, and communication, and provide a salary benchmark.

---

### What I Learned

#### Cloud Operations Thinking with AI Agent

- AI Agent does not fully replace operations engineers; it acts as an assistant for data analysis, context gathering, and response recommendation.
- Observability is essential in cloud systems. Logs, metrics, traces, and alerts must be designed well before an Agent can analyze them reliably.
- Incident response should follow a clear flow: classify the issue, investigate the cause, mitigate impact, and optimize the system for the long term.

#### Building AI Voice Applications

- AI Voice experience depends heavily on latency and continuous streaming across system components.
- Vietnamese introduces specific challenges such as pronouns, regional accents, and conversation context.
- Training data must be selected carefully to balance accuracy, naturalness, and professional behavior.

#### Applying AI in Enterprise Workflows

- AI can automate repetitive work in recruiting, CV analysis, interview scheduling, and onboarding.
- Tools such as Amazon Q help business users create internal applications faster, especially for workflows with many data points and evaluation criteria.
- AI adoption in enterprises must pay attention to data permissions, transparency, and final human control over decisions.

---

### Application to the AWS Proposal and Project

- **Operational design for the serverless system**: AgenticOps concepts can be applied to the AWS damaged-goods detection system by standardizing logs from Lambda, API Gateway, SQS, S3, Rekognition, Textract, and DynamoDB into CloudWatch.
- **Cost optimization through observability**: The AWS cost proposal estimates that the test workload remains within the Free Tier. When scaling up, service-level usage metrics should be monitored to control cost and detect abnormal usage early.
- **Improve image processing reliability**: AI Agent can help inspect failures in the S3 -> SQS -> Lambda -> Rekognition/Textract -> DynamoDB pipeline, especially when image processing fails or AI confidence is low.
- **Improve user experience**: AI Voice knowledge can support future voice-based data entry, allowing warehouse staff to report damaged goods faster.

---

### Workshop Implementation Details

#### Asynchronous Image Processing Flow

The workshop builds an event-driven image processing pipeline for the case where many users upload images at the same time. Instead of invoking Lambda directly for every upload, **Amazon SQS** is used as a buffer between **Amazon S3** and **AWS Lambda**, making the system more stable and easier to scale.

- **Amazon S3** stores raw uploaded images and sends an event notification when a new object is created.
- **Amazon SQS** receives the S3 event message and queues it for controlled processing.
- **AWS Lambda** is triggered by SQS, reads each message, downloads the image from S3, and processes it with AI services.
- **Amazon Rekognition** detects image labels and can support damaged-package identification.
- **Amazon Textract** extracts text from shipping labels, such as tracking codes, route information, phone numbers, or address details.
- **Amazon CloudWatch Logs** stores the Lambda output for validation, debugging, and operational visibility.

#### IAM and Security Preparation

The workshop creates an IAM role named **Lambda-ImageProcessing-Role** for the Lambda function. This role grants Lambda the required permissions to read S3 objects, consume SQS messages, call Rekognition and Textract, and write logs.

In a production environment, the workshop notes that managed policies should be replaced with custom policies scoped to the exact bucket, queue, and services required. This follows the **least privilege** principle and reduces unnecessary access.

#### Testing, Validation, and Cleanup

The testing step validates the full **S3 -> SQS -> Lambda -> AI** flow by uploading test images to S3, checking Lambda execution in CloudWatch Logs, and confirming that the SQS queue becomes empty after processing.

The cleanup step removes SQS, Lambda, S3, and IAM resources created during the lab. This is important because the cost proposal assumes a controlled test workload and Free Tier usage; unused resources should be removed to avoid unexpected charges.

#### Cost Connection from the Proposal

The proposal estimates the system with about **245 images per week** and around **30 active users**. The architecture includes Amplify, Cognito, API Gateway, S3, SQS, Lambda, Rekognition, Textract, DynamoDB, SNS, CloudWatch, and IAM.

For a new AWS account under the stated Free Tier assumptions, the expected actual one-week cost is **$0.00**. Without Free Tier, the same workload is estimated at about **$1.57** for one week. This makes the workshop architecture suitable for learning, validation, and small-scale testing before scaling to production.

---

### Event Experience

The event provided a practical view of how AI is being applied to cloud operations, DevOps, and enterprise workflows. The most useful point was that the sessions went beyond general AI ideas and showed concrete scenarios such as incident investigation, log analysis, MTTR reduction, Vietnamese voice processing, and recruiting automation.

- **Practical learning environment**: Participants heard specific case studies from cloud operations, AI Voice, and HR automation.
- **Clear technical perspective**: The speakers explained how AI Agent can work with telemetry, MCP, CloudWatch, and operations tools to support engineers.
- **Strong connection to my AWS project**: The event reinforced that an AWS system should not only run correctly, but also be observable, cost-aware, and easier to troubleshoot.

#### Some photos from the event

<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
  <img src="/Content/4.%20Events%20Participated/Image_event/event2-1.png" alt="AWS AI and Cloud Operations Workshop 1" width="45%" />
  <img src="/Content/4.%20Events%20Participated/Image_event/event2-2.png" alt="AWS AI and Cloud Operations Workshop 2" width="45%" />
</div>
