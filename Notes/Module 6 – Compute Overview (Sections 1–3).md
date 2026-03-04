# AWS Cloud Foundations  
## Module 6 – Compute Overview (Sections 1–3)

---

## 🎯 Module Objectives

After completing this module, you should be able to:

- Understand the different **AWS compute service models**
- Explain how **Amazon EC2** works and how to configure it
- Identify **EC2 pricing models**
- Apply the **four pillars of EC2 cost optimization**
- Select the appropriate compute solution based on workload requirements

---

# 1. Compute Services Overview

AWS provides multiple compute services designed to support different architectural needs and operational models.

The optimal compute solution depends on:

- Application design
- Usage patterns
- Required level of infrastructure control
- Cost considerations

---

## 1.1 Infrastructure as a Service (IaaS)

### Amazon EC2

Amazon Elastic Compute Cloud (EC2) provides virtual machines in the cloud.

Key characteristics:

- Full control over the operating system (Linux or Windows)
- Instance-based architecture
- Scalable capacity
- Flexible configuration

Best suited for:

- Custom environments
- Legacy applications
- Full OS-level control requirements

---

## 1.2 Serverless Computing

### AWS Lambda

AWS Lambda allows you to run code without provisioning or managing servers.

Key characteristics:

- Event-driven execution
- Automatic scaling
- Pay-per-use pricing model
- Built-in fault tolerance

Best suited for:

- Event-based workloads
- Microservices architectures
- Short-running processes
- Cost-sensitive workloads

---

## 1.3 Container-Based Computing

Examples:

- Amazon ECS
- Amazon EKS
- AWS Fargate
- Amazon ECR

Key characteristics:

- Container orchestration
- Faster deployment cycles
- Microservices support
- Infrastructure abstraction (especially with Fargate)

Best suited for:

- Modern application architectures
- DevOps environments
- Scalable distributed systems

---

## 1.4 Platform as a Service (PaaS)

### AWS Elastic Beanstalk

Elastic Beanstalk simplifies web application deployment.

Key characteristics:

- Automatic provisioning
- Load balancing
- Auto scaling
- Health monitoring
- No additional service charge (pay only for underlying resources)

Best suited for:

- Rapid application deployment
- Developers who want to focus on code instead of infrastructure

---

# 2. Amazon EC2

Amazon EC2 is a foundational AWS service that provides scalable virtual machines in the cloud.

It enables full administrative control over compute resources.

---

## 2.1 Core Components of EC2

### Amazon Machine Image (AMI)

An AMI is a template used to launch EC2 instances.

It contains:

- Operating system
- Preinstalled software (optional)
- Configuration settings

---

### Instance Types

Instance types define the hardware configuration of the virtual machine.

They determine:

- vCPU (processing power)
- Memory (RAM)
- Storage capacity and type
- Network performance

Instance families include:

- General Purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized
- Accelerated Computing

---

## 2.2 Networking Configuration

EC2 instances are launched within a:

- Virtual Private Cloud (VPC)
- Subnet (public or private)

Security is controlled using:

### Security Groups

- Act as virtual firewalls
- Control inbound and outbound traffic
- Define allowed ports, protocols, and sources

---

## 2.3 Identity and Permissions

### IAM Roles

IAM roles allow EC2 instances to securely interact with other AWS services without embedding credentials.

---

## 2.4 Storage Options

### Amazon EBS (Elastic Block Store)

- Persistent block storage
- Data remains after instance stop/start

### Instance Store

- Ephemeral storage
- Data is lost when instance stops or terminates

Additional integrations:

- Amazon S3
- Amazon EFS

---

## 2.5 Monitoring and Lifecycle

### Instance Lifecycle States

- Pending
- Running
- Stopped
- Terminated

### Monitoring

Amazon CloudWatch provides:

- Performance metrics
- Monitoring dashboards
- Historical data

### Elastic IP

Provides a static public IP address that remains associated with your account.

---

# 3. Amazon EC2 Cost Optimization

Effective cost management requires continuous monitoring and strategic resource allocation.

---

## 3.1 EC2 Pricing Models

### On-Demand Instances

- No long-term commitment
- Pay-as-you-go
- Ideal for short-term or unpredictable workloads

---

### Reserved Instances

- 1-year or 3-year commitment
- Discounted pricing
- Best for steady-state workloads

---

### Spot Instances

- Significantly lower cost
- Can be interrupted with a 2-minute notice
- Suitable for fault-tolerant workloads

---

### Dedicated Hosts / Dedicated Instances

- Physically isolated hardware
- Used for compliance or licensing requirements

---

# 3.2 The Four Pillars of Cost Optimization

---

## 1️⃣ Right Sizing

- Match instance type to workload requirements
- Monitor usage with CloudWatch
- Eliminate overprovisioning
- Downsize when possible

---

## 2️⃣ Increase Elasticity

- Stop or hibernate unused instances
- Use Auto Scaling to adjust capacity dynamically
- Avoid paying for idle resources

---

## 3️⃣ Optimal Pricing Model

- Combine On-Demand, Reserved, and Spot Instances strategically
- Consider serverless solutions where appropriate

---

## 4️⃣ Optimize Storage Choices

- Select appropriate EBS volume types
- Resize volumes when needed
- Delete unused snapshots
- Use Amazon S3 lifecycle policies for cost-efficient storage

---

# 4. Key Takeaways

- AWS offers multiple compute models: IaaS, Serverless, Containers, and PaaS
- Amazon EC2 provides full control over virtual machines
- Proper instance selection directly impacts performance and cost
- EC2 offers multiple pricing models for different workload patterns
- Cost optimization requires right sizing, elasticity, pricing strategy, and storage optimization
- Continuous monitoring is essential for long-term cost efficiency