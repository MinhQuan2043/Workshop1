---
title: "3.3 Cài đặt Apache"
weight: 3
---

# 3.3 Cài đặt Apache

Sử dụng SSH để kết nối đến EC2 Instance và chạy các lệnh sau để cài đặt và cấu hình Apache:

1.  Cập nhật các gói phần mềm:
    `sudo yum update -y`
2.  Cài đặt Apache:
    `sudo yum install httpd -y`
3.  Khởi động dịch vụ Apache:
    `sudo systemctl start httpd`
4.  Cho phép Apache tự khởi động cùng hệ thống:
    `sudo systemctl enable httpd`
