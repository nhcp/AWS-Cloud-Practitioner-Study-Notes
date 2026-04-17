# Module 1, Chapter 6: Networking & Content Delivery

## 🧠 Part 1: Deep Theory (The Virtual Data Center)

### 1. Amazon VPC (Virtual Private Cloud)
A VPC is your own private, isolated section of the AWS Cloud. You have full control over your virtual networking environment.
* **Subnets**: A range of IP addresses in your VPC.
    * **Public Subnet**: Has a route to the **Internet Gateway** (Used for Web Servers).
    * **Private Subnet**: No direct internet access (Used for Databases).
* **Internet Gateway (IGW)**: The "Door" that allows your VPC to talk to the internet.
* **NACL vs. Security Groups**: 
    * **Security Group**: A firewall for the **Instance** (Stateful).
    * **NACL (Network Access Control List)**: A firewall for the **Subnet** (Stateless).

### 2. Domain Name System (Route 53)
Amazon Route 53 is a highly available and scalable Cloud DNS web service. It "routes" users to internet applications by translating names (example.com) into numeric IP addresses.

### 3. Content Delivery (CloudFront)
A web service that speeds up distribution of your static and dynamic web content (e.g., .html, .css, .js, image files) to users via **Edge Locations**.

---

## 🏗️ Part 2: 10 Master Scenario-Based Analysis

| # | Scenario | Correct Service / Component | Logic |
| :--- | :--- | :--- | :--- |
| 1 | You want to create a logically isolated section of AWS to launch resources. | **Amazon VPC** | A VPC is the foundation of all networking in AWS. |
| 2 | You have a database that should NEVER be reached from the public internet. | **Private Subnet** | Private subnets are isolated from the Internet Gateway. |
| 3 | You want to register a new domain name like `www.mohammad-aws.com`. | **Amazon Route 53** | Route 53 handles domain registration and DNS routing. |
| 4 | Your users in Australia are complaining that your video site in Germany is slow. | **Amazon CloudFront** | CloudFront caches content in Edge Locations near the users. |
| 5 | You need to block a specific "bad" IP address from entering your entire subnet. | **Network ACL (NACL)** | NACLs are great for blocking specific IPs at the subnet level. |
| 6 | You want a dedicated, private connection between your office and AWS (No Internet). | **AWS Direct Connect** | Bypasses the public internet for consistent, high-speed bandwidth. |
| 7 | You want to connect two different VPCs together so they can talk privately. | **VPC Peering** | Allows you to route traffic between VPCs using private IP addresses. |
| 8 | You want a single "entry point" for all your users that handles millions of requests. | **Elastic Load Balancer (ELB)** | Distributes traffic across multiple targets (EC2, Containers). |
| 9 | You need to connect your home office to your AWS VPC securely over the internet. | **AWS Site-to-Site VPN** | Creates an encrypted "tunnel" over the public internet. |
| 10 | You want to protect your web application from "DDoS" attacks. | **AWS Shield** | A managed Distributed Denial of Service (DDoS) protection service. |

---

## 🎙️ Part 3: Top 10 Priority Interview Q&A

| # | Question | Answer |
| :--- | :--- | :--- |
| 1 | **What is a "VPC"?** | A private, isolated network in the AWS cloud where you define your own IP range. |
| 2 | **What is the difference between a Public and Private subnet?** | A public subnet has a route to an Internet Gateway; a private one does not. |
| 3 | **What is an "Edge Location"?** | A site that CloudFront uses to store (cache) copies of your content closer to users. |
| 4 | **Is a Security Group "Stateful" or "Stateless"?** | **Stateful**. If you allow traffic in, it is automatically allowed back out. |
| 5 | **What is Route 53?** | AWS’s managed DNS service that translates domain names into IP addresses. |
| 6 | **What is a VPC Peering connection?** | A networking connection between two VPCs that enables traffic routing between them. |
| 7 | **What is AWS Direct Connect?** | A physical, private fiber connection from your data center to AWS. |
| 8 | **What is a NAT Gateway?** | Allows instances in a private subnet to connect to the internet (for updates) but prevents the internet from initiating a connection with them. |
| 9 | **What is the purpose of an Internet Gateway (IGW)?** | It provides a target in your VPC route tables for internet-routable traffic. |
| 10 | **What is AWS Global Accelerator?** | A service that improves the availability and performance of your applications using the AWS global network. |

---

## 🛠️ Part 4: 5 Hands-on Practice Tasks
1. **IP Math**: Research what a `/24` CIDR block means (How many IP addresses are in it?).
2. **Route Table Check**: Look up what a "Default Route" (`0.0.0.0/0`) does in a networking table.
3. **CloudFront Search**: Find out how many Edge Locations AWS currently has worldwide.
4. **DNS Lookup**: Use the `nslookup` command in your terminal to find the IP address of `google.com`.
5. **Git Sync**: Use the commands below to finalize Chapter 6 on your GitHub.
