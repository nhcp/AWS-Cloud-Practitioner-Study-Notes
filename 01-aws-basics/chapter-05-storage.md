# Module 1, Chapter 5: Storage Services (The Vault of the Cloud)

## 🧠 Part 1: Deep Theory (Object vs. Block vs. File)

AWS offers different storage "types" based on how you need to access the data. Understanding the difference is key to passing the exam.

### 1. Amazon S3 (Simple Storage Service) - "Object Storage"
* **Logic**: Think of it as a giant, infinite bucket. You upload "Objects" (files) and get a unique URL for each.
* **Key Features**: 99.999999999% (11 Nines) of durability. It is a **Regional** service.
* **Storage Classes**:
    * **S3 Standard**: For frequently accessed data.
    * **S3 Intelligent-Tiering**: Automatically moves data to the cheapest tier based on usage.
    * **S3 Glacier**: For long-term archives (very cheap, but takes minutes/hours to retrieve).

### 2. Amazon EBS (Elastic Block Store) - "Block Storage"
* **Logic**: This is a virtual hard drive for your EC2 instance.
* **Key Features**: It is tied to a **specific Availability Zone**. You cannot (usually) attach it to multiple servers at once.
* **Snapshots**: Point-in-time backups of your EBS volumes stored in S3.

### 3. Amazon EFS (Elastic File System) - "File Storage"
* **Logic**: A "Shared Drive" (like a network folder) that hundreds of EC2 instances can connect to simultaneously.
* **Key Features**: Only works with Linux. Scales automatically.

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Storage Service | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You want to host a static website (HTML/CSS/Images) at the lowest possible cost. | **Amazon S3** | S3 can host static websites without needing a server. |
| 2 | You need a lightning-fast "boot volume" for a Windows server to run an app. | **Amazon EBS** | EBS provides the low-latency "block" storage needed for an OS. |
| 3 | You have a fleet of 50 Linux servers that all need to access the same PDF library. | **Amazon EFS** | EFS allows multiple instances to mount the same file system. |
| 4 | You must keep medical records for 10 years to satisfy the law, but you will never look at them. | **S3 Glacier Deep Archive** | The cheapest storage for data that is rarely accessed. |
| 5 | You want to make sure your data survives even if a whole AWS Region is destroyed. | **S3 Cross-Region Replication** | S3 can automatically copy your data to a different part of the world. |
| 6 | You want to prevent any file in your bucket from being deleted or changed for 1 year. | **S3 Object Lock** | Used for "WORM" (Write Once, Read Many) compliance. |
| 7 | You have 100TB of data in your office in Hof and want to move it to AWS but your internet is slow. | **AWS Snowball Edge** | A physical, rugged device used to transport large amounts of data. |
| 8 | You want your storage to automatically get cheaper as your files get older. | **S3 Lifecycle Policies** | Automatically moves objects from Standard to Glacier based on age. |
| 9 | You need to store "unstructured" data like photos, videos, and logs. | **Amazon S3** | S3 is designed for "Objects" (unstructured data). |
| 10 | You need to move a massive "Exabyte" of data (1,000,000 TB) to AWS. | **AWS Snowmobile** | A literal shipping container on a truck for massive data moves. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A

| # | Question | Answer |
| :--- | :--- | :--- |
| 1 | **What is the difference between EBS and S3?** | EBS is a local hard drive for one server; S3 is a global-access "bucket" for files. |
| 2 | **What does "11 Nines of Durability" mean?** | If you store 10 million objects, you might lose one every 10,000 years. |
| 3 | **Which S3 class is best for data with unknown access patterns?** | **S3 Intelligent-Tiering**. |
| 4 | **Is an EBS volume automatically backed up?** | No. You must manually or automatically create **Snapshots**. |
| 5 | **What is the "Snow" Family?** | A group of physical devices (Snowcone, Snowball, Snowmobile) used for data migration. |
| 6 | **What is "Versioning" in S3?** | A feature that keeps multiple variants of an object in the same bucket (protects against accidental deletes). |
| 7 | **What is AWS Storage Gateway?** | A hybrid service that lets your on-premise office use AWS storage like it's local. |
| 8 | **What is the "Transfer Acceleration" feature in S3?** | Uses Edge Locations to speed up long-distance uploads to S3. |
| 9 | **Can EFS be used with Windows servers?** | No. Use **Amazon FSx** for Windows instead. |
| 10 | **What is a "Bucket" in S3?** | A container for objects. Names must be **globally unique** across all of AWS. |

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **Bucket Naming**: Try to think of an S3 bucket name. Go to the AWS console and see if it's already taken (it likely is!).
2. **Glacier Math**: Look up the cost of storing 1TB in S3 Standard vs. S3 Glacier Deep Archive.
3. **Snowball Logistics**: Research how you actually get a Snowball (Hint: You order it in the console and it arrives via mail).
4. **S3 Versioning**: Imagine you have versioning on. If you delete a file, is it actually gone? (Hint: No, a "Delete Marker" is added).
5. **Git Sync**: Commit and push this Master Storage chapter to your repository.
