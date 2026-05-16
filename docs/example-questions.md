# Example Questions

These are study questions for practice. They are not official AWS exam questions.

## Question 1

A company wants to avoid buying servers upfront and prefers to pay only for what it uses. Which cloud economics concept best describes this benefit?

- A. Capital expenditure
- B. Operational expenditure
- C. Reserved capacity
- D. Vertical scaling

Answer: `B`

Explanation:

`OPEX` means paying for usage over time instead of making large upfront capital purchases. This is one of the core cloud value propositions.

## Question 2

Which AWS service helps record API calls made in an AWS account for governance and audit purposes?

- A. Amazon CloudWatch
- B. AWS CloudTrail
- C. AWS Config
- D. AWS Trusted Advisor

Answer: `B`

Explanation:

`CloudTrail` records API activity. `CloudWatch` is for monitoring metrics/logs/alarms. `Config` tracks resource configuration and compliance state.

## Question 3

Which AWS service is best for object storage with high durability and broad integration across AWS services?

- A. Amazon EBS
- B. Amazon EFS
- C. Amazon S3
- D. Amazon FSx

Answer: `C`

Explanation:

`S3` is AWS object storage. `EBS` is block storage for EC2. `EFS` is shared file storage.

## Question 4

A workload runs only when a file is uploaded and should use the lowest operational overhead possible. Which service is the best fit?

- A. Amazon EC2
- B. AWS Lambda
- C. Amazon EKS
- D. AWS Direct Connect

Answer: `B`

Explanation:

`Lambda` is serverless and event-driven, which matches file-upload triggers well. The other options require more infrastructure or solve unrelated problems.

## Question 5

Which part of the shared responsibility model is AWS responsible for?

- A. Configuring customer IAM policies correctly
- B. Encrypting customer application data by default in every design
- C. Securing the physical infrastructure that runs AWS services
- D. Patching the guest operating system on Amazon EC2 instances

Answer: `C`

Explanation:

AWS is responsible for security `of` the cloud, including physical infrastructure. Customers are responsible for guest OS patching on EC2 and correct IAM configuration.

## Question 6

Which AWS service is primarily used to centrally manage encryption keys?

- A. AWS KMS
- B. Amazon GuardDuty
- C. AWS Shield
- D. Amazon Inspector

Answer: `A`

Explanation:

`AWS KMS` manages encryption keys. `GuardDuty` is threat detection. `Shield` is DDoS protection. `Inspector` helps with vulnerability management.

## Question 7

A company wants a managed relational database. Which service is the best fit?

- A. Amazon DynamoDB
- B. Amazon RDS
- C. Amazon S3
- D. Amazon SQS

Answer: `B`

Explanation:

`RDS` is the standard managed relational database answer. `DynamoDB` is NoSQL.

## Question 8

Which service helps analyze current and forecasted AWS costs with visual reports?

- A. AWS Budgets
- B. AWS Cost Explorer
- C. AWS CloudFormation
- D. AWS Artifact

Answer: `B`

Explanation:

`Cost Explorer` is for cost analysis and forecasting views. `Budgets` is more focused on thresholds and alerts.

## Question 9

Which AWS service is best for decoupling applications by storing messages until consumers are ready to process them?

- A. Amazon SNS
- B. Amazon SQS
- C. Amazon Route 53
- D. AWS Step Functions

Answer: `B`

Explanation:

`SQS` is a queue. `SNS` is pub/sub notification. Both are useful, but the keyword `storing messages until consumers are ready` points to `SQS`.

## Question 10

Which AWS service helps evaluate AWS resources against desired configurations and compliance rules?

- A. AWS Config
- B. Amazon CloudWatch
- C. AWS CloudTrail
- D. AWS Lambda

Answer: `A`

Explanation:

`AWS Config` tracks configuration history and compliance posture.

## Question 11

A company needs a dedicated private network connection from its data center to AWS. Which service should it use?

- A. AWS VPN
- B. AWS Direct Connect
- C. Amazon CloudFront
- D. AWS PrivateLink

Answer: `B`

Explanation:

`Direct Connect` is the dedicated private connectivity option. `VPN` uses the internet.

## Question 12

Which AWS service is best for DNS routing?

- A. Amazon Route 53
- B. AWS Transit Gateway
- C. Amazon VPC
- D. Amazon CloudWatch

Answer: `A`

Explanation:

`Route 53` is AWS DNS and routing.

## Question 13

Which option usually provides the lowest cost for interruptible workloads?

- A. On-Demand Instances
- B. Reserved Instances
- C. Spot Instances
- D. Dedicated Hosts

Answer: `C`

Explanation:

`Spot` is generally the lowest cost option, but workloads must tolerate interruption.

## Question 14

Which AWS service is used to distribute cached content closer to users globally?

- A. Amazon CloudFront
- B. Amazon EC2
- C. AWS Snowball
- D. Amazon RDS

Answer: `A`

Explanation:

`CloudFront` is the CDN answer and uses edge locations.

## Question 15

Which AWS service helps detect suspicious activity and potential threats in AWS accounts and workloads?

- A. AWS GuardDuty
- B. AWS Artifact
- C. AWS Budgets
- D. Amazon SQS

Answer: `A`

Explanation:

`GuardDuty` is the managed threat detection service.

## Multi-Response Question 16

Which two services are commonly used for monitoring and audit visibility?

- A. Amazon CloudWatch
- B. AWS CloudTrail
- C. Amazon S3 Glacier
- D. AWS Snow Family
- E. Amazon Route 53

Answers: `A`, `B`

Explanation:

`CloudWatch` is operational monitoring. `CloudTrail` is API audit history.

## Multi-Response Question 17

Which two statements about AWS Lambda are correct?

- A. It is a serverless compute service.
- B. It requires users to provision the underlying servers.
- C. It can run in response to events.
- D. It is primarily a relational database service.
- E. It always costs less than every other compute option.

Answers: `A`, `C`

Explanation:

Lambda is event-driven serverless compute. The other answers are false or too absolute.

## Multi-Response Question 18

Which two services are primarily used for cost visibility and control?

- A. AWS Budgets
- B. AWS Cost Explorer
- C. AWS WAF
- D. Amazon Inspector
- E. Amazon Route 53

Answers: `A`, `B`

Explanation:

`Budgets` helps with thresholds and alerts. `Cost Explorer` helps analyze spend.

## How To Use These Questions

- Answer without looking first.
- Explain why each wrong option is wrong.
- If you miss a question, add the topic to `practice-review-template.md`.
