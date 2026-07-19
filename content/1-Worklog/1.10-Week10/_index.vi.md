---
title: "Worklog Tuần 10"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10

* Triển khai lớp backend API cho hệ thống **PharmaCare AI**.
* Tạo AWS Lambda backend sử dụng Node.js 22.x và kết nối đến Amazon RDS PostgreSQL.
* Cấu hình biến môi trường để Lambda lấy thông tin kết nối database từ AWS Secrets Manager.
* Tạo Amazon API Gateway HTTP API để frontend có thể gọi backend.
* Cấu hình các API public cho chức năng xem sản phẩm và dữ liệu cửa hàng.
* Tạo Amazon Cognito User Pool để xử lý xác thực người dùng.
* Tạo nhóm Admin và Customer để phân quyền theo vai trò.
* Cấu hình Cognito JWT Authorizer trong API Gateway để bảo vệ các route cần đăng nhập.
* Triển khai các chức năng nghiệp vụ chính cho customer và admin.
* Tạo S3 bucket và CloudFront distribution cho ảnh sản phẩm.
* Kiểm thử backend API với frontend React trong giai đoạn local development.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | - Tạo AWS Lambda backend tên `pharmacare-backend-api`. <br> - Sử dụng runtime Node.js 22.x cho backend API. <br> - Đặt Lambda trong private application subnet để có thể kết nối đến Amazon RDS PostgreSQL. <br> - Tăng timeout cho Lambda vì backend cần thời gian kết nối RDS và xử lý truy vấn database. | 19/06/2026 | 19/06/2026 |
| 2 | - Chuẩn bị source code backend trên VS Code. <br> - Cài đặt các package Node.js cần thiết như `pg` để kết nối PostgreSQL và AWS SDK để đọc secret. <br> - Thêm các biến môi trường gồm `AWS_REGION`, `RDS_SECRET_ARN` và `DB_NAME`. <br> - Nén source code backend thành file ZIP và upload lên Lambda. | 20/06/2026 | 20/06/2026 |
| 3 | - Tạo Amazon API Gateway HTTP API cho backend. <br> - Tích hợp API Gateway với Lambda `pharmacare-backend-api`. <br> - Cấu hình các route public như `/health`, `/categories`, `/products`, `/products/{id}` và `/stores`. <br> - Kiểm thử route `/health` để xác nhận API Gateway và Lambda đã kết nối thành công. | 21/06/2026 | 21/06/2026 |
| 4 | - Tạo Amazon Cognito User Pool để xử lý xác thực người dùng. <br> - Tạo App Client cho web React. <br> - Tạo hai group chính là `Admin` và `Customer`. <br> - Tạo user mẫu để kiểm thử đăng nhập và phân quyền. <br> - Kiểm tra User Pool ID và Client ID để cấu hình cho frontend. | 22/06/2026 | 22/06/2026 |
| 5 | - Cấu hình CORS trong API Gateway để frontend React có thể gọi backend API. <br> - Tạo Cognito JWT Authorizer trong API Gateway. <br> - Gắn JWT Authorizer vào các route cần bảo vệ. <br> - Bảo vệ các route như `/profile`, `/cart`, `/orders` và `/admin/...` để yêu cầu token hợp lệ từ Cognito. | 23/06/2026 | 23/06/2026 |
| 6 | - Triển khai các chức năng nghiệp vụ cho customer trong backend. <br> - Thêm các API hồ sơ người dùng, giỏ hàng và đơn hàng. <br> - Cấu hình các route như `GET /profile`, `GET /cart`, `POST /cart`, `PUT /cart/{productId}`, `DELETE /cart/{productId}`, `POST /orders`, `GET /orders` và `GET /orders/{id}`. <br> - Kiểm thử đăng nhập bằng customer và gọi API bằng JWT token. | 24/06/2026 | 24/06/2026 |
| 7 | - Triển khai các chức năng admin để quản lý hệ thống nhà thuốc. <br> - Thêm chức năng quản lý sản phẩm, danh mục, user, tồn kho và trạng thái đơn hàng. <br> - Tạo S3 bucket để lưu ảnh sản phẩm và tổ chức ảnh trong thư mục product. <br> - Tạo CloudFront distribution để phân phối ảnh sản phẩm. <br> - Cập nhật `image_url` trong RDS để dữ liệu sản phẩm có thể hiển thị ảnh trên frontend. <br> - Tạo và kiểm thử frontend React local bằng Vite và `react-oidc-context` để kiểm tra đăng nhập, kết nối API, hiển thị sản phẩm, giỏ hàng và đặt hàng. | 25/06/2026 | 25/06/2026 |

### Kết quả đạt được trong tuần 10

* Tạo thành công Lambda backend chính `pharmacare-backend-api`.

* Cấu hình Lambda chạy trong private application subnet và kết nối an toàn đến Amazon RDS PostgreSQL.

* Sử dụng AWS Secrets Manager để lấy thông tin kết nối database thay vì lưu thông tin nhạy cảm trực tiếp trong source code.

* Cấu hình các biến môi trường quan trọng cho backend, gồm:

  * `AWS_REGION`
  * `RDS_SECRET_ARN`
  * `DB_NAME`

* Tạo Amazon API Gateway HTTP API để public các dịch vụ backend.

* Tích hợp API Gateway với AWS Lambda backend.

* Tạo và kiểm thử các route public, bao gồm:

  * `GET /health`
  * `GET /categories`
  * `GET /products`
  * `GET /products/{id}`
  * `GET /stores`

* Tạo Amazon Cognito User Pool để xác thực người dùng.

* Tạo Cognito App Client cho web React.

* Tạo hai nhóm quyền chính trong Cognito:

  * `Admin`
  * `Customer`

* Cấu hình Cognito JWT Authorizer trong API Gateway.

* Bảo vệ các route yêu cầu đăng nhập bằng JWT token từ Cognito.

* Triển khai các API cho customer, bao gồm:

  * Hồ sơ người dùng
  * Giỏ hàng
  * Thêm sản phẩm vào giỏ hàng
  * Cập nhật số lượng sản phẩm trong giỏ hàng
  * Xóa sản phẩm khỏi giỏ hàng
  * Tạo đơn hàng
  * Xem lịch sử đơn hàng
  * Xem chi tiết đơn hàng

* Triển khai các API cho admin, bao gồm:

  * Quản lý sản phẩm
  * Quản lý danh mục
  * Quản lý người dùng
  * Cập nhật tồn kho
  * Quản lý đơn hàng
  * Cập nhật trạng thái đơn hàng
  * Khóa/mở khóa user
  * Cập nhật role user

* Tạo S3 bucket để lưu ảnh sản phẩm.

* Tạo CloudFront distribution để phân phối ảnh sản phẩm hiệu quả hơn.

* Cập nhật dữ liệu `image_url` trong RDS để frontend có thể hiển thị ảnh sản phẩm.

* Tạo frontend React ở môi trường local bằng Vite để kiểm thử xác thực và kết nối backend.

* Kiểm thử được luồng nghiệp vụ cơ bản từ frontend đến API Gateway, Lambda, RDS và Cognito.

* Hoàn thành tuần 10 với backend API hoạt động, hệ thống xác thực người dùng, route được bảo vệ, chức năng customer/admin và cấu hình phân phối ảnh sản phẩm.