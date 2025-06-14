# Hosting Django Website Using Amazon EC2

This mini project demonstrates how to host a Django web application on Amazon EC2, leveraging the scalability, reliability, and flexibility of AWS cloud infrastructure. The project includes detailed setup of VPC, subnets, EC2 instances, and deploying a sample Django To-Do application.

📝 Abstract

The project explores deploying Django — a high-level Python web framework — on Amazon EC2, a popular cloud platform. It involves setting up virtual networking using VPCs, configuring security groups, installing necessary packages, and deploying the web app manually via SSH. The goal is to help developers host scalable and secure web apps using cloud technology.

🛠️ Technologies Used

- Backend Framework: Django
- Cloud Platform: Amazon Web Services (AWS)
- Service Used: Amazon EC2
- Networking: VPC, Subnets, Route Tables
- Languages: Python, HTML

🔧 Steps to Deploy Django on EC2

Step 1: Set Up AWS Environment
- Create an AWS account and log in to the console.
- Set up a Virtual Private Cloud (VPC) with CIDR block.
- Create two subnets and an Internet Gateway.
- Associate the Internet Gateway with the VPC.
- Create a Route Table and attach subnets.

 Step 2: Launch EC2 Instance
- Choose Amazon Linux 2 as the base image.
- Open required ports: HTTP (80), HTTPS (443), SSH (22).
- Connect to the instance using SSH and the key pair.

 Step 3: Deploy Django Application
```bash
sudo apt update
cd django-on-ec2
sudo apt install python3-pip -y
pip install django
python3 manage.py migrate
python3 manage.py createsuperuser
python3 manage.py runserver
