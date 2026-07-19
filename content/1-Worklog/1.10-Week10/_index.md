---
title: "Week 10 Worklog"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives

* Deploy the backend API layer for the **PharmaCare AI** system.
* Create AWS Lambda backend using Node.js 22.x and connect it to Amazon RDS PostgreSQL.
* Configure environment variables so Lambda can retrieve database credentials from AWS Secrets Manager.
* Create Amazon API Gateway HTTP API to expose backend services to the frontend.
* Configure public API routes for product browsing and store data.
* Create Amazon Cognito User Pool for user authentication.
* Create Admin and Customer groups for role-based access control.
* Configure Cognito JWT Authorizer in API Gateway to protect authenticated routes.
* Implement main business functions for customer and admin users.
* Create S3 bucket and CloudFront distribution for product images.
* Test backend APIs with a React frontend during local development.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date |
| --- | --- | --- | --- |
| 1 | - Created AWS Lambda backend function named `pharmacare-backend-api`. <br> - Used Node.js 22.x runtime for the backend API. <br> - Placed Lambda inside the private application subnet so that it can connect to Amazon RDS PostgreSQL. <br> - Increased Lambda timeout because backend requests may need time to connect to RDS and process database queries. | 19/06/2026 | 19/06/2026 |
| 2 | - Prepared backend source code in VS Code. <br> - Installed required Node.js packages such as `pg` for PostgreSQL connection and AWS SDK for reading secrets. <br> - Added environment variables including `AWS_REGION`, `RDS_SECRET_ARN`, and `DB_NAME`. <br> - Packaged the backend source code as a ZIP file and uploaded it to Lambda. | 20/06/2026 | 20/06/2026 |
| 3 | - Created Amazon API Gateway HTTP API for the backend. <br> - Integrated API Gateway with `pharmacare-backend-api` Lambda. <br> - Configured public routes such as `/health`, `/categories`, `/products`, `/products/{id}`, and `/stores`. <br> - Tested `/health` to verify that the API and Lambda integration worked correctly. | 21/06/2026 | 21/06/2026 |
| 4 | - Created Amazon Cognito User Pool for authentication. <br> - Created App Client for the React web application. <br> - Created two user groups: `Admin` and `Customer`. <br> - Created sample users for testing login and role-based access. <br> - Verified Cognito User Pool ID and Client ID for frontend configuration. | 22/06/2026 | 22/06/2026 |
| 5 | - Configured CORS in API Gateway so the React frontend can call backend APIs. <br> - Created Cognito JWT Authorizer in API Gateway. <br> - Attached JWT Authorizer to protected routes. <br> - Protected routes such as `/profile`, `/cart`, `/orders`, and `/admin/...` so they require a valid Cognito token. | 23/06/2026 | 23/06/2026 |
| 6 | - Implemented customer business functions in the backend. <br> - Added profile, cart, and order APIs. <br> - Configured routes such as `GET /profile`, `GET /cart`, `POST /cart`, `PUT /cart/{productId}`, `DELETE /cart/{productId}`, `POST /orders`, `GET /orders`, and `GET /orders/{id}`. <br> - Tested customer login and API requests with JWT token. | 24/06/2026 | 24/06/2026 |
| 7 | - Implemented admin business functions for managing the pharmacy system. <br> - Added admin features for product management, category management, user management, inventory update, and order status update. <br> - Created S3 bucket for product images and organized images under the product folder. <br> - Created CloudFront distribution for product image delivery. <br> - Updated `image_url` in RDS so product data can display images on the frontend. <br> - Created and tested a local React frontend using Vite and `react-oidc-context` to verify login, API connection, product display, cart, and order flow. | 25/06/2026 | 25/06/2026 |

### Week 10 Achievements

* Successfully created the main backend Lambda function `pharmacare-backend-api`.

* Configured Lambda to run inside the private application subnet and connect securely to Amazon RDS PostgreSQL.

* Used AWS Secrets Manager to retrieve database credentials instead of storing sensitive information directly in the source code.

* Configured important backend environment variables, including:

  * `AWS_REGION`
  * `RDS_SECRET_ARN`
  * `DB_NAME`

* Created Amazon API Gateway HTTP API to expose backend services.

* Integrated API Gateway with AWS Lambda backend.

* Created and tested public API routes, including:

  * `GET /health`
  * `GET /categories`
  * `GET /products`
  * `GET /products/{id}`
  * `GET /stores`

* Created Amazon Cognito User Pool for user authentication.

* Created Cognito App Client for the React web application.

* Created two main Cognito groups:

  * `Admin`
  * `Customer`

* Configured Cognito JWT Authorizer in API Gateway.

* Protected authenticated routes using Cognito JWT token.

* Implemented customer APIs, including:

  * User profile
  * Shopping cart
  * Add product to cart
  * Update cart item quantity
  * Remove product from cart
  * Create order
  * View order history
  * View order detail

* Implemented admin APIs, including:

  * Product management
  * Category management
  * User management
  * Inventory update
  * Order management
  * Order status update
  * User lock/unlock
  * User role update

* Created S3 bucket for product images.

* Created CloudFront distribution to deliver product images efficiently.

* Updated product `image_url` data in RDS so the frontend can display product images.

* Created a React frontend locally using Vite to test authentication and backend integration.

* Tested the basic business flow from frontend to API Gateway, Lambda, RDS, and Cognito.

* Completed week 10 with a working backend API, authentication system, protected routes, customer/admin business functions, and product image delivery setup.