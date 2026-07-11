---
title: "Worklog Tuần 2"
date: 2026-05-04
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 2:

- Nắm vững kiến thức nền tảng về Amazon EC2 và các tính năng cơ bản như Instance types, AMI, Snapshots
- Thực hành triển khai ứng dụng Node.js trên EC2 instances chạy Amazon Linux và Windows
- Hiểu rõ cách quản lý quyền truy cập và giới hạn tài nguyên sử dụng bằng AWS IAM
- Làm quen với AWS Cloud9 IDE để phát triển ứng dụng trực tiếp trên cloud
- Thành thạo việc hosting static website trên Amazon S3 với các tính năng nâng cao
- Tối ưu hóa hiệu suất website bằng CloudFront CDN
- Quản lý phiên bản object và thực hiện sao chép dữ liệu giữa các regions trên S3

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                   |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------- |
| 2   | **Thực hành lab: Bắt đầu và triển khai ứng dụng trên Amazon Compute Cloud (Amazon EC2)** <br>&emsp; + Giới thiệu về AWS (Amazon Elastic Compute Cloud) - EC2 <br>&emsp;&emsp; • Instance type <br>&emsp;&emsp; • AMI/BackUp/Keypair <br>&emsp; + Các bước chuẩn bị: <br>&emsp;&emsp; • Tạo VPC Linux/Window <br>&emsp;&emsp; • Security group Linux/Window <br>&emsp; + Khởi tạo Window/Linux instance <br>&emsp; + EC2 cơ bản: <br>&emsp;&emsp; • Thay đổi cấu hình EC2 <br>&emsp;&emsp; • Tạo snapshot <br>&emsp;&emsp; • Custom AMI <br>&emsp;&emsp; • Tạo instance từ Custom AMI <br>&emsp;&emsp; • Truy cập EC2 khi mất keypair Linux và Window <br>&emsp;&emsp; • Cấu hình giao diện desktop cho EC2-ubuntu 22.04 <br>&emsp;&emsp; • Amazon EBS Snapshot archive                                                                                                                                                                                                                                                                                                                                                                                                                                             | 11/05/2026   | 12/05/2026      | <https://000004.awsstudygroup.com/vi/5-amazonec2basic/>                                                          |
| 3   | **Tiếp tục hoàn thành bài thực hành lab EC2** <br>&emsp; + Triển khai app Node.js trên Amazon Linux: <br>&emsp;&emsp; • Download LAMP web server <br>&emsp;&emsp; • Chuẩn bị LAMP <br>&emsp;&emsp; • Cấu hình và cài đặt phpMyAdmin <br>&emsp;&emsp; • Cài đặt Node.js trên Linux <br>&emsp;&emsp; • Triển khai app trên Linux instance <br>&emsp; + Triển khai app Node.js trên Amazon Window: <br>&emsp;&emsp; • Cài XAMPP trên Window instance <br>&emsp;&emsp; • Cài Node.js trên Window instance <br>&emsp;&emsp; • Triển khai trên Window instance <br>&emsp; + Giới hạn tài nguyên sử dụng bằng service IAM <br>&emsp;&emsp; • Cho sử dụng theo Region cụ thể <br>&emsp;&emsp; • Giới hạn EC2 theo instance family <br>&emsp;&emsp; • Giới hạn EC2 theo instance type <br>&emsp;&emsp; • Giới hạn EBS volume <br>&emsp;&emsp; • Giới hạn quyền xóa tài nguyên <br>&emsp;&emsp; • Giới hạn xóa tài nguyên theo khoảng thời gian <br> **Thực hành lab: Cấp quyền cho ứng dụng truy cập dịch vụ AWS với IAM Role** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Tạo S3 bucket <br>&emsp; + Sử dụng access key: Tạo IAM user, access key, dùng access key <br>&emsp; + Tạo IAM role <br>&emsp; + Sử dụng IAM role | 12/05/2026   | 12/05/2026      | <https://000048.awsstudygroup.com/vi/3-iamroleec2/> <br> <https://000004.awsstudygroup.com/vi/5-amazonec2basic/> |
| 4   | **Thực hành lab: Sử dụng Cloud IDE trên trình duyệt với AWS Cloud9** <br>&emsp; + Tổng quan về AWS Cloud9 <br>&emsp; + Tạo Cloud9 instance <br>&emsp; + Tính năng cơ bản: <br>&emsp;&emsp; • Dùng command line <br>&emsp;&emsp; • Làm việc với file text <br>&emsp;&emsp; • Giao diện dashboard <br>&emsp; + Dùng AWS CLI <br> **Thực hành lab: Hosting static website với Amazon S3** <br>&emsp; + Giới thiệu tổng quan lý thuyết <br>&emsp; + Tạo S3 bucket <br>&emsp; + Tải dữ liệu <br>&emsp; + Bật tính năng static website <br>&emsp; + Cấu hình Block Public Access <br>&emsp; + Cấu hình public object <br>&emsp; + Kiểm tra Website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 13/05/2026   | 14/05/2026      | <https://000057.awsstudygroup.com/vi/1-introduce/> <br> <https://000049.awsstudygroup.com/vi/>                   |
| 5   | **Thực hành lab: Hosting static website với Amazon S3 (tiếp tục)** <br>&emsp; + Tăng tốc static website với CloudFront <br>&emsp; + Chặn truy cập công cộng vào S3 <br>&emsp; + Cấu hình Amazon CloudFront <br>&emsp; + Kiểm tra Amazon CloudFront <br>&emsp; + Bucket versioning: <br>&emsp;&emsp; • Giới thiệu <br>&emsp;&emsp; • Cách thực hoạt động <br>&emsp;&emsp; • Hướng dẫn thực hiện <br>&emsp; + Di chuyển Object <br>&emsp; + Sao chép S3 Object sang region khác                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | 14/05/2026   | 14/05/2026      | <https://000057.awsstudygroup.com/vi/1-introduce/>                                                               |

