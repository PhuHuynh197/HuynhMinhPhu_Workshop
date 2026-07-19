---
title: "Week 5 Worklog"
date: 2026-05-15
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives

* Understand the purpose of Amazon Relational Database Service (Amazon RDS).
* Learn how to create a database environment for an application on AWS.
* Practice creating VPC, Security Groups, and DB Subnet Group for Amazon RDS.
* Learn how to create and configure an Amazon RDS database instance.
* Practice connecting an application running on EC2 to an RDS database.
* Understand backup and restore operations using Amazon RDS and AWS Backup.
* Learn how to configure backup notifications and clean up backup-related resources.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Studied the overview of Amazon RDS. <br> - Learned why RDS is used for relational database workloads. <br> - Took notes about managed database service, database engines, storage options, backup, high availability, and security features. | 15/05/2026 | 15/05/2026 | <https://000005.awsstudygroup.com/> |
| 2 | - Prepared the network environment for Amazon RDS. <br> - Created a VPC for the database lab. <br> - Created EC2 Security Group and RDS Security Group. <br> - Reviewed how Security Groups control access between the application server and database server. | 16/05/2026 | 16/05/2026 | <https://000005.awsstudygroup.com/> |
| 3 | - Created DB Subnet Group for Amazon RDS. <br> - Selected subnets from different Availability Zones. <br> - Understood why DB Subnet Group is required when launching an RDS instance inside a VPC. <br> - Checked subnet and routing configuration before creating the database. | 17/05/2026 | 17/05/2026 | <https://000005.awsstudygroup.com/> |
| 4 | - Created an Amazon RDS database instance. <br> - Configured database engine, instance class, storage, username, password, VPC, DB Subnet Group, and Security Group. <br> - Waited for the RDS instance to become available. <br> - Checked the database endpoint for application connection. | 18/05/2026 | 18/05/2026 | <https://000005.awsstudygroup.com/> |
| 5 | - Created an EC2 instance for application deployment. <br> - Deployed a sample application on EC2. <br> - Configured the application to connect to the Amazon RDS database. <br> - Tested database connection and application operation through the browser. | 19/05/2026 | 19/05/2026 | <https://000005.awsstudygroup.com/> |
| 6 | - Studied AWS Backup and its role in centralized data protection. <br> - Prepared backup-related resources for the system. <br> - Created a backup plan to automate backup operations. <br> - Configured notification settings using Amazon SNS to receive backup process updates. | 20/05/2026 | 20/05/2026 | <https://000013.awsstudygroup.com/> |
| 7 | - Practiced backup and restore testing. <br> - Reviewed automated backup, manual snapshot, backup plan, and restore concepts. <br> - Verified the importance of restore testing after creating backups. <br> - Cleaned up EC2, RDS, AWS Backup, SNS, Security Groups, DB Subnet Group, and related resources to avoid unnecessary cost. | 21/05/2026 | 21/05/2026 | <https://000005.awsstudygroup.com/> <br> <https://000013.awsstudygroup.com/> |

### Week 5 Achievements

* Understood the role of Amazon RDS as a managed relational database service on AWS.

* Learned that Amazon RDS can reduce database administration tasks such as:

  * Database provisioning
  * Backup management
  * Patching
  * Storage scaling
  * High availability configuration

* Understood common relational database engines supported by Amazon RDS, including:

  * MySQL
  * PostgreSQL
  * MariaDB
  * SQL Server
  * Oracle
  * Amazon Aurora

* Practiced preparing the infrastructure required for an RDS database, including:

  * VPC
  * Subnets
  * EC2 Security Group
  * RDS Security Group
  * DB Subnet Group

* Understood why the database layer should be isolated from direct public access.

* Learned how Security Groups are used to allow the application server to connect to the database securely.

* Created and configured an Amazon RDS database instance.

* Learned how to use the RDS endpoint to connect an application to the database.

* Practiced deploying an application on EC2 and connecting it to an RDS database.

* Understood the basic difference between automated backups, manual snapshots, and AWS Backup plans.

* Learned how AWS Backup can centralize and automate backup operations for AWS resources.

* Learned how Amazon SNS can be used to send backup process notifications.

* Understood the importance of testing restore operations after creating backups.

* Cleaned up temporary lab resources after completing the practice to reduce AWS credit usage.

* Completed week 5 with a stronger understanding of database deployment, database security, backup, and recovery on AWS.