---
title: "2.2 Tạo vai trò IAM"
weight: 2
chapter: true
---

# 2.2 Tạo vai trò IAM

Vai trò IAM (IAM Role) sẽ cung cấp các quyền cần thiết cho EC2 instance để có thể làm việc với các dịch vụ AWS khác như Systems Manager mà không cần quản lý khóa truy cập.

**Các bước tạo IAM Role:**
1.  Trong bảng điều khiển IAM, chọn **Roles**, sau đó **Create role**.
2.  Chọn **AWS service** và **EC2** làm trường hợp sử dụng.
3.  Tìm và gắn các quyền cần thiết, ví dụ: `AmazonSSMManagedInstanceCore`.
4.  Đặt tên cho vai trò và chọn **Create role**.
