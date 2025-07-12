# AWS EC2 Web Server Setup

## Description
This project demonstrates how to launch an EC2 instance using Amazon Linux 2023, install Apache, and serve a simple HTML page accessible via public IP.

## Architecture
- EC2 instance (t2.micro)
- Apache Web Server (`httpd`)
- Amazon Linux 2023
- Security Group with HTTP (port 80) access enabled

## Setup Steps

1. Launch an EC2 instance (Amazon Linux 2023)
2. Open ports 22 and 80 in the security group
3. Connect to the instance using EC2 Instance Connect
4. Run the following commands:

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
echo "Hello from EC2!" | sudo tee /var/www/html/index.html
5. Visit your instance’s public IP in the browser:  
   `http://18.197.158.213`

## Screenshot
![EC2 Web Page](screenshot%20hello%20world.png)

## Technologies Used
- AWS EC2
- Amazon Linux 2023
- Apache Web Server
- SSH / EC2 Instance Connect

## Author
Ciro — 2025
