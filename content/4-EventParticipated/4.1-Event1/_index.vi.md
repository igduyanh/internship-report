---
title: "Event 3"
date: 2026-06-13
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch “FCAJ Meetup (13/06/2026)”

### Mục Đích Của Sự Kiện

- Cung cấp góc nhìn thực tế, trần trụi về công việc của các Kỹ sư (DevOps, Data Analytics) tại các doanh nghiệp và tập đoàn đa quốc gia (MNC), qua đó xóa bỏ những lầm tưởng phổ biến của sinh viên.
- Đi sâu vào văn hóa doanh nghiệp, các tiêu chuẩn làm việc toàn cầu, và định hướng lộ trình phát triển sự nghiệp bền vững—từ bước đệm đầu tiên vào nghề cho đến khi trở thành chuyên gia.
- Truyền cảm hứng và hướng dẫn cách tận dụng bệ phóng từ các cộng đồng công nghệ (như AWS) để thăng tiến và lan tỏa giá trị.

### Danh Sách Diễn Giả

- **Anh Trọng H. Trương** (DevOps Engineer @ Endava Việt Nam): “What does a DevOps Engineer really do?”
- **Anh Đạt Phạm** (Data Analytics Engineer) & **Anh Cường Nguyễn** (Process Engineer): “Câu chuyện thực tế đến văn hóa tại tập đoàn đa quốc gia”
- **Anh Danh Hoàng Hiếu Nghị** (AI Engineer): “From First Cloud AI Journey to AWS Partner”
- **Đinh Trung Kiên & Nguyễn Minh Thọ**: “A scalable URL shortening service on AWS”

### Nội Dung Nổi Bật

Sự kiện bao gồm 4 phần trình bày mang tính "thực chiến" cao:

#### 1) Đinh Trung Kiên & Nguyễn Minh Thọ — A scalable URL shortening service on AWS

- **Mục đích**: Giải quyết bài toán System Design kinh điển là xây dựng một dịch vụ rút gọn URL có khả năng mở rộng tốt, bảo mật cao và tối ưu độ trễ (thay vì chỉ làm một bản MVP đơn giản).
- **Rủi ro của kiến trúc "Cơ bản"**: Mô hình truyền thống (Frontend → Backend → Database) gặp nhiều vấn đề như điểm nghẽn cục bộ (SPOF), khó mở rộng, độ trễ đọc cao và dễ bị tấn công do thiếu lớp bảo mật ở mạng biên.
- **Kiến trúc hệ thống thực tế trên AWS**:
  - **Lớp Bảo vệ & Phân phối (Edge Layer)**: Sử dụng Amazon CloudFront kết hợp AWS WAF để chặn truy cập độc hại và phân phối nội dung tĩnh từ Amplify.
  - **Lớp Ứng dụng (App Layer)**: Backend được container hóa chạy trên Amazon ECS (Fargate), sử dụng ALB để điều phối traffic vào Private Subnet.
- **Cơ chế Sinh Key Độc lập (KGS)**: Tối ưu hóa hiệu suất bằng cách dùng một service chạy ngầm để tạo sẵn các đoạn mã ngắn và đẩy vào hàng đợi Redis (lệnh LPUSH), thay vì sinh mã on-demand (khi có request mới tạo).
- **Luồng Ghi (Create Flow)**: Backend chỉ cần lấy mã đã có sẵn từ Redis (lệnh RPOP), gắn với URL gốc và ghi thẳng vào DynamoDB, triệt tiêu hoàn toàn độ trễ sinh mã.
- **Luồng Đọc (Cache-aside)**: Hệ thống tìm kiếm trong Amazon ElastiCache for Redis trước. Nếu không có (Cache miss), hệ thống mới gọi DynamoDB để lấy dữ liệu, sau đó cập nhật lại vào Cache, giúp giảm tải tối đa cho database.

#### 2) Trọng H. Trương — What does a DevOps Engineer really do?

- **Lầm tưởng vs. Thực tế**: Nhiều người lầm tưởng DevOps chỉ là viết CI/CD pipeline, gõ lệnh Docker/K8s, hay "chữa cháy" server lúc nửa đêm. Thực tế, phạm vi công việc xoay quanh hệ thống nhiều hơn: trực on-call, xử lý sự cố (incident handling), quản lý phân quyền, điều tra chi phí và làm rõ quyền sở hữu vấn đề (ownership clarification).
- **Học gì trước tiên**: Đừng chạy theo công cụ (tool) vì chúng sẽ luôn thay đổi. Hãy nắm thật vững nền tảng (Fundamentals): Linux, Networking, Git, Containers và một ngôn ngữ lập trình (Python/Golang).
- **Bài học "xương máu"**: Copy lệnh trên mạng không có nghĩa là bạn hiểu nó. Hãy luôn hỏi "Tại sao" trước khi hỏi "Làm thế nào". Giao tiếp là kỹ năng cốt lõi của DevOps. Có thể dùng AI để nâng cao kỹ năng, nhưng đừng để AI làm "tắt" tư duy của chính mình.

