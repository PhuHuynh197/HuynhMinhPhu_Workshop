---
title: "Worklog Tuần 12"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12

* Deploy frontend React của hệ thống **PharmaCare AI** lên AWS.
* Lưu trữ frontend production bằng Amazon S3.
* Tạo Amazon CloudFront distribution để public website cho người dùng truy cập.
* Cấu hình CloudFront để hỗ trợ route của React Single Page Application.
* Cập nhật Cognito callback URL và sign-out URL cho domain CloudFront production.
* Cập nhật API Gateway CORS để frontend production có thể gọi backend API.
* Cấu hình CloudWatch Logs, CloudWatch Alarms và Amazon SNS để giám sát và cảnh báo.
* Cấu hình AWS Backup cho Amazon RDS.
* Gắn AWS WAF vào CloudFront để tăng cường bảo vệ lớp web public.
* Rà soát quyền IAM theo nguyên tắc đặc quyền tối thiểu.
* Kiểm thử hệ thống lần cuối và hoàn thiện tài liệu báo cáo/workshop.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | - Bắt đầu giai đoạn deploy cuối cùng cho hệ thống **PharmaCare AI**. <br> - Rà soát lại backend API, Cognito authentication, RDS database và AI chatbot đã hoàn thành ở các tuần trước. <br> - Build frontend React bằng lệnh `npm run build`. <br> - Kiểm tra thư mục `dist` được tạo thành công với `index.html`, `assets/`, `favicon.svg` và các file frontend liên quan. | 03/07/2026 | 03/07/2026 |
| 2 | - Tạo Amazon S3 bucket `pharmacare-frontend-web-phu-2026` để lưu frontend production. <br> - Upload toàn bộ file trong thư mục React `dist` lên S3 bucket. <br> - Giữ S3 bucket ở chế độ private thay vì public trực tiếp. <br> - Kiểm tra lại các file build frontend đã được lưu đúng trong S3. | 04/07/2026 | 04/07/2026 |
| 3 | - Tạo CloudFront distribution tên `pharmacare-frontend-distribution`. <br> - Cấu hình origin của CloudFront trỏ đến S3 frontend bucket. <br> - Sử dụng private origin access để CloudFront truy cập S3 an toàn hơn. <br> - Cấu hình default root object là `index.html`. <br> - Cấu hình custom error response `403 → /index.html → 200` và `404 → /index.html → 200` để hỗ trợ route của React SPA. | 05/07/2026 | 05/07/2026 |
| 4 | - Kiểm thử website production thông qua domain CloudFront. <br> - Xác nhận website truy cập được tại `https://d3tm5364zrtmpq.cloudfront.net/`. <br> - Cập nhật Cognito Allowed callback URLs và Allowed sign-out URLs để thêm domain CloudFront. <br> - Cập nhật API Gateway CORS để cho phép request từ frontend CloudFront. <br> - Cập nhật cấu hình môi trường frontend từ localhost sang domain CloudFront production. <br> - Build lại frontend, upload bản build mới lên S3 và tạo CloudFront invalidation `/*`. | 06/07/2026 | 06/07/2026 |
| 5 | - Cấu hình Amazon CloudWatch Logs để giám sát hệ thống. <br> - Kiểm tra log group của Lambda backend, Lambda chatbot, Lambda indexing và các dịch vụ AWS liên quan. <br> - Tạo Amazon SNS topic để gửi cảnh báo hệ thống. <br> - Đăng ký email nhận thông báo từ SNS topic. <br> - Kiểm tra luồng giám sát và thông báo để chuẩn bị kết nối với CloudWatch Alarm. | 07/07/2026 | 07/07/2026 |
| 6 | - Tạo CloudWatch Alarms cho các metric và điều kiện lỗi quan trọng. <br> - Kết nối CloudWatch Alarms với SNS notification topic. <br> - Cấu hình AWS Backup plan cho Amazon RDS để bảo vệ dữ liệu database. <br> - Tạo backup resource assignment cho RDS database. <br> - Rà soát cấu hình backup để đảm bảo hệ thống có khả năng hỗ trợ khôi phục dữ liệu. | 08/07/2026 | 08/07/2026 |
| 7 | - Gắn AWS WAF vào CloudFront để tăng cường bảo vệ website public. <br> - Rà soát IAM roles và policies của Lambda backend, Lambda migration, Lambda chatbot và Lambda indexing. <br> - Áp dụng nguyên tắc least privilege để mỗi Lambda chỉ có đúng quyền cần thiết cho nhiệm vụ của nó. <br> - Kiểm thử lần cuối các chức năng đăng nhập, xem sản phẩm, giỏ hàng, đặt hàng, quản trị và chatbot. <br> - Hoàn thiện ảnh minh chứng workshop, nội dung worklog và báo cáo thực tập cuối kỳ. | 09/07/2026 | 09/07/2026 |

