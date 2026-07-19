---
title: "Week 3 Worklog"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives

* Understand the core concepts of Amazon Virtual Private Cloud (Amazon VPC).
* Learn how to design a basic network environment on AWS.
* Understand the role of subnets, route tables, Internet Gateway, NAT Gateway, Security Groups, and Network ACLs.
* Practice building a VPC environment and deploying EC2 instances for network testing.
* Learn the basic concept of VPC Peering and how private communication between two VPCs works.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Studied the overview of Amazon VPC. <br> - Learned why VPC is used to isolate and control cloud network resources. <br> - Took notes about CIDR blocks, private IP addresses, public IP addresses, Availability Zones, and subnet design. | 01/05/2026 | 01/05/2026 | <https://000003.awsstudygroup.com/> |
| 2 | - Learned about Subnets and Route Tables. <br> - Understood the difference between public subnet and private subnet. <br> - Studied how route tables control network traffic between subnets and gateways. <br> - Practiced planning a simple VPC network structure. | 02/05/2026 | 02/05/2026 | <https://000003.awsstudygroup.com/> |
| 3 | - Learned about Internet Gateway and NAT Gateway. <br> - Understood how public subnets access the internet through an Internet Gateway. <br> - Understood how private subnets access the internet through a NAT Gateway without being directly exposed. <br> - Compared public access and private outbound access. | 03/05/2026 | 03/05/2026 | <https://000003.awsstudygroup.com/> |
| 4 | - Learned about Security Groups and Network ACLs. <br> - Compared stateful firewall protection and stateless firewall protection. <br> - Practiced defining inbound and outbound rules. <br> - Understood the importance of layered network security in AWS. | 04/05/2026 | 04/05/2026 | <https://000003.awsstudygroup.com/> |
| 5 | - Practiced creating a VPC environment. <br> - Created VPC, subnets, Internet Gateway, route tables, and Security Group. <br> - Enabled VPC Flow Logs to record network traffic information. <br> - Reviewed the VPC Resource Map to understand the relationship between network components. | 05/05/2026 | 05/05/2026 | <https://000003.awsstudygroup.com/> |
| 6 | - Deployed EC2 instances inside the VPC for testing. <br> - Tested network connectivity between resources. <br> - Studied NAT Gateway, Reachability Analyzer, EC2 Instance Connect Endpoint, Systems Manager Session Manager, and CloudWatch monitoring for network troubleshooting. | 06/05/2026 | 06/05/2026 | <https://000003.awsstudygroup.com/> |
| 7 | - Learned about VPC Peering. <br> - Studied how two VPCs can communicate privately through a peering connection. <br> - Practiced updating Network ACLs and Route Tables for VPC Peering. <br> - Learned about Cross-Peer DNS and cleaned up lab resources after completion. | 07/05/2026 | 07/05/2026 | <https://000019.awsstudygroup.com/> |

### Week 3 Achievements

* Understood the role of Amazon VPC in building an isolated and secure cloud network environment.

* Learned the main components of a VPC architecture, including:

  * VPC
  * CIDR block
  * Public subnet
  * Private subnet
  * Route table
  * Internet Gateway
  * NAT Gateway
  * Security Group
  * Network ACL

* Understood the difference between public subnet and private subnet.

* Learned how route tables decide where network traffic is forwarded.

* Understood how Internet Gateway allows resources in public subnets to access the internet.

* Understood how NAT Gateway allows resources in private subnets to access the internet securely without exposing them directly.

* Practiced creating basic VPC components and connecting them into a working network environment.

* Learned the difference between Security Groups and Network ACLs:

  * Security Groups work at the instance or resource level.
  * Network ACLs work at the subnet level.
  * Security Groups are stateful.
  * Network ACLs are stateless.

* Learned how VPC Flow Logs, Reachability Analyzer, Session Manager, and CloudWatch can support network monitoring and troubleshooting.

* Understood the basic concept of VPC Peering and how private communication between two VPCs can be configured.

* Completed week 3 with a stronger foundation in AWS networking, which is important for designing the infrastructure of the PharmaCare AI project.