---
title: "Chuẩn bị IAM Role cho Lambda"
date: 2026-06-21
weight: 2
chapter: false
pre: ""
---

# Bước 1: Chuẩn bị IAM Role cho Lambda

### Giới thiệu

IAM Role là quyền mà Lambda sử dụng để truy cập các dịch vụ AWS cần thiết trong workshop như Amazon S3, Amazon SQS, Amazon Rekognition và Amazon Textract.

Trong bước này, bạn sẽ tạo một IAM Role cho Lambda và gắn các policy cần thiết để Lambda có thể đọc dữ liệu, nhận message và ghi log trong quá trình xử lý ảnh.

---

### Các bước thực hiện

1. Truy cập **AWS Console**, tìm dịch vụ **IAM**.

![Tìm dịch vụ IAM](/images/5-Workshop/5.2-Prerequisite/image1.png)

2. Chọn **Roles**, sau đó chọn **Create role**.

![Chọn Roles và Create role](/images/5-Workshop/5.2-Prerequisite/image2.png)

3. Ở phần **Trusted entity type**, chọn **AWS service**.

4. Ở phần **Use case**, chọn **Lambda**, sau đó chọn **Next**.

![Chọn AWS service và Lambda](/images/5-Workshop/5.2-Prerequisite/image3.png)

5. Tìm và gắn lần lượt các policy cần thiết cho Lambda.

![Tìm policy cho Lambda](/images/5-Workshop/5.2-Prerequisite/image4.png)

![Chọn policy cho Lambda](/images/5-Workshop/5.2-Prerequisite/image5.png)

![Gắn policy AWSLambdaBasicExecutionRole](/images/5-Workshop/5.2-Prerequisite/image6.png)

![Gắn policy AmazonS3ReadOnlyAccess](/images/5-Workshop/5.2-Prerequisite/image7.png)

![Gắn policy AmazonSQSFullAccess](/images/5-Workshop/5.2-Prerequisite/image8.png)

![Gắn policy Rekognition và Textract](/images/5-Workshop/5.2-Prerequisite/image9.png)

6. Đặt tên role là **Lambda-ImageProcessing-Role**, sau đó chọn **Create role**.

![Đặt tên IAM Role](/images/5-Workshop/5.2-Prerequisite/image10.png)

![Tạo IAM Role](/images/5-Workshop/5.2-Prerequisite/image11.png)

---

### Lưu ý bảo mật

Trong môi trường thực tế, thay vì dùng policy có sẵn của AWS, bạn nên tự viết **Custom Policy** để giới hạn quyền chỉ trên đúng bucket hoặc queue cụ thể.

Đây là best practice bảo mật theo nguyên tắc **Least Privilege**, tức là chỉ cấp đúng quyền cần thiết và không cấp dư quyền.

![Custom policy theo nguyên tắc Least Privilege](/images/5-Workshop/5.2-Prerequisite/image12.png)
