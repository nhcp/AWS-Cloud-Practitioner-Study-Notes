# Module 1, Chapter 8: Monitoring, Logging, and AI

## 🧠 Part 1: Deep Theory (Observe & Innovate)
1.  **Amazon CloudWatch**: Monitors **Performance**. It tracks Metrics (CPU usage), Logs, and Alarms.
2.  **AWS CloudTrail**: Monitors **API Calls**. It tracks "Who did what, when, and from where." (Auditing).
3.  **AWS Trusted Advisor**: An automated "Consultant" that scans your account and gives advice on Cost, Security, and Performance.
4.  **Amazon Bedrock**: The new "Serverless" way to build Generative AI apps using Foundation Models (FMs).

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Service | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You want to set an alarm if your server's CPU goes above 80%. | **Amazon CloudWatch** | CloudWatch is for performance monitoring and alarms. |
| 2 | A server was deleted at 2 AM. You need to know which employee did it. | **AWS CloudTrail** | CloudTrail logs every user action (API call). |
| 3 | You want a weekly report telling you which servers you can delete to save money. | **AWS Trusted Advisor** | Provides cost-saving recommendations. |
| 4 | You want to build a "Chatbot" like ChatGPT using AWS. | **Amazon Bedrock / Lex** | Bedrock is the Generative AI platform; Lex is for conversational bots. |
| 5 | You want to automatically detect if a person is wearing a helmet in a photo. | **Amazon Rekognition** | The AI service for image and video analysis. |
| 6 | You want to convert your text documents into a lifelike human voice. | **Amazon Polly** | Text-to-speech AI. |
| 7 | You want to see a "Map" of how traffic flows through your application. | **AWS X-Ray** | Used for debugging and tracing distributed applications. |
| 8 | You want to scan your code for security vulnerabilities automatically. | **Amazon Inspector** | Automated security assessment for EC2 and Containers. |
| 9 | You want to identify "PII" (Personal Information) in your S3 buckets. | **Amazon Macie** | AI-driven data privacy and security service. |
| 10 | You want to predict your future sales based on 5 years of history. | **Amazon Forecast** | Time-series forecasting using Machine Learning. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A
1. **CloudWatch vs. CloudTrail?** CloudWatch is *Performance* (is it working?); CloudTrail is *Compliance* (who did what?).
2. **What is a "Metric" in CloudWatch?** A variable that is monitored over time (e.g., CPU, Disk I/O).
3. **What is an "Alarm"?** A trigger that performs an action (like sending an email) when a metric exceeds a threshold.
4. **What is AWS Health Dashboard?** Shows status of AWS services; Personal Health Dashboard shows status of *your* resources.
5. **What is Amazon SageMaker?** A complete platform for developers to build, train, and deploy Machine Learning models.
6. **What is "Generative AI" in AWS?** Powered primarily by **Amazon Bedrock**.
7. **What is the benefit of Trusted Advisor?** It provides best-practice checks in 5 categories: Cost, Security, Fault Tolerance, Performance, and Service Limits.
8. **What is Amazon GuardDuty?** A threat detection service that uses AI to monitor for malicious activity.
9. **What is Amazon Comprehend?** A service that uses AI to find insights and relationships in text (Sentiment analysis).
10. **What is Amazon Textract?** Automatically extracts text and data from scanned documents.

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **Alarm Logic**: Think of a threshold for your phone's battery. If it hits 10%, what "Alarm" action would you take?
2. **Trusted Advisor**: Open the AWS Console and see how many "Green" checks you have for Security.
3. **CloudTrail Logs**: Look at the "Event History" in CloudTrail to see your own login event.
4. **AI Research**: Look up the difference between Amazon Rekognition (Images) and Amazon Lex (Chat).
5. **Git Sync**: Commit and push Chapter 8.
