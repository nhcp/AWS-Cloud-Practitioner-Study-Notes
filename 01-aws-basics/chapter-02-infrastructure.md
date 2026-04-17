# Module 1, Chapter 2: Global Infrastructure & Shared Responsibility (Master Edition)

## 🧠 Part 1: Core Theory (The "Where" and the "Who")

### 1. AWS Global Infrastructure Breakdown
AWS is built on three levels of scale. You must know the difference for the exam:
* **Regions**: Geographic areas (like Frankfurt). You choose them based on **Compliance** (Legal), **Latency** (Speed), **Cost**, and **Service Availability**.
* **Availability Zones (AZs)**: These are the "Power Houses." Each Region has at least 3 AZs. An AZ is one or more data centers. They are physically separate to provide **High Availability**.
* **Edge Locations**: These are mini-sites (over 600+) used to deliver content via **CloudFront** and **Route 53**. They bring data closer to the user to reduce "Latency."



### 2. The Shared Responsibility Model (CRITICAL THEORY)
This defines who gets blamed if something goes wrong.
* **AWS is responsible for "Security OF the Cloud"**: 
    * Infrastructure (Hardware, Software, Networking, and Facilities).
    * Managed Services (S3, RDS, Lambda).
* **You are responsible for "Security IN the Cloud"**:
    * **Data** (Encryption and Backups).
    * **IAM** (Users and Passwords).
    * **Network Security** (Security Groups/Firewalls).
    * **Operating System** (Patching your EC2 instances).

### 3. Service Scope (Global vs. Regional)
* **Global Services**: IAM, Route 53, CloudFront, WAF.
* **Regional Services**: EC2, S3, RDS, Lambda, VPC.

---

## 🏗️ Part 2: 10 Advanced Exam-Style Scenarios

| # | Scenario | Correct Concept | Explanation |
| :--- | :--- | :--- | :--- |
| 1 | A German company must keep data in the EU to follow GDPR laws. | **Region Selection** | You choose Frankfurt (`eu-central-1`) to meet compliance. |
| 2 | You want to make sure your app survives if a flood hits a data center. | **Availability Zones** | Deploying in 2+ AZs ensures "Fault Tolerance." |
| 3 | Your website in Hof is slow for users in Brazil. | **Edge Locations** | Use CloudFront to cache content in a Brazilian Edge Location. |
| 4 | A hacker enters your account because you had no MFA. Who is at fault? | **Customer** | Managing access (IAM) is the Customer's responsibility. |
| 5 | A power outage in a data center causes a hardware failure. | **AWS** | Maintaining hardware and power is AWS's responsibility. |
| 6 | You want a dedicated, private fiber connection from your office to AWS. | **AWS Direct Connect** | Bypasses the public internet for security and speed. |
| 7 | You need to download an ISO-27001 certificate for an auditor. | **AWS Artifact** | The self-service portal for compliance reports. |
| 8 | You want to run AWS services in your own physical basement. | **AWS Outposts** | Hybrid service that brings AWS hardware to your office. |
| 9 | You want to see the status of all AWS services globally. | **Service Health Dashboard** | Provides the general status of all services. |
| 10 | You want to run a serverless app. Who patches the server? | **AWS** | For serverless/managed services, AWS handles the "heavy lifting." |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A

| # | Question | Answer |
| :--- | :--- | :--- |
| 1 | **What is an Availability Zone (AZ)?** | One or more data centers with redundant power and networking inside a Region. |
| 2 | **Why should you use multiple AZs?** | To achieve High Availability and Fault Tolerance. |
| 3 | **Which service helps with "Low Latency" content delivery?** | **Amazon CloudFront** (via Edge Locations). |
| 4 | **Who is responsible for Guest OS patching on EC2?** | The Customer. |
| 5 | **What is AWS Artifact?** | A portal for downloading compliance reports and managing agreements. |
| 6 | **Name three "Global" AWS services.** | IAM, CloudFront, and Route 53. |
| 7 | **What is the difference between Service Health and Personal Health Dashboards?** | Service Health is global; Personal Health is specific to *your* resources. |
| 8 | **What is "High Availability"?** | A system design that ensures the app is up even if a component fails. |
| 9 | **What is an "AWS Region"?** | A physical location in the world that contains multiple AZs. |
| 10 | **What is "Security of the Cloud"?** | Physical security, hardware, and the software running the cloud infrastructure. |

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **Infrastructure Map**: Visit [Infrastructure.aws](https://infrastructure.aws/) and find the 3 newest regions.
2. **Ping Test**: Ping an AWS endpoint (like `s3.eu-central-1.amazonaws.com`) to see your connection speed.
3. **Artifact Exploration**: Search for "Artifact" in the AWS console and see the list of agreements.
4. **Shared Responsibility Drawing**: Draw a diagram showing the "Line" between AWS and the Customer.
5. **Git Push**: Use the commands below to sync Chapter 2 to your GitHub.
