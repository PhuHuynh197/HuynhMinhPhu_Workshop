---
title: "Worklog Tuần 7"
date: 2026-05-29
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7

* Hiểu cách quản lý chi phí AWS bằng AWS Budgets.
* Tìm hiểu cách giám sát tài nguyên, metric, log và alarm bằng Amazon CloudWatch.
* Hiểu các gói AWS Support và cách tạo support case.
* Tìm hiểu khái niệm hybrid DNS bằng Amazon Route 53 Resolver.
* Hiểu quy trình CI/CD cho ứng dụng container chạy trên Amazon ECS.
* Tìm hiểu cách AWS Security Hub hỗ trợ đánh giá tình trạng bảo mật cloud.
* Hiểu vai trò của AWS Transit Gateway trong việc kết nối nhiều VPC.
* Thực hành dọn dẹp tài nguyên cẩn thận để tránh sử dụng AWS credit không cần thiết.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu AWS Budgets và vai trò của dịch vụ này trong quản lý chi phí cloud. <br> - Phân biệt Cost Budget, Usage Budget, RI Budget và Savings Plans Budget. <br> - Thực hành tạo cost budget và cấu hình ngưỡng cảnh báo. <br> - Xem cách budget notification hỗ trợ kiểm soát AWS credit. | 29/05/2026 | 29/05/2026 | <https://000007.awsstudygroup.com/> |
| 2 | - Tìm hiểu tổng quan về Amazon CloudWatch. <br> - Học cách CloudWatch thu thập metric, log và event từ tài nguyên AWS. <br> - Thực hành xem metric của EC2 và tạo CloudWatch alarm cơ bản. <br> - Xem cách CloudWatch hỗ trợ giám sát và xử lý lỗi hệ thống. | 30/05/2026 | 30/05/2026 | <https://000008.awsstudygroup.com/> |
| 3 | - Tìm hiểu CloudWatch Logs. <br> - Xem lại log group, log stream và lưu trữ log tập trung. <br> - Thực hành kiểm tra log từ tài nguyên AWS và ứng dụng. <br> - Hiểu cách log hỗ trợ phát hiện lỗi, hành vi bất thường và vấn đề vận hành. | 31/05/2026 | 31/05/2026 | <https://000008.awsstudygroup.com/> |
| 4 | - Tìm hiểu AWS Support và AWS Support Plans. <br> - Phân biệt các mức hỗ trợ Basic, Developer, Business, Enterprise và Unified Operations. <br> - Thực hành truy cập AWS Support Center. <br> - Học cách tạo support case và chọn loại yêu cầu, mức độ nghiêm trọng phù hợp. | 01/06/2026 | 01/06/2026 | <https://000009.awsstudygroup.com/> |
| 5 | - Tìm hiểu hybrid DNS với Amazon Route 53 Resolver. <br> - Hiểu vai trò của inbound endpoint, outbound endpoint, resolver rule và forward DNS query. <br> - Xem cách Route 53 Resolver tích hợp DNS trên AWS với hệ thống DNS on-premises. <br> - Tìm hiểu quy trình chuẩn bị bằng CloudFormation và yêu cầu dọn dẹp tài nguyên. | 02/06/2026 | 02/06/2026 | <https://000010.awsstudygroup.com/> |
| 6 | - Tìm hiểu CI/CD deployment với ECS Container. <br> - Xem lại GitHub Actions, GitLab CI/CD, AWS CodeBuild, Amazon ECR, Amazon ECS và AWS CodeDeploy trong pipeline triển khai. <br> - Hiểu cách thay đổi source code có thể tự động kích hoạt build, test, push image và deploy. <br> - Tìm hiểu Container Insights để giám sát workload container trên ECS. | 03/06/2026 | 03/06/2026 | <https://000017.awsstudygroup.com/> |
| 7 | - Tìm hiểu AWS Security Hub và AWS Transit Gateway. <br> - Bật Security Hub trong thời gian ngắn để kiểm tra, xem security standards và security score, sau đó tắt dịch vụ sau khi hoàn thành lab. <br> - Học kiến trúc cơ bản của Transit Gateway, VPC attachment, Transit Gateway route table và cập nhật route table của VPC. <br> - Dọn dẹp Security Hub, Transit Gateway, CloudFormation, EC2, Route 53 Resolver và các tài nguyên liên quan để tránh phát sinh chi phí không cần thiết. | 04/06/2026 | 04/06/2026 | <https://000018.awsstudygroup.com/> <br> <https://000020.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 7

* Hiểu cách AWS Budgets hỗ trợ kiểm soát chi phí cloud và tránh sử dụng AWS credit ngoài dự kiến.

* Nắm được các loại AWS Budgets chính, bao gồm:

  * Cost Budget
  * Usage Budget
  * RI Budget
  * Savings Plans Budget

* Thực hành thiết lập ngưỡng ngân sách và cảnh báo để giám sát chi phí.

* Hiểu cách Amazon CloudWatch được dùng để giám sát tài nguyên và ứng dụng trên AWS.

* Nắm được các thành phần cơ bản của CloudWatch, bao gồm:

  * Metrics
  * Alarms
  * Logs
  * Log groups
  * Log streams
  * Events

* Hiểu cách CloudWatch Logs hỗ trợ xử lý lỗi bằng cách thu thập và lưu trữ log của ứng dụng, hệ thống.

* Hiểu mục đích của AWS Support và sự khác nhau giữa các gói hỗ trợ dựa trên thời gian phản hồi và phạm vi hỗ trợ.

* Thực hành truy cập AWS Support Center và hiểu quy trình tạo support case.

* Hiểu khái niệm cơ bản về hybrid DNS bằng Amazon Route 53 Resolver.

* Biết vai trò của Route 53 Resolver inbound endpoint, outbound endpoint và resolver rule.

* Hiểu quy trình cơ bản của CI/CD cho ứng dụng container trên Amazon ECS.

* Biết cách GitHub Actions, GitLab CI/CD, CodeBuild, ECR, ECS và CodeDeploy có thể phối hợp trong pipeline triển khai tự động.

* Hiểu cách AWS Security Hub cung cấp góc nhìn tập trung về security findings và compliance status.

* Xem các tiêu chuẩn bảo mật như AWS Foundational Security Best Practices và CIS AWS Foundations Benchmark.

* Hiểu vai trò của AWS Transit Gateway như một network hub trung tâm để kết nối nhiều VPC.

* Nhận biết rằng các dịch vụ nâng cao như Security Hub, Transit Gateway, NAT Gateway, Load Balancer và tài nguyên tạo bằng CloudFormation cần được dọn dẹp cẩn thận sau khi thực hành.

* Hoàn thành tuần 7 với nền tảng tốt hơn về quản lý chi phí, giám sát, hỗ trợ, DNS, CI/CD, giám sát bảo mật và networking nâng cao trên AWS.