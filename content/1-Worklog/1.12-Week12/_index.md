---
title: "Week 12 Worklog"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives

* Deploy the React frontend of **PharmaCare AI** to AWS.
* Host the production frontend on Amazon S3.
* Create Amazon CloudFront distribution to publish the website to users.
* Configure CloudFront for React Single Page Application routing.
* Update Cognito callback URLs and sign-out URLs for the production CloudFront domain.
* Update API Gateway CORS configuration so the production frontend can call backend APIs.
* Configure CloudWatch Logs, CloudWatch Alarms, and Amazon SNS for monitoring and alerting.
* Configure AWS Backup for Amazon RDS.
* Attach AWS WAF to CloudFront to improve public web protection.
* Review IAM permissions using the principle of least privilege.
* Perform final system testing and complete the internship report/workshop documentation.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | - Started the final deployment phase for **PharmaCare AI**. <br> - Reviewed the completed backend API, Cognito authentication, RDS database, and AI chatbot integration. <br> - Built the React frontend using `npm run build`. <br> - Verified that the `dist` folder was generated successfully with `index.html`, `assets/`, `favicon.svg`, and related frontend files. | 03/07/2026 | 03/07/2026 |
| 2 | - Created Amazon S3 bucket `pharmacare-frontend-web-phu-2026` for the production frontend. <br> - Uploaded all files from the React `dist` folder to the S3 bucket. <br> - Kept the S3 bucket private instead of making it public directly. <br> - Verified that the frontend build files were stored correctly in S3. | 04/07/2026 | 04/07/2026 |
| 3 | - Created CloudFront distribution named `pharmacare-frontend-distribution`. <br> - Configured the CloudFront origin to point to the S3 frontend bucket. <br> - Used private origin access so CloudFront can access S3 securely. <br> - Configured default root object as `index.html`. <br> - Configured custom error responses `403 → /index.html → 200` and `404 → /index.html → 200` to support React SPA routes. | 05/07/2026 | 05/07/2026 |
| 4 | - Tested the production website using the CloudFront domain. <br> - Verified that the website was accessible at `https://d3tm5364zrtmpq.cloudfront.net/`. <br> - Updated Cognito Allowed callback URLs and Allowed sign-out URLs to include the CloudFront domain. <br> - Updated API Gateway CORS configuration to allow requests from the CloudFront frontend. <br> - Updated frontend environment configuration from localhost to the production CloudFront domain. <br> - Rebuilt the frontend, uploaded the new build to S3, and created CloudFront invalidation `/*`. | 06/07/2026 | 06/07/2026 |
| 5 | - Configured Amazon CloudWatch Logs for system monitoring. <br> - Checked log groups for Lambda backend, Lambda chatbot, Lambda indexing, and related AWS services. <br> - Created Amazon SNS topic for system alert notification. <br> - Subscribed email notification to the SNS topic. <br> - Verified that the monitoring and notification flow was ready for CloudWatch Alarm integration. | 07/07/2026 | 07/07/2026 |
| 6 | - Created CloudWatch Alarms for important system metrics and error conditions. <br> - Connected CloudWatch Alarms with the SNS notification topic. <br> - Configured AWS Backup plan for Amazon RDS to protect database data. <br> - Created backup resource assignment for the RDS database. <br> - Reviewed backup configuration to ensure database recovery support. | 08/07/2026 | 08/07/2026 |
| 7 | - Attached AWS WAF to CloudFront to improve protection for the public website. <br> - Reviewed IAM roles and policies for Lambda backend, Lambda migration, Lambda chatbot, and Lambda indexing. <br> - Applied the principle of least privilege so each Lambda function only has the permissions required for its task. <br> - Performed final testing for user login, product browsing, cart, order, admin management, and chatbot. <br> - Completed workshop screenshots, worklog content, and final internship report preparation. | 09/07/2026 | 09/07/2026 |

### Week 12 Achievements

* Successfully built the React frontend for production deployment.

* Created Amazon S3 bucket `pharmacare-frontend-web-phu-2026` to store frontend build files.

* Uploaded the React `dist` folder to Amazon S3.

* Kept the S3 frontend bucket private and used CloudFront to publish the website securely.

* Created CloudFront distribution `pharmacare-frontend-distribution` for the production website.

* Configured CloudFront with:

  * S3 frontend bucket as origin
  * Default root object `index.html`
  * Custom error response `403 → /index.html → 200`
  * Custom error response `404 → /index.html → 200`
  * CloudFront invalidation `/*` after uploading new frontend builds

* Deployed the website successfully at:

  * `https://d3tm5364zrtmpq.cloudfront.net/`

* Updated Amazon Cognito configuration for production frontend access.

* Updated Cognito Allowed callback URLs and Allowed sign-out URLs with the CloudFront domain.

* Updated API Gateway CORS configuration so the production frontend can call backend APIs.

* Updated frontend environment variables from local development to production deployment.

* Verified that the React frontend can connect to:

  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda backend
  * Amazon RDS data through backend APIs
  * AI chatbot API

* Configured Amazon CloudWatch Logs for observing backend, chatbot, indexing, and system behavior.

* Created Amazon SNS topic for system alert notification.

* Created CloudWatch Alarms and connected them with SNS notification.

* Configured AWS Backup plan for Amazon RDS.

* Created backup resource assignment for the RDS database.

* Attached AWS WAF to CloudFront to improve protection for the public web layer.

* Reviewed IAM permissions for project Lambda functions.

* Applied least-privilege access control for roles used by:

  * Lambda backend
  * Lambda migration
  * Lambda indexing
  * Lambda chatbot

* Performed final testing for the main system flows:

  * User login/logout
  * Product listing
  * Product detail
  * Cart management
  * Order creation
  * Order history
  * Admin product management
  * Admin order management
  * Admin user management
  * AI chatbot question answering

* Completed the final deployment and operational configuration of **PharmaCare AI**.

* Finished week 12 with a complete AWS-based online pharmacy system including frontend deployment, backend API, authentication, database, AI chatbot, monitoring, backup, and security configuration.