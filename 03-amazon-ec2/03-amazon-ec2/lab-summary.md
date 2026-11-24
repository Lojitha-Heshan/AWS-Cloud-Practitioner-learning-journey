# 🧪 Hands-On Lab Summary: Introduction to Amazon EC2

- **Platform:** AWS Skill Builder
- **Certification Focus:** AWS Certified Cloud Practitioner (CLF-C02)
- **Status:** ✅ Completed

---

## 🎯 Lab Objectives
- Launch and configure a virtual server using Amazon EC2 on Amazon Linux.
- Automate web server installation at launch using EC2 User Data scripts.
- Configure Security Groups as virtual firewalls to control HTTP/SSH traffic.
- Vertically scale EC2 compute capacity (Instance Type) and expand EBS root volume storage.
- Protect critical instances against accidental deletion using Termination Protection.

---

## 🛠️ Key Activities Completed
1. **Instance Launch & Bootstrapping:** Launched a `t2.micro` / `t3.micro` Linux instance with a custom [User Data script](./scripts/user-data-apache.sh) to automatically install and start the Apache (`httpd`) web server.
2. **Security Group Configuration:** Verified inbound firewall rules—initially observed connection timeout on Public IPv4 until HTTP (`Port 80`) inbound traffic was explicitly allowed.
3. **Monitoring & System Logs:** Checked instance health checks, system boot logs, and instance screenshots via the EC2 console.
4. **Vertical Scaling & Storage Expansion:** Stopped the instance, upgraded the instance type for higher compute capacity, increased the attached Amazon EBS volume size, and restarted the server.
5. **Termination Protection:** Enabled Termination Protection to prevent accidental deletion, tested the block, and safely disabled it before cleanup.

---

## 💡 Key Takeaways
- **Stateful Firewall Behavior:** Security Groups deny all inbound traffic by default; explicit port rules (such as Port 80 for HTTP) must be added for public web access.
- **Compute vs. Storage Independence:** Stopping an EC2 instance halts compute billing and allows vertical resizing, while EBS storage persists independently.
- **Public IPv4 Behavior:** Auto-assigned Public IPv4 addresses can change across Stop/Start cycles unless an Elastic IP is attached.
