# Module 1, Chapter 7: Database Services

## 🧠 Part 1: Deep Theory (SQL vs. NoSQL)
AWS provides "Purpose-Built" databases. You must know which one to pick for the exam:
1.  **Amazon RDS (Relational Database Service)**: For traditional, structured data (SQL). Supports MySQL, PostgreSQL, Oracle, SQL Server. 
2.  **Amazon Aurora**: AWS's proprietary high-performance database. 5x faster than standard MySQL.
3.  **Amazon DynamoDB**: A **NoSQL** database. It is **Serverless**, has "Single-digit millisecond" performance, and scales to any size.
4.  **Amazon ElastiCache**: An "In-memory" database (Redis/Memcached). Used to speed up applications by caching frequent queries.
5.  **Amazon Redshift**: A **Data Warehouse**. Used for complex analytics, not for daily transactions.

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Service | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You need a traditional MySQL database but don't want to patch the OS. | **Amazon RDS** | RDS is a managed SQL service. |
| 2 | You need a database for a mobile app that will grow from 10 users to 10 million. | **Amazon DynamoDB** | DynamoDB is serverless and scales infinitely. |
| 3 | Your website is slow because it asks the database the same thing 1,000 times/sec. | **Amazon ElastiCache** | Caching reduces the load on your main database. |
| 4 | You want to run "Big Data" analytics on 10 years of sales records. | **Amazon Redshift** | Redshift is built for heavy "OLAP" (Analytics) tasks. |
| 5 | You want the most expensive, highest-performance SQL database AWS offers. | **Amazon Aurora** | Aurora is the "Gold Standard" of AWS relational databases. |
| 6 | You have a "Graph" database requirement (social media connections). | **Amazon Neptune** | Neptune is specifically for graph/relationship data. |
| 7 | You need to store "Documents" like JSON files in a managed service. | **Amazon DocumentDB** | Managed MongoDB-compatible service. |
| 8 | You want to migrate a database from your office to AWS without downtime. | **AWS DMS (Database Migration Service)** | Specifically for moving data into AWS. |
| 9 | You need a database that is "Serverless" but still uses SQL. | **Amazon Aurora Serverless** | Provides SQL power without managing instances. |
| 10 | You want to store simple "Key-Value" pairs for a gaming leaderboard. | **Amazon DynamoDB** | The primary use case for NoSQL key-value stores. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A
1. **What is a "Managed" database?** AWS handles the hardware, OS patching, and backups; you only handle the data.
2. **Difference between RDS and DynamoDB?** RDS is Relational (SQL); DynamoDB is Non-relational (NoSQL).
3. **What is "Read Replicas"?** A feature of RDS that creates copies of your DB to handle more "Read" traffic.
4. **What is "Multi-AZ" for RDS?** A "Disaster Recovery" feature that keeps a sync copy of your DB in another AZ.
5. **What is an "In-memory" database?** A DB like ElastiCache that stores data in RAM for sub-millisecond speed.
6. **When would you use Amazon Redshift?** For Business Intelligence (BI) and data warehousing.
7. **Is DynamoDB Regional or Global?** It is a Regional service with "Global Tables" capability.
8. **What does "Schema-less" mean?** In DynamoDB, you don't have to define columns/rows upfront.
9. **What is the AWS Schema Conversion Tool (SCT)?** Used to convert a database (e.g., Oracle to MySQL) before migration.
10. **What is OLTP vs OLAP?** OLTP (RDS) is for daily transactions; OLAP (Redshift) is for historical analytics.

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **Engine Check**: Go to the RDS console and list the 6 database engines available.
2. **Pricing Compare**: Compare the cost of a `db.t3.micro` instance vs. a `db.r5.large`.
3. **NoSQL JSON**: Create a sample JSON object representing a "User Profile" (Name, Age, Hobbies).
4. **Redshift Logic**: Research why Redshift is called "Columnar" storage.
5. **Git Sync**: Commit and push Chapter 7 to your repository.
