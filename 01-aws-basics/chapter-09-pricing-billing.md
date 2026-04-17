# Module 1, Chapter 9: Pricing, Billing, and Support

## 🧠 Part 1: Deep Theory (How AWS Makes Money)
1.  **Pay-as-you-go**: No long-term contracts. You pay only for what you use.
2.  **Savings Plans / Reserved Instances**: Commit to 1 or 3 years to save up to 72%.
3.  **Consolidated Billing**: If you have 100 AWS accounts, you get **one** bill and benefit from bulk discounts.
4.  **AWS Support Plans**:
    * **Basic**: Free. No tech support.
    * **Developer**: $29/mo. Email support (24hr).
    * **Business**: $100/mo. 24/7 Phone/Chat/Email support. (Full Trusted Advisor).
    * **Enterprise**: $15k/mo. Includes a **TAM** (Technical Account Manager).

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Tool / Plan |
| :--- | :--- | :--- | :--- |
| 1 | You want to estimate the cost of a new project before you build it. | **AWS Pricing Calculator** |
| 2 | You want to see a graph of your spending for the last 6 months. | **AWS Cost Explorer** |
| 3 | You want to receive an email the moment your bill hits €50. | **AWS Budgets** |
| 4 | Your company has 5 departments with 5 AWS accounts; you want one bill. | **AWS Organizations (Consolidated Billing)** |
| 5 | You are a big bank and need a dedicated person (TAM) to help you. | **Enterprise Support Plan** |
| 6 | You want to find out which tags (labels) are costing you the most money. | **Cost Allocation Tags** |
| 7 | You want to see exactly which hour of the day was the most expensive. | **AWS Cost & Usage Report (CUR)** |
| 8 | You are a small developer and just need email support for a bug. | **Developer Support Plan** |
| 9 | You want to download a CSV of your monthly spending. | **AWS Billing Dashboard** |
| 10 | You want to pay a lower price because you use 500TB of storage. | **Volume Discounts (Economies of Scale)** |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A
1. **What is the AWS Pricing Calculator?** A web tool to estimate costs for any AWS service.
2. **What is the benefit of Consolidated Billing?** One bill for multiple accounts and sharing of volume discounts.
3. **What is a TAM?** Technical Account Manager (Available only on Enterprise support).
4. **What is a "Hard Limit" in AWS Budgets?** You can set a budget to alert you, but it **will not** stop your services automatically.
5. **Which Support Plan gives you access to the full Trusted Advisor?** Business and Enterprise.
6. **What is the "Free Tier"?** A way for new users to try services for free (12 months, Always Free, or Short-term).
7. **What are Cost Allocation Tags?** Labels used to track and organize costs by department or project.
8. **What is the AWS Marketplace?** A digital catalog to buy software from 3rd-party vendors that runs on AWS.
9. **How much does the Basic Support plan cost?** $0 (It is included for all AWS customers).
10. **What is the response time for a "System Down" case on Business Support?** Under 1 hour.

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **Price Estimate**: Estimate the cost of 1 S3 bucket with 500GB of data using the Calculator.
2. **Support Compare**: Create a table comparing Developer vs. Business support.
3. **Marketplace Search**: Go to the AWS Marketplace and find "Fortinet" or "Cisco."
4. **Budget Alert**: Research how to set a "Zero Spend" budget alert.
5. **Git Sync**: Commit and push Chapter 9.
