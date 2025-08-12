---
title: "3. Web Server"
date: "`r Sys.Date()`"
weight: 3
chapter: true
pre: "<b> 3. </b> "
---

# 3. Web Server

Phần này sẽ hướng dẫn cách triển khai một Web Server Dual-stack trên AWS EC2. Web server này sẽ được cấu hình để hoạt động đồng thời trên cả hai giao thức mạng **IPv4** và **IPv6**.

Nội dung của phần này bao gồm các bước:

1.  **Khởi chạy và Kết nối EC2 Instance:** Hướng dẫn cách tạo một máy chủ ảo EC2 trên AWS, cấu hình mạng dual-stack để nhận cả địa chỉ IPv4 và IPv6, sau đó kết nối đến máy chủ bằng SSH.
2.  **Cài đặt và Cấu hình Apache:** Chi tiết các lệnh để cài đặt dịch vụ web server Apache và cấu hình các quy tắc tường lửa (Security Group) để cho phép lưu lượng truy cập từ cả hai giao thức.
3.  **Tạo file HTML và Kiểm tra Kết nối:** Hướng dẫn cách tạo một trang web đơn giản và sử dụng cả trình duyệt lẫn lệnh `curl` để xác minh rằng web server đã hoạt động thành công trên cả IPv4 và IPv6.
