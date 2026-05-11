Architecture Diagram
![images alt](https://github.com/teajo99/aws-ec2-vpc-hospital-app/blob/b840ee236ca3b51fd7482c8c2c8adee32183f869/Diagram%20Architecture.png)
# AWS EC2 + VPC Hands-On Project

## Overview

This project demonstrates how to launch an Amazon EC2 instance inside a VPC and verify internet connectivity.

The scenario is based on a hospital application running on AWS.

Instead of buying expensive physical servers that sit unused during quiet hours, Amazon EC2 allows organizations to rent virtual servers only when needed.

---

# Architecture

* VPC (Private AWS Network)
* Public Subnet
* Internet Gateway
* Route Table
* Security Group
* Amazon EC2 Instance

---

# What I Did

## 1. Created a VPC

Created a custom VPC to host the hospital application infrastructure.

## 2. Created a Public Subnet

Configured a public subnet inside the VPC.

## 3. Attached an Internet Gateway

Attached an Internet Gateway to allow internet access.

## 4. Configured Route Tables

Added a route:

```text
0.0.0.0/0 → Internet Gateway
```

This allowed outbound internet connectivity.

## 5. Created a Security Group

Allowed:

* SSH (Port 22)
* HTTP (Port 80)

## 6. Launched an Amazon EC2 Instance

Launched an EC2 instance inside the VPC and subnet.

## 7. Connected to the EC2 Instance

Used EC2 Instance Connect to securely connect to the server.

## 8. Verified the Server Was Running

Executed:

```bash
hostname
```

and:

```bash
uptime
```

---

# Internet Connectivity Test

Verified internet access from the EC2 instance using:

```bash
curl ifconfig.me
```

and:

```bash
ping google.com
```

This confirmed:

* The EC2 instance had internet access
* The VPC networking was configured correctly
* The route table and Internet Gateway worked properly

---

# Key Cloud Concepts Demonstrated

* Amazon EC2
* VPC Networking
* Public Subnet
* Internet Gateway
* Route Tables
* Security Groups
* Cloud Compute
* Infrastructure Scalability

---

# Real-World Scenario

Imagine a hospital application running on AWS.

Before cloud computing, hospitals bought physical servers for peak hours. During quiet periods, many servers remained unused while organizations still paid for them.

Amazon EC2 solves this problem by allowing companies to launch virtual servers only when needed and pay only for what they use.

---

# Outcome

Successfully:

* Built a cloud network using VPC
* Launched an EC2 server
* Configured internet connectivity
* Verified outbound internet access from the server
* Demonstrated foundational AWS cloud architecture

---

# AWS Services Used

* Amazon VPC
* Amazon EC2
* Security Groups
* Internet Gateway
* Route Tables

---

# Author

Temi A
