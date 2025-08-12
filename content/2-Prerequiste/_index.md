---
title : "Chuẩn bị "
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

{{% notice info %}}
Trong phần này, bạn cần tạo một **VPC Dual-stack** và các **Security Group** cần thiết để chuẩn bị cho việc triển khai EC2 Instance hỗ trợ cả IPv4 và IPv6.
{{% /notice %}}

Để hiểu rõ hơn về cách tạo EC2 và VPC, bạn có thể tham khảo các tài liệu sau:
 - [Giới thiệu về Amazon EC2](https://aws.amazon.com/ec2/)
 - [Làm việc với Amazon VPC](https://aws.amazon.com/vpc/)

Để có thể sử dụng các dịch vụ của AWS, đặc biệt là Hệ thống quản lý phiên (Systems Manager) trên các EC2 Instance của chúng ta, chúng ta cần gán các quyền cần thiết cho các Instance đó. Trong phần chuẩn bị này, chúng ta cũng sẽ tiến hành tạo một **IAM Role** để cấp quyền cho các Instance có thể làm việc với Systems Manager.

### Nội dung
 - [Chuẩn bị VPC và EC2](01-vpc-ec2/)
 - [Tạo vai trò IAM](02-iam-role/)
