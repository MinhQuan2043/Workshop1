---
title : "Giới thiệu"
date : "`r Sys.Date()`"
weight : 1
chapter : true
---

# 1. Giới thiệu

### Mục tiêu Workshop

Trong workshop này, chúng ta sẽ học cách triển khai một **Web Server Dual-stack** (hỗ trợ cả IPv4 và IPv6) trên nền tảng AWS. Mục tiêu là để sinh viên thực hành việc cấu hình môi trường mạng IPv6 trong AWS, từ đó hiểu rõ hơn về các thành phần như VPC, EC2 và Security Group khi làm việc với hai giao thức mạng.

Hệ thống sẽ được triển khai với các thành phần chính sau:
* **AWS VPC**: Tạo môi trường mạng ảo, cho phép cấu hình dual-stack.
* **EC2 Instance**: Nền tảng để chạy Web Server Apache.
* **Security Group**: Quản lý truy cập vào EC2 Instance cho cả IPv4 và IPv6.
* **Apache**: Web Server để hiển thị nội dung trang web.

### Nội dung
1.  [Giới thiệu](01-gioi-thieu/)
2.  [Chuẩn bị](02-chuan-bi/)
3.  [Triển khai Web Server](03-web-server/)
4.  [Kiểm tra và Xác nhận](04-kiem-tra-va-xac-nhan/)
5.  [Triển khai trên GitHub Pages](05-don-dep/)

