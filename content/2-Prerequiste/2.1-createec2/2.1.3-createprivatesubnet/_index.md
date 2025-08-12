---
title: "2.1.3 Tạo nhóm bảo mật"
weight: 3
---

# 2.1.3 Tạo Security Group

1.  Trong bảng điều khiển EC2, chọn **Security Groups**, sau đó chọn **Create security group**.
2.  Đặt tên cho Security Group (ví dụ: `web-sg`).
3.  Chọn VPC của bạn (`workshop-ipv6-vpc`).
4.  Thêm các quy tắc Inbound (truy cập đến) sau:
    * **HTTP (cổng 80)**: Cho phép truy cập từ mọi địa chỉ IPv4 (`0.0.0.0/0`) và IPv6 (`::/0`).
    * **SSH (cổng 22)**: Cho phép truy cập từ mọi địa chỉ IPv4 (`0.0.0.0/0`) và IPv6 (`::/0`).
5.  Chọn **Create security group**.
