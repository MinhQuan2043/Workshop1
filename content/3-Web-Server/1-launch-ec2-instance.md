---
title: "3.1 Khởi chạy và Kết nối EC2 Instance"
weight: 1
---

# 3.1 Khởi chạy và Kết nối EC2 Instance

1.  **Khởi chạy EC2 Instance:**
    * Trong bảng điều khiển EC2, chọn **Instances**, sau đó **Launch instances**.
    * Đặt tên cho Instance, ví dụ: `web-server-dual-stack`.
    * Chọn một AMI phù hợp, ví dụ: **Amazon Linux 2023 AMI**.
    * Chọn **t2.micro** để sử dụng trong Free Tier.
    * Trong phần **Network settings**, chọn **Public subnet** và đảm bảo **Auto-assign public IP** được bật.
    * Trong mục **Auto-assign IPv6 IP**, chọn **Assign an IPv6 address**.
    * Tạo hoặc chọn một **Key pair** đã có.
    * Trong phần **Security group**, chọn `web-sg`.
    * Chọn **Launch instance** để khởi chạy.

2.  **Kết nối đến Instance:**
    * Sau khi Instance đã ở trạng thái **Running**, chọn Instance và nhấp vào **Connect**.
    * Sử dụng phương thức kết nối **SSH** với lệnh sau (thay thế tên key và địa chỉ IP):
        ```bash
        ssh -i "your-key-pair.pem" ec2-user@<IPv4 công cộng>
        ```
