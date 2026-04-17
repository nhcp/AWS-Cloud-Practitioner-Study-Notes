# Module 1, Chapter 10: Migration & Innovation

## 🧠 Part 1: Deep Theory (The Journey to Cloud)
1.  **Migration Evaluator**: Helps you build a business case for the move.
2.  **AWS Snow Family**: Physical devices for moving data (Snowcone, Snowball, Snowmobile).
3.  **AWS DMS**: Database Migration Service (No downtime migration).
4.  **AWS Schema Conversion Tool (SCT)**: Converts DB engines (Oracle to Aurora).

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Tool |
| :--- | :--- | :--- |
| 1 | You have 500TB of data and no internet; you need to move it to AWS. | **AWS Snowball Edge** |
| 2 | You want to move your local SQL Server to Amazon RDS with zero downtime. | **AWS DMS** |
| 3 | You want to convert an old IBM database to run on Amazon Aurora. | **AWS SCT** |
| 4 | You want to "assess" your current servers before moving them. | **Migration Evaluator** |
| 5 | You want to move your entire physical server (OS and all) to EC2. | **AWS Application Migration Service (MGN)** |
| 6 | You want to manage 10 different AWS accounts from one place. | **AWS Organizations** |
| 7 | You want to deploy an app using "Augmented Reality" (AR/VR). | **Amazon Sumerian** |
| 8 | You want to connect "IoT" (Internet of Things) devices like smart fridges. | **AWS IoT Core** |
| 9 | You want to use a "Blockchain" for your supply chain. | **Amazon Managed Blockchain** |
| 10 | You want to simulate a "Quantum Computer." | **Amazon Braket** |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A
1. **What is the "6 Rs" of migration?** Retain, Retire, Rehost, Replatform, Refactor, Relocate.
2. **What is "Rehosting" (Lift and Shift)?** Moving an app as-is without changing it.
3. **What is "Refactoring"?** Rewriting an app to be cloud-native (e.g., using Lambda).
4. **What is the AWS Snowball?** A physical, rugged device for petabyte-scale data transfer.
5. **What is the purpose of AWS Organizations?** Centralized management, consolidated billing, and security policies (SCPs) for multiple accounts.
6. **What is an SCP (Service Control Policy)?** A policy that limits what users can do across an entire AWS Organization.
7. **What is AWS Ground Station?** A service to control satellite communications.
8. **What is the benefit of AWS DMS?** The source database remains fully operational during the migration.
9. **What is the "Migration Hub"?** A single place to track the progress of all your migrations.
10. **What is Amazon Braket?** A service to explore and build quantum computing algorithms.

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **The 6 Rs**: Pick 3 apps you use and decide which "R" you would use to migrate them.
2. **Organization Logic**: Research what a "Root" OU (Organizational Unit) is.
3. **Snowball Sizes**: Look up the capacity (in TB) of a Snowball Edge Storage Optimized device.
4. **Innovation Search**: Find one "Weird" AWS service (like Ground Station) and explain it in one sentence.
5. **Final Git Sync**: Push Chapter 10 and celebrate!
