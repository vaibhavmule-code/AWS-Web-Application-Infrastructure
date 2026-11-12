# AWS Web Application Infrastructure with Load Balancing and Managed Database

## Project Overview

This project demonstrates the deployment of a web application infrastructure on Amazon Web Services (AWS), integrating compute, database, load balancing, DNS management, and SSL/TLS certificate services.

The infrastructure uses Amazon EC2 for application hosting, Amazon RDS with MySQL for managed database operations, Elastic Load Balancing for traffic distribution, Amazon Route 53 for DNS management, and AWS Certificate Manager (ACM) for SSL/TLS certificate management.

The project focuses on understanding how different AWS services work together to support reliable, secure, and scalable web application infrastructure.

## Architecture

### AWS Services Used

| AWS Service | Purpose |
|---|---|
| Amazon EC2 | Application hosting and compute |
| Amazon RDS | Managed relational database |
| MySQL | Database engine |
| Classic Load Balancer (CLB) | Application traffic distribution |
| Amazon Route 53 | DNS and domain management |
| AWS Certificate Manager (ACM) | SSL/TLS certificate management |

### Architecture Flow

```text
                 Internet Users
                       |
                       v
                Amazon Route 53
                 (DNS Routing)
                       |
                       v
              Classic Load Balancer
                       |
                       v
                 Amazon EC2
              (Web Application)
                       |
                       v
                Amazon RDS
                  (MySQL)

          AWS Certificate Manager
             (SSL/TLS Certificate)
                       |
                       v
             HTTPS Listener on CLB
```

*Note: The diagram represents the logical service flow. ACM certificate integration is associated with the load balancer's HTTPS listener.*

## Implementation Steps

### 1. Amazon EC2 Configuration

- Provisioned EC2 instances for web application hosting.
- Configured instance access and security groups.
- Prepared the application hosting environment.

### 2. Amazon RDS with MySQL

- Created an Amazon RDS database using the MySQL engine.
- Configured database connectivity.
- Integrated the application environment with the managed database.

### 3. Classic Load Balancer Configuration

- Configured a Classic Load Balancer.
- Set up traffic distribution to registered EC2 instances.
- Configured listener settings and application health checks.

### 4. Amazon Route 53 Configuration

- Configured DNS management using Amazon Route 53.
- Connected the application domain to the load balancer through DNS records.

### 5. AWS Certificate Manager (ACM)

- Configured SSL/TLS certificate management using AWS Certificate Manager.
- Integrated the certificate with the load balancer's HTTPS listener.
- Explored secure application access using HTTPS.

## Security Considerations

- Use security groups to control inbound and outbound traffic.
- Restrict database access to authorized application resources.
- Avoid exposing database ports publicly.
- Use HTTPS for encrypted application communication.
- Follow least-privilege access principles for IAM permissions.
- Never commit AWS access keys, passwords, private keys, or database credentials to GitHub.

## Technologies and Tools

- Amazon Web Services (AWS)
- Amazon EC2
- Amazon RDS
- MySQL
- Classic Load Balancer
- Amazon Route 53
- AWS Certificate Manager
- Security Groups
- DNS
- SSL/TLS
- Git and GitHub

## Key Learning Outcomes

- Understanding AWS compute and managed database services.
- Integrating EC2 with Amazon RDS and MySQL.
- Understanding application traffic distribution through load balancing.
- Configuring DNS management using Route 53.
- Understanding SSL/TLS certificate integration using ACM.
- Learning how multiple AWS services work together in a web application architecture.
- Understanding cloud infrastructure security and application connectivity.

## Project Repository

GitHub: https://github.com/vaibhavmule-code/AWS/tree/main/Projects/EC2-RDS-MySQL-CLB-Route53-ACM

---

**Project Category:** Cloud Infrastructure / AWS

**Platform:** Amazon Web Services

**Focus Areas:** Compute, Database, Load Balancing, DNS Management, and SSL/TLS Security
