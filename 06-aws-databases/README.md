# 🗄️ AWS Database Services (CLF-C02)

Welcome to the **AWS Database Services** module of my **AWS Certified Cloud Practitioner (CLF-C02)** learning journey!  
In this section, I explored managed relational and NoSQL database offerings on AWS, high-availability patterns, caching, database migration tools, and completed a hands-on lab provisioning an **Amazon RDS (MySQL)** instance inside a VPC.

---

## 📂 Folder Contents

* 📄 **[AWS_Database_Services_CLF-C02_Learning_Notes.pdf](./AWS_Database_Services_CLF-C02_Learning_Notes.pdf)** — Comprehensive study notes covering SQL vs. NoSQL, Amazon RDS, Aurora, DynamoDB, ElastiCache, Redshift, AWS DMS, VPC integration, exam traps, and 10 practice questions.
* 📝 **README.md** — Module summary, hands-on lab walkthrough, and key takeaways.

---

## 🧪 Hands-On Lab Completed

* **Lab Title:** Introduction to Amazon Relational Database Service (RDS) (Linux) (`SPL-76`)
* **Platform:** AWS Skill Builder
* **Services Used:** Amazon RDS (MySQL), Amazon VPC, Security Groups, AWS Systems Manager (Session Manager), Amazon EC2

### **What I Practiced in This Lab:**
1. **Provisioned a Managed MySQL Database:** Created a `db.t3.micro` Amazon RDS MySQL instance (`my-rds`) using the Dev/Test template inside `Lab VPC`.
2. **Configured Network Security:** Attached a dedicated `RDS Security Group` (removing the default security group) to restrict database access strictly to authorized resources.
3. **Connected via Session Manager:** Accessed the EC2 command host terminal securely through **AWS Systems Manager Session Manager** without opening SSH ports.
4. **Executed SQL Operations:** Connected to the RDS DNS **Endpoint** using the `mysql` CLI client, created the `lab.staff` table, inserted records, and verified data retrieval via SQL queries.

---

## 🧠 Key Concepts & Exam Takeaways

| Service / Feature | Category | Best Use Case & Key Exam Point |
| :--- | :--- | :--- |
| **Amazon RDS** | Managed Relational (SQL) | Supports MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, and Db2. Automates backups, patching, and failover. |
| **RDS Multi-AZ** | High Availability | Synchronous replication to a standby instance in another AZ for **automatic failover** (not for read scaling). |
| **RDS Read Replicas** | Read Scaling | Asynchronous replication to offload **read-heavy traffic** from the primary DB instance. |
| **Amazon Aurora** | Cloud-Native Relational | MySQL- & PostgreSQL-compatible; stores **6 copies across 3 AZs** with auto-scaling storage up to 128 TiB. |
| **Amazon DynamoDB** | Serverless NoSQL | Key-value & document database with single-digit millisecond latency at any scale (On-Demand or Provisioned capacity). |
| **Amazon ElastiCache** | In-Memory Caching | Managed **Valkey, Redis OSS, and Memcached** to reduce database load and speed up frequent reads. |
| **Amazon Redshift** | Data Warehouse (OLAP) | Columnar storage built for large-scale **Big Data analytics** and Business Intelligence (BI) queries. |
| **AWS DMS & Schema Conversion** | Database Migration | **AWS DMS** migrates data with minimal downtime; **DMS Schema Conversion** converts schemas across different engines. |

---

## 🔗 Quick Navigation

* ⬅️ **Previous Module:** [05 - AWS Networking (Amazon VPC)](../05-aws-networking)
* 🏠 **Main Repository:** [AWS Cloud Practitioner Learning Journey](https://github.com/Lojitha-Heshan/AWS-Cloud-Practitioner-learning-journey)
