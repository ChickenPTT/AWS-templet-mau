---
title: "Worklog Tuần 9"
date: 2026-06-29
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 9:

- Tiếp tục thực hành các nội dung còn lại trong workshop.
- Hoàn thiện file báo cáo workshop từ các bước thực hành.
- Kiểm tra lại luồng xử lý, hình ảnh minh họa và nội dung cleanup.
- Rà soát tính nhất quán giữa proposal, diagram và workshop.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | **Thực hành Lambda function** <br>&emsp; + Tạo Lambda function xử lý message từ SQS <br>&emsp; + Cấu hình permission cần thiết <br>&emsp; + Kiểm tra log trên CloudWatch | 29/06/2026 | 29/06/2026 | [Lambda Workshop](/Content/5.%20Workshop/5.CreateAndCode-LambdaFunction/lambda.md) |
| 3 | **Testing và validation** <br>&emsp; + Upload ảnh vào S3 để tạo event <br>&emsp; + Kiểm tra message đi qua SQS <br>&emsp; + Theo dõi Lambda xử lý và ghi log | 30/06/2026 | 30/06/2026 | [Testing](/Content/5.%20Workshop/6.Testing-Validation/testing.md) |
| 4 | **Chỉnh sửa báo cáo workshop** <br>&emsp; + Rà soát văn phong từng phần <br>&emsp; + Bổ sung ảnh minh họa còn thiếu <br>&emsp; + Kiểm tra đường dẫn ảnh và tiêu đề | 01/07/2026 | 01/07/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |
| 5 | **Hoàn thiện cleanup và tổng kết** <br>&emsp; + Ghi lại các bước xóa tài nguyên để tránh phát sinh chi phí <br>&emsp; + Kiểm tra lại toàn bộ báo cáo workshop <br>&emsp; + Đối chiếu nội dung với proposal | 02/07/2026 | 02/07/2026 | [Cleanup](/Content/5.%20Workshop/7.CleanUp/cleanup.md) |

### Kết quả đạt được tuần 9

**Workshop Completion:**

- Hoàn thành các phần thực hành chính:
  <br> + IAM Role preparation
  <br> + SQS queue creation
  <br> + S3 event configuration
  <br> + Lambda function implementation
  <br> + Testing and validation
  <br> + Cleanup resources

- Hoàn thiện file báo cáo workshop:
  <br> + Nội dung có thứ tự theo từng bước
  <br> + Có hình ảnh minh họa
  <br> + Có phần kiểm thử và dọn dẹp tài nguyên

**Project Alignment:**

- Đảm bảo workshop bám sát kiến trúc proposal.
- Làm rõ vai trò của từng dịch vụ trong pipeline xử lý ảnh serverless.
