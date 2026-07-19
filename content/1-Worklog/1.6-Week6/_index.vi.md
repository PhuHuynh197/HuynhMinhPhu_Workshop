---
title: "Worklog Tuần 6"
date: 2026-05-22
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6

* Hiểu cách cải thiện tính sẵn sàng và khả năng mở rộng của ứng dụng bằng Elastic Load Balancing và Auto Scaling Group.
* Tìm hiểu cách tạo Launch Template, Target Group, Application Load Balancer và Auto Scaling Group.
* Thực hành kiểm thử manual scaling, scheduled scaling, dynamic scaling và đọc metric của predictive scaling.
* Tìm hiểu khái niệm cơ bản về Docker và triển khai ứng dụng dạng container.
* Thực hành triển khai ứng dụng bằng Docker image và Docker Compose.
* Hiểu quy trình cơ bản khi triển khai ứng dụng container trên Amazon ECS.
* Biết cách dọn dẹp tài nguyên compute, container, load balancing và database để tránh phát sinh chi phí không cần thiết.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu tổng quan về triển khai ứng dụng với Auto Scaling Group. <br> - Ôn lại quy trình triển khai ứng dụng cơ bản từ các bài lab EC2 trước đó. <br> - Hiểu lý do sử dụng Auto Scaling Group và Load Balancer để tăng tính sẵn sàng, khả năng chịu lỗi và khả năng mở rộng. | 22/05/2026 | 22/05/2026 | <https://000006.awsstudygroup.com/> |
| 2 | - Chuẩn bị hạ tầng ứng dụng cho Auto Scaling. <br> - Thiết lập network infrastructure, EC2 instance, RDS database và môi trường web server. <br> - Chuẩn bị dữ liệu mẫu cho database và kiểm tra ứng dụng trước khi cấu hình scaling. | 23/05/2026 | 23/05/2026 | <https://000006.awsstudygroup.com/> |
| 3 | - Tạo Launch Template cho EC2 instance. <br> - Tạo Target Group cho ứng dụng. <br> - Cấu hình Application Load Balancer để phân phối traffic đến các application instance. <br> - Kiểm tra truy cập ứng dụng thông qua endpoint của Load Balancer. | 24/05/2026 | 24/05/2026 | <https://000006.awsstudygroup.com/> |
| 4 | - Tạo Auto Scaling Group bằng Launch Template. <br> - Gắn Auto Scaling Group với Target Group và Load Balancer. <br> - Kiểm thử manual scaling và quan sát cách EC2 instance được thêm hoặc giảm. <br> - Tìm hiểu scheduled scaling, dynamic scaling và metric của predictive scaling. | 25/05/2026 | 25/05/2026 | <https://000006.awsstudygroup.com/> |
| 5 | - Tìm hiểu khái niệm cơ bản về Docker và containerization. <br> - Cài đặt các dependency cần thiết để deploy Docker ở môi trường local. <br> - Triển khai và kiểm thử ứng dụng ở môi trường local. <br> - Chuẩn bị VPC, Security Group, IAM role, EC2 và RDS cho việc deploy Docker trên AWS. | 26/05/2026 | 26/05/2026 | <https://000015.awsstudygroup.com/> |
| 6 | - Triển khai ứng dụng bằng Docker image trên EC2. <br> - Triển khai ứng dụng bằng Docker Compose. <br> - Thực hành push Docker image lên Amazon ECR hoặc Docker Hub. <br> - Kiểm tra ứng dụng container thông qua trình duyệt. | 27/05/2026 | 27/05/2026 | <https://000015.awsstudygroup.com/> |
| 7 | - Tìm hiểu quy trình cơ bản khi deploy ứng dụng trên Amazon ECS. <br> - Xem lại ECS Cluster, Task Definition, ECS Service, Cloud Map và Application Load Balancer. <br> - Hiểu sự khác nhau giữa Blue/Green deployment và Rolling deployment. <br> - Dọn dẹp Auto Scaling, Load Balancer, EC2, RDS, Docker, ECS, ECR, NAT Gateway và các tài nguyên liên quan để hạn chế phát sinh chi phí. | 28/05/2026 | 28/05/2026 | <https://000016.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 6

* Hiểu cách Auto Scaling Group giúp duy trì tính sẵn sàng của ứng dụng và tự động điều chỉnh số lượng instance theo nhu cầu.

* Hiểu cách Application Load Balancer phân phối traffic người dùng đến nhiều application instance.

* Thực hành chuẩn bị hạ tầng cho ứng dụng có khả năng mở rộng, bao gồm:

  * VPC
  * EC2 instance
  * RDS database
  * Launch Template
  * Target Group
  * Application Load Balancer
  * Auto Scaling Group

* Hiểu mục đích của các phương pháp scaling khác nhau, bao gồm:

  * Manual scaling
  * Scheduled scaling
  * Dynamic scaling
  * Predictive scaling metrics

* Hiểu mối quan hệ giữa Load Balancer, Target Group và Auto Scaling Group.

* Nắm được khái niệm cơ bản về Docker và lý do container giúp đóng gói ứng dụng cùng các dependency cần thiết.

* Thực hành deploy ứng dụng bằng Docker image.

* Thực hành deploy ứng dụng bằng Docker Compose.

* Biết cách Docker image có thể được lưu trữ và chia sẻ thông qua Amazon ECR hoặc Docker Hub.

* Hiểu các thành phần cơ bản của Amazon ECS, bao gồm:

  * ECS Cluster
  * Task Definition
  * ECS Service
  * Container image
  * Application Load Balancer
  * Cloud Map

* Hiểu sự khác nhau cơ bản giữa Blue/Green deployment và Rolling deployment.

* Nhận biết rằng một số tài nguyên như Load Balancer, NAT Gateway, RDS, ECS và EC2 đang chạy có thể phát sinh chi phí nếu không dọn dẹp.

* Hoàn thành tuần 6 với nền tảng tốt hơn về khả năng mở rộng ứng dụng, triển khai container và quản lý container trên AWS.