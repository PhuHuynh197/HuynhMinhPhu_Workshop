---
title: "Worklog Tuần 8"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8

* Bắt đầu dự án cuối kỳ với tên **PharmaCare AI**.
* Phân tích yêu cầu của website nhà thuốc online tích hợp chatbot AI.
* Xác định các module chính, luồng tương tác người dùng, luồng xử lý backend API, lớp database và luồng AI chatbot/RAG.
* Thiết kế kiến trúc AWS cho hệ thống PharmaCare AI.
* Lựa chọn các dịch vụ AWS phù hợp cho frontend, xác thực người dùng, backend API, database, AI chatbot, giám sát, bảo mật và backup.
* Chuẩn bị sơ đồ kiến trúc và nội dung giải thích kỹ thuật cho các phần Proposal, Project và Workshop.

### Kiến trúc PharmaCare AI

Sơ đồ bên dưới thể hiện kiến trúc AWS được đề xuất cho dự án **PharmaCare AI – Website Nhà Thuốc Online & Chatbot AI**.

{{< figure src="/images/proposal/dia1.png" title="AWS Architecture - PharmaCare AI" width="900px" >}}

Hệ thống được thiết kế theo hướng serverless và sử dụng các dịch vụ được quản lý trên AWS. Frontend được lưu trữ trên Amazon S3 và phân phối thông qua Amazon CloudFront. Chức năng xác thực người dùng sử dụng Amazon Cognito. Các API nghiệp vụ được tiếp nhận bởi Amazon API Gateway và xử lý bằng AWS Lambda. Dữ liệu chính của nhà thuốc được lưu trong Amazon RDS Multi-AZ, còn phần chatbot sử dụng Amazon OpenSearch Service làm vector store và Amazon Bedrock để tạo câu trả lời AI.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Bắt đầu dự án cuối kỳ **PharmaCare AI**. <br> - Xác định đề tài: website nhà thuốc online, quản lý thuốc, quản lý đơn hàng và chatbot AI tư vấn khách hàng. <br> - Xác định mục đích chính của hệ thống: hỗ trợ nghiệp vụ nhà thuốc và giúp người dùng tra cứu thông tin thuốc thuận tiện hơn. | 05/06/2026 | 05/06/2026 | Tài liệu yêu cầu dự án |
| 2 | - Phân tích các chức năng chính của website. <br> - Liệt kê các module như quản lý thuốc/sản phẩm, tài khoản người dùng, xem sản phẩm, quản lý đơn hàng, dữ liệu tồn kho và chatbot tư vấn. <br> - Xác định luồng tương tác chính của người dùng từ lúc truy cập website đến khi sử dụng các chức năng hệ thống. | 06/06/2026 | 06/06/2026 | Tài liệu yêu cầu dự án |
| 3 | - Thiết kế lớp frontend của hệ thống. <br> - Chọn Amazon S3 làm static web UI bucket. <br> - Chọn Amazon CloudFront để tăng hiệu năng và độ ổn định khi phân phối website. <br> - Bổ sung AWS WAF ở lớp web public để hỗ trợ bảo vệ hệ thống trước các request bất thường. | 07/06/2026 | 07/06/2026 | <https://000057.awsstudygroup.com/> |
| 4 | - Thiết kế lớp xác thực và API của hệ thống. <br> - Chọn Amazon Cognito để xử lý đăng nhập khách hàng và cấp JWT token. <br> - Chọn Amazon API Gateway làm điểm tiếp nhận API public. <br> - Chọn AWS Lambda Backend API để xử lý nghiệp vụ người dùng, sản phẩm, đơn hàng và dữ liệu nhà thuốc. | 08/06/2026 | 08/06/2026 | <https://000081.awsstudygroup.com/> <br> <https://000055.awsstudygroup.com/> |
| 5 | - Thiết kế lớp database và mạng riêng. <br> - Chọn Amazon RDS Multi-AZ làm cơ sở dữ liệu quan hệ chính để lưu user, thuốc, danh mục, đơn hàng và dữ liệu tồn kho. <br> - Lên kế hoạch đặt RDS trong private DB subnet thuộc Amazon VPC. <br> - Chọn AWS Secrets Manager để lưu credential kết nối database an toàn thay vì ghi trực tiếp trong source code. | 09/06/2026 | 09/06/2026 | <https://000005.awsstudygroup.com/> |
| 6 | - Thiết kế lớp AI Chatbot/RAG. <br> - Chọn Amazon S3 Knowledge Docs để lưu tài liệu nhà thuốc, thông tin thuốc, FAQ và tài liệu nội bộ. <br> - Lên kế hoạch sử dụng AWS Lambda Indexing để xử lý tài liệu và lưu dữ liệu vector vào Amazon OpenSearch Service. <br> - Chọn Amazon Bedrock để tạo câu trả lời chatbot dựa trên dữ liệu truy xuất từ OpenSearch. | 10/06/2026 | 10/06/2026 | Thiết kế kiến trúc dự án |
| 7 | - Hoàn thành phiên bản đầu tiên của sơ đồ kiến trúc AWS. <br> - Bổ sung các dịch vụ giám sát và bảo mật như Amazon CloudWatch, CloudWatch Alarms, Amazon SNS, AWS IAM và AWS Backup. <br> - Rà soát toàn bộ luồng xử lý từ Route 53 đến CloudFront, S3, Cognito, API Gateway, Lambda, RDS, OpenSearch và Bedrock. <br> - Chuẩn bị ghi chú để viết các trang Proposal và Workshop. | 11/06/2026 | 11/06/2026 | Sơ đồ kiến trúc dự án |

