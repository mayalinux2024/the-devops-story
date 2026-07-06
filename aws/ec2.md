# EC2 - The First Workshop

## Objective

Launch a Linux server in AWS and connect to it using SSH.

---

## 🔘 Show Me the Real Implementation

↓

## 📄 Implementation Guide

### Implementation Summary 

The implementation

This is the first real implementation in the project.

The learner should only do these steps:

1. Open EC2

↓

2. Click Launch Instance

↓

3. Configure
Amazon Linux 2023
t2.micro (or t3.micro if that's what's available on your account)
Create/select a key pair
Allow SSH

↓

4. Launch

↓

5. Connect
ssh -i my-key.pem ec2-user@YOUR_PUBLIC_IP

↓

6. Verify
hostname
pwd
ls

That's it.

The learner has successfully built the King's first workshop.

## Detailed Explaination

## Launch Configuration

- AMI: Ubuntu 26.04 LTS
- Instance Type: t3.micro (free)
- Inbound Rule:
  - SSH (TCP 22)

---

## Connect

```bash
ssh -i ~/devops-story.pem ubuntu@<PUBLIC-IP>
```

---

## Verify

```bash
hostname
pwd
ls
```

Expected output:

- `hostname` shows the EC2 host name.
- `pwd` shows `/home/ubuntu`.
- `ls` is initially empty.

---

## Screenshots

- EC2 Dashboard
- Running Instance
- SSH Terminal
