---
title: "Worklog Tuần 1"
date: 2026-05-04
weight: 1
chapter: false
pre: ""
---

### Mục tiêu tuần 1:

- Nắm vững kiến thức nền tảng về AWS Cloud Platform, các dịch vụ cơ bản và kiến trúc cloud
- Làm quen với các công cụ quản lý AWS: AWS Management Console & AWS CLI
- Nắm vững các khái niệm về quản lý chi phí, bảo mật IAM, và mạng VPC
- Thực hành Infrastructure as Code để tự động hóa triển khai trên AWS
- Xây dựng quan hệ tốt với các thành viên trong First Cloud AI Journey

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                    |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------- |
| 2   | Làm quen với các thành viên và các anh chị mentor tại FCAJ <br> Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập <br> Học 5 video lý thuyết FCAJ Workforce Bootcamp - 2026: <br>&emsp; + Giới thiệu về AWS <br>&emsp; + FCAJ là gì và những kiến thức bạn sẽ nhận được <br>&emsp; + Gen AI trên AWS: Kuro AI <br>&emsp; + Hướng dẫn Management Console: Sign in ROOT USER & IAM USER <br>&emsp; + Cost optimization on AWS <br>&emsp; + AWS Global Infrastructure: Data center, AZ, Region, Cost optimization, Edge location                                                                                                                                                                                                                                                                              | 04/05/2026   | 04/05/2026      | <https://www.youtube.com/watch?v=Gz56QzLQ_Yo&list=PLahN4TLWtox3TSYFbN1DNX7NZgTVXNj3x>             |
| 3   | Học cơ bản về cách vẽ kiến trúc AWS trên draw.io <br> Tìm hiểu AWS và các loại dịch vụ <br>&emsp; + Dịch vụ hạ tầng cơ bản <br>&emsp; + Lưu trữ và Cơ sở dữ liệu <br>&emsp; + Quản lý và Tối ưu <br>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 05/05/2026   | 05/05/2026      | <https://www.youtube.com/watch?v=l8isyDe-GwY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=2>     |
| 4   | **Thực hành lab: Quản lý mức chi phí sử dụng trên AWS với AWS Budgets** <br>&emsp; + Tạo Cost Budget <br>&emsp; + Tạo Budget <br>&emsp; + Tạo Usage Budget <br>&emsp; + Tạo RI Budget <br>&emsp; + Tạo Saving Plans Budget <br> - Tìm hiểu về các yêu cầu hỗ trợ từ AWS                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | 06/05/2026   | 06/05/2026      | <https://000007.awsstudygroup.com/vi/> <br> <https://000009.awsstudygroup.com/vi/3-manage-cases/> |
| 5   | **Thực hành lab: Quản trị quyền truy cập với AWS Identity and Access Management (IAM)** <br>&emsp; + Giới thiệu về IAM <br>&emsp; + Tạo IAM group và IAM user <br>&emsp; + Tạo IAM role và operation user <br>&emsp; + Chuyển đổi IAM Role <br>**Thực hành lab: Amazon Virtual Private Cloud (VPC)** <br>&emsp; + Giới thiệu về Amazon VPC: [Subnets](https://000003.awsstudygroup.com/vi/1-introduce/1.1-subnets/), [Route Table](https://000003.awsstudygroup.com/vi/1-introduce/1.2-routetable/), [Internet Gateway](https://000003.awsstudygroup.com/vi/1-introduce/1.3-internetgateway/), [NAT Gateway](https://000003.awsstudygroup.com/vi/1-introduce/1.4-natgateway/) <br>&emsp; + Tường lửa trong VPC <br>&emsp; + Các bước chuẩn bị trước khi triển khai lên EC2 <br>&emsp; + Triển khai EC2 instance | 07/05/2026   | 08/05/2026      | <https://000003.awsstudygroup.com/vi/1-introduce/> <br> <https://000002.awsstudygroup.com/vi/>    |
| 6   | **Thực hành lab tiếp tục: Amazon Virtual Private Cloud (VPC)** <br>&emsp; + Giới thiệu về site to site VPN <br>&emsp; + Thực hành: <br>&emsp;&emsp; • Tạo môi trường VPN <br>&emsp;&emsp; • Cấu hình kết nối VPN <br>&emsp;&emsp; • Cấu hình VPN bằng strongSwan với Transit Gateway <br>&emsp; + Tự động hóa triển khai VPC với Infrastructure as Code <br> Ôn lại kiến thức tuần 1                                                                                                                                                                                                                                                                                                                                                                                                                            | 08/05/2026   | 08/05/2026      | <https://000003.awsstudygroup.com/vi/1-introduce/>                                                |

### Kết quả đạt được tuần 1:

- Hiểu rõ các dịch vụ AWS cơ bản và các nhóm dịch vụ có bắn:
  <br> + Compute (EC2)
  <br> + Networking (VPC, Route 53)
  <br> + Quản lý chi phí (AWS Budgets, Cost Explorer)
  <br> + Bảo mật (IAM, Security Groups)

- Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web

- Học cơ bản cách vẽ kiến trúc AWS trên draw.io để thiết kế hệ thống

- Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  <br> + Access Key & Secret Key
  <br> + Region mặc định
  <br> + Profile configuration

- Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:
  <br> + Kiểm tra thông tin tài khoản & cấu hình
  <br> + Lấy danh sách region
  <br> + Xem dịch vụ EC2
  <br> + Tạo và quản lý key pair
  <br> + Kiểm tra thông tin dịch vụ đang chạy

- Nắm vững IAM concepts và thực hành:
  <br> + Tạo IAM users
  <br> + Tạo IAM groups
  <br> + Tạo IAM roles
  <br> + Gán quyền (Permissions)
  <br> + Chuyển đổi IAM Roles

- Thực hành quản lý chi phí AWS với AWS Budgets:
  <br> + Tạo Cost Budget
  <br> + Tạo Usage Budget
  <br> + Tạo Saving Plans Budget

- Hiểu rõ VPC và các thành phần:
  <br> + Subnets (Public & Private)
  <br> + Route Tables
  <br> + Internet Gateway
  <br> + NAT Gateway
  <br> + Security Groups

- Triển khai EC2 instance với cấu hình VPC và kết nối SSH

- Học cấu hình VPN:
  <br> + Site-to-Site VPN
  <br> + Cấu hình VPN bằng strongSwan
  <br> + AWS Transit Gateway
- Hiểu Infrastructure as Code và tự động hóa triển khai VPC