### Kết quả đạt được trong tuần 8

* Hoàn thành phân tích yêu cầu ban đầu cho dự án **PharmaCare AI**.

* Xác định dự án là website nhà thuốc online tích hợp chatbot AI theo mô hình RAG.

* Xác định các module chính của hệ thống, bao gồm:

  * Xác thực người dùng
  * Xem thông tin thuốc/sản phẩm
  * Quản lý sản phẩm nhà thuốc
  * Quản lý đơn hàng
  * Quản lý dữ liệu tồn kho
  * Chatbot AI tư vấn
  * Xử lý và indexing tài liệu tri thức
  * Giám sát, cảnh báo và backup

* Thiết kế luồng tương tác người dùng:

  * Người dùng truy cập website thông qua Amazon Route 53.
  * Amazon CloudFront phân phối nội dung frontend từ Amazon S3.
  * AWS WAF hỗ trợ bảo vệ lớp web public.
  * Người dùng đăng nhập thông qua Amazon Cognito.
  * Cognito cấp JWT token để frontend gọi các API được bảo vệ.

* Thiết kế luồng xử lý backend API:

  * Frontend gửi request đến Amazon API Gateway.
  * API Gateway chuyển request đến AWS Lambda Backend API.
  * Lambda xử lý các nghiệp vụ như user, sản phẩm, đơn hàng và dữ liệu nhà thuốc.
  * Lambda lấy credential database từ AWS Secrets Manager.
  * Lambda kết nối đến Amazon RDS để đọc và ghi dữ liệu quan hệ.

* Thiết kế lớp database và VPC data layer:

  * Amazon RDS được sử dụng làm database chính của nhà thuốc.
  * RDS lưu user, thuốc, danh mục, đơn hàng và dữ liệu tồn kho.
  * RDS được đặt trong private DB subnet thuộc Amazon VPC.
  * Mô hình Multi-AZ được sử dụng để tăng tính sẵn sàng cho database.

* Thiết kế luồng AI Chatbot/RAG:

  * Người dùng gửi câu hỏi chatbot từ giao diện website.
  * AWS Lambda Chatbot Handler xử lý request chatbot.
  * Lambda truy xuất dữ liệu liên quan từ Amazon OpenSearch Service.
  * Amazon Bedrock tạo câu trả lời dựa trên ngữ cảnh được truy xuất.
  * Chatbot hỗ trợ tra cứu thông tin thuốc, tài liệu nhà thuốc và FAQ, không thay thế tư vấn y tế chuyên môn.

* Thiết kế luồng Knowledge Indexing Pipeline:

  * Tài liệu tri thức nhà thuốc được lưu trong Amazon S3 Knowledge Docs.
  * AWS Lambda Indexing xử lý tài liệu mới.
  * Dữ liệu sau xử lý được lưu vào Amazon OpenSearch Service dưới dạng vector.
  * OpenSearch hỗ trợ tìm kiếm ngữ nghĩa cho chatbot.

* Bổ sung các thành phần giám sát, cảnh báo và quản trị bảo mật:

  * Amazon CloudWatch để thu thập logs và metrics
  * CloudWatch Alarms để cảnh báo khi chỉ số vượt ngưỡng
  * Amazon SNS để gửi thông báo
  * AWS IAM để phân quyền theo nguyên tắc đặc quyền tối thiểu
  * AWS Backup để quản lý sao lưu dữ liệu

* Hoàn thành tuần 8 với sơ đồ kiến trúc AWS rõ ràng và định hướng kỹ thuật phù hợp để triển khai hệ thống PharmaCare AI trong các tuần tiếp theo.