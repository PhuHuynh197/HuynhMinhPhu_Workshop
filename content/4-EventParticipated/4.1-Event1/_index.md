---
title: "Event 1"
date: 2026-06-06
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Event Report: AWS Community Day

### Event Information

* **Event Name:** AWS Community Day
* **Date:** 09:00, June 06, 2026
* **Location:** Floor 26, Bitexco Financial Tower
* **Role:** Attendee

### Event Objectives

* Learn from real-world AWS cloud implementation experience.
* Understand the difference between Virtual Machines, Containers, and Serverless architecture.
* Explore practical challenges when deploying cloud-native systems.
* Learn how AWS WAF and Machine Learning can support network attack detection.
* Gain career orientation from professionals working in cloud, system administration, DevOps, and cybersecurity.

### Event Description

AWS Community Day was a technology event focused on cloud computing, modern system architecture, cybersecurity, artificial intelligence, and career development in the IT industry.

The event provided practical knowledge from speakers who have real experience working with AWS and enterprise systems. The topics were not limited to theory but also included operational challenges, security thinking, system design, and career lessons.

For me, this event was useful because the content was closely related to my internship project **PharmaCare AI**, especially in areas such as AWS Lambda, API Gateway, CloudFront, WAF, monitoring, serverless architecture, and AI-based security.

### Speakers & Agenda

| Time | Speaker | Main Topic |
| --- | --- | --- |
| 09:20 - 10:00 | Nguyen Quoc Bao | AWS cloud architecture and real-world implementation experience |
| 10:00 - 10:35 | Nguyen Huynh Quoc Bao | Virtual Machines, Containers, and deployment models |
| 10:35 - 10:50 | Viet Phat | Serverless architecture and practical implementation challenges |
| 10:50 - 11:10 | Le Hoang Gia Dai | AWS WAF and Machine Learning for cyber attack detection |
| 11:10 - 12:00 | Tran Trung Vinh | Career journey from Sysadmin to DevOps and interview experience |

### Key Highlights

#### 1. Virtual Machines vs. Containers

One important topic was the comparison between Virtual Machines and Containers.

Virtual Machines usually run with a full guest operating system on top of a hypervisor. This provides strong isolation but consumes more CPU, RAM, and storage. Containers, such as Docker containers, share the host operating system kernel and package only the application and its dependencies.

Because of this, containers are lighter, start faster, and are more suitable for modern application deployment. This helped me understand why many real-world systems use containers or serverless services instead of relying only on traditional virtual machines.

#### 2. Serverless Architecture Challenges

The event also discussed practical challenges when using serverless services such as AWS Lambda and DynamoDB.

Although AWS Lambda reduces server management work, it is stateless by design. This means the application state should be stored in external services such as databases. If database access is not optimized, operations such as scanning an entire table can become slow and expensive when the system grows.

This lesson is useful for my PharmaCare AI project because my backend uses AWS Lambda. It reminded me that Lambda functions should be designed carefully, database queries should be optimized, and unnecessary processing should be avoided.

#### 3. AWS WAF and Machine Learning for Security

Another impressive session was about combining AWS WAF with Machine Learning to detect cyber attacks.

Traditional WAF rules are usually based on known attack patterns. However, modern attacks can include zero-day attacks or abnormal behaviors that do not match existing signatures. Machine Learning can help analyze traffic behavior and identify suspicious patterns.

As an Information Security student, this topic was highly relevant to my learning direction. It showed me that AI can be used not only for chatbot systems but also for security monitoring and cyber defense.

#### 4. Career Journey from Sysadmin to DevOps

The career sharing session helped me understand the development path from Helpdesk or Sysadmin to DevOps Engineer.

The speaker emphasized that cloud engineers need more than technical knowledge. They also need an operational mindset, automation skills, monitoring experience, communication skills, and the ability to handle incidents in real systems.

This gave me a clearer direction for improving my skills after the internship.

### Key Takeaways

* Cloud computing requires system thinking, not only service usage.
* Virtual Machines, Containers, and Serverless each have different advantages and limitations.
* Serverless systems need careful design for state management, database performance, and cost control.
* AWS WAF can be improved with Machine Learning to detect abnormal network behavior.
* DevOps focuses on automation, monitoring, reliability, and continuous improvement.
* A good cloud or security engineer needs both technical knowledge and practical operational experience.

### Application to My Internship Project

The knowledge from this event can be applied directly to my **PharmaCare AI** project.

First, the serverless architecture discussion helped me understand how to design AWS Lambda functions more carefully. In PharmaCare AI, Lambda is used as the backend API layer, so the API logic should be simple, secure, and optimized.

Second, the AWS WAF topic helped me understand why WAF should be attached to CloudFront to protect the public web layer from abnormal requests.

Third, the operational mindset from the event helped me complete the monitoring and security part of my project. I applied this by configuring CloudWatch Logs, CloudWatch Alarms, SNS notifications, AWS Backup, and IAM least privilege.

Finally, the career sharing session motivated me to continue learning AWS, Linux, networking, automation, DevOps, and cybersecurity.

### Personal Experience at the Event

This event gave me a practical view of AWS and cloud security. Instead of only studying documents or labs, I was able to listen to real experiences from people who have worked with enterprise systems.

The most impressive topic for me was the combination of AWS WAF and Machine Learning for attack detection. Since my major is Information Security, this topic helped me see a strong connection between cloud computing, AI, and cybersecurity.

The event also helped me understand that building a cloud system is not only about making the application run. A real system also needs monitoring, backup, security, cost control, and a clear operation process.

### Event Photos

***(Cloud architecture and serverless challenges)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh4.jpg" style="width: 35%; margin: 0;" alt="Serverless architecture challenges">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh5.jpg" style="width: 35%; margin: 0;" alt="AWS architecture sharing">
</div>

***(Virtual Machines vs Containers)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh6.jpg" style="width: 35%; margin: 0;" alt="Virtual Machines and Containers comparison">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh7.jpg" style="width: 35%; margin: 0;" alt="Detailed comparison between VM and Container">
</div>

***(AWS WAF and Machine Learning for Security)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh9.jpg" style="width: 35%; margin: 0;" alt="AWS WAF and Machine Learning session">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh10.jpg" style="width: 35%; margin: 0;" alt="Cyber attack detection with WAF and ML">
</div>

***(Career orientation and professional sharing)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/HuynhMinhPhu_Workshop/images/events/event1/anh12.jpg" style="width: 35%; margin: 0;" alt="Career journey from Sysadmin to DevOps">
</div>

> In conclusion, AWS Community Day helped me connect my academic knowledge with real cloud practices. It improved my understanding of AWS architecture, serverless systems, cloud security, AI-based security monitoring, and career development in the IT industry.