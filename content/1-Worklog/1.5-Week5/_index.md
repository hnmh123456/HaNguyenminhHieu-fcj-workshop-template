---
title: "Internship Worklog Week 5"
date: 2026-05-15
weight: 5
chapter: false
pre: "<b> 1.5. </b>"
---

### Week 5 Objectives:
* Study cloud security standards and rigorous enterprise resource-governance mechanisms.
* Build a comprehensive monitoring solution to collect performance metrics and activity traces.
* Set up an automated alerting system to detect operational incidents and cost risks early.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 13]:** Explored Security & Governance tooling and studied AWS CloudTrail for logging system activity. | 15/05/2026 | 15/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 13]:** Configured AWS CloudTrail log collection and set up AWS Config to check account resource-configuration compliance. | 16/05/2026 | 16/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Researching Lab 14]:** Analyzed advanced cloud-monitoring mechanisms and studied Amazon CloudWatch (Metrics, Logs, Alarms). | 17/05/2026 | 17/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Practicing Lab 14 - Part 1]:** Configured the CloudWatch Logs Agent to collect logs from an EC2 server and built a visual monitoring Dashboard. | 18/05/2026 | 18/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 14 - Part 2]:** Created CloudWatch Metric Filters for log error codes and configured automated CloudWatch Alarm thresholds. | 19/05/2026 | 19/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 14 - Part 3]:** Simulated a system failure to test alert delivery via SNS email, then cleaned up test resources. | 20/05/2026 | 20/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 19/05 (Focus Area: Lab 14):**
* Set up metric filters against the centralized server log stream to extract application error codes.
* Defined safe resource thresholds (such as CPU overload and memory exhaustion) using CloudWatch Alarms.

**Planned Tasks for 20/05 (Focus Area: Lab 14):**
* Link CloudWatch alarm scenarios to Amazon SNS to automatically notify administrators by email during incidents.
* Run a load-simulation test and generate synthetic log errors to verify the real-time alerting cycle, then tear down the configured infrastructure to protect account credit.

---

### Accomplishments in Week 5:

* **Security Governance & Auditing (Lab 13):**
    * Developed proficiency tracking system behavior and recording every architecture change for incident-investigation purposes.
    * Gained a standardized governance mindset by automatically flagging resources that don't comply with enterprise security policy.
* **Comprehensive System Monitoring (Lab 14):**
    * Shifted from reactive to proactive infrastructure-health monitoring, configuring centralized log collection for cloud servers.
    * Built visual Dashboards tracking technical load metrics and set up rapid-response mechanisms for abnormal signals.
* **Operational Optimization Skills:**
    * Developed troubleshooting skills grounded in real data extracted from monitoring logs, while keeping the lab environment clean and progress synced to GitHub.
