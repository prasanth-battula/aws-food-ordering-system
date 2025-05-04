# AWS Food-Ordering System

A simple, cloud-based food‐ordering web application built and deployed on AWS. Customers can browse a menu, place orders, and upload images; all backed by secure AWS infrastructure.

---

## 📋 Table of Contents
1. [Overview](#overview)  
2. [Features](#features)  
3. [Architecture](#architecture)  
4. [AWS Services Used](#aws-services-used)  
5. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation & Deployment](#installation--deployment)  
6. [Usage](#usage)  
7. [Folder Structure](#folder-structure)  
8. [Contributing](#contributing)  
9. [License](#license)  

---

## 🧐 Overview
This project demonstrates a basic food‐ordering system deployed entirely on AWS. It includes:
- A front‐end web application for browsing a menu and placing orders  
- Back‐end APIs running on EC2 instances  
- A MySQL database managed by Amazon RDS  
- Static assets (images, CSS) stored in S3  
- Secure networking via a custom VPC and Security Groups  
- Monitoring and alerts with CloudWatch  

---

## ✨ Features
- **Browse Menu**: View available dishes with images and prices  
- **Place Order**: Submit orders via form; data persisted to RDS  
- **Image Upload**: Customers can upload a photo to S3  
- **Security**: Network isolation with public/private subnets and firewall rules  
- **Resilience**: CloudWatch alarms and auto-recovery of unhealthy EC2 instances  

---

## 🏗 Architecture
[Internet]
↓
Elastic Load Balancer
↓
EC2 Instances (Node.js/Python APIs)
↓
Amazon RDS (MySQL)
↑
Amazon S3 ← Customer Image Uploads

All resources live inside a custom VPC with public and private subnets. Security Groups allow only HTTP(S) to EC2 and MySQL port access from within the VPC.

---

## ☁️ AWS Services Used
- **Compute**: EC2  
- **Database**: Amazon RDS (MySQL)  
- **Storage**: Amazon S3  
- **Networking**: VPC, Subnets, Security Groups  
- **Monitoring**: CloudWatch (metrics, logs, alarms)  
- **Deployment**: AWS CLI & CloudShell 
