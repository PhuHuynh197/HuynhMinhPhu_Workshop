---
title: "Week 7 Worklog"
date: 2026-05-29
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives

* Understand AWS cost management using AWS Budgets.
* Learn how to monitor AWS resources, metrics, logs, and alarms using Amazon CloudWatch.
* Understand AWS Support plans and how to create support cases.
* Learn the basic concept of hybrid DNS using Amazon Route 53 Resolver.
* Understand CI/CD deployment for containerized applications on Amazon ECS.
* Learn how AWS Security Hub helps evaluate cloud security posture.
* Understand the role of AWS Transit Gateway in connecting multiple VPCs.
* Practice cleanup steps carefully to avoid unnecessary AWS credit usage.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Studied AWS Budgets and its role in cloud cost management. <br> - Learned the difference between Cost Budget, Usage Budget, RI Budget, and Savings Plans Budget. <br> - Practiced creating a cost budget and configuring alert thresholds. <br> - Reviewed how budget notifications help control AWS credit usage. | 29/05/2026 | 29/05/2026 | <https://000007.awsstudygroup.com/> |
| 2 | - Studied Amazon CloudWatch overview. <br> - Learned how CloudWatch collects metrics, logs, and events from AWS resources. <br> - Practiced viewing EC2 metrics and creating basic CloudWatch alarms. <br> - Reviewed how CloudWatch supports monitoring and troubleshooting. | 30/05/2026 | 30/05/2026 | <https://000008.awsstudygroup.com/> |
| 3 | - Learned about CloudWatch Logs. <br> - Reviewed log groups, log streams, and centralized log storage. <br> - Practiced checking logs from AWS resources and applications. <br> - Studied how logs can help detect errors, abnormal behavior, and operational issues. | 31/05/2026 | 31/05/2026 | <https://000008.awsstudygroup.com/> |
| 4 | - Studied AWS Support and AWS Support Plans. <br> - Learned the difference between Basic, Developer, Business, Enterprise, and Unified Operations support levels. <br> - Practiced navigating the AWS Support Center. <br> - Learned how to create a support case and select the suitable case type and severity level. | 01/06/2026 | 01/06/2026 | <https://000009.awsstudygroup.com/> |
| 5 | - Studied hybrid DNS with Amazon Route 53 Resolver. <br> - Learned the role of inbound endpoint, outbound endpoint, resolver rule, and forwarding DNS queries. <br> - Reviewed how Route 53 Resolver can integrate AWS DNS with an on-premises DNS system. <br> - Studied the CloudFormation-based preparation process and cleanup requirements. | 02/06/2026 | 02/06/2026 | <https://000010.awsstudygroup.com/> |
| 6 | - Studied CI/CD deployment with ECS Container. <br> - Reviewed GitHub Actions, GitLab CI/CD, AWS CodeBuild, Amazon ECR, Amazon ECS, and AWS CodeDeploy in a deployment pipeline. <br> - Learned how source code changes can trigger build, test, image push, and deployment steps automatically. <br> - Reviewed Container Insights for monitoring ECS container workloads. | 03/06/2026 | 03/06/2026 | <https://000017.awsstudygroup.com/> |
| 7 | - Studied AWS Security Hub and AWS Transit Gateway. <br> - Enabled Security Hub for a short test, reviewed security standards and security score, then disabled it after the lab. <br> - Learned the basic architecture of Transit Gateway, VPC attachments, Transit Gateway route tables, and VPC route updates. <br> - Cleaned up Security Hub, Transit Gateway, CloudFormation, EC2, Route 53 Resolver, and related resources to avoid unnecessary charges. | 04/06/2026 | 04/06/2026 | <https://000018.awsstudygroup.com/> <br> <https://000020.awsstudygroup.com/> |

### Week 7 Achievements

* Understood how AWS Budgets helps control cloud spending and avoid unexpected AWS credit usage.

* Learned the main types of AWS Budgets, including:

  * Cost Budget
  * Usage Budget
  * RI Budget
  * Savings Plans Budget

* Practiced setting budget thresholds and notification alerts for cost monitoring.

* Understood how Amazon CloudWatch is used for monitoring AWS resources and applications.

* Learned the basic CloudWatch components, including:

  * Metrics
  * Alarms
  * Logs
  * Log groups
  * Log streams
  * Events

* Understood how CloudWatch Logs supports troubleshooting by collecting and storing application and system logs.

* Learned the purpose of AWS Support and how support plans are different based on response time and support scope.

* Practiced navigating AWS Support Center and understood how to create a support case.

* Understood the basic concept of hybrid DNS using Amazon Route 53 Resolver.

* Learned the purpose of Route 53 Resolver inbound endpoint, outbound endpoint, and resolver rule.

* Understood the basic workflow of CI/CD for containerized applications on Amazon ECS.

* Learned how GitHub Actions, GitLab CI/CD, CodeBuild, ECR, ECS, and CodeDeploy can work together in an automated deployment pipeline.

* Understood how AWS Security Hub can provide a centralized view of security findings and compliance status.

* Reviewed security standards such as AWS Foundational Security Best Practices and CIS AWS Foundations Benchmark.

* Understood the role of AWS Transit Gateway as a central network hub for connecting multiple VPCs.

* Learned that advanced services such as Security Hub, Transit Gateway, NAT Gateway, Load Balancer, and CloudFormation-created resources must be cleaned up carefully after practice.

* Completed week 7 with a stronger understanding of AWS cost control, monitoring, support, DNS, CI/CD, security monitoring, and advanced networking.