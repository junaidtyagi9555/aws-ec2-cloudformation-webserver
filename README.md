# EC2 Web Server Deployment using AWS CloudFormation

## 📋 Project Overview
This project demonstrates Infrastructure as Code (IaC) by deploying a fully functional Apache web server on AWS EC2 using AWS CloudFormation. The template automates security group configuration, instance deployment, and web server installation.

## 🏗️ Architecture
- **AWS CloudFormation**: Infrastructure definition and deployment
- **EC2 Instance**: Hosts Apache web server (Amazon Linux 2)
- **Security Groups**: Controls SSH and HTTP access
- **User Data Script**: Automates software installation and configuration

## 🛠️ Technologies Used
- AWS CloudFormation (YAML)
- Amazon EC2
- Security Groups
- Apache HTTP Server
- Bash Scripting

## 🚀 Deployment Steps

### Prerequisites
- AWS Account
- EC2 Key Pair
- CloudFormation Access

### Quick Start
1. Create or use existing EC2 Key Pair
2. Deploy CloudFormation stack:
   ```bash
   aws cloudformation create-stack \
     --stack-name ec2-webserver \
     --template-body file://templates/ec2-webserver.yaml \
     --parameters ParameterKey=KeyName,ParameterValue=junaid-key