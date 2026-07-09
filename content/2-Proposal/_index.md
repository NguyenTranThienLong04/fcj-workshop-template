---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Sports Field Booking System

## AWS-Based Web Application Deployment Solution

### 1. Executive Summary

The Sports Field Booking System is designed to help users search for sports venues, book fields online, and manage their booking history through a web-based platform. The system is deployed on AWS using a **Multi-tier Architecture** to provide high availability, security, scalability, and operational efficiency.

The architecture uses **Amazon ECS** to deploy the application as Docker containers, **Amazon RDS** as the relational database, **Amazon ElastiCache for Redis** for caching, **Amazon S3** for storing static assets and uploaded images, **Amazon CloudFront** for fast content delivery, and **Amazon Route 53** for DNS management. The system is protected by **AWS WAF**, while **AWS Certificate Manager (ACM)** provides SSL/TLS certificates for secure HTTPS communication.

---

## 2. Problem Statement

### Current Challenges

Many sports facilities still manage bookings manually through phone calls or paper records, resulting in:

- Difficulty managing booking schedules.
- Risk of double bookings.
- No centralized booking or payment management.
- Poor scalability as the number of sports fields increases.
- Limited availability during periods of high traffic.

### Proposed Solution

Deploy the application on AWS using a cloud-native architecture.

Users access the application through **Amazon Route 53** and **Amazon CloudFront**.

CloudFront works together with **AWS WAF** to accelerate content delivery while protecting the application from common web attacks.

An **Application Load Balancer (ALB)** distributes incoming requests to containers running on **Amazon ECS**.

The application accesses **Amazon RDS**, which is deployed inside private subnets.

**Amazon ElastiCache for Redis** caches frequently accessed data to reduce database workload.

Images and static assets are stored in **Amazon S3**.

Application Docker images are stored in **Amazon ECR**.

Sensitive information such as database credentials and API secrets is managed securely using **AWS Secrets Manager**.

**Amazon CloudWatch** continuously monitors the infrastructure and sends notifications through **Amazon SNS** when issues occur.

### Benefits

- Automatic scaling.
- High security.
- High availability.
- Easier application deployment.
- Reduced operational overhead.
- Improved performance through CloudFront and Redis caching.

---

## 3. Solution Architecture

The system is deployed within an **Amazon VPC** consisting of **Public Subnets** and **Private Subnets** across two **Availability Zones** to achieve high availability.

The system workflow is as follows:

1. Users access the website through Amazon Route 53.
2. Amazon CloudFront delivers content from the nearest edge location.
3. AWS WAF filters malicious requests.
4. Valid requests are forwarded to the Application Load Balancer.
5. The ALB distributes traffic to containers running on Amazon ECS.
6. ECS processes business logic.
7. Application data is stored in the primary Amazon RDS instance.
8. Amazon ElastiCache for Redis caches frequently accessed data.
9. Amazon RDS Multi-AZ maintains a standby database instance for disaster recovery.
10. Amazon S3 stores frontend files and user-uploaded content.
11. Docker images are stored in Amazon ECR.
12. AWS Secrets Manager securely manages database credentials and application secrets.
13. Amazon CloudWatch monitors the entire infrastructure.
14. Amazon SNS sends email notifications when alarms are triggered.

![System Architecture](/images/diagram_aws.jpg)

### AWS Services Used

- Amazon Route 53
- Amazon CloudFront
- AWS WAF
- AWS Certificate Manager (ACM)
- Amazon S3
- Amazon VPC
- Public Subnets
- Private Subnets
- NAT Gateway
- Application Load Balancer
- Amazon ECS
- Amazon RDS
- Amazon ElastiCache for Redis
- Amazon ECR
- AWS Secrets Manager
- Amazon CloudWatch
- Amazon SNS

### Component Design

**Edge Layer**

- Amazon Route 53 manages DNS.
- Amazon CloudFront delivers content globally.
- AWS WAF protects against web attacks.
- AWS Certificate Manager provides SSL/TLS certificates.
- Amazon S3 stores frontend files and uploaded content.

**Application Layer**

- Application Load Balancer distributes traffic.
- Amazon ECS hosts backend containers.
- Amazon ECR stores Docker container images.

**Database Layer**

- Amazon RDS Primary Database.
- Amazon RDS Multi-AZ Standby Database.
- Amazon ElastiCache for Redis.

**Monitoring Layer**

- Amazon CloudWatch monitors infrastructure.
- Amazon SNS sends email notifications and alerts.

---

## 4. Technical Implementation

### Phase 1

- Analyze system requirements.
- Design the database.
- Design the AWS architecture.

### Phase 2

- Create the Amazon VPC.
- Configure Public and Private Subnets.
- Configure NAT Gateway.
- Configure Security Groups.

### Phase 3

- Deploy Amazon ECS.
- Push Docker images to Amazon ECR.
- Configure the Application Load Balancer.

### Phase 4

- Deploy Amazon RDS.
- Deploy Amazon ElastiCache for Redis.
- Configure AWS Secrets Manager.

### Phase 5

- Configure Amazon CloudFront.
- Configure Amazon Route 53.
- Configure AWS WAF.
- Configure AWS Certificate Manager.

### Phase 6

- Configure Amazon CloudWatch.
- Configure Amazon SNS.
- Perform system testing.
- Deploy the production environment.

---

## 5. Deployment Roadmap

| Phase | Activities |
|--------|------------|
| Month 1 | System design |
| Month 2 | Backend and database development |
| Month 3 | Deploy Amazon ECS and Amazon RDS |
| Month 4 | Testing and production deployment |

---

## 6. Estimated Budget

The deployment cost includes:

- Amazon ECS
- Amazon RDS
- Amazon ElastiCache for Redis
- Amazon CloudFront
- Amazon Route 53
- Amazon S3
- NAT Gateway
- Application Load Balancer
- Amazon CloudWatch
- Amazon SNS

The total cost depends on the ECS configuration, database size, and actual application traffic.

---

## 7. Risk Assessment

### Risks

- Amazon ECS service failures.
- Database overload.
- Redis service failures.
- DDoS attacks.
- Database storage exhaustion.

### Mitigation Strategies

- Deploy ECS services across multiple Availability Zones.
- Enable Amazon RDS Multi-AZ.
- Use Amazon CloudFront to reduce origin traffic.
- Protect the application using AWS WAF.
- Monitor the system with Amazon CloudWatch and receive alerts through Amazon SNS.

---

## 8. Expected Outcomes

- Stable 24/7 system availability.
- Automatic scalability as user traffic grows.
- Strong security and data protection.
- Faster deployments using Docker containers and Amazon ECS.
- High database availability through Amazon RDS Multi-AZ.
- Simplified maintenance and future upgrades.