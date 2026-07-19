---
title: "Worklog Tuần 11"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11

* Triển khai chức năng AI chatbot cho hệ thống **PharmaCare AI** theo kiến trúc RAG.
* Chuẩn bị kho tri thức nội bộ của nhà thuốc để chatbot có thể truy xuất thông tin.
* Tạo Amazon S3 bucket để lưu tài liệu tri thức.
* Cấu hình Amazon Bedrock để tạo embedding và tạo câu trả lời AI.
* Tạo Amazon OpenSearch Serverless collection làm vector store.
* Cấu hình VPC Endpoint, Security Group và IAM Role cho các Lambda AI.
* Tạo Lambda Indexing để xử lý tài liệu và lưu vector vào OpenSearch.
* Tạo Lambda Chatbot để nhận câu hỏi người dùng và trả lời dựa trên kho tri thức nội bộ.
* Tích hợp chatbot API với API Gateway và frontend.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| --- | --- | --- | --- |
| 1 | - Bắt đầu triển khai lớp AI/RAG cho hệ thống **PharmaCare AI**. <br> - Rà soát lại luồng chatbot trong sơ đồ kiến trúc. <br> - Chuẩn bị tài liệu tri thức nhà thuốc ở định dạng `.txt`. <br> - Phân loại dữ liệu tri thức thành các nhóm như sản phẩm, FAQ, hướng dẫn y tế, bài viết sức khỏe, thông tin an toàn và index. | 26/06/2026 | 26/06/2026 |
| 2 | - Tạo Amazon S3 bucket `pharmacare-knowledge-docs-phu-2026`. <br> - Tạo prefix `knowledge/` để lưu tài liệu tri thức nội bộ. <br> - Upload các file tri thức lên S3. <br> - Kiểm tra lại dữ liệu trong S3 để chuẩn bị cho quá trình indexing. | 27/06/2026 | 27/06/2026 |
| 3 | - Cấu hình quyền truy cập model trong Amazon Bedrock. <br> - Sử dụng `cohere.embed-multilingual-v3` để tạo vector embedding cho nội dung tiếng Việt và tiếng Anh. <br> - Chuẩn bị Amazon Nova Micro làm LLM model để tạo câu trả lời tự nhiên khi bật chế độ LLM. <br> - Xem lại embedding dimension và luồng tạo câu trả lời của chatbot. | 28/06/2026 | 28/06/2026 |
| 4 | - Tạo Security Group cho các Lambda AI. <br> - Cấu hình VPC Endpoint cho các workload AI chạy trong private subnet. <br> - Tạo S3 Gateway Endpoint để Lambda đọc tài liệu tri thức từ S3. <br> - Tạo Bedrock Runtime VPC Endpoint để Lambda gọi model embedding và LLM qua mạng riêng. <br> - Tạo OpenSearch Serverless VPC Endpoint để Lambda truy cập vector store an toàn. | 29/06/2026 | 29/06/2026 |
| 5 | - Tạo Amazon OpenSearch Serverless collection tên `pharmacare-rag-vector-store`. <br> - Cấu hình collection loại Vector Search. <br> - Cấu hình network policy để OpenSearch được truy cập riêng thông qua VPC Endpoint. <br> - Cấu hình data access policy để IAM Role của Lambda AI có quyền tạo index, ghi tài liệu và truy vấn vector. | 30/06/2026 | 30/06/2026 |
| 6 | - Tạo IAM Role `pharmacare-rag-lambda-role` cho các Lambda AI. <br> - Cấp quyền ghi log vào CloudWatch, chạy trong VPC, đọc S3, gọi Bedrock Runtime và truy cập OpenSearch Serverless. <br> - Tạo Lambda function `pharmacare-rag-indexing`. <br> - Cấu hình environment variables cho S3 bucket, knowledge prefix, embedding model, OpenSearch endpoint, index name và AWS region. <br> - Chạy Lambda Indexing để xử lý tài liệu tri thức từ S3. | 01/07/2026 | 01/07/2026 |
| 7 | - Tạo Lambda function `pharmacare-rag-chatbot`. <br> - Cấu hình logic chatbot để nhận câu hỏi, tạo embedding cho câu hỏi, truy vấn OpenSearch Vector Store và tạo câu trả lời từ ngữ cảnh tìm được. <br> - Thêm biến môi trường `ENABLE_LLM` để hỗ trợ cả chế độ trả lời bằng LLM và chế độ RAG search-only. <br> - Tạo route API Gateway `POST /chat`. <br> - Tích hợp API chatbot với component chatbot ở frontend. <br> - Kiểm thử chatbot với các câu hỏi về thông tin thuốc, gợi ý nhóm sản phẩm, chính sách nhà thuốc và FAQ. | 02/07/2026 | 02/07/2026 |

