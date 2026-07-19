---
title: "Week 9 Worklog"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives

* Start implementing the foundational AWS infrastructure for the **PharmaCare AI** system.
* Create a custom VPC to separate frontend, backend, database, and AI-related resources.
* Design public subnets, private application subnets, and private database subnets based on the project architecture.
* Deploy Amazon RDS PostgreSQL as the main relational database for the pharmacy system.
* Configure Security Groups so that Lambda backend can securely connect to RDS through port `5432`.
* Use AWS Secrets Manager to store database credentials instead of hard-coding them in source code.
* Create VPC Endpoint so that private resources can access internal AWS services securely.
* Create a Lambda migration function to initialize the first version of the database schema.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | - Started implementing AWS infrastructure for the **PharmaCare AI** project. <br> - Reviewed the overall system architecture diagram. <br> - Identified the main layers: Global layer, Frontend layer, Private App Subnet, RDS DB Subnet, OpenSearch VPC Subnet, and Monitoring & Security layer. <br> - Planned the implementation order: VPC → subnets → route tables → security groups → RDS → Secrets Manager → Lambda migration. | 12/06/2026 | 12/06/2026 |
| 2 | - Created a custom VPC named `pharmacare-vpc`. <br> - Used the `ap-southeast-1` region. <br> - Configured CIDR block `10.0.0.0/16` for the VPC. <br> - Checked the VPC Resource Map to verify that the VPC was created correctly before creating subnets for system layers. | 13/06/2026 | 13/06/2026 |
| 3 | - Created subnets inside the VPC based on system layers. <br> - Created public subnets for resources that require internet-facing connectivity. <br> - Created private application subnets for Lambda backend, Lambda chatbot, and Lambda indexing. <br> - Created private database subnets for Amazon RDS PostgreSQL. <br> - Distributed subnets across multiple Availability Zones to support better availability. | 14/06/2026 | 14/06/2026 |
| 4 | - Created and attached an Internet Gateway to the VPC. <br> - Created route tables for public and private subnets. <br> - Configured the public route table to route internet traffic through the Internet Gateway. <br> - Kept private application subnets and private database subnets without direct public internet exposure. <br> - Verified route table configuration according to the architecture design. | 15/06/2026 | 15/06/2026 |
| 5 | - Created Security Groups for application and database layers. <br> - Configured the RDS Security Group to allow PostgreSQL traffic on port `5432` only from the Lambda backend Security Group. <br> - Avoided opening database access to the public internet. <br> - Created a Security Group for VPC Endpoint so that Lambda functions in private subnets can call internal AWS services. | 16/06/2026 | 16/06/2026 |
| 6 | - Created Amazon RDS PostgreSQL as the main system database. <br> - Created database name `pharmacare_ai`. <br> - Placed RDS inside private database subnets. <br> - Disabled public access for the RDS database. <br> - Created a secret in AWS Secrets Manager to store database username, password, host, port, and connection information. <br> - Created VPC Endpoint for Secrets Manager so that Lambda can retrieve database credentials securely from the private network. | 17/06/2026 | 17/06/2026 |
| 7 | - Created IAM Role for Lambda migration. <br> - Created Lambda function `pharmacare-db-migration`. <br> - Attached the migration Lambda to the VPC and private application subnet so that it can connect to RDS. <br> - Configured environment variables such as `AWS_REGION`, `RDS_SECRET_ARN`, and `DB_NAME`. <br> - Increased Lambda timeout because the migration needs to execute SQL for creating multiple tables. <br> - Packaged the migration code as a ZIP file and uploaded it to Lambda. <br> - Ran the migration to create the initial database schema for PharmaCare AI. | 18/06/2026 | 18/06/2026 |

### Week 9 Achievements

* Completed the foundational AWS infrastructure for the **PharmaCare AI** system.

* Created a custom VPC named `pharmacare-vpc` in the `ap-southeast-1` region.

* Designed the network into clear separated layers:

  * Public subnet
  * Private application subnet
  * Private database subnet
  * RDS DB subnet group
  * OpenSearch VPC subnet for the later AI/RAG layer

* Understood the role of each network layer in the architecture:

  * Public subnet is used for resources that require internet-facing connectivity.
  * Private application subnet is used for Lambda backend, Lambda chatbot, and Lambda indexing.
  * Private database subnet is used for Amazon RDS PostgreSQL.
  * OpenSearch VPC subnet is used for vector store access in the AI/RAG layer.

* Created and configured Internet Gateway and route tables for the VPC.

* Configured Security Groups using the principle of opening only required traffic.

* Ensured that Amazon RDS PostgreSQL is not publicly accessible from the internet.

* Created Amazon RDS PostgreSQL as the main project database with database name `pharmacare_ai`.

* Used AWS Secrets Manager to store database connection information securely.

* Created VPC Endpoint for Secrets Manager so that Lambda functions in private subnets can retrieve secrets without using the public internet.

* Created IAM Role and Lambda migration function to initialize the database schema.

* Configured timeout and environment variables for the migration Lambda.

* Created the main database tables, including:

  * `users`
  * `categories`
  * `brands`
  * `products`
  * `stores`
  * `carts`
  * `cart_items`
  * `orders`
  * `order_items`
  * `payments`
  * `prescriptions`
  * `articles`
  * `chatbot_documents`
  * `chat_sessions`
  * `chat_messages`

* Completed week 9 with a working infrastructure foundation, private database layer, Secrets Manager integration, and database migration process for backend API implementation in week 10.