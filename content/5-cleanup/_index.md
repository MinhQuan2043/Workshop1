---
title: "5. Dọn dẹp tài nguyên"
weight: 5
chapter: true
pre: "<b> 5. </b> "
---

# 5. Dọn dẹp tài nguyên

Để tránh phát sinh chi phí không mong muốn, bạn cần dọn dẹp tất cả các tài nguyên AWS đã tạo trong quá trình thực hiện đồ án. Các bước dọn dẹp cần được thực hiện theo thứ tự ngược lại với quá trình tạo, bắt đầu từ các tài nguyên phụ thuộc và kết thúc bằng tài nguyên chính.

**Lưu ý:** Việc xóa tài nguyên là vĩnh viễn và không thể khôi phục. Hãy chắc chắn rằng bạn không cần sử dụng các tài nguyên này nữa trước khi thực hiện.

1.  **Xóa các báo động (Alarms) trên CloudWatch và các SNS Topic (nếu có):**
    * **CloudWatch Alarms:** Vào bảng điều khiển **CloudWatch**, chọn **Alarms**. Chọn các báo động bạn đã tạo và chọn **Actions** > **Delete**.
    * **SNS Topic:** Vào bảng điều khiển **SNS (Simple Notification Service)**, chọn **Topics**. Chọn topic bạn đã tạo và chọn **Delete**.

2.  **Chấm dứt (Terminate) EC2 Instance:**
    * Trong bảng điều khiển **EC2**, chọn **Instances**.
    * Chọn EC2 Instance của bạn (ví dụ: `web-server-dual-stack`), sau đó chọn **Instance state** > **Terminate instance**.
    * Quá trình này sẽ mất một vài phút để hoàn tất.

3.  **Xóa Security Group:**
    * Trong bảng điều khiển **EC2**, chọn **Security Groups**.
    * Chọn Security Group bạn đã tạo (`web-sg`) và nhấp vào **Actions** > **Delete security group**.
    * Lưu ý: Bạn chỉ có thể xóa Security Group khi không có tài nguyên nào khác đang sử dụng nó.

4.  **Xóa Elastic IP (nếu có):**
    * Nếu bạn đã cấp phát Elastic IP, hãy xóa nó để tránh phát sinh chi phí.
    * Trong bảng điều khiển **EC2**, chọn **Elastic IPs**.
    * Chọn địa chỉ Elastic IP của bạn, sau đó chọn **Actions** > **Release Elastic IP addresses**.

5.  **Xóa Route Table:**
    * Trong bảng điều khiển **VPC**, chọn **Route Tables**.
    * Chọn bảng định tuyến bạn đã tạo, chọn **Actions** > **Delete route table**.

6.  **Xóa Internet Gateway:**
    * Trong bảng điều khiển **VPC**, chọn **Internet Gateways**.
    * Chọn Internet Gateway của bạn, sau đó nhấp vào **Actions** > **Detach from VPC**.
    * Sau khi đã tách, nhấp vào **Actions** > **Delete internet gateway**.

7.  **Xóa Subnet:**
    * Trong bảng điều khiển **VPC**, chọn **Subnets**.
    * Chọn các Subnet bạn đã tạo và nhấp vào **Actions** > **Delete subnet**.

8.  **Xóa VPC:**
    * Trong bảng điều khiển **VPC**, chọn **Your VPCs**.
    * Chọn VPC của bạn và nhấp vào **Actions** > **Delete VPC**.
    * Nếu VPC của bạn vẫn còn tài nguyên (như Subnet, Route Table), AWS sẽ báo lỗi. Hãy đảm bảo bạn đã xóa tất cả các tài nguyên liên quan trước khi xóa VPC.
