---
title: "4.2 Giám sát với CloudWatch"
weight: 2
---

# 4.2 Giám sát với CloudWatch

**Amazon CloudWatch** là một dịch vụ giám sát mạnh mẽ của AWS, giúp bạn theo dõi các tài nguyên và ứng dụng. Tại đây, chúng ta sẽ sử dụng CloudWatch để giám sát EC2 Instance và thiết lập cảnh báo khi có sự cố.

1.  **Xem các chỉ số mặc định:**
    * Trên bảng điều khiển EC2, chọn Instance của bạn.
    * Chuyển đến tab **Monitoring** để xem các biểu đồ về CPU Utilization, Network In/Out, Disk Read/Write.

2.  **Thiết lập báo động (Alarm) cho CPU Utilization:**
    * Chọn **Actions** > **Monitor and troubleshoot** > **Manage CloudWatch alarms**.
    * Tạo một báo động mới:
        * **Specify metric and condition:** Chọn **Metric > EC2 > Per-Instance Metrics > CPUUtilization**.
        * **Threshold:** Đặt ngưỡng `CPUUtilization` là `>= 80%` trong vòng `5 phút`.
        * **Configure actions:** Cấu hình hành động gửi thông báo. Chọn một SNS Topic đã có hoặc tạo mới để gửi thông báo qua email.
        * Đặt tên cho báo động (ví dụ: `CPU-High-Alarm`).
    * **Lưu báo động** để hoàn tất.

3.  **Ý nghĩa của việc giám sát:**
    * Việc giám sát giúp bạn chủ động theo dõi hiệu suất của máy chủ.
    * Báo động giúp bạn nhận được thông báo tức thì khi có vấn đề (như CPU quá tải), cho phép bạn khắc phục sự cố kịp thời.
    * Điều này rất quan trọng để đảm bảo tính sẵn sàng và ổn định của dịch vụ.
