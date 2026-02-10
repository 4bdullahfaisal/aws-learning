
# My AWS EC2 Learning Journey

## Screenshots:
![My EC2 Instance Running](images/ec2/ec2-running.png)
![EC2 Screenshot](images/ec2/ec2-instance-running2.png)

# AWS EC2 Hands-On Lab

## Objectives
- Launch and configure an EC2 instance
- Connect via SSH using Git Bash
- Practice essential Linux commands
- Understand security groups and key pairs

## Prerequisites
- AWS Account (Free Tier)
- Git Bash installed on Windows
- Basic understanding of cloud concepts

---

## Steps Completed

### 1. Instance Launch & Configuration

**Instance Details:**
- **Instance Type:** t2.micro (Free Tier eligible)
- **AMI:** Amazon Linux 2023
- **Region:** us-east-1
- **Storage:** 8 GB GP3
- **Key Pair:** my-first-key.pem (RSA)

**SNetwork settings:**
- Check shh and http 
- **SSH (Port 22):** 0.0.0.0/0 (for learning)
- **HTTP (Port 80):** 0.0.0.0/0
- **Custom TCP (Port 8080):** 0.0.0.0/0

---

### 2. SSH Connection Setup

**Git Bash Commands Used:**
```bash
# Navigate to key file location
cd ~/Documents

# Set secure permissions
chmod 400 my-first-key.pem

# Connect to EC2 instance
ssh -i my-first-key.pem ec2-user@YOUR_PUBLIC_IP

## Commands I Ran:
- mkdir test
- cd test
- echo "I did this myself!" > success.txt
- cat success.txt

# Current directory
pwd
# Output: /home/ec2-user

# List files
ls -la

# Create directory
mkdir practice_folder

# Navigate into directory
cd practice_folder

# Create files
echo "Learning AWS EC2" > file1.txt
touch file2.txt

