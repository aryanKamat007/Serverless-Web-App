# Serverless Student Data Web App

A simple serverless web application for managing student data, leveraging AWS services like DynamoDB, Lambda, API Gateway, S3, and CloudFront for a scalable, secure, and performant solution.

---

## 🚀 Deployment Process

### 1. Create DynamoDB Table
- Set up a **DynamoDB** table on AWS to store student data.
- Define appropriate primary key(s) for efficient data retrieval and insertion.

### 2. Build Lambda Functions
- Developed two **AWS Lambda** functions:
  - `getStudent` — Retrieves student data from DynamoDB (handles **GET** requests).
  - `insertStudent` — Adds new student data to DynamoDB (handles **POST** requests).

### 3. Configure API Gateway
- Created an **API Gateway** REST API with two endpoints:
  - One linked to the `getStudent` Lambda function.
  - One linked to the `insertStudent` Lambda function.
- Enables secure and scalable client-server communication.

### 4. Host Static Website on S3
- Make sure to change the API_ENDPOINT in `scripts.js` to your API Endpoint
- Uploaded frontend files (`index.html` and `scripts.js`) to an **S3 bucket**.
- Configured the bucket for **static website hosting** to serve the client interface.

### 5. Secure and Accelerate with CloudFront
- Set up a **CloudFront distribution** with the S3 bucket as the origin.
- Provides:
  - **HTTPS** delivery for secure access.
  - Global caching to optimize performance and reduce latency.

---