### Kết quả đạt được trong tuần 12

* Build thành công frontend React để chuẩn bị deploy production.

* Tạo Amazon S3 bucket `pharmacare-frontend-web-phu-2026` để lưu các file build frontend.

* Upload thư mục React `dist` lên Amazon S3.

* Giữ S3 frontend bucket ở chế độ private và sử dụng CloudFront để public website an toàn hơn.

* Tạo CloudFront distribution `pharmacare-frontend-distribution` cho website production.

* Cấu hình CloudFront với:

  * S3 frontend bucket làm origin
  * Default root object `index.html`
  * Custom error response `403 → /index.html → 200`
  * Custom error response `404 → /index.html → 200`
  * CloudFront invalidation `/*` sau khi upload bản build mới

* Deploy thành công website tại:

  * `https://d3tm5364zrtmpq.cloudfront.net/`

* Cập nhật cấu hình Amazon Cognito để hỗ trợ frontend production.

* Cập nhật Cognito Allowed callback URLs và Allowed sign-out URLs với domain CloudFront.

* Cập nhật API Gateway CORS để frontend production có thể gọi backend API.

* Cập nhật biến môi trường frontend từ môi trường local sang môi trường production.

* Kiểm tra frontend React kết nối được với:

  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda backend
  * Dữ liệu Amazon RDS thông qua backend API
  * API chatbot AI

* Cấu hình Amazon CloudWatch Logs để theo dõi backend, chatbot, indexing và hoạt động hệ thống.

* Tạo Amazon SNS topic để gửi thông báo cảnh báo hệ thống.

* Tạo CloudWatch Alarms và kết nối với SNS notification.

* Cấu hình AWS Backup plan cho Amazon RDS.

* Tạo backup resource assignment cho RDS database.

* Gắn AWS WAF vào CloudFront để tăng cường bảo vệ lớp web public.

* Rà soát quyền IAM của các Lambda function trong dự án.

* Áp dụng phân quyền theo nguyên tắc least privilege cho các role dùng bởi:

  * Lambda backend
  * Lambda migration
  * Lambda indexing
  * Lambda chatbot

* Kiểm thử cuối cùng các luồng chức năng chính của hệ thống:

  * Đăng nhập/đăng xuất người dùng
  * Xem danh sách sản phẩm
  * Xem chi tiết sản phẩm
  * Quản lý giỏ hàng
  * Tạo đơn hàng
  * Xem lịch sử đơn hàng
  * Admin quản lý sản phẩm
  * Admin quản lý đơn hàng
  * Admin quản lý người dùng
  * Chatbot AI trả lời câu hỏi

* Hoàn thành cấu hình deploy và vận hành cuối cùng của hệ thống **PharmaCare AI**.

* Hoàn thành tuần 12 với một hệ thống nhà thuốc online triển khai trên AWS, có frontend production, backend API, xác thực người dùng, database, chatbot AI, monitoring, backup và bảo mật cơ bản.