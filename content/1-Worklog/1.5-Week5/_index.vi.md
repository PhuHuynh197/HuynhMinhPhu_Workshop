---
title: "Worklog Tuần 5"
date: 2026-05-15
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5

* Hiểu mục đích của Amazon Relational Database Service (Amazon RDS).
* Tìm hiểu cách tạo môi trường database cho ứng dụng trên AWS.
* Thực hành tạo VPC, Security Group và DB Subnet Group cho Amazon RDS.
* Tìm hiểu cách tạo và cấu hình Amazon RDS database instance.
* Thực hành kết nối ứng dụng chạy trên EC2 với RDS database.
* Hiểu các thao tác backup và restore bằng Amazon RDS và AWS Backup.
* Biết cách cấu hình thông báo backup và dọn dẹp tài nguyên liên quan đến backup.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu tổng quan về Amazon RDS. <br> - Hiểu lý do sử dụng RDS cho các workload cơ sở dữ liệu quan hệ. <br> - Ghi chú về managed database service, database engine, storage option, backup, high availability và security feature. | 15/05/2026 | 15/05/2026 | <https://000005.awsstudygroup.com/> |
| 2 | - Chuẩn bị môi trường mạng cho Amazon RDS. <br> - Tạo VPC cho bài lab database. <br> - Tạo EC2 Security Group và RDS Security Group. <br> - Xem lại cách Security Group kiểm soát kết nối giữa application server và database server. | 16/05/2026 | 16/05/2026 | <https://000005.awsstudygroup.com/> |
| 3 | - Tạo DB Subnet Group cho Amazon RDS. <br> - Chọn subnet từ các Availability Zone khác nhau. <br> - Hiểu lý do cần DB Subnet Group khi tạo RDS instance trong VPC. <br> - Kiểm tra cấu hình subnet và routing trước khi tạo database. | 17/05/2026 | 17/05/2026 | <https://000005.awsstudygroup.com/> |
| 4 | - Tạo Amazon RDS database instance. <br> - Cấu hình database engine, instance class, storage, username, password, VPC, DB Subnet Group và Security Group. <br> - Chờ RDS instance chuyển sang trạng thái available. <br> - Kiểm tra database endpoint để phục vụ kết nối ứng dụng. | 18/05/2026 | 18/05/2026 | <https://000005.awsstudygroup.com/> |
| 5 | - Tạo EC2 instance để triển khai ứng dụng. <br> - Deploy ứng dụng mẫu trên EC2. <br> - Cấu hình ứng dụng kết nối đến Amazon RDS database. <br> - Kiểm tra kết nối database và hoạt động của ứng dụng thông qua trình duyệt. | 19/05/2026 | 19/05/2026 | <https://000005.awsstudygroup.com/> |
| 6 | - Tìm hiểu AWS Backup và vai trò của dịch vụ này trong việc bảo vệ dữ liệu tập trung. <br> - Chuẩn bị các tài nguyên liên quan đến backup cho hệ thống. <br> - Tạo backup plan để tự động hóa quá trình sao lưu. <br> - Cấu hình thông báo bằng Amazon SNS để nhận cập nhật về quá trình backup. | 20/05/2026 | 20/05/2026 | <https://000013.awsstudygroup.com/> |
| 7 | - Thực hành kiểm tra backup và restore. <br> - Ôn lại khái niệm automated backup, manual snapshot, backup plan và restore. <br> - Hiểu tầm quan trọng của việc kiểm tra khả năng restore sau khi tạo backup. <br> - Dọn dẹp EC2, RDS, AWS Backup, SNS, Security Group, DB Subnet Group và các tài nguyên liên quan để tránh phát sinh chi phí không cần thiết. | 21/05/2026 | 21/05/2026 | <https://000005.awsstudygroup.com/> <br> <https://000013.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 5

* Hiểu được vai trò của Amazon RDS là dịch vụ cơ sở dữ liệu quan hệ được quản lý trên AWS.

* Biết rằng Amazon RDS giúp giảm bớt các công việc quản trị database như:

  * Khởi tạo database
  * Quản lý backup
  * Cập nhật bản vá
  * Mở rộng storage
  * Cấu hình high availability

* Hiểu các database engine phổ biến được Amazon RDS hỗ trợ, bao gồm:

  * MySQL
  * PostgreSQL
  * MariaDB
  * SQL Server
  * Oracle
  * Amazon Aurora

* Thực hành chuẩn bị hạ tầng cần thiết cho RDS database, bao gồm:

  * VPC
  * Subnet
  * EC2 Security Group
  * RDS Security Group
  * DB Subnet Group

* Hiểu lý do tầng database nên được tách biệt và không public trực tiếp ra Internet.

* Biết cách sử dụng Security Group để cho phép application server kết nối đến database một cách an toàn.

* Tạo và cấu hình được Amazon RDS database instance.

* Biết cách sử dụng RDS endpoint để kết nối ứng dụng với database.

* Thực hành deploy ứng dụng trên EC2 và kết nối ứng dụng đó với RDS database.

* Hiểu sự khác nhau cơ bản giữa automated backup, manual snapshot và AWS Backup plan.

* Biết cách AWS Backup hỗ trợ quản lý và tự động hóa quá trình backup cho các tài nguyên AWS.

* Biết cách Amazon SNS được sử dụng để gửi thông báo về quá trình backup.

* Hiểu tầm quan trọng của việc kiểm tra restore sau khi tạo backup.

* Dọn dẹp tài nguyên lab tạm thời sau khi hoàn thành để hạn chế sử dụng AWS credit.

* Hoàn thành tuần 5 với nền tảng tốt hơn về triển khai database, bảo mật database, backup và recovery trên AWS.