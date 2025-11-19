Module 19: Cloud Computing

1. Introduction to Cloud Computing

Cloud = on-demand delivery of computing services (servers, storage, networking).

Cloud characteristics:

On-demand self-service

Broad network access

Resource pooling

Rapid elasticity

Measured service

Major cloud models: Public, Private, Hybrid, Community Cloud

2. Cloud Service Models
IaaS (Infrastructure as a Service)

Virtual machines, storage, networks

Examples: AWS EC2, Azure VM, Google Compute Engine

PaaS (Platform as a Service)

Development frameworks, runtime, databases

Examples: AWS Elastic Beanstalk, Google App Engine

SaaS (Software as a Service)

End-user applications

Examples: Gmail, Salesforce, Office 365

3. Cloud Reference Architecture

Cloud Consumer – uses cloud services

Cloud Provider – manages infrastructure

Cloud Carrier – network layer

Cloud Broker – manages service usage

Cloud Auditor – evaluates security & compliance

4. Cloud Threat Landscape

Common vulnerabilities in cloud environments:

Misconfigured storage buckets (S3, Blob storage)

Exposed SSH/RDP

Weak IAM policies

Insecure APIs

Unpatched virtual machines

Hypervisor attacks

Multi-tenancy risks

Data remanence (residual data after deletion)

5. Cloud Attack Vectors
1. Cloud Reconnaissance

Discover exposed cloud assets

Tools: Shodan, CloudEnum, S3Scanner

2. Credential Attacks

Brute-force or stolen API keys

Weak IAM users/roles

3. Misconfiguration Exploits

Public S3 buckets

Over-permissive IAM roles

Open security groups

4. Exploiting Cloud Services

Exploit insecure APIs

SSRF to access internal metadata (AWS Instance Metadata: 169.254.169.254)

5. Hypervisor & Container Attacks

VM escape attacks

Container breakout vulnerabilities (Docker/ Kubernetes)

6. Cloud Security Tools (As seen in GitHub CEH reports)

ScoutSuite – multi-cloud auditing

Prowler – AWS security assessment

PacBot – cloud compliance

CloudSploit – cloud misconfiguration scanner

S3Scanner / S3Ripper – S3 bucket discovery

GCP Brute / AzureHound – identity enumeration

Burp Suite – API testing

Nikto / Nmap – cloud-exposed services scanning

7. Cloud Security Controls
Identity and Access Management (IAM)

MFA

Least privilege

Strong access key rotation

Role-based access control

Data Security

Encryption at rest & in transit

Key Management Service (KMS)

Tokenization

Network Security

Security groups

Network ACLs

VPN connectivity

VPC segmentation

Monitoring & Logging

AWS CloudTrail

Azure Monitor

GCP Cloud Logging

SIEM integration (Splunk, QRadar)

8. Virtualization Security (Important for CEH exam)

Types: Full virtualization, Para-virtualization, Hardware-assisted

Threats:

VM Escape

Hyperjacking

Side-channel attacks

Snapshots misuse

Privilege escalation in shared hosts

9. Cloud Pentesting Guidelines

Cloud pentesting requires written authorization

Follow cloud provider rules:

AWS Pentest Policy

Google Cloud PenTest Restrictions

Azure Allowed Activities

Typical targets:

Web apps hosted in cloud

APIs

Cloud storage

Identity configurations

Serverless functions (AWS Lambda, Azure Functions)

10. Cloud Security Best Practices

Enable MFA for all IAM users

Encrypt all data

Apply least privilege

Disable unused services

Monitor API activity

Regular vulnerability scanning

Rotate keys frequently

Block public access to cloud storage

Use Cloud WAF & DDoS protection
