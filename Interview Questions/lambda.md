# AWS Lambda - Overview & FAQ

AWS Lambda is a serverless compute service that runs code in response to events and automatically manages the underlying compute resources for you. It allows developers to focus on code rather than infrastructure.

---

## ⚙️ 1. What is AWS Lambda?
AWS Lambda lets you run code without provisioning or managing servers. It automatically scales and charges you only for the compute time you consume.

---

## 🔄 2. How Does AWS Lambda Work?
You upload code and configure an event source (e.g., S3, API Gateway). Lambda handles the execution, scaling, and logging of your function in response to the event.

---

## 🌟 3. Key Benefits of AWS Lambda
- Serverless infrastructure
- Automatic scaling
- Cost efficiency (pay-per-use)
- Event-driven architecture support
- Integrated monitoring with CloudWatch

---

## 🚀 4. Event Sources That Can Trigger Lambda
- **S3** (file uploads)
- **DynamoDB** (table updates)
- **API Gateway** (HTTP requests)
- **SNS**, **SQS**, **CloudWatch**, and more

---

## 📈 5. How Is Concurrency Managed?
Lambda automatically scales horizontally to handle requests. You can also configure **reserved** and **provisioned concurrency** to control limits.

---

## ⏱️ 6. Maximum Execution Time
A single Lambda invocation can run for up to **15 minutes**.

---

## 📥 7. Passing Data to/from Lambda
- **Input**: Event object (JSON)
- **Output**: Return values or response objects
- Common formats include API Gateway payloads or S3 event structures.

---

## 🌐 8. External Resource Access
Yes, Lambda can access external services (e.g., APIs, databases) using:
- AWS SDKs
- HTTP clients
- VPC configurations (for private resources)

---

## 📦 9. What Are AWS Lambda Layers?
Lambda Layers let you **share libraries, custom runtimes, or other dependencies** across multiple Lambda functions.

---

## 🛠️ 10. Error Handling in Lambda
- Use `try-catch` blocks in code
- Monitor with **CloudWatch Logs**
- Set up **dead-letter queues**, retries, or destinations for async error handling

---

## 🌍 11. Internet Access in Lambda
- Public internet: Available by default (if not in a VPC)
- VPC: Requires a NAT Gateway for external internet access

---

## 🔧 12. Supported Execution Environments
Lambda supports:
- **Node.js**
- **Python**
- **Java**
- **Go**
- **Ruby**
- **.NET Core**
- **Custom Runtimes** via Runtime API

---

## 🌱 13. Environment Variables
You can configure **environment variables** during creation or update, accessible in code via language-specific APIs (e.g., `process.env` in Node.js).

---

## 🔁 14. Synchronous vs Asynchronous Invocations
- **Synchronous**: Waits for function response (e.g., API Gateway)
- **Asynchronous**: Returns immediately (e.g., S3, SNS)

---

## 🔗 15. Event Source Mapping
Maps event sources like **DynamoDB Streams** or **Kinesis Streams** to Lambda, allowing it to poll and process records automatically.

---

## 🔐 16. Permissions and Execution Roles
Use **IAM roles** to define permissions for Lambda:
- Execution Role: Grants access to AWS services the function interacts with
- Resource-based Policies: Control who can invoke the function

---

## 🧩 17. AWS Step Functions
AWS Step Functions is a service to **orchestrate multiple Lambda functions** and AWS services using workflows and state machines.

---

## ⚙️ 18. Deployment Automation
- **AWS SAM**
- **AWS CloudFormation**
- **AWS CDK**
- **CI/CD Tools**: CodePipeline, GitHub Actions, etc.

---

## 🏢 19. On-Premises Access
Yes, using:
- **VPC configuration**
- **VPN** or **AWS Direct Connect**

---

## ❄️ 20. What is a Cold Start?
A Cold Start occurs when a Lambda function is invoked after being idle. AWS initializes the execution environment, causing a slight **startup latency**.

---

## 📚 Summary
AWS Lambda empowers developers to build scalable, event-driven applications without worrying about server management. With rich integrations and flexible runtime support, it's a cornerstone of modern cloud-native architecture.

