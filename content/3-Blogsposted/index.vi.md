---
title: "Các bài Blog đã đăng"
date: 2026-07-13
weight: 3
chapter: false
pre: " <b> 3. </b> "
---



Phần này liệt kê và giới thiệu các bài blog bạn đã đăng lên [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

###  [Blog 1 - S3 INTELLIGENT-TIERING – KHI KHO LƯU TRỮ "BIẾT" NÓ NÊN NẰM Ở ĐÂU](3.1-Blog1/index.md)
Bài blog này giới thiệu S3 Intelligent-Tiering, một storage class tự động quan sát hành vi truy cập của từng object và đưa nó vào đúng tầng chi phí phù hợp mà không cần can thiệp thủ công. Nó có 3 tầng truy cập hoàn toàn tự động (Frequent Access, Infrequent Access, Archive Instant Access) cùng 2 tầng lưu trữ bổ sung để tiết kiệm sâu hơn, rất phù hợp cho các data lake với nhiều nguồn dữ liệu đa dạng, nơi việc dự đoán mẫu truy cập gần như là bất khả thi.

###  [Blog 2 - CÁCH SAMSUNG ĐẠT ĐƯỢC ĐỊNH GIÁ THỜI GIAN THỰC VỚI AWS LAMBDA RESPONSE STREAMING](3.1-Blog2/_index.md)
Bài blog này giải thích cách Samsung tận dụng AWS Lambda Response Streaming để loại bỏ thách thức về độ trễ trong hệ thống thương mại điện tử toàn cầu của họ. Bằng cách loại bỏ các lớp caching trung gian và truy vấn trực tiếp Pricing Engine theo thời gian thực, họ đã giảm 98% độ trễ P90 (từ 4.500ms xuống còn 50ms) và cắt giảm đáng kể chi phí hạ tầng, từ hơn 100 instance auto-scaled xuống chỉ còn 5–10 Lambda function.

###  [Blog 3 - ĐẢM BẢO CÔNG BẰNG BẰNG CÁCH PHÁT HIỆN VÀ NGĂN CHẶN VIỆC CHỈNH SỬA HỒ SƠ VỚI AMAZON TEXTRACT](3.1-Blog3/index.md)
Bài blog này trình bày một kiến trúc Serverless sử dụng Amazon Textract để tự động phát hiện và làm mờ chữ trong ảnh hồ sơ (profile) game nhằm ngăn chặn hành vi thông đồng và gian lận. Giải pháp xử lý các ảnh được tải lên S3, trích xuất toạ độ chữ bằng Textract, áp dụng Gaussian Blur lên các vùng thông tin nhạy cảm, và gửi cảnh báo qua SNS. Cách tiếp cận này mang lại độ chính xác AI cao, khả năng tự động mở rộng quy mô, và tối ưu chi phí mà không cần quản lý bất kỳ máy chủ nào.