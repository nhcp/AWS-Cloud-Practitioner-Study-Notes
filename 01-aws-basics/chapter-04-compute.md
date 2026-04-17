# Module 1, Chapter 4: Compute Services (The Engine of AWS)

## 🧠 Part 1: Deep Theory (Control vs. Convenience)

In AWS, "Compute" refers to the processing power required to run applications. The services are categorized by how much of the underlying server you have to manage.

### 1. Amazon EC2 (Elastic Compute Cloud)
* **Definition**: Virtual servers in the cloud.
* **Service Model**: **IaaS** (Infrastructure as a Service).
* **Key Concept**: You have full control over the Operating System (Linux/Windows), the CPU, and the RAM.
* **Instance Types**: Optimized for different tasks (e.g., T-type for general use, C-type for Compute, R-type for RAM/Memory).

### 2. AWS Lambda
* **Definition**: A serverless, event-driven compute service.
* **Service Model**: **PaaS / Serverless**.
* **Key Concept**: You upload your code; AWS runs it only when triggered (e.g., a file is uploaded or a button is clicked). 
* **Scaling**: Scales automatically from zero to thousands of requests. You pay only for the milliseconds your code runs.

### 3. Container Services (ECS, EKS, and Fargate)
* **Amazon ECS/EKS**: Orchestration services for running Docker/Kubernetes containers.
* **AWS Fargate**: The "Serverless" way to run containers. You don't manage the underlying EC2 instances.

### 4. Amazon Lightsail
* **Definition**: A simplified, low-cost "all-in-one" solution for small websites (WordPress, simple blogs). It includes compute, storage, and networking in one flat monthly price.

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Service / Option | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You need to run a legacy accounting software that requires a specific version of Windows. | **Amazon EC2** | EC2 gives you full "OS-level" control to install custom software. |
| 2 | You want to run a small script to resize photos only when a user uploads them. | **AWS Lambda** | Lambda is perfect for "event-driven" tasks where you don't want a server running 24/7. |
| 3 | You want to save 70% on costs for a database server that you know will run for 3 years. | **EC2 Reserved Instances** | Reserved Instances (RI) provide massive discounts for long-term commitments. |
| 4 | You have a massive data analysis job that can be stopped and started without losing progress. | **EC2 Spot Instances** | Spot Instances use spare AWS capacity for up to 90% off, but can be taken back by AWS. |
| 5 | You want to launch a simple WordPress blog for your local bakery in Hof. | **Amazon Lightsail** | Lightsail is the easiest, lowest-cost way to start a simple website. |
| 6 | Your website traffic doubles every Friday night. You want the servers to grow automatically. | **Amazon EC2 Auto Scaling** | Auto Scaling adds/removes instances based on traffic or schedules. |
| 7 | You want to run Docker containers but you don't want to manage or patch the servers. | **AWS Fargate** | Fargate is the "Serverless" engine for containers. |
| 8 | You need a physical server dedicated entirely to your business for regulatory reasons. | **EC2 Dedicated Host** | Dedicated hosts ensure no other customers share the physical hardware. |
| 9 | You want to distribute incoming web traffic across a group of 10 EC2 instances. | **Elastic Load Balancing (ELB)** | ELB acts as the "Traffic Cop" to ensure no single server is overwhelmed. |
| 10 | You want to test a new application for 2 hours and then delete it. | **EC2 On-Demand** | On-Demand is for short-term, unpredictable workloads with no commitment. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A

| # | Question | Answer |
| :--- | :--- | :--- |
| 1 | **What is an AMI (Amazon Machine Image)?** | A template that contains the OS, software, and configuration needed to launch an EC2 instance. |
| 2 | **What is "Serverless"?** | A model where the cloud provider manages the server infrastructure, and you only care about the code. |
| 3 | **What is the maximum execution time for an AWS Lambda function?** | 15 minutes. |
| 4 | **Difference between Vertical and Horizontal Scaling?** | Vertical (Up/Down) is making one server bigger; Horizontal (In/Out) is adding more servers. |
| 5 | **What is a "Fleet" in EC2?** | A collection of EC2 instances (On-Demand, Spot, or RI) working together as one unit. |
| 6 | **What is the benefit of an Elastic Load Balancer (ELB)?** | It increases "Fault Tolerance" by redirecting traffic away from unhealthy servers. |
| 7 | **What is AWS Batch?** | A service that runs hundreds of thousands of batch computing jobs efficiently. |
| 8 | **When should you NOT use AWS Lambda?** | For long-running processes (over 15 mins) or apps that require high-performance disk access. |
| 9 | **What is "Pay-as-you-go" in the context of Lambda?** | You are billed based on the number of requests and the duration (time) your code runs. |
| 10 | **Can you change the Instance Type of a running EC2?** | No. You must stop the instance, change the type (e.g., t2 to t3), and then start it again. |

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **AMI Selection**: Go to the EC2 console and list three different operating systems available in the "Quick Start" menu.
2. **Pricing Compare**: Use the AWS Pricing Calculator to see the cost of a `t3.large` instance in Frankfurt vs. North Virginia.
3. **Security Groups**: Research the difference between "Inbound" and "Outbound" rules for an EC2 firewall.
4. **Lambda Trigger**: List 3 AWS services that can "trigger" a Lambda function (e.g., S3, DynamoDB, API Gateway).
5. **Git Sync**: Use the commands below to finalize Chapter 4 on your GitHub.
