---
title: "Proposal"
date: 2026-07-12
weight: 2
chapter: false
pre: "<b> 2. </b>"
---

# Real-time Serverless Game Platform
## Unified AWS Serverless Solution for Real-time Multiplayer Games

### 1. Executive Summary
The **DoAnMiniGame** project is designed to build an optimal Real-time Multiplayer Game platform system. The system smoothly handles concurrent connection streams from a client application written in Flutter. The platform fully leverages the power of the **AWS Serverless** model and the **automated CI/CD pipeline (GitHub Actions + AWS SAM)** to completely eliminate the cost of managing physical server infrastructure, provide real-time monitoring capabilities, optimize security, and save operational costs based on actual resource consumption.

---

### 2. Problem Statement

#### Current Problem
Traditional multiplayer game architectures require maintaining dedicated server clusters running 24/7, leading to very high fixed costs even when there are no players. Furthermore, manual Auto-scaling configurations often fail to respond in time when player traffic spikes, easily causing network congestion or system crashes. Real-time Game State synchronization between game rooms is also very complex and requires ultra-low latency infrastructure.

#### Solution
The platform uses **Amazon API Gateway (WebSocket API)** to maintain continuous two-way connections, **AWS Lambda** to handle independent game logic (Event-driven), and **Amazon DynamoDB** as a NoSQL database to store connection sessions (`Connections`) and game room states (`Games`). The Distribution & Edge Layer is completely streamlined by using **AWS Amplify (Web Hosting & CDN)** for stable Flutter Web distribution, combined with **AWS WAF** to block DDoS attacks and **Route 53** for domain name resolution. The deployment process is fully automated through **GitHub Actions** coordinated with the **AWS SAM CLI** to package and deploy the infrastructure as code (IaC).

#### Benefits and Return on Investment (ROI)
The solution creates a solid foundation for a real-time multiplayer game system that runs stably with minimal latency (just a few milliseconds) and auto-scaling capabilities. The system reduces the burden of infrastructure administration, simplifies the process of updating backend and frontend source code, and improves the reliability of game room data. The estimated monthly cost is extremely optimal because most services fall within the AWS Free Tier limit during the testing phase, with a fast payback period thanks to maximizing savings on fixed server resource costs.

---

### 3. Solution Architecture 
The platform applies an AWS Serverless architecture to manage data from 5 Raspberry Pi-based stations, scalable up to 15 stations. Data is ingested via AWS IoT Core, stored in an S3 data lake, and processed by AWS Glue Crawlers and ETL jobs to transform and load into another S3 bucket for analysis purposes. Lambda and API Gateway handle additional processing, while Amplify with Next.js provides a dashboard secured by Cognito. 

![image1](/images/2-Proposal/FinalDiagram.png)


*AWS Services Used* 
- *AWS IoT Core*: Ingests MQTT data from 5 stations, scalable to 15. 
- *AWS Lambda*: Processes data and triggers Glue jobs (2 functions). 
- *Amazon API Gateway*: Communicates with the web application. 
- *Amazon S3*: Stores raw data (data lake) and processed data (2 buckets). 
- *AWS Glue*: Crawlers index data, ETL jobs transform and load data. 
- *AWS Amplify*: Hosts the Next.js web interface. 
- *Amazon Cognito*: Manages access permissions for lab users. 

*Component Design* 
- *Edge Devices*: Raspberry Pis collect and filter sensor data, sending it to IoT Core. 
- *Data Ingestion*: AWS IoT Core receives MQTT messages from edge devices. 
- *Data Storage*: Raw data is stored in an S3 data lake; processed data is stored in another S3 bucket. 
- *Data Processing*: AWS Glue Crawlers index the data; ETL jobs transform it for analysis. 
- *Web Interface*: AWS Amplify hosts the Next.js application for a real-time dashboard and analysis. 
- *User Management*: Amazon Cognito limits active accounts to 5. 

### 4. Technical Implementation

#### Deployment Phases
The project is comprehensively implemented through 4 sequential rolling phases:
1.  **Research and architecture design**: Conduct an in-depth survey of the WebSocket API connection protocol on API Gateway, build the entity schema structure for DynamoDB NoSQL, and finalize the system graphic design model on the Draw.io online platform.
2.  **Cost calculation and feasibility check**: Use the professional AWS Pricing Calculator tool from AWS to accurately estimate the operational budget and configure cost alert thresholds.
3.  **Optimal architecture adjustment**: Fine-tune the entire model to a 100% Serverless solution. Migrate the web interface distribution layer to **AWS Amplify**, and integrate the CI/CD automation flow via **GitHub Actions + AWS SAM** to complete infrastructure as code (IaC) management.
4.  **Development, testing, deployment**: Write business logic source code for Lambda using Node.js, complete the client-side application programming (Flutter client), organize the CI/CD workflow script files, and conduct load testing for connections using the wscat command-line tool.

