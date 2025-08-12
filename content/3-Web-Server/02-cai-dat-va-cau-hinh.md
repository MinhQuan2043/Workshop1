---
title: "3.2 Cài đặt và Cấu hình Apache"
weight: 2
---

# 3.2 Cài đặt và Cấu hình Apache

Sử dụng SSH để kết nối đến EC2 Instance và chạy các lệnh sau:

1.  **Cập nhật và Cài đặt Apache:**
    * Cập nhật các gói phần mềm: `sudo apt update`
    * Cài đặt Apache: `sudo apt install apache2 -y`

2.  **Cấu hình Apache để hỗ trợ IPv6:**
    * Mở tệp cấu hình chính của Apache: `sudo nano /etc/apache2/ports.conf`
    * Đảm bảo rằng dòng `Listen 80` tồn tại để Apache lắng nghe trên cả IPv4 và IPv6.
    * Lưu và đóng tệp.
    * Khởi động lại Apache để áp dụng các thay đổi: `sudo systemctl restart apache2`

3.  **Cấu hình tường lửa (Security Group) cho IPv6:**
    * Truy cập [AWS EC2 console](https://console.aws.amazon.com/ec2/v2/home) và chọn **Security Groups**.
    * Chọn Security Group của instance.
    * Trong tab Inbound rules (Quy tắc vào), thêm một quy tắc mới: **Type**: HTTP, **Source**: Custom IPv6, nhập `::/0`.
    * Lưu lại các thay đổi.
