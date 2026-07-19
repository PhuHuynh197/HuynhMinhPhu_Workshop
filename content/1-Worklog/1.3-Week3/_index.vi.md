---
title: "Worklog Tuần 3"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3

* Hiểu các khái niệm cốt lõi của Amazon Virtual Private Cloud (Amazon VPC).
* Tìm hiểu cách thiết kế một môi trường mạng cơ bản trên AWS.
* Hiểu vai trò của Subnet, Route Table, Internet Gateway, NAT Gateway, Security Group và Network ACL.
* Thực hành xây dựng môi trường VPC và triển khai EC2 để kiểm tra kết nối mạng.
* Tìm hiểu khái niệm cơ bản về VPC Peering và cách giao tiếp riêng tư giữa hai VPC.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu tổng quan về Amazon VPC. <br> - Hiểu lý do sử dụng VPC để cô lập và kiểm soát tài nguyên mạng trên cloud. <br> - Ghi chú các khái niệm về CIDR block, private IP, public IP, Availability Zone và thiết kế subnet. | 01/05/2026 | 01/05/2026 | <https://000003.awsstudygroup.com/> |
| 2 | - Tìm hiểu Subnet và Route Table. <br> - Hiểu sự khác nhau giữa public subnet và private subnet. <br> - Học cách route table điều hướng traffic giữa subnet và gateway. <br> - Thực hành lên kế hoạch cho một mô hình VPC đơn giản. | 02/05/2026 | 02/05/2026 | <https://000003.awsstudygroup.com/> |
| 3 | - Tìm hiểu Internet Gateway và NAT Gateway. <br> - Hiểu cách public subnet truy cập internet thông qua Internet Gateway. <br> - Hiểu cách private subnet truy cập internet thông qua NAT Gateway mà không bị public trực tiếp. <br> - So sánh public access và private outbound access. | 03/05/2026 | 03/05/2026 | <https://000003.awsstudygroup.com/> |
| 4 | - Tìm hiểu Security Group và Network ACL. <br> - So sánh cơ chế firewall stateful và stateless. <br> - Thực hành xác định inbound rule và outbound rule. <br> - Hiểu tầm quan trọng của bảo mật mạng nhiều lớp trên AWS. | 04/05/2026 | 04/05/2026 | <https://000003.awsstudygroup.com/> |
| 5 | - Thực hành tạo môi trường VPC. <br> - Tạo VPC, Subnet, Internet Gateway, Route Table và Security Group. <br> - Bật VPC Flow Logs để ghi nhận thông tin traffic mạng. <br> - Xem VPC Resource Map để hiểu mối liên hệ giữa các thành phần mạng. | 05/05/2026 | 05/05/2026 | <https://000003.awsstudygroup.com/> |
| 6 | - Triển khai EC2 instance bên trong VPC để kiểm thử. <br> - Kiểm tra kết nối mạng giữa các tài nguyên. <br> - Tìm hiểu NAT Gateway, Reachability Analyzer, EC2 Instance Connect Endpoint, Systems Manager Session Manager và CloudWatch Monitoring để hỗ trợ xử lý lỗi mạng. | 06/05/2026 | 06/05/2026 | <https://000003.awsstudygroup.com/> |
| 7 | - Tìm hiểu VPC Peering. <br> - Học cách hai VPC có thể giao tiếp riêng tư thông qua peering connection. <br> - Thực hành cập nhật Network ACL và Route Table cho VPC Peering. <br> - Tìm hiểu Cross-Peer DNS và dọn dẹp tài nguyên sau khi hoàn thành lab. | 07/05/2026 | 07/05/2026 | <https://000019.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 3

* Hiểu được vai trò của Amazon VPC trong việc xây dựng môi trường mạng cloud riêng biệt và an toàn.

* Nắm được các thành phần chính trong kiến trúc VPC, bao gồm:

  * VPC
  * CIDR block
  * Public subnet
  * Private subnet
  * Route table
  * Internet Gateway
  * NAT Gateway
  * Security Group
  * Network ACL

* Hiểu sự khác nhau giữa public subnet và private subnet.

* Biết cách route table quyết định hướng đi của traffic mạng.

* Hiểu cách Internet Gateway cho phép tài nguyên trong public subnet truy cập internet.

* Hiểu cách NAT Gateway cho phép tài nguyên trong private subnet truy cập internet an toàn mà không cần public trực tiếp.

* Thực hành tạo các thành phần VPC cơ bản và kết nối chúng thành một môi trường mạng hoạt động được.

* Phân biệt được Security Group và Network ACL:

  * Security Group hoạt động ở mức instance hoặc resource.
  * Network ACL hoạt động ở mức subnet.
  * Security Group là stateful.
  * Network ACL là stateless.

* Tìm hiểu cách VPC Flow Logs, Reachability Analyzer, Session Manager và CloudWatch hỗ trợ giám sát, kiểm tra và xử lý lỗi mạng.

* Hiểu khái niệm cơ bản về VPC Peering và cách cấu hình giao tiếp riêng tư giữa hai VPC.

* Hoàn thành tuần 3 với nền tảng tốt hơn về AWS networking, phục vụ cho việc thiết kế hạ tầng của dự án PharmaCare AI.