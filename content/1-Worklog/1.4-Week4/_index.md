---
title: "Internship Worklog Week 4"
date: 2026-05-08
weight: 4
chapter: false
pre: "<b> 1.4. </b>"
---

### Week 4 Objectives:
* Approach and master application containerization technology with Docker on the cloud platform.
* Understand the mechanism for managing, storing, and orchestrating large-scale container clusters.
* Research advanced developer tooling to build an automated continuous integration and deployment (CI/CD) cycle.

### Tasks Implemented This Week:

| Day | Task Details | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **[Researching Lab 10]:** Studied AWS container-packaging architecture, distinguished Docker Images from Containers, and researched Amazon ECR and ECS. | 08/05/2026 | 08/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **2** | **[Practicing Lab 10 - Part 1]:** Wrote a Dockerfile, packaged a web application into a Docker Image, and pushed it to an Amazon ECR repository. | 09/05/2026 | 09/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **3** | **[Practicing Lab 10 - Part 2]:** Configured Task Definitions and created a cluster to automatically orchestrate containers on Amazon ECS (Fargate). | 10/05/2026 | 10/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **4** | **[Researching Lab 11]:** Explored the AWS Developer Tools suite and the operating principles of an automated CI/CD system. | 11/05/2026 | 11/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **5** | **[Practicing Lab 11 - Part 1]:** Set up an AWS CodeCommit repository and configured a buildspec file for the AWS CodeBuild packaging service. | 12/05/2026 | 12/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| **6** | **[Practicing Lab 11 - Part 2]:** Built and linked the automation cycle with AWS CodePipeline, tested automatic deployment on code changes, and released resources. | 13/05/2026 | 13/05/2026 | [AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

---

### Daily Progress Details

**Tasks Completed on 12/05 (Focus Area: Lab 11):**
* Set up the internal source-code repository and configured an automated build environment using a buildspec configuration file.
* Optimized source-code validation commands to prepare for the automated packaging process.

**Planned Tasks for 13/05 (Focus Area: Lab 11):**
* Build a complete automation pipeline connecting code intake, automatic build, and direct deployment.
* Push a small code change to test the pipeline's automatic update feature via the web console, then clean up infrastructure to protect account limits.

---

### Accomplishments in Week 4:

* **Container Packaging & Orchestration (Lab 10):**
    * Developed proficiency packaging applications, optimizing image sizes, and managing a Docker image repository.
    * Gained a modern container-operations mindset, configuring automatic compute allocation without touching physical servers.
* **CI/CD Automation Pipeline (Lab 11):**
    * Shifted from manual workflows to fully automated testing and release processes.
    * Successfully linked cloud developer services together, speeding up project delivery and reducing human error.
* **Technical Workflow Optimization:**
    * Strengthened debugging skills for automation-system configuration files, while maintaining the habit of releasing resources after each lab and keeping source code synced to GitHub.
