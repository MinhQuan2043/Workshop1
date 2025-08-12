---
title: "4. Giám sát và Kiểm tra hiệu suất"
date: "`r Sys.Date()`"
weight: 4
chapter: true
pre: "<b> 4. </b> "
---



Sau khi đã triển khai thành công Web Server Dual-stack, việc tiếp theo là đảm bảo máy chủ hoạt động ổn định và hiệu quả. Phần này sẽ tập trung vào hai khía cạnh chính:
- **Kiểm tra hiệu suất:** Sử dụng công cụ Apache Benchmark (ab) để so sánh tốc độ xử lý của web server trên hai giao thức IPv4 và IPv6.
- **Giám sát:** Cấu hình và sử dụng dịch vụ Amazon CloudWatch để theo dõi các chỉ số quan trọng của EC2 Instance và thiết lập báo động khi có sự cố.

