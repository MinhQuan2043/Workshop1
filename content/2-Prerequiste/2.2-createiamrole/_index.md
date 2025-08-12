---
title: "2.2 Tạo vai trò IAM"
weight: 2
chapter: true
---

Vai trò IAM (IAM Role) sẽ cung cấp các quyền cần thiết cho EC2 instance để có thể làm việc với các dịch vụ AWS khác như Systems Manager mà không cần quản lý khóa truy cập. Việc này giúp tăng cường bảo mật và đơn giản hóa quá trình quản lý.

**Các bước tạo IAM Role:**
1.  Trong bảng điều khiển IAM, chọn **Roles**, sau đó **Create role**.
2.  Chọn **AWS service** và **EC2** làm trường hợp sử dụng. Chọn **Next**.
3.  Trên trang **Add permissions**, tìm kiếm và gắn các chính sách quyền cần thiết. Ví dụ:
    * `AmazonSSMManagedInstanceCore` (cung cấp quyền cho EC2 để sử dụng AWS Systems Manager).
    * `AmazonEC2ContainerRegistryReadOnly` (nếu bạn cần quyền truy cập vào ECR).
    * Chọn **Next**.
4.  Đặt tên cho vai trò (ví dụ: `EC2-SSM-Role`) và chọn **Create role**.

Sau khi tạo, bạn có thể gán vai trò này cho EC2 instance của mình khi khởi chạy hoặc sau đó.
