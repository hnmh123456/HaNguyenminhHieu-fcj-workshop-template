---
title: "Internship Worklog Week 8"
date: 2026-06-05
weight: 8
chapter: false
pre: "<b> 1.8. </b>"
---

### Week 8 Objectives:
* Research a solution for collecting, transforming, and analyzing large-scale system log streams in real time.
* Study strategies and tools for securely migrating databases from on-premises infrastructure to the cloud.
* Build a direct data-query system to improve monitoring and information-mining capability.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 19]:** Studied Analytics data-stream processing architecture on AWS, including Amazon Kinesis and Amazon Athena. | 05/06/2026 | 05/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 19 - Part 1]:** Configured Amazon Kinesis Data Firehose to collect and automatically deliver the system log stream into Amazon S3. | 06/06/2026 | 06/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Practicing Lab 19 - Part 2]:** Created an AWS Glue Data Catalog to define the log data schema and used Amazon Athena to query the data directly with SQL. | 07/06/2026 | 07/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Researching Lab 20]:** Explored advanced Migration models and the AWS Database Migration Service (DMS) tool. | 08/06/2026 | 08/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 20]:** Configured a Replication Instance, set up Source/Target Endpoints, and created a simulated Migration Task. | 09/06/2026 | 09/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 20 - Testing]:** Ran the migration task, verified database-structure integrity after the transfer, and released resources. | 10/06/2026 | 10/06/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 09/06 (Focus Area: Lab 20):**
* Set up and configured encrypted connection endpoints for the standalone AWS DMS database-migration service.
* Defined table-mapping rules and started the Replication process to prepare for schema synchronization.

**Planned Tasks for 10/06 (Focus Area: Lab 20):**
* Trigger the Migration Task to run the simulated data transfer from the on-premises source to the cloud database service.
* Reconcile record counts between both environments to confirm no data loss occurred, then tear down the test infrastructure to protect account credit.

---

### Accomplishments in Week 8:

* **Large-Scale Data-Stream Analytics (Lab 19):**
    * Mastered setting up an automated log-collection pipeline, solving the challenge of storing and analyzing large-scale unstructured data.
    * Gained the ability to query system information directly with serverless tools, without standing up a traditional database.
* **Infrastructure Migration Administration (Lab 20):**
    * Shifted from risky manual data conversion to an automated migration model that keeps the target system running continuously.
    * Developed skills configuring connection parameters and handling smooth, synchronized data mapping between different database platforms.
* **Raised Technical Standards & Resource Management:**
    * Strengthened the ability to validate data-system integrity after advanced configuration work, while keeping the lab environment clean and report data synced to GitHub.
