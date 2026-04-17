# Module 1, Chapter 3: Identity & Access Management (IAM) & Security

## 🧠 Part 1: Deep Theory (The "Lock and Key" of AWS)

### 1. What is IAM?
**Identity and Access Management (IAM)** is a **Global Service** that allows you to manage access to AWS services and resources securely. It handles **Authentication** (Who are you?) and **Authorization** (What are you allowed to do?).

### 2. The 4 Essential Components of IAM
* **Users**: Individual people (e.g., Mohammad, Admin).
* **Groups**: A collection of users. Permissions granted to a group apply to all users within it (e.g., "Developers").
* **Roles**: Used to grant permissions to **AWS Services** (e.g., an EC2 instance) or users from a different account. Roles provide **Temporary Credentials**.
* **Policies**: JSON documents that define permissions.
    * **Effect**: Allow or Deny.
    * **Action**: What can be done (e.g., `s3:ListBucket`).
    * **Resource**: Which specific resource (e.g., a specific S3 bucket).

### 3. Crucial Security Principles
* **The Root User**: The identity used to create the account. **Best Practice:** Stop using it immediately, enable **MFA**, and create an IAM Admin user instead.
* **Principle of Least Privilege**: Give users only the minimum permissions they need to do their job.
* **MFA (Multi-Factor Authentication)**: Adds an extra layer of protection (Password + Token).

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Action | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You hired 10 new interns who only need to "see" S3 files but not delete them. | Create a **Group**, add users, and attach a **ReadOnlyAccess** Policy. | Groups simplify management; ReadOnly follows Least Privilege. |
| 2 | A server (EC2) needs to automatically save backup files to an S3 bucket. | Assign an **IAM Role** to the EC2 instance. | Never put passwords on servers. Roles provide secure, temporary access. |
| 3 | You want to ensure that even if someone steals your password, they can't log in. | Enable **Multi-Factor Authentication (MFA)**. | MFA requires a physical device (phone) to verify identity. |
| 4 | You need to grant a temporary consultant access to your account for 4 hours. | Create an **IAM Role** for cross-account access. | Roles are designed for temporary, secure "hand-off" of permissions. |
| 5 | Your company requires all employees to have passwords that are 14 characters long. | Configure an **IAM Password Policy**. | Password policies enforce security standards across the whole account. |
| 6 | You are using the email address you signed up with for your daily work. | **STOP.** Create an IAM User with Admin rights and use that. | The Root User is too powerful and dangerous for daily use. |
| 7 | You want to allow a developer to manage ONLY the "Production" database. | Use a **Specific Resource ARN** in an IAM Policy. | ARNs allow you to pinpoint exact resources for permissions. |
| 8 | You want to see who deleted a specific database at 3:00 AM on Sunday. | Check **AWS CloudTrail**. | CloudTrail logs every API call (who, what, when, where). |
| 9 | You have 1,000 employees and don't want to attach policies to them one by one. | Use **IAM Groups**. | Attaching a policy to a Group updates 1,000 people instantly. |
| 10 | You need to provide AWS access to an application running in your own office. | Create an **IAM User** with **Access Keys** (ID/Secret). | Access Keys are for programmatic (machine) access, not browser login. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A

| # | Question | Answer |
| :--- | :--- | :--- |
| 1 | **Is IAM a Global or Regional service?** | Global. You create users once, and they exist for the whole world. |
| 2 | **What is the "Principle of Least Privilege"?** | Only giving a user the exact permissions they need to do their job. |
| 3 | **What is the difference between an IAM User and an IAM Role?** | A User is a permanent identity for a person; a Role is temporary and for services/machines. |
| 4 | **How do you manage permissions in IAM?** | By attaching JSON-based **Policies** to Users, Groups, or Roles. |
| 5 | **What is an IAM Access Key?** | A combination of an Access Key ID and Secret Access Key used for CLI/API access. |
| 6 | **What should you do with your Root Account?** | Enable MFA, delete Access Keys, and use IAM users instead. |
| 7 | **What is "Federation"?** | Allowing users to log in to AWS using their existing company passwords (e.g., Active Directory). |
| 8 | **What is an Inline Policy?** | A policy attached to a single user (not recommended; use managed policies instead). |
| 9 | **What is AWS CloudTrail's role in security?** | It records all actions taken in the account for auditing and compliance. |
| 10 | **Can an IAM Group be a member of another Group?** | No. Groups cannot be nested in IAM. |

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **JSON Review**: Copy a "Sample S3 Policy" from Google and identify the **Action**, **Effect**, and **Resource**.
2. **Password Policy**: Research the AWS default password requirements (how many symbols/numbers?).
3. **MFA Research**: List 3 types of MFA AWS supports (Virtual, U2F Security Key, Hardware Key).
4. **AWS CloudTrail**: Look up what a "Management Event" is vs. a "Data Event."
5. **Git Push**: Use the commands below to save this master IAM chapter to your repo.
