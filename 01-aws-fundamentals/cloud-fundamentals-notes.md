# ☁️ AWS Cloud Fundamentals — CLF-C02 Study Notes

## 1. What is Cloud Computing?
Cloud computing is the on-demand delivery of IT resources (compute power, database storage, applications, and other IT resources) over the internet with **pay-as-you-go pricing**. Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services on an as-needed basis from a cloud provider like **Amazon Web Services (AWS)**.

---

## 2. Six Advantages of Cloud Computing
1. **Trade Fixed Expense for Variable Expense:** Pay only when you consume computing resources, rather than investing heavily in physical data centers upfront (CapEx → OpEx).
2. **Benefit from Massive Economies of Scale:** Lower variable costs because AWS aggregates usage from hundreds of thousands of customers.
3. **Stop Guessing Capacity:** Eliminate guessing about infrastructure capacity needs; scale up or down automatically based on actual demand.
4. **Increase Speed and Agility:** New IT resources are only a click away, reducing deployment time from weeks to minutes.
5. **Stop Spending Money Running and Maintaining Data Centers:** Focus on your business and applications rather than racking, stacking, and powering servers.
6. **Go Global in Minutes:** Easily deploy applications in multiple AWS Regions around the world with lower latency for end users.

---

## 3. Cloud Deployment Models
| Model | Description | Use Case |
| :--- | :--- | :--- |
| **Cloud-Based (Public)** | All parts of the application run in the cloud; either migrated from existing infrastructure or built natively in the cloud. | Startups, SaaS apps, scalable web applications. |
| **On-Premises (Private)** | Deploying resources on-premises using virtualization and resource management tools. | Strict regulatory/compliance environments with legacy hardware. |
| **Hybrid** | Connects cloud-based resources with on-premises infrastructure. | Gradual cloud migration or keeping sensitive data locally while bursting compute to AWS. |

---

## 4. Cloud Service Models (Shared Control Spectrum)
- **IaaS (Infrastructure as a Service):** Provides basic building blocks for cloud IT (networking, virtual servers, storage). Maximum flexibility and OS control. *(Example: **Amazon EC2**, Amazon VPC, Amazon EBS)*
- **PaaS (Platform as a Service):** Removes the need to manage underlying infrastructure (hardware and OS) so you focus on deploying and managing applications. *(Example: **AWS Elastic Beanstalk**, AWS Lambda)*
- **SaaS (Software as a Service):** A complete product run and managed by the service provider. *(Example: Amazon WorkMail, Salesforce, Microsoft 365)*

---

## 5. AWS Global Infrastructure
- **AWS Region:** A physical geographical location around the world where AWS clusters data centers (e.g., `us-east-1` N. Virginia, `ap-south-1` Mumbai, `ap-southeast-1` Singapore). Data does not leave a Region unless explicitly replicated.
- **Availability Zone (AZ):** One or more discrete data centers with redundant power, networking, and connectivity within an AWS Region. AZs are physically separated (miles apart) to isolate disasters, yet connected via low-latency fiber links.
- **Edge Locations (Points of Presence):** Data centers used by **Amazon CloudFront** (CDN) and **Amazon Route 53** to cache content closer to end users globally for ultra-low latency.

---

## 6. AWS Shared Responsibility Model
Security and compliance is a shared responsibility between AWS and the customer:
- **AWS — Security OF the Cloud:** Responsible for protecting the global infrastructure that runs all AWS services (physical data centers, hardware, software, networking, and virtualization layer).
- **Customer — Security IN the Cloud:** Responsible for customer data, platform/application management, IAM access control, OS/firewall configuration (e.g., EC2 patching, Security Groups), and encryption settings.

---

## 📝 Quick CLF-C02 Exam Tips
- **High Availability:** Deploy workloads across **multiple Availability Zones** within a Region.
- **Disaster Recovery / Compliance:** Replicate data across **multiple AWS Regions**.
- **Low-Latency Content Delivery:** Use **Edge Locations** via Amazon CloudFront.
