---
title: "4.1 Kiểm tra hiệu suất web server"
weight: 1
---

# 4.1 Kiểm tra hiệu suất web server

Sử dụng công cụ **Apache Benchmark (ab)** để đo lường và so sánh hiệu suất của web server khi truy cập bằng cả IPv4 và IPv6.

1.  **Cài đặt Apache Benchmark:**
    * Nếu công cụ `ab` chưa được cài đặt, bạn có thể cài đặt gói `httpd-tools` bằng lệnh sau trên Amazon Linux:
        ```bash
        sudo yum install httpd-tools -y
        ```

2.  **Chạy kiểm tra hiệu suất:**
    * Chạy kiểm tra với **1000** yêu cầu (-n) và **100** yêu cầu đồng thời (-c) để có kết quả chính xác.

    * **Kiểm tra với IPv4:**
        ```bash
        ab -n 1000 -c 100 http://<Địa chỉ IPv4 công cộng của bạn>/
        ```

    * **Kiểm tra với IPv6:**
        ```bash
        ab -n 1000 -c 100 http://[<Địa chỉ IPv6 công cộng của bạn>]/
        ```
![Kết quả](../images/gen-h-ab4.jpg)
![Kết quả](../images/gen-n-ab6.jpg)
3.  **Phân tích kết quả:**
    * Sau khi chạy xong, công cụ `ab` sẽ trả về một báo cáo chi tiết.
    * Đính kèm kết quả đầu ra của hai lệnh trên vào đồ án.
    * Tập trung so sánh các chỉ số sau:
        * **Requests per second:** Số lượng yêu cầu được xử lý mỗi giây.
        * **Time per request:** Thời gian trung bình để xử lý một yêu cầu.
    * Đưa ra nhận xét về sự khác biệt giữa hai giao thức và lý do bạn nghĩ rằng kết quả đó xảy ra (ví dụ: có thể IPv6 có hiệu suất tốt hơn do header đơn giản hơn, không cần NAT, v.v.).
