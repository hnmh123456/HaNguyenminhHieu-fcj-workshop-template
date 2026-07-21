---
title: "Internship Worklog Week 7"
date: 2026-05-29
weight: 7
chapter: false
pre: "<b> 1.7. </b>"
---

### Week 7 Objectives:
* Study cloud financial-management strategy and analyze performance to cut wasted resources.
* Deploy an enterprise data-protection model through a multi-tier automated backup plan.
* Set up and test a rapid system-recovery process for simulated incident scenarios.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 17]:** Explored Cost Optimization principles and how to use AWS Trusted Advisor and AWS Compute Optimizer. | 29/05/2026 | 29/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 17]:** Measured real server-cluster performance and audited the account to detect and reclaim unused EBS volumes to optimize budget. | 30/05/2026 | 30/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Researching Lab 18]:** Analyzed Backup & Recovery solutions and defined RPO and RTO on AWS Backup. | 31/05/2026 | 31/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Practicing Lab 18 - Part 1]:** Created a Backup Vault and set up an automated Backup Plan covering EC2 instances and EBS volumes. | 01/06/2026 | 01/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 18 - Part 2]:** Configured a lifecycle policy to transition older backups to Cold Storage tiers to optimize storage cost. | 02/06/2026 | 02/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 18 - Part 3]:** Simulated a data-loss scenario, performed a Restore from a snapshot, and released the lab resources. | 03/06/2026 | 03/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 02/06 (Focus Area: Lab 18):**
* Set up a Lifecycle policy for centralized infrastructure backups.
* Configured an automated process migrating older snapshots to lower-cost, long-term storage once the retention period elapsed.

**Planned Tasks for 03/06 (Focus Area: Lab 18):**
* Delete a running test instance to simulate a hardware-failure scenario.
* Launch an emergency-recovery process from the most recent Backup Vault snapshot, verify data integrity, then remove all configurations to protect account credit.

---

### Accomplishments in Week 7:

* **Cloud Financial Governance (Lab 17):**
    * Developed the ability to evaluate system performance and right-size resources to actual demand.
    * Used automated analysis tooling to systematically eliminate hidden resource waste in the cloud.
* **Comprehensive Data-Protection Solution (Lab 18):**
    * Mastered configuring a centralized backup system, ensuring high availability and recovery capability for the business.
    * Established standardized information-safety metrics (RPO/RTO) that meet continuous-operation requirements.
* **Standardized Technical & Operational Skills:**
    * Built structured disaster-recovery skills through a real recovery exercise, while keeping the lab environment clean and technical logs synced to GitHub.
