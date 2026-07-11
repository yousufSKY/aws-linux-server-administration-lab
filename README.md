# AWS EC2 Linux Administration & SSH Lab

A hands-on cloud infrastructure project demonstrating secure remote administration of an Amazon Linux EC2 instance using SSH from both **Windows 11** and **Ubuntu Linux**. This project focuses on practical Linux system administration, AWS cloud fundamentals, secure remote access, networking verification, and technical documentation.

![AWS](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazonaws)
![Linux](https://img.shields.io/badge/Linux-Amazon%20Linux-success?style=for-the-badge&logo=linux)
![SSH](https://img.shields.io/badge/OpenSSH-Remote%20Access-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## Project Overview

This home lab was built to gain practical experience with Linux server administration in a real AWS cloud environment. The project demonstrates how to securely connect to an Amazon EC2 instance using SSH, perform basic Linux administration tasks, verify network connectivity, and document the complete implementation following industry best practices.

Rather than using a local virtual machine, the server was deployed on AWS to simulate a real-world cloud administration environment.

---

## Objectives

- Launch an Amazon Linux EC2 instance.
- Configure secure SSH remote access.
- Connect to the server from Windows 11.
- Connect to the server from Ubuntu Linux.
- Perform Linux system administration tasks.
- Verify network connectivity.
- Practice Linux command-line operations.
- Document the complete implementation.

---

# Architecture Diagram

<p align="center">
<img src="architecture/Untitled%20Diagram-2026-07-11T06-20-43.png" width="100%">
</p>

---

# Technologies Used

| Category | Technology |
|-----------|------------|
| Cloud Platform | Amazon Web Services (AWS) |
| Compute | Amazon EC2 |
| Operating System | Amazon Linux 2023 |
| Remote Access | OpenSSH |
| Client Systems | Windows 11, Ubuntu Linux |
| Networking | Public IPv4, Security Groups |
| Terminal | PowerShell, Ubuntu Terminal |
| Documentation | Markdown |
| Version Control | Git & GitHub |

---

# AWS Services Used

- Amazon EC2
- Amazon VPC
- Public Subnet
- Security Groups
- Internet Gateway
- Route Tables
- Elastic Network Interface (ENI)
- Key Pair Authentication

---

# Repository Structure

```text
.
├── architecture/
│   └── Untitled Diagram-2026-07-11T06-20-43.png
│
├── commands/
│   ├── ssh-from-ubuntu.md
│   └── ssh-from-windows.md
│
├── docs/
│   ├── learning-notes.md
│   ├── references.md
│   └── troubleshooting.md
│
├── screenshots/
│   ├── 01-launch-ec2-instance.png
│   ├── ...
│   └── 13-ubuntu-live-server-commands-and-exit-connection.jpg
│
├── LICENSE
└── README.md
```

---

# Lab Environment

| Component | Value |
|----------|--------|
| AWS Region | us-east-2 |
| Instance Type | t3.micro |
| Operating System | Amazon Linux 2023 |
| Authentication | SSH Key Pair |
| Client 1 | Windows 11 PowerShell |
| Client 2 | Ubuntu Linux Terminal |

---

# Implementation Steps

## Step 1

Launch an Amazon Linux EC2 instance.

---

## Step 2

Generate and download an AWS Key Pair (.pem).

---

## Step 3

Configure the Security Group to allow:

- SSH (TCP Port 22)

---

## Step 4

Verify that the EC2 instance has a Public IPv4 Address.

---

## Step 5

Connect from Windows using OpenSSH.

---

## Step 6

Connect from Ubuntu using OpenSSH.

---

## Step 7

Execute Linux administration commands.

---

## Step 8

Verify Internet connectivity.

---

## Step 9

Document the complete implementation.

---

# Linux Administration Tasks Performed

## User Administration

- whoami
- id
- groups

---

## System Information

- hostname
- uname -a
- uptime
- date
- cat /etc/os-release

---

## File Management

- pwd
- ls
- ls -l
- mkdir
- touch
- cp
- mv
- rm

---

## Network Administration

- hostname -I
- ip addr
- ip route
- ping google.com

---

## Storage Management

- df -h
- lsblk

---

## Memory & CPU Monitoring

- free -h
- top
- ps -ef

---

## Package Management

- dnf check-update
- dnf update

---

## Service Management

- systemctl status sshd

---

# Project Screenshots

The repository contains step-by-step screenshots demonstrating the complete implementation.

| Screenshot | Description |
|------------|-------------|
| 01 | Launch EC2 Instance |
| 02 | Select Amazon Linux |
| 03 | Create Key Pair |
| 04 | Download Private Key |
| 05 | EC2 Running |
| 06 | Configure Security Group |
| 07 | Connect using SSH |
| 08 | Windows PowerShell SSH |
| 09 | Ping Test |
| 10 | Ubuntu SSH Connection |
| 11 | Linux Commands |
| 12 | Linux Administration |
| 13 | Exit SSH Session |

---

# Additional Documentation

This repository contains detailed documentation for each stage of the project.

| File | Description |
|------|-------------|
| ssh-from-windows.md | SSH connection using Windows PowerShell |
| ssh-from-ubuntu.md | SSH connection using Ubuntu Terminal |
| troubleshooting.md | Common issues and resolutions |
| learning-notes.md | Key concepts learned |
| references.md | Official documentation and learning resources |

---

# Skills Demonstrated

- AWS Cloud Fundamentals
- Amazon EC2
- Linux Administration
- SSH Remote Access
- Cloud Networking
- Security Groups
- Public Key Authentication
- System Administration
- Network Diagnostics
- Technical Documentation
- Troubleshooting
- Command-Line Interface (CLI)

---

# Learning Outcomes

After completing this project, I gained practical experience in:

- Deploying cloud-based Linux servers.
- Securely accessing EC2 instances using SSH.
- Performing basic Linux system administration.
- Understanding AWS networking components involved in remote access.
- Executing Linux command-line operations.
- Diagnosing connectivity issues.
- Documenting cloud infrastructure projects professionally.

---

# Future Improvements

- Configure additional Linux users.
- SSH key-based authentication for multiple users.
- Install Apache/Nginx Web Server.
- Configure firewall rules.
- Automate administration using Shell Scripts.
- Configure CloudWatch monitoring.
- Deploy multiple EC2 instances.
- Practice log analysis.
- Explore IAM Roles for EC2.

---

# 🔗 Related Project

If you're interested in AWS networking fundamentals, check out my previous project:

**AWS Custom VPC & Network Infrastructure Lab**

https://github.com/yousufSKY/aws-custom-vpc-network-lab

---

# Author

**Syed Khaja Yousufuddin**

- LinkedIn: https://www.linkedin.com/in/syed-yousufuddin-a64265276/
- GitHub: https://github.com/yousufSKY

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.
