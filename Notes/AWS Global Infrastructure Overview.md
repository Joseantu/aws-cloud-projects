# AWS Cloud Foundations  
## Module 3 – AWS Global Infrastructure Overview

---

## 🎯 Module Objectives

After completing this module, you should be able to:

- Understand the difference between **AWS Regions**, **Availability Zones**, and **Edge Locations**
- Identify major **AWS service categories**
- Understand how AWS achieves **high availability**, **fault tolerance**, and **scalability**

---

# 1. AWS Global Infrastructure

The AWS Global Infrastructure is designed to provide a cloud environment that is:

- **Flexible**
- **Scalable**
- **Reliable**
- **Secure**
- **High-performance**

It is composed of:

- **Regions**
- **Availability Zones (AZs)**
- **Edge Locations**
- **Regional Edge Caches**

---

## 1.1 AWS Regions

An **AWS Region** is a physical geographic area that contains multiple Availability Zones.

### Key Characteristics

- Each Region contains **two or more Availability Zones**
- Data replication across Regions is controlled by the customer
- Regions are connected via AWS’s private backbone network
- Designed for full redundancy and high availability

### How to Choose a Region

When selecting a Region, consider:

- **Data governance and compliance requirements**
- **Proximity to customers (latency)**
- **Service availability**
- **Pricing differences between Regions**

---

## 1.2 Availability Zones (AZs)

An **Availability Zone (AZ)** is one or more isolated data centers within a Region.

### Key Characteristics

- Each Region has multiple AZs
- AZs are **physically separated**
- Designed for **fault isolation**
- Connected via high-speed private networking
- Best practice: deploy applications across multiple AZs

---

## 1.3 AWS Data Centers

Data centers are the physical facilities where AWS infrastructure operates.

Each data center includes:

- Redundant power systems
- Backup generators
- Cooling systems
- Network redundancy

Typically, a data center contains **50,000–80,000 physical servers**.

---

## 1.4 Edge Locations and Content Delivery

AWS operates global **Points of Presence (PoP)**, including:

- **Edge Locations**
- **Regional Edge Caches**

These are primarily used by Amazon CloudFront (AWS CDN).

### Purpose

- Reduce latency
- Deliver content closer to end users
- Cache frequently accessed content
- Improve application performance

---

## 1.5 Infrastructure Design Principles

### Elasticity
Automatically adjusts capacity based on demand.

### Scalability
Supports growth as application usage increases.

### Fault Tolerance
Continues operating even when components fail.

### High Availability
Minimizes downtime through redundancy and automation.

---

# 2. AWS Service Categories Overview

AWS services are grouped into categories.

---

## 2.1 Compute Services

Examples:

- Amazon EC2
- Auto Scaling
- AWS Lambda
- Amazon ECS
- Amazon EKS
- AWS Elastic Beanstalk
- AWS Fargate

---

## 2.2 Storage Services

Examples:

- Amazon S3
- Amazon EBS
- Amazon EFS
- Amazon S3 Glacier

---

## 2.3 Database Services

Examples:

- Amazon RDS
- Amazon Aurora
- Amazon DynamoDB
- Amazon Redshift

---

## 2.4 Networking & Content Delivery

Examples:

- Amazon VPC
- Elastic Load Balancing
- AWS Direct Connect
- Amazon Route 53
- Amazon CloudFront
- AWS Transit Gateway
- AWS VPN

---

## 2.5 Security, Identity & Compliance

Examples:

- AWS IAM
- AWS Organizations
- Amazon Cognito
- AWS KMS
- AWS Shield
- AWS Artifact

---

## 2.6 Management & Governance

Examples:

- AWS Management Console
- AWS CloudWatch
- AWS CloudTrail
- AWS Config
- AWS Trusted Advisor
- AWS CLI
- AWS Well-Architected Tool

---

## 2.7 Cost Management

Examples:

- AWS Cost Explorer
- AWS Budgets
- AWS Cost and Usage Report

---

# 3. Key Takeaways

- AWS Global Infrastructure = **Regions + Availability Zones + Edge Locations**
- Choose Regions based on **compliance, latency, service availability, and cost**
- Deploy across multiple AZs for **high availability**
- Edge Locations reduce latency using caching
- AWS services are organized into functional categories