---
title: "Sự kiện 1"
date: 2026-06-06
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Báo cáo sự kiện: AWS Community Day

### Thông tin sự kiện

* **Tên sự kiện:** AWS Community Day
* **Thời gian:** 09:00, ngày 06/06/2026
* **Địa điểm:** Tầng 26, Bitexco Financial Tower
* **Vai trò tham gia:** Người tham dự

### Mục tiêu sự kiện

* Tìm hiểu kinh nghiệm triển khai thực tế về AWS Cloud.
* Hiểu sự khác nhau giữa Virtual Machines, Containers và Serverless architecture.
* Tìm hiểu các thách thức thực tế khi triển khai hệ thống cloud-native.
* Biết cách AWS WAF và Machine Learning có thể hỗ trợ phát hiện tấn công mạng.
* Nhận định hướng nghề nghiệp từ các anh/chị đang làm trong lĩnh vực cloud, system administration, DevOps và cybersecurity.

### Mô tả sự kiện

AWS Community Day là một sự kiện công nghệ tập trung vào cloud computing, kiến trúc hệ thống hiện đại, cybersecurity, artificial intelligence và định hướng nghề nghiệp trong ngành công nghệ thông tin.

Sự kiện mang lại nhiều kiến thức thực tế từ các diễn giả đã có kinh nghiệm làm việc với AWS và hệ thống doanh nghiệp. Nội dung không chỉ dừng ở lý thuyết mà còn đề cập đến các vấn đề vận hành, tư duy bảo mật, thiết kế hệ thống và bài học nghề nghiệp.

Đối với em, sự kiện này rất hữu ích vì nhiều nội dung có liên quan trực tiếp đến dự án thực tập **PharmaCare AI**, đặc biệt là AWS Lambda, API Gateway, CloudFront, WAF, monitoring, serverless architecture và bảo mật có ứng dụng AI.

### Diễn giả và nội dung chính

| Thời gian | Diễn giả | Nội dung chính |
| --- | --- | --- |
| 09:20 - 10:00 | Nguyễn Quốc Bảo | Kiến trúc AWS Cloud và kinh nghiệm triển khai thực tế |
| 10:00 - 10:35 | Nguyễn Huỳnh Quốc Bảo | Virtual Machines, Containers và mô hình triển khai hệ thống |
| 10:35 - 10:50 | Việt Phát | Serverless architecture và các thách thức khi triển khai |
| 10:50 - 11:10 | Lê Hoàng Gia Đại | AWS WAF và Machine Learning trong phát hiện tấn công mạng |
| 11:10 - 12:00 | Trần Trung Vinh | Hành trình từ Sysadmin đến DevOps và kinh nghiệm phỏng vấn |

### Nội dung nổi bật

#### 1. So sánh Virtual Machines và Containers

Một nội dung quan trọng trong sự kiện là phần so sánh giữa Virtual Machines và Containers.

Virtual Machines thường chạy một hệ điều hành riêng trên hypervisor. Cách này giúp tăng tính cô lập nhưng tiêu tốn nhiều CPU, RAM và storage hơn. Trong khi đó, Containers như Docker chia sẻ kernel của hệ điều hành host và chỉ đóng gói ứng dụng cùng các thư viện cần thiết.

Vì vậy, container nhẹ hơn, khởi động nhanh hơn và phù hợp hơn với các hệ thống triển khai hiện đại. Nội dung này giúp em hiểu vì sao nhiều hệ thống thực tế sử dụng container hoặc serverless thay vì chỉ dùng máy chủ ảo truyền thống.

#### 2. Thách thức khi triển khai Serverless

Sự kiện cũng đề cập đến các thách thức thực tế khi sử dụng serverless như AWS Lambda và DynamoDB.

Mặc dù AWS Lambda giúp giảm công việc quản lý server, nhưng Lambda có tính stateless. Điều này có nghĩa là trạng thái của ứng dụng cần được lưu ở các dịch vụ bên ngoài như database. Nếu truy vấn database không được tối ưu, các thao tác như quét toàn bộ bảng có thể trở nên chậm và tốn chi phí khi hệ thống mở rộng.

Bài học này rất hữu ích cho dự án PharmaCare AI vì backend của em cũng sử dụng AWS Lambda. Nó giúp em hiểu rằng Lambda function cần được thiết kế gọn, truy vấn database phải tối ưu và nên tránh xử lý dư thừa.

#### 3. AWS WAF và Machine Learning trong bảo mật

Một phần gây ấn tượng khác là chủ đề kết hợp AWS WAF với Machine Learning để phát hiện tấn công mạng.

Các rule WAF truyền thống thường dựa trên những mẫu tấn công đã biết. Tuy nhiên, các kiểu tấn công hiện đại có thể bao gồm zero-day hoặc hành vi bất thường không khớp với chữ ký có sẵn. Machine Learning có thể hỗ trợ phân tích hành vi traffic và nhận diện các mẫu nghi ngờ.

