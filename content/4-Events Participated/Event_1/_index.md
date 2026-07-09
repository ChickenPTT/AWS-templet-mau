---
title: "AWS Community Day 2026"
date: 2026-05-23
weight: 4
chapter: false
pre: " <b> 4.2. </b> "
---

# Reflection on "AWS Community Day Workshop"

### Event Objectives

- Share best practices for designing modern applications and building effective learning habits.
- Provide practical knowledge, technical insights, and real-world case studies related to Amazon CloudFront.
- Introduce advanced AI tools and models that support optimization across the software development lifecycle.

### Speakers

- **Vy Lam** - Senior Business Systems Analyst, VPBank
- **Duc Dao** - Solutions Architect, Cloud Kinetics
- **Thao Nguyen** - GenAI Engineer
- **Mai Nguyen** - GenAI Engineer
- **Uyen Le** - GenAI Engineer
- **Anh Pham** - Cloud Consultant, G-AsiaPacific Vietnam
- **Tinh Truong** - Platform Engineer, GoTymeX
- **Thinh Nguyen** - DevOps Engineer, FCAJ

---

### Key Highlights

#### Practical Project Experience from the 36H Code Competition

- The GenAI Engineer team (**Thao Nguyen, Mai Nguyen, Uyen Le**) shared how they handled time pressure during a 36-hour coding challenge.
- They explained how to break a large problem into smaller tasks and use Generative AI to speed up coding, testing, and prototype completion.

#### AI Trends and AI-First Thinking

- **AI-first mindset**: Rethinking how problems are solved by placing AI at the center of workflows and system optimization.
- **Second AI Brain**: Building an AI-supported knowledge assistant that helps store information, analyze data, and support better decisions.

#### Track Line Content Mean Framework

The workshop introduced a structured way to communicate technical ideas clearly and persuasively through four core elements:

- **Goal**: Define the final outcome that needs to be achieved.
- **Situation**: Evaluate the current context and real conditions objectively.
- **Constraints**: Identify limitations, blockers, and technical or resource boundaries.
- **Evidence**: Use data, examples, and real proof to support the argument.

#### LLM Settings and Optimization

The session explained how LLM configuration affects model behavior, creativity, cost, and safety:

- _Model selection_: Choosing the right model based on technical and business requirements.
- _Temperature_: Controlling randomness and creativity in generated responses.
- _Max tokens_: Limiting output length to manage cost and keep responses focused.
- _Role/system prompts_: Defining the role, context, and expected response style of the AI.
- _Fine-tuning/adapters_: Customizing models for domain-specific data and workflows.
- _Safety & moderation_: Applying filters to reduce harmful, sensitive, or inappropriate outputs.

#### Performance Optimization with Amazon CloudFront

- The workshop covered core CDN concepts and how Amazon CloudFront distributes content globally.
- It also introduced best practices such as caching strategies and edge security to reduce latency and bandwidth usage.

---

### What I Learned

#### Teamwork and Practical Execution

- **Effective role allocation**: Understanding each member's strengths helps distribute tasks more efficiently in time-limited projects such as hackathons.
- **Using AI in the workflow**: GenAI can support repetitive tasks, speed up implementation, and give the team more time for architecture and logic.

#### Architecture and System Design Thinking

- The **Goal -> Situation -> Constraints -> Evidence** framework is useful for presenting technical solutions clearly to stakeholders.
- Understanding LLM settings helps improve AI application accuracy and reduce hallucination.
- CloudFront configuration requires both architecture knowledge and operational thinking to improve content delivery performance.

---

### Connection to the Workshop and AWS Proposal

- **Event-driven image processing**: The workshop project applies the same cloud architecture thinking by building an asynchronous image processing flow with **Amazon S3 -> Amazon SQS -> AWS Lambda**.
- **AI services in practice**: The Lambda function receives SQS messages, reads uploaded images from S3, calls **Amazon Rekognition** to detect image labels or damaged package conditions, and calls **Amazon Textract** to extract text such as tracking codes and label information.
- **Operational visibility**: Results are written to **Amazon CloudWatch Logs**, making it easier to validate the pipeline and troubleshoot failed processing steps.
- **Security mindset**: The IAM preparation step reinforces the least-privilege principle. Lambda should receive only the permissions needed to read from S3, consume SQS messages, call Rekognition/Textract, and write logs.
- **Cost awareness**: The AWS proposal estimates a one-week test workload of about **245 images** and **30 active users**. Under AWS Free Tier assumptions, the expected actual cost is **$0.00**, while the standard-price estimate without Free Tier is about **$1.57**.
- **Cleanup discipline**: The workshop includes deleting SQS, Lambda, S3, and IAM resources after testing to avoid unnecessary charges.

---

### Application to Work and Study

- **Build a personal second brain**: Use AI tools to summarize learning materials, store project knowledge, and support technical study.
- **Optimize prompts**: Apply system prompts and temperature settings based on task type, such as using a lower temperature for precise coding and a higher one for test case ideas.
- **Practice cloud architecture**: Configure Amazon CloudFront for personal projects or assignments to improve page loading and static asset delivery.
- **Improve presentation skills**: Use the Track Line Content Mean structure for project reports, progress updates, and technical presentations.

---

### Event Experience

Joining **AWS Community Day** provided an energetic and practical learning environment. The sessions connected classroom knowledge with real industry experience through technical talks, case studies, and architecture examples.

- **Technology networking space**: Listening directly to experts from VPBank, Cloud Kinetics, GoTymeX, and other companies helped narrow the gap between theory and real-world practice.
- **Inspiration from practical competitions**: The 36H Code story highlighted persistence, pressure handling, and a learning-by-doing mindset.
- **Visual and practical learning**: The workshop included real case studies and architecture diagrams, making the technical concepts easier to understand.

#### Some photos from the event

<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
  <img src="/Content/4.%20Events%20Participated/Image_event/2.png" alt="AWS Community Day Workshop 1" width="45%" />
  <img src="/Content/4.%20Events%20Participated/Image_event/Haiz.png" alt="AWS Community Day Workshop 2" width="45%" />
</div>