#### Environment Technical Requirements
* **Development Environment**: Workstation system pre-installed with AWS CLI v2, AWS SAM CLI, Node.js version 18+ environment, Flutter SDK toolkit, and the wscat library locally.
* **Backend System (IaC)**: The entire component structure, from API Gateway and Lambda to DynamoDB, is centrally defined and explicitly managed in the `template.yaml` file of AWS SAM, strictly applying flexible configuration environment variables to avoid hardcoding the source code.
* **Frontend Application (Flutter)**: Integrate the `amplifyconfiguration.dart` configuration link file to synchronize authentication with the Cognito User Pool. Use the `flutter_secure_storage` security library on the client to keep the JWT Token string absolutely safe.

---

### 5. Roadmap & Deployment Milestones
* **Pre-internship (Month 0)**: Spend 1 month researching in-depth the WebSocket real-time connection mechanism and drafting the preliminary architecture drawing on the Draw.io software.
* **Internship (Months 1–3)**:
    * **Month 1**: Master the AWS SAM CLI tool to automate the definition of IaC source code resources. Initialize the Cognito User Pool user management service and set up the IAM Role policy model according to the Least Privilege principle.
    * **Month 2**: Initialize the structure of DynamoDB Tables storage partitions, configure the Index system to accelerate queries, and the TTL auto-deletion mechanism. Focus on developing processing source code for 4 Node.js Lambda functional functions and complete the data routing structure for the WebSocket API Gateway.
    * **Month 3**: Complete the entire interface and functionality of the Flutter application, and configure standard GitHub Actions workflow script files to run testing and parallel deployment for both Frontend (Amplify) and Backend (SAM) components. Configure CloudWatch Alarms to automatically send email notifications if errors arise from Lambda.

---

### 6. Budget Estimate
The monthly operational budget estimate table below is calculated in detail based on the AWS Pricing Calculator tool for the Singapore region data center (`ap-southeast-1`):

| AWS Service Component | Monthly Cost (USD) | Notes & Cost Optimization |
| :--- | :--- | :--- |
| **AWS Lambda** | 0.00 USD | Falls within the long-term Free Tier limit (First 1 million invocations are free). |
| **Amazon API Gateway (WebSocket)** | 0.00 USD | Leverages the basic Free Tier plan (Completely free for 1 million exchanged messages). |
| **Amazon Cognito** | 0.00 USD | No costs incurred for a small scale of Monthly Active Users (MAUs). |
| **AWS Amplify** | ~0.35 USD | Accumulates low capacity costs based on the Web application's actual storage space. |
| **Amazon DynamoDB** | ~0.30 USD | Applies the On-Demand pay-per-use configuration mode. |
| **Amazon CloudWatch** | ~0.15 USD | Optimizes budget by limiting log trace Retention time to 14 days. |
| **AWS WAF** | ~5.00 USD | Fixed maintenance fee applied for 1 basic Web ACL rule configuration at the edge layer. |
| **TOTAL** | **~5.80 USD / month** | *Equivalent to about ~69.60 USD for a full year of operating the testing system.* |

---

### 7. Risk Assessment

#### Risk Assessment Matrix
* **Zombie Connection**: Occurs when users hide the game application into background mode but the WebSocket connection session is not fully released, causing the system to continue charging maintenance fees, leading to wasted network resources. *(Impact level: Medium | Probability of occurrence: High)*
* **Cold Start Delay**: For Lambda functions that are not invoked continuously for a long time, the execution environment will be automatically revoked, leading to a delay of 1-3 seconds for the first user accessing it again as the system restarts the environment. *(Impact level: Low | Probability of occurrence: Medium)*
* **Credential Leak**: Technical negligence leading to accidentally committing files containing dangerous security access keys (such as AWS Access Key/Secret Key) publicly to shared repositories on GitHub. *(Impact level: Very High | Probability of occurrence: Low)*

#### Mitigation Strategy & Contingency Plan
* **Handling Zombie Connections**: The client application (Flutter Client) proactively catches application state change events and immediately disconnects the WebSocket upon detecting the user switching the app to the background. On the Backend, write code for the Lambda function integrating a periodic Heartbeat Ping/Pong check mechanism, while flexibly combining with the TTL auto-deletion configuration property on the DynamoDB database to thoroughly clean up all virtual connections.
* **Minimizing Cold Starts**: Organize the initialization of all extended SDK connections (e.g., connections to DynamoDB) completely outside the main event handler function (`exports.handler`) to maximize the reuse of the execution environment from previous requests. Shrink the size of the backend deployment package using the optimized `npm ci --production` command.
* **Absolute Source Code Security**: Fully declare `.env` environment definition files or sensitive configuration folders in the ignore list of `.gitignore` before pushing any source code to GitHub. At the same time, set up the AWS Billing Alert budget warning system to receive emergency Email notifications as soon as total costs exceed the initially established control threshold.

---

### 8. Expected Outcomes 
*Technical Improvements*: Real-time data and analytics replace manual processes. Expandable up to 10–15 stations. 
*Long-term Value*: A 1-year data platform for AI research, reusable for future projects.