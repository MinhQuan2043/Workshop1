---
title : "Giới thiệu"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1. </b> "
---
**Mục tiêu Workshop**

Trong workshop này, chúng ta sẽ học cách triển khai một **Web Server Dual-stack** (hỗ trợ cả IPv4 và IPv6) trên nền tảng AWS. Mục tiêu là để sinh viên thực hành việc cấu hình môi trường mạng IPv6 trong AWS, từ đó hiểu rõ hơn về các thành phần như VPC, EC2 và Security Group khi làm việc với hai giao thức mạng.

Hệ thống sẽ được triển khai với các thành phần chính sau:
- **AWS VPC**: Tạo môi trường mạng ảo, cho phép cấu hình dual-stack.
- **EC2 Instance**: Nền tảng để chạy Web Server Apache.
- **Security Group**: Quản lý truy cập vào EC2 Instance cho cả IPv4 và IPv6.
- **Apache**: Web Server để hiển thị nội dung trang web.

**Kiến trúc Hệ thống**

- **VPC Dual-stack**: Cung cấp một môi trường mạng có cả dải địa chỉ IPv4 và IPv6.
- **EC2 Instance**: Khởi chạy một máy chủ ảo trong VPC, có cả địa chỉ IPv4 công khai và IPv6.
- **Security Group**: Hoạt động như một tường lửa ảo, cho phép lưu lượng truy cập HTTP (cổng 80) và SSH (cổng 22) từ mọi địa chỉ IP.
- **Route Table**: Định tuyến lưu lượng Internet cho cả hai giao thức ra Internet Gateway.
- **Apache Web Server**: Cài đặt và cấu hình để lắng nghe các yêu cầu trên cả IPv4 và IPv6.

**Quy trình làm việc**

- **Cấu hình hạ tầng AWS**: Bắt đầu bằng việc thiết lập một VPC mới với Subnet dual-stack, sau đó cấu hình Route Table và Security Group.
- **Triển khai Web Server**: Khởi chạy một instance EC2 và cài đặt Apache trên đó.
- **Tạo nội dung**: Tạo một trang web HTML đơn giản.
- **Kiểm tra**: Xác nhận rằng trang web có thể được truy cập thành công thông qua cả địa chỉ IPv4 và IPv6 của instance.
- **Tài liệu hóa**: Sử dụng Hugo để tạo tài liệu hướng dẫn cho toàn bộ quy trình.

**Nội dung Workshop**

- Cấu hình VPC, Subnet, Route Table và Security Group hỗ trợ IPv6.
- Khởi chạy một EC2 instance có cấu hình dual-stack.
- Cài đặt và cấu hình Apache Web Server trên EC2.
- Kiểm tra truy cập web bằng địa chỉ IPv4 và IPv6.
- Sử dụng Hugo để tạo một trang web tài liệu cho đồ án.
