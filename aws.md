# AWS Interview Questions & Answers

## 1. What AWS services have you worked with?
**Answer:**
- Worked with **AWS S3** as a file storage solution.
- Used **AWS Lambda** for event-driven notifications.
- Implemented **AWS SNS/SQS** for asynchronous messaging.
- Experience with **EC2**, **RDS**, **CloudWatch**, and **IAM**.
- Working on **migrating monolith to microservices** using AWS services.

---

## 2. What is AWS IAM, and what are its key components?
**Answer:**
AWS IAM (Identity and Access Management) controls access to AWS resources securely.

### Key Components:
- **Users** – Individual identities with specific permissions.
- **Groups** – Collections of users with common permissions.
- **Roles** – Temporary permissions for AWS services or users.
- **Policies** – JSON documents defining permissions.
- **MFA (Multi-Factor Authentication)** – Extra security layer.
- **Permissions Boundaries** – Restrict excessive privileges.

### Best Practices:
- Follow **Principle of Least Privilege**.
- Use **IAM Roles** instead of storing credentials.
- Enable **MFA** and **rotate access keys regularly**.
- Audit IAM permissions frequently.

---

## 3. How do you secure an S3 bucket in AWS?
**Answer:**
1. **Block Public Access** – Prevents accidental exposure.
2. **Use IAM & Bucket Policies** – Control access at bucket and object levels.
3. **Enable Encryption** – SSE-S3, SSE-KMS, or Client-Side Encryption.
4. **Use Access Control Lists (ACLs) carefully** – Prefer IAM policies.
5. **Enable MFA Delete** – Prevent accidental/malicious deletions.
6. **Use VPC Endpoints** – Restrict access to a specific VPC.
7. **Enable Logging & Monitoring** – Use **CloudTrail** and **S3 Access Logs**.

### Example:
If storing sensitive customer data in S3:
- **Block public access**, **use IAM roles**, **enable encryption**, and **monitor activity** using CloudTrail.

---

## 4. What is AWS Lambda, and how does it work?
**Answer:**
AWS Lambda is a serverless compute service that runs code in response to events.

### How It Works:
- Code runs **without provisioning or managing servers**.
- Supports multiple languages (**C#, Python, Node.js, etc.**).
- Triggers include **API Gateway, S3, SNS, DynamoDB, CloudWatch**.
- Bills based on execution time and memory usage.

### Example Use Case:
- An **S3 upload** triggers a Lambda function that **processes the file** and **stores metadata in a database**.

---

## 5. How do you optimize AWS Lambda performance?
**Answer:**
1. **Reduce cold starts** – Use **Provisioned Concurrency**.
2. **Use appropriate memory settings** – Higher memory means faster execution.
3. **Optimize package size** – Reduce dependencies.
4. **Use async processing** – Avoid synchronous API calls.
5. **Enable caching** – Use **AWS Lambda Extensions or DynamoDB**.

---

## 6. What is the difference between AWS SNS and SQS?
**Answer:**
| Feature  | AWS SNS (Simple Notification Service) | AWS SQS (Simple Queue Service) |
|----------|-------------------------------------|------------------------------|
| Type     | **Pub/Sub (Push Model)**          | **Message Queue (Pull Model)** |
| Use Case | Send messages to multiple subscribers (e.g., email, Lambda) | Store messages until consumed |
| Message Retention | No retention | Up to 14 days |
| Example | Notify users about an event | Process jobs asynchronously |

### Example Use Case:
- **SNS**: Notify users about a new product.
- **SQS**: Queue tasks for background processing.

---

## 7. What are AWS VPC and its components?
**Answer:**
AWS **VPC (Virtual Private Cloud)** allows you to create an isolated network in AWS.

### Key Components:
- **Subnets** – Divide the VPC into private and public zones.
- **Internet Gateway** – Enables internet access for public subnets.
- **NAT Gateway** – Allows private subnets to access the internet securely.
- **Route Tables** – Control traffic flow.
- **Security Groups & NACLs** – Firewalls for inbound/outbound rules.

### Example:
- **Web app** with a **public subnet (EC2 + Load Balancer)** and a **private subnet (RDS, Redis, etc.)**.

---

## 8. How do you monitor and troubleshoot AWS applications?
**Answer:**
1. **AWS CloudWatch** – Monitors metrics, logs, and events.
2. **AWS CloudTrail** – Tracks API calls and changes.
3. **AWS X-Ray** – Traces application requests.
4. **S3 Access Logs** – Tracks who accessed data.
5. **AWS Config** – Monitors compliance and configuration changes.

### Example:
If an **EC2 instance crashes**, check **CloudWatch logs**, **system metrics**, and **CloudTrail** for API changes.

---

## 9. How do you handle scalability in AWS?
**Answer:**
1. **Auto Scaling** – Automatically adjust EC2 instances.
2. **Load Balancing (ALB, NLB)** – Distributes traffic.
3. **S3 & CloudFront** – Cache static assets.
4. **RDS Read Replicas** – Scale databases.
5. **DynamoDB On-Demand Scaling** – Handle variable traffic.
6. **Message Queues (SQS, SNS, Kinesis)** – Decouple microservices.

### Example:
- **Web app** with **EC2 Auto Scaling**, **ALB**, and **RDS Read Replicas** to handle increased traffic.

---

## 10. What is AWS Fargate, and how does it compare to EC2?
**Answer:**
AWS **Fargate** is a **serverless compute engine** for containers, whereas **EC2** provides full control over virtual machines.

| Feature | AWS Fargate | AWS EC2 |
|---------|------------|---------|
| Management | Fully managed | Requires setup & maintenance |
| Scaling | Auto-scales containers | Manual scaling needed |
| Pricing | Pay per task execution | Pay for instance uptime |
| Use Case | Short-lived, event-driven workloads | Long-running applications |

### Example Use Case:
- **Fargate**: Run microservices without managing infrastructure.
- **EC2**: Host a full-stack web app with persistent storage.

---

## Final Tips for AWS Interview Success 🚀
✅ **Understand core AWS services** (IAM, EC2, S3, Lambda, RDS, VPC, CloudWatch).
✅ **Practice security best practices** (IAM roles, S3 policies, encryption).
✅ **Be ready to discuss scalability & performance optimization**.
✅ **Use real-world examples from your projects**.
✅ **Explain concepts clearly & concisely**.

---

🔹 **Next Step:** Review this document, try to **say answers out loud**, and let me know if you need clarifications! 🎯

