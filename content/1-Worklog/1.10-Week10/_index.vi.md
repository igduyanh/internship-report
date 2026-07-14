---
title: 'Worklog Tuần 10'
date: 2026-06-22
weight: 10
chapter: false
pre: ' <b> 1.10. </b> '
---

### Mục tiêu tuần 10:

- Xây dựng hệ thống phản ứng sự cố tự động dựa trên các dịch vụ serverless của AWS.
- Phát triển các AWS Lambda Functions để xử lý cảnh báo bảo mật và tự động thực hiện các hành động khắc phục.
- Tích hợp Amazon EventBridge nhằm kích hoạt quy trình phản ứng sự cố một cách tự động.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | ------------ | --------------- | --------------- |
| 2 | - Tạo Amazon SNS Topic phục vụ việc gửi cảnh báo bảo mật.<br>- Đăng ký địa chỉ email nhận thông báo. | 22/06/2026 | 22/06/2026 | https://docs.aws.amazon.com/sns/ |
| 3 | - Phát triển AWS Lambda Function đầu tiên để xử lý GuardDuty Findings.<br>- Phân tích mức độ nghiêm trọng của sự kiện và gửi cảnh báo thông qua Amazon SNS. | 23/06/2026 | 23/06/2026 | https://docs.aws.amazon.com/lambda/ |
| 4 | - Phát triển AWS Lambda Function thứ hai để tự động chặn các địa chỉ IP đáng ngờ bằng cách cập nhật Security Group của Amazon EC2. | 24/06/2026 | 24/06/2026 | https://docs.aws.amazon.com/ec2/ |
| 5 | - Tạo Amazon EventBridge Rule để kích hoạt Lambda khi GuardDuty phát hiện cảnh báo mức High.<br>- Kiểm thử toàn bộ quy trình từ GuardDuty đến email cảnh báo. | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/eventbridge/ |
| 6 | - Phát triển AWS Lambda Function thứ ba để tự động thu hồi IAM Access Key bị lộ.<br>- Thiết kế quy trình phản ứng sự cố nhiều bước bằng AWS Step Functions. | 26/06/2026 | 26/06/2026 | https://docs.aws.amazon.com/step-functions/ |

### Kết quả đạt được tuần 10:

- Hoàn thành cấu hình Amazon SNS để gửi cảnh báo bảo mật qua email.
- Phát triển các AWS Lambda Functions sử dụng Python 3.12 nhằm tự động xử lý GuardDuty Findings.
- Xây dựng chức năng tự động gửi email cảnh báo dựa trên mức độ nghiêm trọng của các sự kiện bảo mật.
- Hoàn thiện chức năng tự động cập nhật Security Group của Amazon EC2 để chặn các địa chỉ IP đáng ngờ.
- Cấu hình Amazon EventBridge để tự động kích hoạt AWS Lambda khi GuardDuty phát hiện các mối đe dọa ở mức High.
- Kiểm thử thành công toàn bộ quy trình phản ứng sự cố, bao gồm:
  - GuardDuty Sample Finding
  - Amazon EventBridge Rule
  - AWS Lambda
  - Amazon SNS Email Notification
- Triển khai chức năng tự động thu hồi IAM Access Key khi GuardDuty phát hiện thông tin xác thực bị lộ.
- Thiết kế workflow bằng AWS Step Functions để điều phối quy trình xử lý sự cố nhiều bước.
- Áp dụng các thực hành bảo mật theo khuyến nghị của AWS, bao gồm:
  - Sử dụng IAM Roles thay cho việc lưu trữ Access Keys trong mã nguồn.
  - Ghi nhật ký thực thi vào Amazon CloudWatch Logs.
