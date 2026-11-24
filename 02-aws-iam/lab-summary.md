# 🧪 Hands-On Lab Summary: Introduction to AWS Identity and Access Management (IAM)

- **Platform:** AWS Skill Builder
- **Certification Focus:** AWS Certified Cloud Practitioner (CLF-C02)
- **Status:** ✅ Completed

---

## 🎯 Lab Objectives
- Understand how IAM Users, Groups, and Policies work together to control access in AWS.
- Assign IAM users to specific job-function groups to manage permissions efficiently.
- Verify access restrictions across AWS services (Amazon S3 and Amazon EC2) using separate IAM user sessions.

---

## 🛠️ Key Activities Completed
1. **Explored Pre-Configured IAM Identities:** Reviewed existing IAM users, groups (`EC2-Admin`, `EC2-Support`, `S3-Support`), and attached permission policies.
2. **Managed Group Memberships:** Added designated IAM users (`user-1`, `user-2`, `user-3`) to their respective groups based on the Principle of Least Privilege.
3. **Tested Multi-User Access via Incognito Session:** Signed into the AWS Management Console using an Incognito browser window with individual IAM user credentials to avoid session conflicts.
4. **Validated Service Permissions:** Tested read/write actions on Amazon S3 and Amazon EC2 under different user roles to confirm expected `Access Denied` vs. `Allowed` behavior.

---

## 💡 Key Takeaways
- **Group-Based Access Control:** Attaching policies to IAM groups instead of individual users simplifies permission management and reduces administrative errors.
- **Least Privilege in Action:** Users only receive the exact permissions needed for their role (e.g., S3 read-only users cannot stop or terminate EC2 instances).
- **Session Isolation:** Using private/incognito browser sessions is essential when testing multiple IAM identities simultaneously.
