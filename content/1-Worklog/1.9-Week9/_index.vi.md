```markdown
---
title: 'Worklog Tuần 9'
date: 2026-06-15
weight: 9
chapter: false
pre: ' <b> 1.9. </b> '
---

### Mục tiêu tuần 9:

- Xây dựng môi trường giám sát bảo mật cơ bản trên AWS.
- Cấu hình các dịch vụ ghi log, giám sát và phát hiện mối đe dọa nhằm theo dõi hoạt động của hệ thống.

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | ------------ | --------------- | --------------- |
| 2 | - Tạo tài khoản AWS và kích hoạt xác thực đa yếu tố (MFA) cho Root User.<br>- Tạo IAM User với quyền `AdministratorAccess` để sử dụng cho các tác vụ quản trị hằng ngày. | 15/06/2026 | 15/06/2026 | https://docs.aws.amazon.com/iam/ |
| 3 | - Kích hoạt AWS CloudTrail để ghi nhận toàn bộ API Calls trong tài khoản.<br>- Cấu hình VPC Flow Logs và chuyển log đến Amazon CloudWatch Logs. | 16/06/2026 | 16/06/2026 | https://docs.aws.amazon.com/cloudtrail/ |
| 4 | - Bật AWS Config để theo dõi các thay đổi cấu hình của tài nguyên.<br>- Thiết lập AWS Budgets và tạo cảnh báo chi phí theo tháng. | 17/06/2026 | 17/06/2026 | https://docs.aws.amazon.com/config/ |
| 5 | - Kích hoạt Amazon GuardDuty tại khu vực `ap-southeast-1`.<br>- Bật AWS Security Hub với tiêu chuẩn bảo mật NIST 800-53.<br>- Tích hợp các GuardDuty Findings vào AWS Security Hub. | 18/06/2026 | 18/06/2026 | https://docs.aws.amazon.com/securityhub/ |
| 6 | - Kích hoạt IAM Access Analyzer.<br>- Tạo CloudWatch Alarm để giám sát các sự kiện đăng nhập thất bại và việc sử dụng Root User.<br>- Sinh GuardDuty Sample Findings và kiểm tra các cảnh báo trên AWS Security Hub. | 19/06/2026 | 19/06/2026 | https://docs.aws.amazon.com/guardduty/ |

### Kết quả đạt được tuần 9:

- Hoàn thành việc thiết lập các biện pháp bảo mật IAM cơ bản bằng cách kích hoạt MFA cho Root User và sử dụng IAM User có quyền quản trị cho các tác vụ hằng ngày.
- Kích hoạt AWS CloudTrail để ghi nhận toàn bộ API Calls phát sinh trong tài khoản AWS.
- Cấu hình VPC Flow Logs nhằm thu thập nhật ký lưu lượng mạng và gửi dữ liệu đến Amazon CloudWatch Logs.
- Bật AWS Config để theo dõi và ghi nhận các thay đổi cấu hình của tài nguyên AWS.
- Thiết lập AWS Budgets cùng cảnh báo chi phí hằng tháng nhằm hỗ trợ kiểm soát ngân sách sử dụng dịch vụ.
- Kích hoạt Amazon GuardDuty để phát hiện các hoạt động bất thường và các mối đe dọa bảo mật tiềm ẩn.
- Cấu hình AWS Security Hub và tích hợp các GuardDuty Findings vào hệ thống quản lý bảo mật tập trung.
- Thiết lập IAM Access Analyzer để phát hiện các tài nguyên được chia sẻ ra ngoài tài khoản AWS.
- Tạo CloudWatch Alarm nhằm giám sát các sự kiện quan trọng như đăng nhập thất bại và việc sử dụng Root User.
- Sinh GuardDuty Sample Findings và xác nhận các cảnh báo được hiển thị chính xác trên AWS Security Hub.
```
