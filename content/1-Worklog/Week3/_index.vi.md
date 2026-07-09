---
title: "Worklog Tuần 3"
date: 2026-05-18
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 3:

- Nắm vững cơ bản kiến thức về Amazon Relational Database Service (Amazon RDS) và các tính năng quản lý cơ sở dữ liệu
- Thực hành tạo và cấu hình RDS database instance trên AWS
- Hiểu rõ cách thiết lập VPC, Security Groups, và DB Subnet Groups cho RDS
- Thực hành Backup và Restore dữ liệu trên RDS
- Làm quen với Amazon Lightsail để triển khai ứng dụng nhẹ và hiệu quả về chi phí
- Hiểu về triển khai các ứng dụng trên Lightsail (WordPress, PrestaShop, Akaunting)
- Nắm khái niệm các tính năng quản lý Lightsail như Snapshots, scaling instances, và monitoring

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------ |
| 2   | **Thực hành lab: Tạo cơ sở dữ liệu trên Amazon Relational Database Service (Amazon RDS)** <br>&emsp; + Tổng quan giới thiệu <br>&emsp; + Các bước chuẩn bị: <br>&emsp;&emsp; • Tạo VPC <br>&emsp;&emsp; • Tạo EC2 security group <br>&emsp;&emsp; • Tạo RDS subnet group <br>&emsp;&emsp; • Tạo DB Subnet group <br>&emsp; + Tạo ec2 instance <br>&emsp; + Tạo RDS database instance <br>&emsp; + Triển khai ứng dụng <br>&emsp; + Backup và restore                                                                                                                                                                                                                                                                                                                                                                                                                                                              | 18/05/2026   | 18/05/2026      | <https://000005.awsstudygroup.com/vi/>                 |
| 3   | **Thực hành lab: Tối ưu chi phí tính toán với Amazon Lightsail** <br>&emsp; + Tổng quan và giới thiệu <br>&emsp; + Triển khai lightsail database <br>&emsp; + Triển khai Wordpress Instance: <br>&emsp;&emsp; • Triển khai instance <br>&emsp;&emsp; • Cấu hình ubuntu <br>&emsp;&emsp; • Cấu hình Networking <br>&emsp;&emsp; • Cấu hình WordPress <br>&emsp; + Triển khai Prestashop E-Commerce Instance: <br>&emsp;&emsp; • Triển khai instance <br>&emsp;&emsp; • Cấu hình Networking <br>&emsp;&emsp; • Triển khai ứng dụng <br>&emsp; + Triển khai Akaunting Instance: <br>&emsp;&emsp; • Triển khai instance <br>&emsp;&emsp; • Cấu hình networking <br>&emsp;&emsp; • Triển khai ứng dụng <br>&emsp; + Bảo mật ứng dụng <br>&emsp; + Tạo Snapshot <br>&emsp; + Chuyển sang instance lớn hơn khi lượng tài nguyên truy cập ứng dụng tăng lên <br>&emsp; + Tạo cảnh báo khi sử dụng tài nguyên CPU tăng cao | 19/05/2026   | 20/05/2026      | <https://000045.awsstudygroup.com/vi/8-create-alarms/> |
| 4   | **Thực hành lab: Tự động mở rộng qui mô ứng dụng với Amazon EC2 Autoscaling** <br>&emsp; + Tổng quan và lợi ích của Auto Scaling Group <br>&emsp; + Giới thiệu về Auto Scaling Group <br>&emsp; + Các bước chuẩn bị: <br>&emsp;&emsp; • Thiết lập hạ tầng mạng <br>&emsp;&emsp; • Khởi tạo ec2 instance <br>&emsp;&emsp; • Khởi tạo Database instance với RDS <br>&emsp;&emsp; • Cài dữ liệu database <br>&emsp;&emsp; • Triển khai máy chủ web <br>&emsp;&emsp; • Chuẩn bị các metric cho Predictive Scaling <br>&emsp;&emsp; • Tạo Launch Template                                                                                                                                                                                                                                                                                                                                                              | 20/05/2026   | 20/05/2026      | <https://000006.awsstudygroup.com/vi/1-introduction/>  |
| 5   | **Tiếp tục thực hành lab: Tự động mở rộng qui mô ứng dụng với Amazon EC2 Autoscaling** <br>&emsp; + Thiết lập load balancer <br>&emsp; + Kiểm tra kết quả <br>&emsp; + Tạo auto scaling group <br>&emsp; + Kiểm thử các giải pháp: <br>&emsp;&emsp; • Manual scaling <br>&emsp;&emsp; • Scheduled scaling <br>&emsp;&emsp; • Dynamic scaling <br>&emsp;&emsp; • Predictive scaling <br>&emsp; + Ôn lại bài lab Autoscaling                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 21/05/2026   | 21/05/2026      | <https://000006.awsstudygroup.com/vi/1-introduction/>  |

### Kết quả đạt được tuần 3

**RDS Core Knowledge:**

- Hiểu cơ bản các khái niệm về RDS:
  <br> + Tổng quan về Amazon RDS
  <br> + VPC setup và configuration
  <br> + EC2 Security Groups cấu hình cho RDS
  <br> + RDS Subnet Groups
  <br> + DB Subnet Groups
  <br> + EC2 Instance setup

- Triển khai RDS Database:
  <br> + RDS database instance creation
  <br> + Database configuration và setup
  <br> + Application deployment trên RDS
  <br> + Backup và Restore operations
  <br> + Data management và recovery

**Amazon Lightsail Overview:**

- Hiểu cơ bản các khái niệm về Amazon Lightsail:
  <br> + Lightsail overview và giới thiệu
  <br> + Cost-effective solutions
  <br> + Lightsail database setup

**Lightsail Application Deployment:**

- Triển khai các ứng dụng trên Lightsail:
  <br> + WordPress Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Ubuntu configuration
  <br>&emsp;&emsp; • Networking setup
  <br>&emsp;&emsp; • WordPress configuration
  <br> + PrestaShop E-Commerce Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Networking configuration
  <br>&emsp;&emsp; • Application deployment
  <br> + Akaunting Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Networking configuration
  <br>&emsp;&emsp; • Application deployment
  <br>&emsp;&emsp; • Application security

**Lightsail Management và Optimization:**

- Quản lý và tối ưu Lightsail instances:
  <br> + Snapshot creation và management
  <br> + Instance scaling khi tài nguyên tăng
  <br> + CPU resource monitoring
  <br> + Alert configuration cho resource usage
  <br> + Automatic scaling dựa trên tài nguyên consumption

**Tối ưu chi phí tính toán với Amazon Lightsail**

- Bảo mật ứng dụng
- Tạo Snapshot
- Chuyển sang instance lớn hơn khi lượng tài nguyên truy cập ứng dụng tăng lên
- Tạo cảnh báo khi sử dụng tài nguyên CPU tăng cao

**Tự động mở rộng qui mô ứng dụng với Amazon EC2 Autoscaling**

- Tổng quan và lợi ích của Auto Scaling Group
- Giới thiệu về Auto Scaling Group
- Các bước chuẩn bị:
  <br> + Thiết lập hạ tầng mạng
  <br> + Khởi tạo ec2 instance
  <br> + Khởi tạo Database instance với RDS
  <br> + Cài dữ liệu database
  <br> + Triển khai máy chủ web
  <br> + Chuẩn bị các metric cho Predictive Scaling
  <br> + Tạo Launch Template
