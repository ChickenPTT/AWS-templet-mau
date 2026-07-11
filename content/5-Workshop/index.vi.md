---
title: "Workshop"
date: 2026-07-11
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Giải pháp tự động hóa giám sát chất lượng hàng hóa dựa trên Serverless và AI/ML

#### Tổng quan

Workshop này hướng dẫn xây dựng hệ thống tự động hóa giám sát chất lượng hàng hóa dựa trên kiến trúc Serverless và Trí tuệ nhân tạo (AI/ML) trên AWS. Hệ thống cho phép nhân viên giao hàng hoặc khách hàng chụp ảnh kiện hàng gặp sự cố như rách, vỡ, móp méo hoặc hư hỏng, sau đó tải trực tiếp hình ảnh lên hệ thống để được phân tích tự động.

Hệ thống sử dụng Amazon Rekognition để phân tích hình ảnh hàng hóa và nhận diện dấu hiệu hư hỏng, Amazon Textract để trích xuất thông tin vận đơn, lưu trữ bằng chứng và gửi cảnh báo cho bộ phận liên quan. Nhờ đó, quy trình xử lý sự cố có thể được rút ngắn từ vài giờ hoặc vài ngày xuống còn vài giây.

#### Nội dung

1. [Tổng quan Workshop](1.WorkShop-overview/index.md)
2. [Chuẩn bị IAM Role](2.IAM-Role-Prepare/index.md)
3. [Tạo Chat Queue với AWS SQS](3.Create-Chat-Queue(AWS-SQS)/index.md)
4. [Cấu hình S3 và Event Notification](4.Congif-Save-And-Event(AWS-S3)/index.md)
5. [Tạo và Code Lambda Function](5.CreateAndCode-LambdaFunction/index.md)
6. [Testing và Validation](6.Testing-Validation/index.md)
7. [Dọn dẹp tài nguyên](7.CleanUp/index.md)