---
title: "Giới thiệu"
date: "`r Sys.Date()`"
weight: 1
chapter: true
---

# 1. Giới thiệu

### Mục tiêu Workshop

Trong workshop này, chúng ta sẽ học cách triển khai một **Web Server Dual-stack** (hỗ trợ cả IPv4 và IPv6) trên nền tảng AWS. Mục tiêu là để sinh viên thực hành việc cấu hình môi trường mạng IPv6 trong AWS, từ đó hiểu rõ hơn về các thành phần như VPC, EC2 và Security Group khi làm việc với hai giao thức mạng.

Hệ thống sẽ được triển khai với các thành phần chính sau:
* **AWS VPC**: Tạo môi trường mạng ảo, cho phép cấu hình dual-stack.
* **EC2 Instance**: Nền tảng để chạy Web Server Apache.
* **Security Group**: Quản lý truy cập vào EC2 Instance cho cả IPv4 và IPv6.
* **Apache**: Web Server để hiển thị nội dung trang web.

### Nội dung chi tiết của Workshop

1.  **Giới thiệu**
    * Mục tiêu và các thành phần chính của workshop.
    * Tạo VPC Dual-stack hỗ trợ cả IPv4 và IPv6.
    * Tạo một cặp Public và Private Subnet trong VPC.
    * Tạo Security Group để kiểm soát lưu lượng truy cập.
2.  **Cấu hình Hạ tầng AWS**
    * **Tạo VPC Dual-stack**:
        * Tạo VPC với IPv4 CIDR block là `10.0.0.0/16` và IPv6 CIDR block được AWS cung cấp.
        * `![Mô tả hình ảnh Tạo VPC](/images/gen-h-Tao-VPC.jpg)`
    * **Tạo Subnet**:
        * Tạo Public Subnet với IPv4 CIDR block `
