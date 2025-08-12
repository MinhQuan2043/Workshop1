---
title: "5. Dọn dẹp tài nguyên"
weight: 5
chapter: true
---

# 5. Dọn dẹp tài nguyên

Để tránh phát sinh chi phí không mong muốn, bạn cần dọn dẹp tất cả các tài nguyên AWS đã tạo trong quá trình thực hiện đồ án. Các bước dọn dẹp cần được thực hiện theo thứ tự ngược lại với quá trình tạo.

1.  **Chấm dứt (Terminate) EC2 Instance:**
    * Trong bảng điều khiển EC2, chọn **Instances**.
    * Chọn EC2 Instance của bạn, sau đó chọn **Instance state** > **Terminate instance**.
    
2.  **Xóa Security Group:**
    * Trong bảng điều khiển EC2, chọn **Security Groups**.
    * Chọn Security Group bạn đã tạo và nhấp vào **Actions** > **Delete security group**.

3.  **Xóa Internet Gateway:**
    * Trong bảng điều khiển VPC, chọn **Internet Gateways**.
    * Chọn Internet Gateway của bạn, sau đó nhấp vào **Actions** > **Detach from VPC**.
    * Sau khi đã tách, nhấp vào **Actions** > **Delete internet gateway**.

4.  **Xóa Subnet:**
    * Trong bảng điều khiển VPC, chọn **Subnets**.
    * Chọn các Subnet bạn đã tạo (Public và Private), sau đó nhấp vào **Actions** > **Delete subnet**.

5.  **Xóa VPC:**
    * Trong bảng điều khiển VPC, chọn **Your VPCs**.
    * Chọn VPC của bạn và nhấp vào **Actions** > **Delete VPC**.
