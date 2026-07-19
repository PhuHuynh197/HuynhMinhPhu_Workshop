---
title: "Week 2 Worklog"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives

* Understand the purpose of AWS Identity and Access Management (IAM).
* Learn how to manage access permissions using IAM users, groups, policies, and roles.
* Practice creating IAM groups and IAM users with suitable permissions.
* Understand how IAM Role and Switch Role are used to provide temporary and controlled access.
* Learn how to clean up IAM resources after finishing the practice lab.

### Tasks to be carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Studied the overview of AWS Identity and Access Management. <br> - Learned why IAM is important for securing AWS accounts and resources. <br> - Took notes about authentication, authorization, and the principle of least privilege. | 24/04/2026 | 24/04/2026 | <https://000002.awsstudygroup.com/> |
| 2 | - Learned about IAM User and IAM Group. <br> - Understood how groups help manage permissions for multiple users. <br> - Practiced creating an Admin Group and assigning suitable permissions. | 25/04/2026 | 25/04/2026 | <https://000002.awsstudygroup.com/> |
| 3 | - Created an IAM Admin User. <br> - Added the user to the Admin Group. <br> - Practiced signing in with the IAM user instead of using the root account. <br> - Compared the difference between root user and IAM user. | 26/04/2026 | 26/04/2026 | <https://000002.awsstudygroup.com/> |
| 4 | - Learned about IAM Policy. <br> - Studied how policies define allowed and denied actions. <br> - Reviewed the basic policy structure, including Effect, Action, Resource, and Condition. <br> - Applied permissions to users and groups. | 27/04/2026 | 27/04/2026 | <https://000002.awsstudygroup.com/> |
| 5 | - Learned about IAM Role. <br> - Created an Admin Role for temporary access. <br> - Created an OperatorUser and prepared permission configuration for role switching. <br> - Understood why roles are safer than sharing long-term credentials. | 28/04/2026 | 28/04/2026 | <https://000002.awsstudygroup.com/> |
| 6 | - Practiced Switch Role in AWS Console. <br> - Allowed OperatorUser to switch to the Admin Role. <br> - Tested access after switching role. <br> - Verified that permissions changed according to the selected role. | 29/04/2026 | 29/04/2026 | <https://000002.awsstudygroup.com/> |
| 7 | - Reviewed IAM best practices. <br> - Checked the created IAM users, groups, policies, and roles. <br> - Cleaned up IAM resources after completing the lab. <br> - Summarized the role of IAM in securing AWS projects. | 30/04/2026 | 30/04/2026 | <https://000002.awsstudygroup.com/> |

### Week 2 Achievements

* Understood the role of AWS IAM in managing secure access to AWS services and resources.

* Learned the difference between:

  * Root user
  * IAM user
  * IAM group
  * IAM policy
  * IAM role

* Practiced creating IAM groups and IAM users for access management.

* Understood how IAM policies are used to control permissions through policy documents.

* Learned the basic structure of an IAM policy, including:

  * Effect
  * Action
  * Resource
  * Condition

* Practiced using IAM Role and Switch Role to provide temporary permissions.

* Understood the principle of least privilege, which means each user should only receive the permissions required for their tasks.

* Understood why the root account should not be used for daily operations.

* Learned the importance of cleaning up IAM resources after practice to keep the AWS environment secure and organized.

* Completed the second week with a stronger understanding of identity management and permission control on AWS.