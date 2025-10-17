# HVAC Project - Family-Owned Business Website

## Client
A family-owned HVAC business (brother & cousin) seeking to go online to improve customer care and streamline service bookings.

---

## Project Goal
Build a professional, fast, secure, and scalable website where customers can easily:

- Learn about HVAC services
- Book appointments online
- Access the website from anywhere with fast load times and high availability

---

## Client Requirements

- Showcase HVAC services professionally
- Online booking for customers
- Fast, highly available, and globally accessible
- Secure (HTTPS)
- Minimal maintenance with automated deployments

---

## Implementation & Architecture

To meet the client’s requirements, the project uses **AWS services** and a **CI/CD pipeline** for automation:

| Service          | Purpose |
|-----------------|---------|
| **S3**           | Static web hosting for website files (`index.html`, CSS, JS, etc.) |
| **CloudFront**   | Content Delivery Network (CDN) for fast, global access |
| **Route 53**     | Domain management for easy website access via browser |
| **ACM**          | SSL/TLS certificate to secure the website (HTTPS) |
| **CodePipeline** | Orchestrates Continuous Integration / Continuous Deployment (CI/CD) |
| **CloudFormation** | Target deployment service that provisions AWS resources automatically |
| **GitHub**       | Source repository where project files are stored |

**Workflow:**  
The project uses **GitHub as the source**. Every push triggers **CodePipeline**, which automatically provisions and updates the website using **CloudFormation**, ensuring fully automated, repeatable, and reliable deployments.

---

## CI/CD Pipeline Stages

This project is designed as a **3-stage pipeline**:

1. **Source Stage** – Pulls code from GitHub.  
2. **Build/Test Stage** – Optional build or validation steps.  
3. **Deploy-DEV Stage** – Deploys the website to a development environment.  

---

## Features

- Fully responsive static website
- Online booking system integrated
- Secure with HTTPS
- Automated deployment using GitHub → CodePipeline → CloudFormation
- 5-stage CI/CD pipeline ensuring safe, controlled production releases

---

## How to Deploy

1. Clone the repository:

```bash
git clone https://github.com/lalacloudspace/HVAC-Project.git
