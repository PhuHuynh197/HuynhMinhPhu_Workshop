---
title: "Blogs Posted"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

This section lists and introduces the blogs I posted to the [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj). These blogs summarize the AWS articles and technical topics that I studied during the internship period.

### [Blog 1 - Session Policies in Amazon EKS Pod Identity](3.1-Blog1/)

This blog introduces the Session Policies feature in Amazon EKS Pod Identity. The topic focuses on how Kubernetes workloads running on Amazon EKS can obtain AWS IAM credentials more securely and how Session Policies help narrow permissions for each pod.

The main idea of this blog is that Session Policies support the principle of least privilege by limiting the effective permissions of a pod. Instead of creating many separate IAM roles for different workloads, teams can reuse a shared IAM role and apply different scoped-down policies at runtime. This helps reduce IAM role sprawl, simplify permission management, and improve security in large-scale Kubernetes environments.

### [Blog 2 - Data Masking in Amazon RDS for Oracle](3.2-Blog2/)

This blog discusses Data Masking in Amazon RDS for Oracle. The topic explains why Production data should not be used directly in Development, Testing, or UAT environments without protection.

The blog introduces the concept of replacing sensitive real data with masked data while keeping the same format and structure for testing purposes. It also describes a workflow that can include Amazon RDS for Oracle, Amazon EventBridge Scheduler, AWS Step Functions, AWS Systems Manager, AWS Secrets Manager, and snapshot restore operations. Through this topic, I learned that data protection is not only about encryption and access control, but also about handling sensitive data safely when it is copied or restored to non-production environments.

### [Blog 3 - Updates to the AWS Well-Architected Framework Guidance](3.3-Blog3/)

This blog summarizes the AWS Architecture Blog article about updates to the AWS Well-Architected Framework guidance. The topic helped me understand that cloud architecture design should not only focus on individual AWS services, but should also be evaluated based on proven architectural best practices.

The blog focuses on the six pillars of the AWS Well-Architected Framework: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. It also highlights that architecture review should be a continuous process throughout the workload lifecycle. This topic helped me better understand how AWS guides architects and cloud engineers to design systems that are secure, reliable, efficient, cost-aware, and sustainable.