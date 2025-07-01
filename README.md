# AWS Windows EC2 Instance (Manual Setup via Console)

This project documents the creation and configuration of a Windows EC2 instance on AWS using the AWS Console (no Terraform or automation).

Project Summary

- Purpose: Test Windows EC2 setup via AWS Console
- Instance Type: t3.micro
- OS: Windows Server 2019 Base
- Public IP: [Your EC2 Public IP Here]
- Access Method: RDP (Remote Desktop)

How I Created the Instance

1. Logged into AWS Management Console
2. Navigated to EC2 Dashboard and clicked Launch Instance
3. Selected:
   - AMI: Windows Server 2019 Base
   - Instance Type: t3.micro
4. Configured:
   - Network: Default VPC
   - Auto-assign public IP: Enabled
5. Added 30 GB General Purpose SSD (gp2)
6. Created or selected an existing key pair (.pem)
7. Configured Security Group:
   - Allowed RDP (port 3389) only from my IP
   - (Optional) Allowed HTTP and HTTPS
8. Launched the instance

Connection Setup

- Used the .pem key file to decrypt the Windows Administrator password
- Connected using the downloaded RDP file
- Entered the decrypted password to log in

Optional Screenshots

You may include screenshots of:
- EC2 instance launch summary
- Security group rules
- Windows login screen (RDP)

Cleanup Instructions

To avoid unnecessary charges:
1. Stop or terminate the EC2 instance from the AWS EC2 Console
2. Release any associated Elastic IPs
3. Delete unused volumes or snapshots

Notes

- t3.micro is not always included in the Free Tier. Charges may apply.
- Store the .pem file securely. It cannot be downloaded again after creation.
