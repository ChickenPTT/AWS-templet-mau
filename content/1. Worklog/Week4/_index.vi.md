---
title: "Worklog Tuần 4"
date: 2026-05-25
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 4:

- Nắm vững kiến thức về Amazon CloudWatch để theo dõi và giám sát tài nguyên AWS
- Thực hành tạo metrics, logs, alarms và dashboards trên CloudWatch
- Hiểu rõ cách thiết lập hybrid DNS với Route 53 Resolver
- Làm quen với AWS CLI và cách sử dụng nó trên EC2 instances
- Thực hành AWS CLI với các dịch vụ AWS khác nhau (S3, SNS, IAM, VPC)
- Ôn lại kiến thức về các dịch vụ cơ bản: EC2, VPC, IAM Role, S3

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                             |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | **Thực hành lab: Tạo bảng theo dõi hệ thống với Amazon CloudWatch** <br>&emsp; + Giới thiệu về CloudWatch <br>&emsp; + Thiết lập AWS CloudFormation Stack <br>&emsp; + CloudWatch Metric: <br>&emsp;&emsp; • Xem các metric <br>&emsp;&emsp; • Thực hiện các phép tìm kiếm <br>&emsp;&emsp; • Thực hiện các phép toán học <br>&emsp;&emsp; • Tạo dynamic labels <br>&emsp; + CloudWatch Logs: <br>&emsp;&emsp; • CloudWatch Logs Insight <br>&emsp;&emsp; • CloudWatch Metric Filter <br>&emsp; + CloudWatch Alarm <br>&emsp; + CloudWatch Dashboards                                                                                                                                                                                                      | 25/05/2026   | 25/05/2026      | <https://000008.awsstudygroup.com/vi/>                                                                                                                                     |
| 3   | **Thực hành lab: Thiết lập Hybrid DNS với Route 53 Resolver** <br>&emsp; + Giới thiệu về Route 53 <br>&emsp; + Bước chuẩn bị: <br>&emsp;&emsp; • Tạo keypair <br>&emsp;&emsp; • Tạo Cloud Formation Template <br>&emsp;&emsp; • Khởi tạo security group <br>&emsp;&emsp; • Kết nối đến RDGW (Remote Desktop Gateway) <br>&emsp;&emsp; • Triển khai Microsoft AD <br>&emsp;&emsp; • Thiết lập DNS <br>&emsp; + Tạo Route 53 Outbound Endpoint <br>&emsp; + Tạo Route 53 Resolver Rules <br>&emsp; + Tạo Route 53 Inbound Endpoints <br>&emsp; + Test result                                                                                                                                                                                                 | 26/05/2026   | 26/05/2026      | <https://000010.awsstudygroup.com/vi/>                                                                                                                                     |
| 4   | **Thực hành lab: Sử dụng AWS CLI trên các Amazon EC2 (Windows/Ubuntu)** <br>&emsp; + Làm quen với AWS CLI: <br>&emsp;&emsp; • AWS CLI là gì? <br>&emsp;&emsp; • Môi trường hỗ trợ <br>&emsp;&emsp; • Khả năng của AWS CLI <br>&emsp;&emsp; • Định dạng đầu ra <br>&emsp;&emsp; • Thiết lập cơ bản <br>&emsp; + IAM User Group: <br>&emsp;&emsp; • IAM User <br>&emsp;&emsp; • AWS Access Key <br>&emsp;&emsp; • EC2 Instance và thiết lập quyền truy cập SSH <br>&emsp;&emsp; • Cài đặt AWS CLI <br>&emsp; + Kiểm tra tài nguyên qua CLI <br>&emsp; + AWS CLI với Amazon S3 <br>&emsp; + AWS CLI với Amazon SNS <br>&emsp; + AWS CLI với Amazon IAM <br>&emsp; + AWS CLI với Amazon VPC <br>&emsp; + Tạo EC2 và sử dụng AWS CLI <br>&emsp; + Khắc phục lỗi | 27/05/2026   | 27/05/2026      | <https://000011.awsstudygroup.com/vi/1-introduce/>                                                                                                                         |
| 5   | **Ôn lại dịch vụ của các lab** <br>&emsp; + EC2 <br>&emsp; + VPC <br>&emsp; + IAM Role (AWS IAM) <br>&emsp; + S3 bucket                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 28/05/2026   | 28/05/2026      | <https://000004.awsstudygroup.com/vi/> <br> <https://000003.awsstudygroup.com/vi/> <br> <https://000048.awsstudygroup.com/vi/> <br> <https://000057.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 4

**Amazon CloudWatch Knowledge:**

- Nắm vững các khái niệm về CloudWatch:
  <br> + CloudWatch overview
  <br> + AWS CloudFormation Stack setup
  <br> + CloudWatch Metrics
  <br> + CloudWatch Logs và Logs Insight
  <br> + CloudWatch Metric Filters
  <br> + CloudWatch Alarms
  <br> + CloudWatch Dashboards

- Thực hành CloudWatch Metrics:
  <br> + Viewing metrics
  <br> + Performing searches
  <br> + Mathematical operations
  <br> + Creating dynamic labels

**Route 53 Resolver Knowledge:**

- Nắm vững các khái niệm về Route 53:
  <br> + Route 53 overview
  <br> + Hybrid DNS setup
  <br> + Network infrastructure preparation
  <br> + CloudFormation Template
  <br> + Security Groups configuration
  <br> + Remote Desktop Gateway connectivity
  <br> + Microsoft AD deployment
  <br> + DNS setup

- Thực hành Route 53 Resolver:
  <br> + Route 53 Outbound Endpoint creation
  <br> + Route 53 Resolver Rules configuration
  <br> + Route 53 Inbound Endpoints setup
  <br> + Testing and verification

**AWS CLI Knowledge:**

- Hiểu rõ về AWS CLI:
  <br> + AWS CLI overview
  <br> + Supported environments
  <br> + CLI capabilities
  <br> + Output formats
  <br> + Basic configuration

- IAM User và Access Management:
  <br> + IAM User creation
  <br> + AWS Access Key management
  <br> + EC2 Instance SSH access configuration
  <br> + AWS CLI installation

- AWS CLI praktikum với các dịch vụ:
  <br> + AWS CLI with Amazon S3
  <br> + AWS CLI with Amazon SNS
  <br> + AWS CLI with Amazon IAM
  <br> + AWS CLI with Amazon VPC
  <br> + EC2 resource management
  <br> + Troubleshooting common issues

**AWS Services Review:**

- Ôn lại các dịch vụ AWS cơ bản:
  <br> + EC2 instance management
  <br> + VPC networking configuration
  <br> + IAM Roles and permissions
  <br> + S3 bucket operations
