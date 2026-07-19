---
title: "Week 6 Worklog"
date: 2026-05-22
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives

* Understand how to improve application availability and scalability using Elastic Load Balancing and Auto Scaling Group.
* Learn how to create Launch Template, Target Group, Application Load Balancer, and Auto Scaling Group.
* Practice testing manual scaling, scheduled scaling, dynamic scaling, and predictive scaling metrics.
* Learn the basic concept of Docker and containerized application deployment.
* Practice deploying an application using Docker image and Docker Compose.
* Understand the basic workflow of deploying containerized applications on Amazon ECS.
* Learn how to clean up compute, container, load balancing, and database resources to avoid unnecessary cost.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Studied the overview of deploying an application with Auto Scaling Group. <br> - Reviewed the base application deployment from previous EC2 labs. <br> - Learned why Auto Scaling Group and Load Balancer are used to improve availability, fault tolerance, and scalability. | 22/05/2026 | 22/05/2026 | <https://000006.awsstudygroup.com/> |
| 2 | - Prepared the application infrastructure for Auto Scaling. <br> - Set up network infrastructure, EC2 instance, RDS database, and web server environment. <br> - Prepared sample data for the database and verified the application before scaling. | 23/05/2026 | 23/05/2026 | <https://000006.awsstudygroup.com/> |
| 3 | - Created Launch Template for EC2 instances. <br> - Created Target Group for the application. <br> - Configured Application Load Balancer to distribute traffic to application instances. <br> - Tested access through the Load Balancer endpoint. | 24/05/2026 | 24/05/2026 | <https://000006.awsstudygroup.com/> |
| 4 | - Created Auto Scaling Group using the Launch Template. <br> - Attached Auto Scaling Group to the Target Group and Load Balancer. <br> - Tested manual scaling and reviewed how EC2 instances were added or removed. <br> - Studied scheduled scaling, dynamic scaling, and predictive scaling metrics. | 25/05/2026 | 25/05/2026 | <https://000006.awsstudygroup.com/> |
| 5 | - Studied the basic concept of Docker and containerization. <br> - Installed required dependencies for local Docker deployment. <br> - Deployed and tested the application on the local environment. <br> - Prepared VPC, Security Group, IAM role, EC2, and RDS resources for Docker deployment on AWS. | 26/05/2026 | 26/05/2026 | <https://000015.awsstudygroup.com/> |
| 6 | - Deployed the application using Docker image on EC2. <br> - Deployed the application using Docker Compose. <br> - Practiced pushing Docker image to Amazon ECR or Docker Hub. <br> - Tested the containerized application through the browser. | 27/05/2026 | 27/05/2026 | <https://000015.awsstudygroup.com/> |
| 7 | - Studied the basic workflow of Amazon ECS deployment. <br> - Reviewed ECS Cluster, Task Definition, ECS Service, Cloud Map, and Application Load Balancer. <br> - Learned the difference between Blue/Green deployment and Rolling deployment. <br> - Cleaned up Auto Scaling, Load Balancer, EC2, RDS, Docker, ECS, ECR, NAT Gateway, and related resources to reduce unnecessary cost. | 28/05/2026 | 28/05/2026 | <https://000016.awsstudygroup.com/> |

### Week 6 Achievements

* Understood how Auto Scaling Group helps maintain application availability and automatically adjusts capacity based on demand.

* Understood how Application Load Balancer distributes user traffic across multiple application instances.

* Practiced preparing infrastructure for a scalable application, including:

  * VPC
  * EC2 instance
  * RDS database
  * Launch Template
  * Target Group
  * Application Load Balancer
  * Auto Scaling Group

* Learned the purpose of different scaling approaches, including:

  * Manual scaling
  * Scheduled scaling
  * Dynamic scaling
  * Predictive scaling metrics

* Understood the relationship between Load Balancer, Target Group, and Auto Scaling Group.

* Learned the basic concept of Docker and why containers help package applications with their dependencies.

* Practiced deploying an application using Docker image.

* Practiced deploying an application using Docker Compose.

* Learned how container images can be stored and shared using Amazon ECR or Docker Hub.

* Understood the basic components of Amazon ECS, including:

  * ECS Cluster
  * Task Definition
  * ECS Service
  * Container image
  * Application Load Balancer
  * Cloud Map

* Learned the difference between Blue/Green deployment and Rolling deployment at a basic level.

* Understood that some resources such as Load Balancer, NAT Gateway, RDS, ECS, and running EC2 instances can generate cost if not cleaned up.

* Completed week 6 with a stronger understanding of application scalability, container deployment, and container orchestration on AWS.