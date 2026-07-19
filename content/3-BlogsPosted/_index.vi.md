---
title: "Các bài blogs đã đăng"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Phần này liệt kê và giới thiệu các bài blog em đã đăng trên [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj). Các bài blog này tóm tắt những bài viết AWS và các chủ đề kỹ thuật mà em đã tìm hiểu trong quá trình thực tập.

### [Blog 1 - Session Policies trong Amazon EKS Pod Identity](3.1-Blog1/)

Bài blog này giới thiệu về tính năng Session Policies trong Amazon EKS Pod Identity. Nội dung tập trung vào cách các workload Kubernetes chạy trên Amazon EKS có thể lấy AWS IAM credentials an toàn hơn và cách Session Policies giúp thu hẹp quyền truy cập cho từng pod.

Ý chính của bài viết là Session Policies hỗ trợ thực thi nguyên tắc least privilege bằng cách giới hạn quyền hiệu lực của pod. Thay vì phải tạo nhiều IAM role riêng cho từng workload khác nhau, các nhóm kỹ thuật có thể tái sử dụng một IAM role dùng chung và áp dụng các policy thu hẹp quyền khác nhau tại runtime. Cách tiếp cận này giúp giảm số lượng IAM role cần quản lý, đơn giản hóa việc phân quyền và cải thiện bảo mật trong môi trường Kubernetes quy mô lớn.

### [Blog 2 - Data Masking trong Amazon RDS for Oracle](3.2-Blog2/)

Bài blog này trình bày về Data Masking trong Amazon RDS for Oracle. Nội dung giải thích lý do không nên sử dụng trực tiếp dữ liệu Production cho các môi trường Development, Testing hoặc UAT nếu chưa có biện pháp bảo vệ phù hợp.

Bài viết giới thiệu khái niệm thay thế dữ liệu nhạy cảm thật bằng dữ liệu đã được che giấu nhưng vẫn giữ nguyên định dạng và cấu trúc để phục vụ kiểm thử. Ngoài ra, bài blog cũng mô tả một quy trình có thể kết hợp Amazon RDS for Oracle, Amazon EventBridge Scheduler, AWS Step Functions, AWS Systems Manager, AWS Secrets Manager và thao tác restore snapshot. Thông qua chủ đề này, em hiểu rằng bảo vệ dữ liệu không chỉ dừng lại ở mã hóa và phân quyền, mà còn liên quan đến cách xử lý dữ liệu nhạy cảm khi dữ liệu được sao chép hoặc restore sang môi trường non-production.

### [Blog 3 - Các cập nhật trong hướng dẫn AWS Well-Architected Framework](3.3-Blog3/)

Bài blog này tóm tắt bài viết trên AWS Architecture Blog về các cập nhật trong hướng dẫn AWS Well-Architected Framework. Chủ đề này giúp em hiểu rằng thiết kế kiến trúc cloud không chỉ là lựa chọn từng dịch vụ AWS riêng lẻ, mà còn cần đánh giá toàn bộ hệ thống dựa trên các best practice đã được kiểm chứng.

Bài viết tập trung vào sáu trụ cột của AWS Well-Architected Framework, bao gồm Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization và Sustainability. Nội dung cũng nhấn mạnh rằng việc đánh giá kiến trúc nên là một quá trình liên tục trong suốt vòng đời của workload. Chủ đề này giúp em hiểu rõ hơn cách AWS hướng dẫn kiến trúc sư và kỹ sư cloud thiết kế hệ thống an toàn, đáng tin cậy, hiệu quả, có kiểm soát chi phí và bền vững.