#### 3) Đạt Phạm & Cường Nguyễn — Câu chuyện thực tế & Văn hóa MNC

- **Kỹ năng sống còn**: Để tồn tại và phát triển ở MNC, ngoài kỹ năng cứng, bạn bắt buộc phải trang bị Tư duy phản biện, Kỹ năng giao tiếp, Giải quyết vấn đề và đặc biệt là "Kể chuyện với dữ liệu" (Data Storytelling).
- **Mô hình 5 cấp độ sự nghiệp**: Follower (Thực thi) → Learner (Học hỏi chủ động) → Problem Solver (Tự giải quyết trọn vẹn) → System Thinker (Nhìn bức tranh toàn cảnh, tối ưu dài hạn) → Super Star (Định hướng chiến lược và dẫn dắt).
- **Giải mã Văn hóa Doanh nghiệp**: Tại các MNC công nghệ, văn hóa "No-Blame Post-Mortem" rất được đề cao: khi có lỗi, đội ngũ sẽ tập trung tìm nguyên nhân gốc rễ để sửa hệ thống chứ không chỉ trích cá nhân.
- **Triết lý "Đúng Việc"**: Dựa trên 3 trụ cột: Làm Người (quản trị nội tâm), Làm Nghề (phụng sự bằng chuyên môn) và Làm Dân (trách nhiệm với quốc gia, tạo di sản công nghệ).

#### 4) Danh Hoàng Hiếu Nghị — From First Cloud AI Journey to AWS Partner

- **Lộ trình 8 bước**: Bắt đầu từ sự tò mò của sinh viên (Student Curiosity) → Tìm đúng môi trường (First Cloud AI Journey) → Học qua thực hành (Hands-on Labs) → Thể hiện năng lực (Portfolio) → Trở thành AWS Partner → Lan tỏa lại giá trị cho cộng đồng (Share Back).
- **Sức mạnh cộng đồng**: Có được việc làm mới chỉ là khởi đầu. Dấn thân vào cộng đồng (như AWS Student Builder Group, AWS Community Builder) mang lại một mạng lưới quan hệ (network) tuyệt vời và những hỗ trợ thiết thực: voucher thi chứng chỉ, AWS Credits, và quà tặng (swags).

### Những Gì Học Được

- **Nhận thức rõ ràng**: Công cụ thay đổi liên tục, chỉ có nền tảng vững chắc (Fundamentals) và tư duy hệ thống (System Thinking) mới giúp người kỹ sư đi được đường dài.
- **Bước đệm vào MNC**: Cần chuyển đổi tư duy từ việc chỉ "Làm được việc" sang "Làm đúng chuẩn mực", kết hợp với tinh thần "No-Blame" để liên tục cải tiến bản thân và hệ thống.
- **Tầm quan trọng của đóng góp**: Chuyên môn kỹ thuật khi được kết hợp với sự hỗ trợ từ cộng đồng công nghệ sẽ tạo ra một bệ phóng cực kỳ mạnh mẽ cho lộ trình sự nghiệp.
- **Tối ưu kiến trúc (System Design)**: Nắm bắt được tư duy Separation of Concerns (tách biệt luồng Đọc/Ghi), Defense at the Edge (bảo vệ ở mạng biên) và chiến lược Pre-computation over On-demand (tính toán trước để tối ưu độ trễ).

### Ứng Dụng Vào Công Việc

- **Tự học & Thực hành**: Từ bỏ thói quen copy-paste lệnh máy móc. Khi sử dụng AI để hỗ trợ viết script hay cấu hình, phải tự ép bản thân phân tích và hiểu rõ mục đích của từng dòng lệnh.
- **Nâng cấp tư duy đồ án**: Áp dụng mindset "System Thinker" vào các dự án thực tập thay vì chỉ làm một "Follower". Không chỉ code cho chạy, mà phải tính toán đến việc tối ưu hiệu suất, lường trước rủi ro và rèn luyện kỹ năng báo cáo tiến độ rõ ràng.
- **Phát triển thương hiệu cá nhân**: Lên kế hoạch tham gia tích cực vào AWS Student Builder Group nhằm tích lũy dự án cho Portfolio và định hướng xây dựng cộng đồng trong tương lai.
- **Áp dụng Cache-aside Pattern**: Sử dụng Redis vào các dự án cá nhân hoặc đồ án để tối ưu hóa tốc độ phản hồi cho các API có tần suất đọc dữ liệu cao.
- **Decouple tác vụ nặng**: Học cách tách biệt các tác vụ nặng (heavy tasks) ra khỏi luồng xử lý chính bằng các worker chạy ngầm, chuẩn bị sẵn dữ liệu để luồng chính hoạt động mượt mà hơn.

#### Một số hình ảnh khi tham gia sự kiện
