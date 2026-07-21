---
title: "Internship Worklog Week 3"
date: 2026-05-01
weight: 3
chapter: false
pre: "<b> 1.3. </b>"
---

### Week 3 Objectives:
* Master the mechanism for automatically scaling server resources based on real infrastructure demand.
* Approach application-development thinking for Serverless architecture, optimizing code-execution performance.
* Set up an automated data-connection cycle between the logic-processing layer and the cloud API communication layer.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 6]:** Analyzed how Amazon EC2 Auto Scaling works, load-monitoring mechanisms, and Launch Template configurations. | 01/05/2026 | 01/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 6 - Part 1]:** Configured a sample server template, created an Auto Scaling Group, and set up a Manual Scaling policy. | 02/05/2026 | 02/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Practicing Lab 6 - Part 2]:** Configured Dynamic Scaling and simulated system load to test automatic scale-in/scale-out of EC2 instances. | 03/05/2026 | 03/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Researching Lab 8]:** Explored AWS Serverless architecture, event-driven mechanisms, and how AWS Lambda works. | 04/05/2026 | 04/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 8 - Part 1]:** Wrote and deployed a logic-processing function on AWS Lambda, and set up a test runtime environment. | 05/05/2026 | 05/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 8 - Part 2]:** Integrated AWS Lambda with Amazon API Gateway, exposed a Function URL to handle external HTTP requests, and cleaned up resources. | 06/05/2026 | 06/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 05/05 (Focus Area: Lab 8):**
* Created and configured a Lambda function that executes logic tasks without managing an underlying operating system.
* Configured the runtime environment, allocated appropriate memory, and optimized the input-handling code ahead of the next networking-integration step.

**Planned Tasks for 06/05 (Focus Area: Lab 8):**
* Create and connect an Amazon API Gateway endpoint as the entry point for incoming user requests.
* Route HTTP traffic directly to the AWS Lambda function via a Function URL, test live requests from the browser, then tear down the test infrastructure to protect account limits.

---

### Accomplishments in Week 3:

* **Automated Compute Scaling (Lab 6):**
    * Mastered the design thinking for self-healing, elastically scaling systems driven by concrete performance metrics (CPU, RAM).
    * Developed proficiency building standardized server templates and configuring alert thresholds that help optimize enterprise infrastructure costs.
* **Serverless Architecture Development (Lab 8):**
    * Shifted the operations mindset from managing an operating system to managing independent, event-driven code execution.
    * Gained skills building high-speed cloud APIs, smoothly wiring event-driven compute services together into a complete web application.
* **Resource Optimization & Supporting Skills:**
    * Strengthened log-analysis capability using real system load metrics, while continuing to release resources promptly and keep lab source code synchronized on GitHub.
