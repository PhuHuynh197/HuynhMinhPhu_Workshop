---
title: "Worklog Tuần 4"
date: 2026-05-08
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4

* Hiểu các khái niệm cơ bản của Amazon Elastic Compute Cloud (Amazon EC2).
* Tìm hiểu cách khởi tạo và quản lý EC2 instance Linux và Windows.
* Thực hành kết nối EC2 instance bằng SSH và Remote Desktop Protocol (RDP).
* Tìm hiểu cách Security Group kiểm soát traffic inbound và outbound cho EC2.
* Hiểu các khái niệm Amazon EBS, Snapshot, AMI và khôi phục instance.
* Tìm hiểu quy trình cơ bản của VM Import/Export và cách di chuyển máy ảo lên AWS.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu tổng quan về Amazon EC2. <br> - Hiểu mục đích của EC2 trong điện toán đám mây. <br> - Ghi chú các khái niệm về instance type, AMI, key pair, public IP, private IP và Security Group. | 08/05/2026 | 08/05/2026 | <https://000004.awsstudygroup.com/> |
| 2 | - Chuẩn bị môi trường mạng cho EC2. <br> - Ôn lại yêu cầu về VPC và subnet cho Linux instance và Windows instance. <br> - Tạo Security Group cho Linux và Windows instance. <br> - Cấu hình inbound rule cho SSH và RDP. | 09/05/2026 | 09/05/2026 | <https://000004.awsstudygroup.com/> |
| 3 | - Khởi tạo Microsoft Windows Server EC2 instance. <br> - Tải và quản lý file key pair. <br> - Lấy mật khẩu administrator của Windows instance. <br> - Kết nối vào Windows instance bằng RDP. | 10/05/2026 | 10/05/2026 | <https://000004.awsstudygroup.com/> |
| 4 | - Khởi tạo Amazon Linux instance. <br> - Kết nối vào Linux instance bằng SSH. <br> - Thực hành một số lệnh Linux cơ bản trên EC2 instance. <br> - So sánh phương thức kết nối giữa Linux EC2 và Windows EC2. | 11/05/2026 | 11/05/2026 | <https://000004.awsstudygroup.com/> |
| 5 | - Tìm hiểu các thao tác cơ bản với Amazon EC2. <br> - Thực hành thay đổi instance type. <br> - Tạo và quản lý EBS Snapshot. <br> - Tạo custom AMI từ EC2 instance. <br> - Khởi tạo instance mới từ custom AMI. | 12/05/2026 | 12/05/2026 | <https://000004.awsstudygroup.com/> |
| 6 | - Thực hành triển khai ứng dụng mẫu AWS User Management. <br> - Cài đặt và cấu hình môi trường web server trên Amazon Linux. <br> - Tìm hiểu cách triển khai ứng dụng Node.js trên EC2. <br> - Kiểm tra ứng dụng thông qua trình duyệt. | 13/05/2026 | 13/05/2026 | <https://000004.awsstudygroup.com/> |
| 7 | - Tìm hiểu quy trình cơ bản của AWS VM Import/Export. <br> - Học cách một máy ảo có thể được export từ môi trường on-premises và import lên AWS. <br> - Xem vai trò của S3, AMI và EC2 trong quá trình migration máy ảo. <br> - Dọn dẹp EC2, EBS, AMI và các tài nguyên liên quan để tránh phát sinh chi phí không cần thiết. | 14/05/2026 | 14/05/2026 | <https://000014.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 4

* Hiểu được vai trò của Amazon EC2 trong việc cung cấp máy chủ ảo có khả năng mở rộng trên AWS.

* Nắm được các thành phần chính khi khởi tạo một EC2 instance, bao gồm:

  * Amazon Machine Image
  * Instance type
  * Key pair
  * Security Group
  * Public IP address
  * Private IP address
  * VPC và subnet

* Thực hành khởi tạo và kết nối vào Windows EC2 instance bằng Remote Desktop Protocol.

* Thực hành khởi tạo và kết nối vào Amazon Linux EC2 instance bằng SSH.

* Hiểu cách Security Group bảo vệ EC2 instance thông qua việc kiểm soát inbound và outbound traffic.

* Phân biệt được cách kết nối giữa Linux EC2 và Windows EC2.

* Hiểu cách Amazon EBS cung cấp block storage lâu dài cho EC2 instance.

* Thực hành tạo EBS Snapshot để phục vụ mục đích sao lưu.

* Biết cách tạo custom AMI từ một EC2 instance đã cấu hình sẵn.

* Thực hành khởi tạo EC2 instance mới từ custom AMI.

* Hiểu quy trình cơ bản khi triển khai ứng dụng web trên EC2.

* Nắm được khái niệm cơ bản về VM Import/Export và cách dịch vụ này hỗ trợ di chuyển máy ảo từ môi trường on-premises lên AWS.

* Dọn dẹp các tài nguyên EC2 tạm thời sau khi hoàn thành lab để hạn chế sử dụng AWS credit không cần thiết.

* Hoàn thành tuần 4 với nền tảng tốt hơn về dịch vụ compute và quản lý máy chủ ảo trên AWS.