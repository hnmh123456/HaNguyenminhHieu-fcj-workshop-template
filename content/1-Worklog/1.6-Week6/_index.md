---
title: "Internship Worklog Week 6"
date: 2026-05-22
weight: 6
chapter: false
pre: "<b> 1.6. </b>"
---

### Week 6 Objectives:
* Research a large-capacity shared file-storage solution that can be mounted to multiple servers simultaneously.
* Master automated systems-management tooling to configure and patch servers remotely at scale.
* Optimize the centralized management process for configuration code and system secrets.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 15]:** Studied how Amazon EFS (Elastic File System) works and how it differs from EBS and S3. | 22/05/2026 | 22/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 15]:** Created an Amazon EFS file system, configured Mount Targets, and mounted the shared volume across an EC2 cluster. | 23/05/2026 | 23/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Researching Lab 16]:** Explored the AWS Management Tools suite and the core features of AWS Systems Manager (SSM). | 24/05/2026 | 24/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Practicing Lab 16 - Part 1]:** Configured an IAM Role for the SSM Agent and connected securely to a Linux server without using traditional SSH keys. | 25/05/2026 | 25/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 16 - Part 2]:** Used SSM Run Command to execute batch software installations across the server cluster and managed secrets with SSM Parameter Store. | 26/05/2026 | 26/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 16 - Part 3]:** Tested the real-time automated OS patch-update cycle (Patch Manager) and released the lab resources. | 27/05/2026 | 27/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 26/05 (Focus Area: Lab 16):**
* Integrated and securely stored environment configuration variables and database passwords inside the centralized SSM Parameter Store.
* Ran a batch application-update script against the entire fleet of target servers via Run Command, with no manual login required.

**Planned Tasks for 27/05 (Focus Area: Lab 16):**
* Configure an automated scan-and-install process for critical OS security patches across the EC2 cluster using Patch Manager.
* Verify the compliance-status log confirms success, then remove the storage configuration and shut down test servers to protect the internship account's credit.

---

### Accomplishments in Week 6:

* **Shared Data Storage (Lab 15):**
    * Mastered the design of a shared network-storage layer for a Linux server cluster, thoroughly solving the distributed data-synchronization problem.
    * Developed configuration skills to optimize read/write throughput across specialized file-storage tiers.
* **Large-Scale Infrastructure Automation (Lab 16):**
    * Shifted from managing individual servers to a centralized, remote, code-driven control model.
    * Gained an advanced infrastructure-security mindset by closing the SSH port and replacing it with session-based access control (Session Manager).
* **Standardized Technical Processes & Resource Governance:**
    * Mastered secure secret-management and configuration-encryption practices for the cloud application ecosystem, while consistently cleaning up test infrastructure and syncing logs to GitHub.
