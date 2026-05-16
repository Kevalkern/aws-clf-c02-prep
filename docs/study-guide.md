# Study Guide

This guide is built for `AWS Certified Cloud Practitioner (CLF-C02)` preparation as of `2026-05-16`.

Official AWS references:

- Exam guide: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html`
- In-scope services: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html`

## What The Exam Actually Tests

The exam is not a hands-on build exam. It is mainly a recognition and decision exam:

- What problem does a service solve?
- Which service is the best fit for a scenario?
- Which option reduces operational overhead?
- Which option is more secure, more cost-aware, or more highly available?

Do not over-study implementation details. Study service purpose, tradeoffs, and common comparisons.

## Domain 1: Cloud Concepts

### AWS Value Proposition

You need to explain why companies use AWS:

- trade `CAPEX` for `OPEX`
- gain elasticity instead of overprovisioning
- deploy globally faster
- improve speed of experimentation
- increase resilience with managed infrastructure

### Global Infrastructure

Know these exactly:

- `Region`: geographic area with multiple AWS data centers
- `Availability Zone`: isolated location within a Region
- `Edge location`: location used mainly for content delivery and some edge services

Common trap:

- high availability inside one Region usually means using multiple Availability Zones, not multiple Regions

### Shared Responsibility Model

High-value rule:

- AWS secures `of` the cloud
- customer secures `in` the cloud

Examples AWS handles:

- physical facilities
- hardware
- managed service infrastructure

Examples customer handles:

- IAM permissions
- data classification
- encryption choices
- guest OS patching on EC2
- security group configuration

### Well-Architected Framework

Know the pillars:

- Operational Excellence
- Security
- Reliability
- Performance Efficiency
- Cost Optimization
- Sustainability

You usually do not need deep framework mechanics. You do need to recognize pillar intent.

## Domain 2: Security And Compliance

### IAM

This is one of the most important exam areas.

Know:

- `User`: identity for a person or workload when used directly
- `Group`: collection of users
- `Role`: temporary permissions assumed by users, apps, or services
- `Policy`: JSON permissions document

Exam-safe rules:

- use roles for AWS services
- avoid daily use of the root user
- enable MFA
- grant least privilege

### IAM Identity Center

Use for centralized workforce access across AWS accounts and integrated applications.

Typical trap:

- do not confuse `IAM` with `IAM Identity Center`
- IAM is foundational permission control
- IAM Identity Center is broader workforce access and account access management

### Security Services

Know the purpose of these:

- `KMS`: manage encryption keys
- `Secrets Manager`: store and rotate secrets
- `ACM`: manage TLS/SSL certificates
- `WAF`: protect web apps from common web exploits
- `Shield`: DDoS protection
- `GuardDuty`: threat detection
- `Security Hub`: aggregate security findings
- `Macie`: discover sensitive data in S3
- `Inspector`: vulnerability management and scanning context

### Monitoring And Audit

This comparison appears constantly:

- `CloudWatch`: metrics, logs, alarms, operational monitoring
- `CloudTrail`: API activity and account audit history
- `AWS Config`: resource configuration history and compliance evaluation

If the question asks:

- "Who changed what?" -> `CloudTrail`
- "Is this resource compliant?" -> `Config`
- "What is the CPU utilization or alarm status?" -> `CloudWatch`

### Governance

Know:

- `Organizations`: multi-account management
- `Control Tower`: landing zone and governance setup
- `Trusted Advisor`: recommendations for cost, security, limits, performance
- `Artifact`: compliance reports and agreements

## Domain 3: Cloud Technology And Services

This is the biggest domain. Focus on service recognition.

### Compute

- `EC2`: virtual servers with the most control
- `Lambda`: event-driven serverless compute
- `Elastic Beanstalk`: platform for deploying applications with reduced management overhead
- `Lightsail`: simplified hosting
- `Auto Scaling`: adjusts capacity
- `Elastic Load Balancing`: distributes incoming traffic

Decision pattern:

