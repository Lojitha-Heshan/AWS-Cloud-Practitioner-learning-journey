# Day 03: Amazon Simple Storage Service (Amazon S3)

![AWS](https://img.shields.io/badge/AWS-Amazon%20S3-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Certification](https://img.shields.io/badge/CLF--C02-Exam%20Prep-232F3E?style=flat-square)
![Lab](https://img.shields.io/badge/AWS%20Skill%20Builder-Hands--On%20Lab-146EB4?style=flat-square)

## Overview
On **Day 03** of my AWS Certified Cloud Practitioner (CLF-C02) and DevOps learning journey, I explored **Amazon Simple Storage Service (Amazon S3)**—AWS's highly scalable, durable object storage service. Through the **AWS Skill Builder: Introduction to Amazon S3** hands-on lab, I practiced bucket creation, access security controls, IAM/Bucket policies, AWS CLI operations from EC2 via Systems Manager Session Manager, and S3 Versioning.

📄 **Full Study Notes (PDF with Diagrams):** [Download Amazon S3 CLF-C02 Study Notes](./Note/amazon-s3-clf-c02-study-notes.pdf)  
📝 **Published Technical Article:** *Day 03 of My AWS Cloud Journey: Exploring Amazon S3, Bucket Policies, and Versioning* (AWS Builder Center)

---

## Key Concepts Covered
- **Object Storage Fundamentals:** Buckets (globally unique namespace), Objects, Keys, Prefixes, and Metadata.
- **Durability & Availability:** `99.999999999%` (11 nines) durability across multiple Availability Zones and `99.99%` availability for S3 Standard.
- **S3 Storage Classes:** S3 Standard, Intelligent-Tiering, Standard-IA, One Zone-IA, Express One Zone, Glacier Instant/Flexible Retrieval, Glacier Deep Archive, and S3 on Outposts.
- **Lifecycle Management:** Automating cost optimization with **Transition Actions** and **Expiration Actions**.
- **Security & Encryption:** Block Public Access (BPA), Resource-Based Bucket Policies, IAM Identity-Based Policies, ACLs, and Encryption at Rest (`SSE-S3`, `SSE-KMS`, `SSE-C`) & in Transit (`HTTPS/TLS`).
- **Data Protection & Replication:** S3 Versioning, **Delete Markers**, Same-Region Replication (SRR), and Cross-Region Replication (CRR).
- **Advanced CLF-C02 Features:** Presigned URLs, Static Website Hosting, Object Lock (WORM), Transfer Acceleration, and S3 Storage Lens.

---

## Hands-On Lab Architecture & Workflow

```text
+-----------------------------------+       AWS CLI (aws s3 cp)       +----------------------------------------+
|  EC2 Instance + IAM Role          | ------------------------------> |  S3 Bucket: reportbucket-<account-id>  |
|  (Accessed via SSM Session Mgr)   |   Allowed via Bucket Policy     |  ├── new-report.png                    |
+-----------------------------------+   (s3:PutObject on reports/*)   |  └── reports/                          |
                                                                      |       └── report-test1.txt (Versioned) |
+-----------------------------------+                                 +----------------------------------------+
|  Public Internet                  | ------- X (Blocked by Default via S3 Block Public Access)
+-----------------------------------+