### Kết quả đạt được tuần 2

**EC2 Core Knowledge:**

- Nắm vững các khái niệm về EC2:
  <br> + Instance types
  <br> + AMI, Backup, Keypair
  <br> + Security Groups và VPC cấu hình
  <br> + Snapshots và Custom AMI
  <br> + Xử lý mất keypair cho cả Linux và Windows
  <br> + Desktop GUI setup cho EC2-ubuntu 22.04
  <br> + Amazon EBS Snapshot archive

- Triển khai ứng dụng Node.js:
  <br> + LAMP stack setup trên Amazon Linux
  <br> + phpMyAdmin cấu hình
  <br> + Node.js installation trên Linux instance
  <br> + Node.js app deployment trên Linux
  <br> + XAMPP setup trên Windows instance
  <br> + Node.js installation trên Windows instance
  <br> + Node.js app deployment trên Windows

**IAM Resource Control:**

- Giới hạn tài nguyên sử dụng bằng IAM policies:
  <br> + Region-specific access control
  <br> + Instance family restrictions
  <br> + Instance type limitations
  <br> + EBS volume quotas
  <br> + Resource deletion permissions
  <br> + Time-based resource deletion policies

**IAM Role Practice:**

- Thực hành cấp quyền với IAM Roles:
  <br> + EC2 instance tạo và cấu hình
  <br> + S3 bucket setup
  <br> + IAM user và access key management
  <br> + IAM role creation và usage
  <br> + Application access to AWS services

**AWS Cloud9 IDE:**

- Nắm vững các khái niệm về AWS Cloud9:
  <br> + Cloud IDE overview
  <br> + Cloud9 instance creation
  <br> + Command line usage
  <br> + Text file editing
  <br> + Dashboard interface
  <br> + AWS CLI integration

**Amazon S3 Static Website Hosting:**

- Hosting static website trên S3:
  <br> + S3 bucket creation
  <br> + Data upload
  <br> + Static website hosting configuration
  <br> + Block Public Access settings
  <br> + Public object configuration
  <br> + Website testing

- CloudFront CDN optimization:
  <br> + CloudFront distribution creation
  <br> + Public S3 access blocking
  <br> + CloudFront configuration
  <br> + CloudFront verification

- S3 Advanced Features:
  <br> + Bucket versioning setup và quản lý
  <br> + Object movement between buckets
  <br> + Object replication to different regions
