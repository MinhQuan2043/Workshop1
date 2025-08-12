---
title: "3.1 Khởi chạy và Kết nối EC2 Instance"
weight: 1
---

# 3.1 Khởi chạy và Kết nối EC2 Instance

1.  **Khởi chạy EC2 Instance:**
    * Trong bảng điều khiển EC2, chọn **Instances**, sau đó **Launch instances**.
    * Đặt tên cho Instance (ví dụ: `web-server-ipv6`).
    * Chọn một AMI (Amazon Machine Image) phù hợp, ví dụ: **Amazon Linux**.
    * Trong phần **Network settings**, chọn VPC bạn đã tạo và chọn **Public subnet**.
    * Trong phần **Security group**, chọn Security Group bạn đã tạo trước đó (`web-sg`).
    * Chọn **Launch instance** để khởi chạy máy chủ.

2.  **Kết nối đến Instance:**
    * Sau khi Instance đã khởi chạy, chọn Instance của bạn và nhấp vào **Connect**.
    * Sử dụng phương thức kết nối **SSH** để truy cập vào máy chủ.
    * Làm theo hướng dẫn để sử dụng terminal hoặc một công cụ SSH client như PuTTY.
