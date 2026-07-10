---
title: 'Worklog Tuần 12'
date: 2026-07-06
weight: 12
chapter: false
pre: ' <b> 1.12. </b> '
---

### Mục tiêu tuần 12:

- Xây dựng hệ thống giám sát tập trung cho toàn bộ kiến trúc.
- Kiểm thử và đánh giá khả năng vận hành của hệ thống Security Operations Center.
- Hoàn thiện tài liệu triển khai và tổng kết kết quả thực hiện dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2 | - Xây dựng Amazon CloudWatch Dashboard phục vụ giám sát tập trung.<br>- Thiết kế Dashboard hiển thị các chỉ số về bảo mật và vận hành của hệ thống. | 06/07/2026 | 06/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| 3 | - Cấu hình Amazon CloudWatch Alarms.<br>- Kiểm thử chức năng gửi cảnh báo qua Amazon SNS bằng Email Notification. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| 4 | - Thực hiện các kịch bản mô phỏng tấn công để đánh giá hệ thống.<br>- Kiểm tra Security Findings trên Amazon GuardDuty và AWS Security Hub. | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/guardduty/ |
| 5 | - Đánh giá hiệu quả của quy trình Detect → Respond → Recover.<br>- Tối ưu IAM Policies theo nguyên tắc Least Privilege nhằm tăng cường bảo mật. | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/iam/ |
| 6 | - Hoàn thiện tài liệu triển khai và hướng dẫn sử dụng hệ thống.<br>- Đánh giá chi phí vận hành và đề xuất các phương án mở rộng trong tương lai. | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/wellarchitected/ |

### Kết quả đạt được tuần 12:

- Hoàn thành việc xây dựng Amazon CloudWatch Dashboard, cung cấp giao diện giám sát tập trung cho toàn bộ hệ thống.
- Dashboard hiển thị đầy đủ các chỉ số quan trọng, bao gồm:
  - GuardDuty Findings
  - Security Hub Findings
  - Lambda Invocations
  - Step Functions Executions
  - EC2 Health
  - WAF Blocked Requests
  - CloudFront Requests
  - ALB Request Count
- Cấu hình thành công Amazon CloudWatch Alarms và xác minh chức năng gửi cảnh báo qua Amazon SNS hoạt động ổn định.
- Thực hiện nhiều kịch bản mô phỏng tấn công để đánh giá khả năng phát hiện, phản ứng và xử lý sự cố của hệ thống.
- Xác nhận quy trình Detect → Respond → Recover vận hành đúng theo thiết kế và đáp ứng yêu cầu đề ra.
- Tối ưu IAM Policies theo nguyên tắc Least Privilege nhằm hạn chế quyền truy cập không cần thiết và nâng cao mức độ an toàn.
- Đánh giá chi phí triển khai hệ thống, đồng thời đề xuất các hướng mở rộng như Multi-AZ, Multi-Account, Infrastructure as Code, Amazon Macie và Amazon Detective.
- Hoàn thiện báo cáo tổng kết, tài liệu triển khai và tài liệu hướng dẫn sử dụng, đảm bảo sẵn sàng cho việc bàn giao và vận hành.
