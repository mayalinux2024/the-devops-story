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

- EC2 Dashboard & Running Instance
 
  <img width="742" height="350" alt="EC2-Dashboard" src="https://github.com/user-attachments/assets/8d6da0ea-a70f-47ee-82c7-a66d76c0a45d" />

- Security Groups

  <img width="616" height="169" alt="security-groups" src="https://github.com/user-attachments/assets/f6564ddb-68c1-48eb-b4a9-11aea5c55768" />

  
- SSH Terminal
  
           Your Laptop
                │
                │ SSH
                ▼
        The King's First Workshop (EC2)

    <img width="571" height="468" alt="SSH-a" src="https://github.com/user-attachments/assets/a2712a65-b1fe-4ba5-8db6-ad5ec5201c05" />

    <img width="488" height="119" alt="SSH-b" src="https://github.com/user-attachments/assets/ce79ac98-8ab9-4b86-8e97-a6a6c62a59b2" />

  ## "I now have a workshop that I can enter."
  
    <img width="244" height="70" alt="enter-workshop" src="https://github.com/user-attachments/assets/a31a6825-f2f7-439f-b5b8-1bc747c7e4c7" />
    
