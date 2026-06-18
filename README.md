# AWS-Secure-Infrastructure-Project

## Services Used

- AWS VPC  
- EC2  
- OpenVPN  
- S3  
- CloudFront  
- AWS WAF  
- IAM  
- Linux Administration


Architecture Flow
                    User / Client
                         │
                         │ Secure VPN Connection
                         ▼
                   OpenVPN Client
                         │
                         ▼
                ┌─────────────────┐
                │ EC2 Ubuntu Server│
                │ (OpenVPN Server) │
                └─────────────────┘
                         │
                         │ Inside AWS Network
                         ▼
                ┌─────────────────┐
                │      AWS VPC     │
                │ Public + Private │
                │     Subnets      │
                └─────────────────┘
                         │
                         ▼
                ┌─────────────────┐
                │   Amazon S3      │
                │ Static Website   │
                └─────────────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Amazon CloudFront│
                │ CDN Distribution │
                └─────────────────┘
                         │
                         ▼
                ┌─────────────────┐
                │    AWS WAF       │
                │ Security Rules   │
                └─────────────────┘
                         │
                         ▼
                  Protected Website

## Project Overview
Built secure cloud infrastructure using AWS services with VPN access, static website hosting, CDN delivery, and web security.

## Step 1: Created VPC

Created custom VPC with public and private subnet for network isolation.
<img width="1920" height="1080" alt="Screenshot (148) - Copy" src="https://github.com/user-attachments/assets/576fab05-1e10-4afa-9268-a76a5edeecdc" />

## Step 2: Launched EC2 Instance

Created Ubuntu EC2 instance and configured security groups.

<img width="1920" height="1080" alt="Screenshot (167) - Copy" src="https://github.com/user-attachments/assets/03be5d56-5649-406c-89c9-40cf3a69c6ff" />

## Step 3: OpenVPN Configuration

Installed OpenVPN on Ubuntu server and verified service status.

Command used:
sudo systemctl status openvpn-server@server

Successfully confirmed service is active and running.
<img width="1920" height="1080" alt="Screenshot (153)" src="https://github.com/user-attachments/assets/59040bb3-032c-4d42-8f41-9f8e83321460" />

## Step 4: Created S3 Bucket

Created S3 bucket for static website hosting.
<img width="1920" height="1080" alt="Screenshot (154) - Copy - Copy" src="https://github.com/user-attachments/assets/56a5f9ab-47b1-4765-8ab8-2ad0652bb5b9" />

## Step 5: CloudFront Distribution

Configured CloudFront for faster global content delivery.
<img width="1920" height="1080" alt="Screenshot (160) - Copy" src="https://github.com/user-attachments/assets/b42a7dd5-8084-4ce3-a5c4-f7b7c802c4cc" />


## Step 6: AWS WAF Security

Created WAF rules to protect web application traffic.
<img width="1920" height="1080" alt="Screenshot (158)" src="https://github.com/user-attachments/assets/ac6b442a-e94d-4011-a04a-09f7c067fd95" />

result
<img width="1920" height="1080" alt="Screenshot (159) - Copy" src="https://github.com/user-attachments/assets/067fae37-c416-4041-8d6a-ea09aafc290c" />






