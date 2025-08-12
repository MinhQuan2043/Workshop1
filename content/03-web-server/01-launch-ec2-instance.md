---
title: "3.1 Khởi chạy EC2 Instance"
weight: 1
---

# 3.1 Khởi chạy EC2 Instance

1.  Trong bảng điều khiển EC2, chọn **Instances**, sau đó **Launch instances**.
2.  Đặt tên cho Instance (ví dụ: `web-server-ipv6`).
3.  Chọn một AMI (Amazon Machine Image) phù hợp, ví dụ: **Amazon Linux**.
4.  Trong phần **Network settings**, chọn VPC bạn đã tạo và chọn **Public subnet**.
5.  Trong phần **Security group**, chọn Security Group bạn đã tạo trước đó (`web-sg`).
6.  Chọn **Launch instance** để khởi chạy máy chủ.