Với ngành An toàn thông tin của em, nội dung này rất phù hợp. Nó cho thấy AI không chỉ dùng cho chatbot mà còn có thể ứng dụng trong giám sát bảo mật và phòng thủ mạng.

#### 4. Hành trình từ Sysadmin đến DevOps

Phần chia sẻ nghề nghiệp giúp em hiểu rõ hơn về lộ trình phát triển từ Helpdesk hoặc Sysadmin lên DevOps Engineer.

Diễn giả nhấn mạnh rằng kỹ sư cloud không chỉ cần kiến thức kỹ thuật mà còn cần tư duy vận hành, kỹ năng tự động hóa, giám sát hệ thống, xử lý sự cố và giao tiếp với các nhóm khác.

Điều này giúp em có định hướng rõ hơn để tiếp tục phát triển kỹ năng sau kỳ thực tập.

### Kiến thức rút ra

* Cloud computing không chỉ là sử dụng dịch vụ AWS mà còn là tư duy thiết kế hệ thống.
* Virtual Machines, Containers và Serverless đều có ưu điểm và giới hạn riêng.
* Serverless system cần thiết kế kỹ về quản lý trạng thái, hiệu năng database và kiểm soát chi phí.
* AWS WAF có thể kết hợp với Machine Learning để phát hiện hành vi mạng bất thường.
* DevOps tập trung vào automation, monitoring, reliability và cải tiến liên tục.
* Một kỹ sư cloud hoặc security cần kết hợp kiến thức kỹ thuật và trải nghiệm vận hành thực tế.

### Ứng dụng vào dự án thực tập

Kiến thức từ sự kiện này có thể áp dụng trực tiếp vào dự án **PharmaCare AI** của em.

Thứ nhất, phần serverless architecture giúp em hiểu cách thiết kế AWS Lambda cẩn thận hơn. Trong PharmaCare AI, Lambda được dùng làm backend API, vì vậy logic API cần gọn, bảo mật và tối ưu.

Thứ hai, chủ đề AWS WAF giúp em hiểu lý do nên gắn WAF vào CloudFront để bảo vệ lớp website public khỏi các request bất thường.

Thứ ba, tư duy vận hành từ sự kiện giúp em hoàn thiện phần monitoring và security của dự án. Em áp dụng bằng cách cấu hình CloudWatch Logs, CloudWatch Alarms, SNS notification, AWS Backup và IAM least privilege.

Cuối cùng, phần chia sẻ nghề nghiệp giúp em có thêm động lực tiếp tục học AWS, Linux, networking, automation, DevOps và cybersecurity.

### Cảm nhận cá nhân

Sự kiện này giúp em có góc nhìn thực tế hơn về AWS và bảo mật cloud. Thay vì chỉ học qua tài liệu hoặc lab, em được nghe các kinh nghiệm thật từ những anh/chị đã làm việc với hệ thống doanh nghiệp.

Nội dung gây ấn tượng nhất với em là việc kết hợp AWS WAF và Machine Learning để phát hiện tấn công. Vì em học ngành An toàn thông tin, chủ đề này giúp em thấy rõ sự kết nối giữa cloud computing, AI và cybersecurity.

Sự kiện cũng giúp em hiểu rằng xây dựng hệ thống cloud không chỉ là làm cho ứng dụng chạy được. Một hệ thống thực tế còn cần monitoring, backup, security, cost control và quy trình vận hành rõ ràng.

### Hình ảnh sự kiện

***(Kiến trúc cloud và thách thức serverless)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/images/events/event1/anh4.jpg" style="width: 35%; margin: 0;" alt="Thách thức khi triển khai serverless">
  <img src="/images/events/event1/anh5.jpg" style="width: 35%; margin: 0;" alt="Chia sẻ kiến trúc AWS">
</div>

***(Virtual Machines và Containers)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/images/events/event1/anh6.jpg" style="width: 35%; margin: 0;" alt="So sánh Virtual Machines và Containers">
  <img src="/images/events/event1/anh7.jpg" style="width: 35%; margin: 0;" alt="Chi tiết khác nhau giữa VM và Container">
</div>

***(AWS WAF và Machine Learning trong bảo mật)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/images/events/event1/anh9.jpg" style="width: 35%; margin: 0;" alt="AWS WAF và Machine Learning">
  <img src="/images/events/event1/anh10.jpg" style="width: 35%; margin: 0;" alt="Phát hiện tấn công mạng bằng WAF và ML">
</div>

***(Định hướng nghề nghiệp và chia sẻ kinh nghiệm thực tế)***

<div style="display: flex; flex-direction: row; justify-content: center; gap: 2%; margin-bottom: 15px;">
  <img src="/images/events/event1/anh12.jpg" style="width: 35%; margin: 0;" alt="Hành trình nghề nghiệp từ Sysadmin đến DevOps">
</div>

> Tóm lại, AWS Community Day giúp em kết nối kiến thức học ở trường với thực tế triển khai cloud. Sự kiện giúp em hiểu rõ hơn về kiến trúc AWS, serverless system, cloud security, AI-based security monitoring và định hướng nghề nghiệp trong ngành công nghệ thông tin.