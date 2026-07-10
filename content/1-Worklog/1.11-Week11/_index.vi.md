---
title: 'Worklog Tuần 11'
date: 2026-06-29
weight: 11
chapter: false
pre: ' <b> 1.11. </b> '
---

### Mục tiêu tuần 11:

- Hoàn thiện quy trình phản ứng sự cố tự động trên nền tảng AWS.
- Tích hợp các dịch vụ serverless thành một quy trình xử lý thống nhất và liền mạch.
- Kiểm thử khả năng phản ứng của hệ thống đối với nhiều loại Security Findings khác nhau.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------------------------------- |
| 2 | - Hoàn thiện quy trình điều phối bằng AWS Step Functions.<br>- Thiết lập kết nối giữa Amazon EventBridge và AWS Step Functions để kích hoạt quy trình phản ứng tự động. | 29/06/2026 | 29/06/2026 | https://docs.aws.amazon.com/step-functions/ |
| 3 | - Phát triển Lambda Function thực hiện cô lập EC2 bằng Isolation Security Group.<br>- Kiểm thử và xác minh quy trình cô lập EC2 sau khi phát hiện sự cố. | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/ec2/ |
| 4 | - Phát triển Lambda Function tự động vô hiệu hóa IAM Access Key.<br>- Chặn quyền đăng nhập AWS Management Console của IAM User khi phát hiện Credential Compromise. | 01/07/2026 | 01/07/2026 | https://docs.aws.amazon.com/iam/ |
| 5 | - Lưu trữ lịch sử xử lý sự cố trên Amazon S3.<br>- Ghi nhận log thực thi của toàn bộ quy trình trên Amazon CloudWatch Logs. | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/s3/ |
| 6 | - Kiểm thử toàn bộ quy trình Detect → Respond bằng GuardDuty Sample Findings và Security Hub Findings nhằm đánh giá khả năng vận hành của hệ thống. | 03/07/2026 | 03/07/2026 | https://docs.aws.amazon.com/guardduty/ |

### Kết quả đạt được tuần 11:

- Hoàn thiện quy trình phản ứng sự cố tự động bằng AWS Step Functions, đảm bảo khả năng điều phối các bước xử lý theo đúng kịch bản.
- Cấu hình Amazon EventBridge tự động kích hoạt AWS Step Functions ngay khi AWS Security Hub phát sinh Security Findings.
- Xây dựng thành công Lambda Function tự động cô lập EC2 thông qua Isolation Security Group nhằm hạn chế nguy cơ lây lan của sự cố.
- Hoàn thiện chức năng tự động vô hiệu hóa IAM Access Key và chặn quyền đăng nhập AWS Management Console của IAM User khi phát hiện dấu hiệu lộ thông tin xác thực.
- Lưu trữ toàn bộ lịch sử xử lý sự cố trên Amazon S3, hỗ trợ công tác kiểm toán và điều tra sau sự cố.
- Ghi nhận đầy đủ log thực thi của Lambda Functions và AWS Step Functions trên Amazon CloudWatch Logs để phục vụ giám sát và theo dõi hệ thống.
- Kiểm thử thành công toàn bộ quy trình phản ứng tự động theo luồng: Security Hub → EventBridge → Step Functions → Lambda → SNS, đảm bảo các thành phần hoạt động đồng bộ và ổn định.