- lowest ops, event-driven -> `Lambda`
- full server control -> `EC2`
- simple app deployment without managing much infra detail -> `Elastic Beanstalk`

### Containers

- `ECS`: AWS container orchestration
- `EKS`: managed Kubernetes
- `ECR`: container registry
- `Fargate`: serverless container compute

Decision pattern:

- want containers without managing servers -> `Fargate`
- standardized on Kubernetes -> `EKS`

### Storage

- `S3`: object storage
- `EBS`: block storage for EC2
- `EFS`: shared file storage across instances
- `FSx`: managed file system families
- `S3 Glacier`: archival storage
- `Storage Gateway`: hybrid storage integration

Critical comparison:

- `S3` is object storage
- `EBS` is block storage for an EC2 instance
- `EFS` is shared file storage

### Databases

- `RDS`: managed relational database
- `Aurora`: AWS relational engine compatible with MySQL/PostgreSQL
- `DynamoDB`: serverless NoSQL
- `ElastiCache`: caching
- `DocumentDB`: document database
- `Neptune`: graph database

Critical comparison:

- relational -> `RDS` or `Aurora`
- key-value/document at scale -> `DynamoDB`
- cache layer -> `ElastiCache`

### Networking

- `VPC`: isolated network
- `Route 53`: DNS and routing
- `CloudFront`: CDN
- `API Gateway`: managed APIs
- `Direct Connect`: dedicated private connectivity
- `VPN`: encrypted network tunnel over the internet
- `PrivateLink`: private access to services
- `Transit Gateway`: connect multiple networks

Critical comparison:

- private dedicated line -> `Direct Connect`
- encrypted tunnel over public internet -> `VPN`

### Integration

- `SQS`: message queue
- `SNS`: pub/sub notifications
- `EventBridge`: event bus and routing
- `Step Functions`: workflow orchestration

Critical comparison:

- fan-out notification -> `SNS`
- decoupled queued messages -> `SQS`

### Migration

- `DMS`: database migration
- `Migration Hub`: migration tracking
- `Application Migration Service`: server migration
- `Snow Family`: physical transfer / edge devices

### Analytics And ML

You do not need deep expertise. You do need broad recognition:

- `Athena`: query S3 with SQL
- `Redshift`: data warehouse
- `QuickSight`: BI dashboards
- `Glue`: ETL/data integration
- `Kinesis`: streaming data
- `SageMaker AI`: machine learning platform
- `Textract`: extract text/data from documents
- `Rekognition`: image/video analysis

## Domain 4: Billing, Pricing, And Support

### Pricing Models

Know these clearly:

- `On-Demand`: pay as you go
- `Reserved Instances`: commit for discount on some services like EC2/RDS
- `Savings Plans`: flexible commitment-based savings
- `Spot`: use spare capacity at steep discounts with interruption risk

Decision pattern:

- predictable long-term usage -> `Reserved` or `Savings Plans`
- interruptible workloads -> `Spot`

### Cost Tools

- `Budgets`: alerts and thresholds
- `Cost Explorer`: analyze spending trends
- `Cost and Usage Reports`: detailed billing data
- `Marketplace`: third-party software

### Support Plans

Know support plan differences at a high level:

- response time differences
- architectural guidance availability
- TAM-style features at higher tiers
- basic support gives limited support features

### Billing Concepts

Know:

- consolidated billing
- tagging for cost allocation
- free tier at a high level
- pricing calculators and estimation concepts

## Best Study Method

Use this loop:

1. Learn the service purpose.
2. Compare it against the closest competing service.
3. Answer scenario questions.
4. Write one-sentence explanations for mistakes.

## Common Exam Traps

- choosing a real AWS service that works but is not the best fit
- overcomplicating a simple managed-service answer
- mixing operational monitoring with audit logging
- mixing storage types
- confusing governance tools with security tools
- picking the most powerful service instead of the most cost-effective or lowest-ops service

## Final Advice

For CLF-C02, breadth matters more than depth. If you can explain what a service is, when to use it, and how it differs from the obvious alternatives, you are studying the right way.
