---
title: "Worklog Tuần 8"
date: 2026-06-22
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 8:

- Vẽ structure/architecture của project trong 2 ngày.
- Hoàn thiện sơ đồ kiến trúc cho proposal và workshop.
- Thực hành các nội dung chính trong workshop.
- Bắt đầu chỉnh sửa nội dung workshop thành file báo cáo rõ ràng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | **Vẽ structure của project - ngày 1** <br>&emsp; + Xác định các lớp kiến trúc: Frontend/Auth, Storage, Backend/AI-ML, Monitoring/Security <br>&emsp; + Phác thảo luồng xử lý từ upload ảnh đến lưu kết quả <br>&emsp; + Chọn dịch vụ AWS phù hợp cho từng lớp | 22/06/2026 | 22/06/2026 | [Proposal](/Content/2.%20Proposal/_proposal.md) |
| 3 | **Vẽ structure của project - ngày 2** <br>&emsp; + Hoàn thiện diagram kiến trúc <br>&emsp; + Kiểm tra lại luồng S3 -> SQS -> Lambda -> Rekognition/Textract -> DynamoDB <br>&emsp; + Bổ sung CloudWatch và IAM vào sơ đồ | 23/06/2026 | 23/06/2026 | [DiagramStructure](/Content/2.%20Proposal/image/DiagramStructure.png) |
| 4 | **Thực hành nội dung workshop** <br>&emsp; + Chuẩn bị IAM Role cho Lambda <br>&emsp; + Tạo SQS queue nhận sự kiện xử lý ảnh <br>&emsp; + Cấu hình S3 bucket và event notification | 24/06/2026 | 24/06/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |
| 5 | **Chỉnh sửa báo cáo workshop** <br>&emsp; + Rà soát phần overview, IAM, SQS, S3 <br>&emsp; + Chuẩn hóa mô tả từng bước thực hành <br>&emsp; + Bổ sung hình ảnh minh họa và kết quả kiểm tra | 25/06/2026 | 25/06/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |

### Kết quả đạt được tuần 8

**Architecture Design:**

- Hoàn thiện cấu trúc tổng quan của project:
  <br> + Frontend/Auth dùng Amplify, Cognito, API Gateway
  <br> + Storage dùng Amazon S3
  <br> + Backend xử lý bằng SQS và Lambda
  <br> + AI/ML dùng Rekognition và Textract
  <br> + Data layer dùng DynamoDB
  <br> + Monitoring/Security dùng CloudWatch và IAM

**Workshop Practice:**

- Thực hành các bước nền tảng của workshop:
  <br> + Tạo IAM Role
  <br> + Tạo SQS queue
  <br> + Cấu hình S3
  <br> + Chuẩn bị Lambda function

- Bắt đầu chuyển nội dung thực hành thành báo cáo workshop có cấu trúc rõ ràng.
