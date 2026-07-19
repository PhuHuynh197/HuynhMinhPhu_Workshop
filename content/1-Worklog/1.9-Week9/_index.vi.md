---
title: "Worklog Tuần 9"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9

* Bắt đầu triển khai hạ tầng AWS nền tảng cho hệ thống **PharmaCare AI**.
* Tạo VPC riêng cho hệ thống để tách biệt các lớp frontend, backend, database và AI.
* Thiết kế public subnet, private app subnet và private database subnet theo kiến trúc đã xây dựng.
* Triển khai Amazon RDS PostgreSQL làm cơ sở dữ liệu chính cho website nhà thuốc.
* Cấu hình Security Group để Lambda backend kết nối an toàn đến RDS qua port `5432`.
* Sử dụng AWS Secrets Manager để lưu thông tin kết nối database thay vì hard-code trong source code.
* Tạo VPC Endpoint để các tài nguyên trong private subnet có thể truy cập dịch vụ AWS nội bộ.
* Tạo Lambda migration để khởi tạo schema database ban đầu cho hệ thống.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | - Bắt đầu triển khai hạ tầng AWS cho dự án **PharmaCare AI**. <br> - Rà soát lại sơ đồ kiến trúc tổng thể của hệ thống. <br> - Xác định các lớp chính gồm Global layer, Frontend layer, Private App Subnet, RDS DB Subnet, OpenSearch VPC Subnet, Monitoring & Security layer. <br> - Lên kế hoạch triển khai hạ tầng theo thứ tự: VPC → subnet → route table → security group → RDS → Secrets Manager → Lambda migration. | 12/06/2026 | 12/06/2026 |
| 2 | - Tạo VPC riêng cho hệ thống với tên `pharmacare-vpc`. <br> - Sử dụng region `ap-southeast-1`. <br> - Cấu hình CIDR block `10.0.0.0/16` cho VPC. <br> - Kiểm tra VPC Resource Map để đảm bảo VPC được tạo đúng và có thể tiếp tục chia subnet cho các lớp hệ thống. | 13/06/2026 | 13/06/2026 |
| 3 | - Tạo các subnet trong VPC theo từng lớp mạng. <br> - Tạo public subnet cho các thành phần cần kết nối Internet. <br> - Tạo private app subnet để đặt Lambda backend, Lambda chatbot và Lambda indexing. <br> - Tạo private database subnet để đặt Amazon RDS PostgreSQL. <br> - Phân bổ subnet theo nhiều Availability Zone để hỗ trợ tính sẵn sàng của hệ thống. | 14/06/2026 | 14/06/2026 |
| 4 | - Tạo và gắn Internet Gateway cho VPC. <br> - Tạo route table cho public subnet và private subnet. <br> - Cấu hình public route table trỏ ra Internet Gateway. <br> - Giữ private app subnet và private database subnet không public trực tiếp ra Internet. <br> - Kiểm tra lại route table để đảm bảo traffic của từng subnet đi đúng theo thiết kế. | 15/06/2026 | 15/06/2026 |
| 5 | - Tạo Security Group cho các lớp ứng dụng và database. <br> - Cấu hình Security Group của RDS chỉ cho phép kết nối PostgreSQL port `5432` từ Security Group của Lambda backend. <br> - Không mở port database cho public internet. <br> - Tạo Security Group cho VPC Endpoint để các Lambda trong private subnet có thể gọi dịch vụ AWS nội bộ. | 16/06/2026 | 16/06/2026 |
| 6 | - Tạo Amazon RDS PostgreSQL làm database chính của hệ thống. <br> - Tạo database tên `pharmacare_ai`. <br> - Đặt RDS trong private database subnet. <br> - Tắt public access cho RDS để database không bị truy cập trực tiếp từ Internet. <br> - Tạo secret trong AWS Secrets Manager để lưu username, password, host, port và thông tin kết nối database. <br> - Tạo VPC Endpoint cho Secrets Manager để Lambda lấy database credential an toàn trong mạng riêng. | 17/06/2026 | 17/06/2026 |
| 7 | - Tạo IAM Role cho Lambda migration. <br> - Tạo Lambda function `pharmacare-db-migration`. <br> - Gắn Lambda migration vào VPC và private app subnet để có thể kết nối RDS. <br> - Cấu hình environment variables gồm `AWS_REGION`, `RDS_SECRET_ARN` và `DB_NAME`. <br> - Tăng timeout cho Lambda vì migration cần chạy SQL tạo nhiều bảng. <br> - Nén code migration thành file ZIP và upload lên Lambda. <br> - Chạy migration để tạo schema database ban đầu cho hệ thống PharmaCare AI. | 18/06/2026 | 18/06/2026 |

### Kết quả đạt được trong tuần 9

* Hoàn thành hạ tầng AWS nền tảng cho hệ thống **PharmaCare AI**.

* Tạo được VPC riêng tên `pharmacare-vpc` tại region `ap-southeast-1`.

* Thiết kế hệ thống mạng thành nhiều lớp rõ ràng:

  * Public subnet
  * Private app subnet
  * Private database subnet
  * RDS DB subnet group
  * OpenSearch VPC subnet cho các thành phần AI/RAG ở giai đoạn sau

* Hiểu rõ vai trò của từng lớp mạng trong kiến trúc:

  * Public subnet phục vụ các thành phần cần giao tiếp Internet.
  * Private app subnet dùng cho Lambda backend, Lambda chatbot và Lambda indexing.
  * Private database subnet dùng cho Amazon RDS PostgreSQL.
  * OpenSearch VPC subnet dùng cho vector store ở phần AI/RAG.

* Tạo và cấu hình Internet Gateway, route table cho VPC.

* Cấu hình Security Group theo nguyên tắc chỉ mở đúng kết nối cần thiết.

* Đảm bảo RDS PostgreSQL không public trực tiếp ra Internet.

* Tạo Amazon RDS PostgreSQL làm database chính của dự án với database name `pharmacare_ai`.

* Sử dụng AWS Secrets Manager để lưu thông tin kết nối database an toàn.

* Tạo VPC Endpoint cho Secrets Manager để Lambda trong private subnet có thể lấy secret mà không cần đi qua public internet.

* Tạo IAM Role và Lambda migration để khởi tạo database schema.

* Cấu hình timeout và environment variables cho Lambda migration.

* Tạo các bảng chính cho hệ thống, bao gồm:

  * `users`
  * `categories`
  * `brands`
  * `products`
  * `stores`
  * `carts`
  * `cart_items`
  * `orders`
  * `order_items`
  * `payments`
  * `prescriptions`
  * `articles`
  * `chatbot_documents`
  * `chat_sessions`
  * `chat_messages`

* Hoàn thành tuần 9 với nền tảng hạ tầng, database private, Secrets Manager và database migration hoạt động ổn định để chuẩn bị triển khai backend API ở tuần 10.