### Kết quả đạt được trong tuần 11

* Hoàn thành lớp AI/RAG cho hệ thống **PharmaCare AI**.

* Tạo S3 bucket `pharmacare-knowledge-docs-phu-2026` để lưu tài liệu tri thức nội bộ.

* Tổ chức tài liệu tri thức dưới prefix `knowledge/`, bao gồm:

  * `products`
  * `faq`
  * `medical-guides`
  * `health-articles`
  * `safety`
  * `indexes`

* Chuẩn bị khoảng 250 file tri thức cho chatbot.

* Trong đó có khoảng 193 file liên quan đến sản phẩm thuốc và sản phẩm chăm sóc sức khỏe.

* Cấu hình Amazon Bedrock để xử lý tác vụ AI.

* Sử dụng `cohere.embed-multilingual-v3` để tạo vector embedding.

* Chuẩn bị Amazon Nova Micro làm LLM model để tạo câu trả lời tự nhiên khi `ENABLE_LLM=true`.

* Tạo OpenSearch Serverless collection `pharmacare-rag-vector-store` làm vector store.

* Cấu hình OpenSearch Serverless theo loại Vector Search.

* Cấu hình truy cập mạng riêng cho lớp AI bằng:

  * S3 Gateway Endpoint
  * Bedrock Runtime VPC Endpoint
  * OpenSearch Serverless VPC Endpoint

* Tạo IAM Role `pharmacare-rag-lambda-role` cho các Lambda AI.

* Cấp quyền theo nguyên tắc tối thiểu để Lambda có thể:

  * Ghi log vào CloudWatch
  * Chạy trong VPC
  * Đọc tài liệu tri thức từ S3
  * Gọi Bedrock Runtime
  * Truy cập OpenSearch Serverless

* Tạo Lambda Indexing để xử lý tài liệu tri thức.

* Lambda Indexing thực hiện được các chức năng:

  * Đọc file `.txt` từ S3
  * Chia nhỏ nội dung tài liệu thành các chunk
  * Tạo embedding bằng Amazon Bedrock
  * Ghi dữ liệu vector vào OpenSearch Serverless

* Index thành công 250 file và tạo 1186 chunks trong OpenSearch Vector Store.

* Tạo Lambda Chatbot để xử lý câu hỏi người dùng.

* Lambda Chatbot thực hiện được các chức năng:

  * Nhận câu hỏi từ người dùng
  * Tạo embedding cho câu hỏi
  * Tìm kiếm tài liệu liên quan trong OpenSearch
  * Trả lời dựa trên tài liệu nội bộ của nhà thuốc

* Bổ sung chế độ `ENABLE_LLM=false` để giảm tiêu thụ token khi quota Bedrock LLM bị giới hạn.

* Tạo route API Gateway `POST /chat` cho request chatbot.

* Tích hợp chatbot vào giao diện frontend.

* Kiểm thử chatbot với các câu hỏi liên quan đến thuốc, gợi ý sản phẩm khi bị sốt, gợi ý sản phẩm khi tiêu chảy, FAQ và chính sách nhà thuốc.

* Hoàn thành tuần 11 với pipeline AI/RAG hoạt động, kết nối đầy đủ S3, Bedrock, OpenSearch Serverless, Lambda, API Gateway và frontend.