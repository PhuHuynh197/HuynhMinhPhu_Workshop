---
title: "Week 8 Worklog"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives

* Start the final internship project named **PharmaCare AI**.
* Analyze the requirements of an online pharmacy website integrated with an AI chatbot.
* Identify the main system modules, user interaction flow, backend API flow, database layer, and AI chatbot/RAG flow.
* Design the AWS architecture for the PharmaCare AI system.
* Select suitable AWS services for frontend hosting, authentication, backend API, database, AI chatbot, monitoring, security, and backup.
* Prepare the architecture diagram and technical explanation for the Proposal, Project, and Workshop sections.

### PharmaCare AI Architecture

The following diagram shows the proposed AWS architecture for the **PharmaCare AI – Online Pharmacy Website & AI Chatbot** project.

{{< figure src="/HuynhMinhPhu_Workshop/images/proposal/dia1.png" title="AWS Architecture - PharmaCare AI" width="900px" >}}

The system is designed using a serverless and managed-service approach on AWS. The frontend is hosted on Amazon S3 and distributed through Amazon CloudFront. User authentication is handled by Amazon Cognito. Business APIs are exposed through Amazon API Gateway and processed by AWS Lambda. The main pharmacy data is stored in Amazon RDS Multi-AZ, while chatbot knowledge retrieval uses Amazon OpenSearch Service as a vector store and Amazon Bedrock for AI response generation.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Started the final project **PharmaCare AI**. <br> - Defined the project topic: online pharmacy website, medicine management, order management, and AI chatbot consultation. <br> - Identified the main purpose of the system: supporting pharmacy operations and helping users look up medicine-related information more conveniently. | 05/06/2026 | 05/06/2026 | Project requirement document |
| 2 | - Analyzed the main website functions. <br> - Listed key modules such as medicine/product management, user account, product browsing, order management, inventory-related data, and chatbot consultation. <br> - Identified the main user interaction flow from accessing the website to using system features. | 06/06/2026 | 06/06/2026 | Project requirement document |
| 3 | - Designed the frontend layer. <br> - Selected Amazon S3 as the static web UI bucket. <br> - Selected Amazon CloudFront to improve website delivery performance and stability. <br> - Added AWS WAF in front of the public web layer to help protect the system from abnormal requests. | 07/06/2026 | 07/06/2026 | <https://000057.awsstudygroup.com/> |
| 4 | - Designed the authentication and API layer. <br> - Selected Amazon Cognito for customer login and JWT token generation. <br> - Selected Amazon API Gateway as the public API entry point. <br> - Selected AWS Lambda Backend API to process user, product, order, and pharmacy business logic. | 08/06/2026 | 08/06/2026 | <https://000081.awsstudygroup.com/> <br> <https://000055.awsstudygroup.com/> |
| 5 | - Designed the database and private network layer. <br> - Selected Amazon RDS Multi-AZ as the main relational database for users, medicines, categories, orders, and inventory data. <br> - Planned to place RDS inside private DB subnets in Amazon VPC. <br> - Selected AWS Secrets Manager to store database credentials securely instead of hardcoding them in source code. | 09/06/2026 | 09/06/2026 | <https://000005.awsstudygroup.com/> |
| 6 | - Designed the AI Chatbot/RAG layer. <br> - Selected Amazon S3 Knowledge Docs to store pharmacy documents, medicine information, FAQ, and internal knowledge files. <br> - Planned AWS Lambda Indexing to process documents and store vector data in Amazon OpenSearch Service. <br> - Selected Amazon Bedrock to generate chatbot responses based on retrieved context from OpenSearch. | 10/06/2026 | 10/06/2026 | Project architecture design |
| 7 | - Completed the first version of the AWS architecture diagram. <br> - Added monitoring and security governance services, including Amazon CloudWatch, CloudWatch Alarms, Amazon SNS, AWS IAM, and AWS Backup. <br> - Reviewed the complete request flow from Route 53 to CloudFront, S3, Cognito, API Gateway, Lambda, RDS, OpenSearch, and Bedrock. <br> - Prepared notes for writing the Proposal and Workshop pages. | 11/06/2026 | 11/06/2026 | Project architecture diagram |

### Week 8 Achievements

* Completed the initial requirement analysis for the **PharmaCare AI** project.

* Defined the project as an online pharmacy website integrated with an AI chatbot based on the RAG architecture.

* Identified the main system modules, including:

  * User authentication
  * Medicine/product browsing
  * Pharmacy product management
  * Order management
  * Inventory-related data management
  * AI chatbot consultation
  * Knowledge document indexing
  * Monitoring, alerting, and backup

* Designed the user interaction flow:

  * User accesses the website through Amazon Route 53.
  * Amazon CloudFront distributes frontend content from Amazon S3.
  * AWS WAF helps protect the public web layer.
  * User logs in through Amazon Cognito.
  * Cognito provides a JWT token for calling protected APIs.

* Designed the backend API flow:

  * Frontend sends requests to Amazon API Gateway.
  * API Gateway forwards requests to AWS Lambda Backend API.
  * Lambda processes business logic such as users, products, orders, and pharmacy data.
  * Lambda retrieves database credentials from AWS Secrets Manager.
  * Lambda connects to Amazon RDS to read and write relational data.

* Designed the database and VPC data layer:

  * Amazon RDS is used as the main pharmacy database.
  * RDS stores users, medicines, categories, orders, and inventory-related data.
  * RDS is placed in private DB subnets inside Amazon VPC.
  * Multi-AZ architecture is used to improve database availability.

* Designed the AI Chatbot/RAG flow:

  * User sends chatbot questions from the website.
  * AWS Lambda Chatbot Handler processes chatbot requests.
  * Lambda retrieves relevant knowledge from Amazon OpenSearch Service.
  * Amazon Bedrock generates responses based on retrieved context.
  * The chatbot supports medicine information lookup, pharmacy documents, and FAQ, but does not replace professional medical consultation.

* Designed the knowledge indexing pipeline:

  * Pharmacy knowledge documents are stored in Amazon S3 Knowledge Docs.
  * AWS Lambda Indexing processes new documents.
  * Processed data is stored in Amazon OpenSearch Service as vector data.
  * OpenSearch supports semantic search for the chatbot.

* Added monitoring, alerting, and security governance components:

  * Amazon CloudWatch for logs and metrics
  * CloudWatch Alarms for threshold-based alerts
  * Amazon SNS for notification
  * AWS IAM for least-privilege access control
  * AWS Backup for backup management

* Completed week 8 with a clear AWS architecture design and a technical direction for implementing the PharmaCare AI system in the following weeks.