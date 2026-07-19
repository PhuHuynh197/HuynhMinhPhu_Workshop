---
title: "Worklog Tuần 2"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2

* Hiểu mục đích của dịch vụ AWS Identity and Access Management (IAM).
* Tìm hiểu cách quản lý quyền truy cập bằng IAM User, Group, Policy và Role.
* Thực hành tạo IAM Group và IAM User với quyền phù hợp.
* Hiểu cách sử dụng IAM Role và Switch Role để cấp quyền truy cập tạm thời, có kiểm soát.
* Biết cách dọn dẹp tài nguyên IAM sau khi hoàn thành bài thực hành.

### Các công việc cần thực hiện trong tuần

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 1 | - Tìm hiểu tổng quan về AWS Identity and Access Management. <br> - Hiểu lý do IAM quan trọng trong việc bảo mật tài khoản và tài nguyên AWS. <br> - Ghi chú các khái niệm về xác thực, phân quyền và nguyên tắc cấp quyền tối thiểu. | 24/04/2026 | 24/04/2026 | <https://000002.awsstudygroup.com/> |
| 2 | - Tìm hiểu IAM User và IAM Group. <br> - Hiểu cách Group hỗ trợ quản lý quyền cho nhiều User. <br> - Thực hành tạo Admin Group và gán quyền phù hợp. | 25/04/2026 | 25/04/2026 | <https://000002.awsstudygroup.com/> |
| 3 | - Tạo IAM Admin User. <br> - Thêm User vào Admin Group. <br> - Thực hành đăng nhập bằng IAM User thay vì sử dụng tài khoản root. <br> - So sánh sự khác nhau giữa root user và IAM user. | 26/04/2026 | 26/04/2026 | <https://000002.awsstudygroup.com/> |
| 4 | - Tìm hiểu IAM Policy. <br> - Học cách Policy xác định các hành động được phép hoặc bị từ chối. <br> - Tìm hiểu cấu trúc cơ bản của Policy gồm Effect, Action, Resource và Condition. <br> - Áp dụng quyền cho User và Group. | 27/04/2026 | 27/04/2026 | <https://000002.awsstudygroup.com/> |
| 5 | - Tìm hiểu IAM Role. <br> - Tạo Admin Role để cấp quyền truy cập tạm thời. <br> - Tạo OperatorUser và chuẩn bị cấu hình quyền để thực hiện Switch Role. <br> - Hiểu lý do sử dụng Role an toàn hơn so với chia sẻ thông tin đăng nhập dài hạn. | 28/04/2026 | 28/04/2026 | <https://000002.awsstudygroup.com/> |
| 6 | - Thực hành Switch Role trên AWS Console. <br> - Cho phép OperatorUser chuyển sang Admin Role. <br> - Kiểm tra quyền truy cập sau khi chuyển Role. <br> - Xác nhận quyền thay đổi theo Role đã chọn. | 29/04/2026 | 29/04/2026 | <https://000002.awsstudygroup.com/> |
| 7 | - Ôn lại các best practice của IAM. <br> - Kiểm tra các IAM User, Group, Policy và Role đã tạo. <br> - Dọn dẹp tài nguyên IAM sau khi hoàn thành bài lab. <br> - Tổng kết vai trò của IAM trong việc bảo mật các dự án AWS. | 30/04/2026 | 30/04/2026 | <https://000002.awsstudygroup.com/> |

### Kết quả đạt được trong tuần 2

* Hiểu được vai trò của AWS IAM trong việc quản lý truy cập an toàn đến các dịch vụ và tài nguyên AWS.

* Phân biệt được các thành phần chính trong IAM, bao gồm:

  * Root user
  * IAM user
  * IAM group
  * IAM policy
  * IAM role

* Thực hành tạo IAM Group và IAM User để quản lý quyền truy cập.

* Hiểu cách IAM Policy được sử dụng để kiểm soát quyền thông qua các tài liệu chính sách.

* Nắm được cấu trúc cơ bản của một IAM Policy, bao gồm:

  * Effect
  * Action
  * Resource
  * Condition

* Thực hành sử dụng IAM Role và Switch Role để cấp quyền truy cập tạm thời.

* Hiểu nguyên tắc cấp quyền tối thiểu, tức là mỗi User chỉ nên được cấp đúng quyền cần thiết cho công việc.

* Hiểu lý do không nên sử dụng tài khoản root cho các thao tác hằng ngày.

* Biết tầm quan trọng của việc dọn dẹp tài nguyên IAM sau khi thực hành để giữ môi trường AWS an toàn và gọn gàng.

* Hoàn thành tuần 2 với nền tảng tốt hơn về quản lý định danh và kiểm soát quyền truy cập trên AWS.