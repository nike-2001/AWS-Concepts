# Amazon Virtual Private Cloud (VPC) - Overview & FAQ

Amazon Virtual Private Cloud (VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. This README outlines the fundamentals and key concepts related to Amazon VPC.

---

## 📘 1. What is Amazon Virtual Private Cloud (VPC)?
Amazon VPC is a logically isolated section of the AWS Cloud where you can launch resources in a virtual network that you define. It allows full control over network settings like IP addresses, subnets, and security.

---

## 🔑 2. What are the Key Components of Amazon VPC?
- **Subnets**
- **Route Tables**
- **Network ACLs (Access Control Lists)**
- **Security Groups**
- **Virtual Private Gateways (VPGs)**

---

## ⚙️ 3. How does Amazon VPC Work?
You create a private network, define IP address ranges (CIDR blocks), launch subnets, and apply security layers like NACLs and Security Groups.

---

## 🧱 4. What are VPC Subnets?
Subnets divide your VPC’s IP range into smaller sections. They help organize and isolate resources into public and private zones.

---

## 🌐 5. How Can You Connect Your On-Premises Network to Amazon VPC?
- **VPN Connection** – Secure tunnel over the internet
- **AWS Direct Connect** – Dedicated network connection

---

## 🔗 6. What is a VPC Peering Connection?
A VPC peering connection connects two VPCs, allowing them to communicate as if they are in the same network.

---

## 🗺️ 7. What is a Route Table in Amazon VPC?
Route tables contain rules that determine how traffic is directed between subnets and external endpoints.

---

## 🛡️ 8. How Do Security Groups Work in Amazon VPC?
Security groups are stateful firewalls that control traffic to and from EC2 instances.

---

## 🧱 9. What are Network Access Control Lists (ACLs) in Amazon VPC?
Network ACLs are stateless firewalls that operate at the subnet level and provide an extra security layer.

---

## 🔒 10. How Can You Ensure Private Communication Between Instances?
Use:
- **Private Subnets**
- **Security Groups** configured for internal-only traffic

---

## 🧭 11. What is the Default VPC in AWS?
A default, pre-configured VPC available in each region for easier instance launching with basic networking.

---

## 🌍 12. Can You Peer VPCs in Different Regions?
**No.** VPC peering is limited to the same region. For inter-region connections, use **VPN** or **AWS Direct Connect**.

---

## 📛 13. How Can You Control Public and Private IPs in VPC?
- Private IPs are auto-assigned based on subnet.
- Public IPs can be manually assigned or automatically associated in public subnets.

---

## 🔐 14. What is a VPN Connection in Amazon VPC?
A **VPN connection** creates a secure and encrypted connection between your on-premises network and AWS VPC.

---

## 🌐 15. What is an Internet Gateway (IGW) in Amazon VPC?
An IGW is a horizontally scaled, redundant, and highly available component that enables VPC instances to connect to the internet.

---

## ♻️ 16. How Can You Ensure High Availability in VPC?
Deploy subnets and resources across **multiple Availability Zones (AZs)**.

---

## 🔐 17. How Does Amazon VPC Provide Isolation?
VPC lets you define your own:
- **IP range**
- **Subnets**
- **Routing rules**
- **Security policies**

---

## ⚠️ 18. Can You Modify a VPC After Creation?
You can:
- **Add/remove subnets**
- **Modify route tables and ACLs**
But **some settings (like primary CIDR block)** are immutable after creation.

---

## 🛣️ 19. What is a Default Route in Amazon VPC?
A default route (usually `0.0.0.0/0`) in a route table directs all traffic to an **Internet Gateway (IGW)** for internet-bound communication.

---

## 🧩 20. What is the Purpose of an Amazon VPC Endpoint?
A **VPC Endpoint** enables **private access** to AWS services (like S3, DynamoDB) without needing an internet gateway or VPN.

---

## 📚 Summary
Amazon VPC is essential for secure and customizable cloud networking on AWS. Mastering its components and functionality allows for building robust, scalable, and secure cloud environments.

