# Đồ án: Triển khai Web Server Dual-stack trên AWS và Kiểm tra Hiệu suất

### 1. Giới thiệu

Đồ án này trình bày quá trình triển khai một Web Server đơn giản trên nền tảng Amazon Web Services (AWS). Web Server được cấu hình để hoạt động với cả hai giao thức mạng là IPv4 và IPv6 (Dual-stack). Sau khi triển khai, chúng tôi đã sử dụng công cụ Apache Benchmark để kiểm tra hiệu suất và Amazon CloudWatch để giám sát tài nguyên của máy chủ.

### 2. Các bước triển khai

#### 2.1. Cấu hình và khởi chạy EC2 Instance

* Một EC2 Instance đã được tạo với hệ điều hành Amazon Linux.
* Instance này được cấu hình để có địa chỉ IPv4 công khai (`44.201.67.84`) và địa chỉ IPv6 công khai (`2600:1f10:4ff6:a8e0:38c9:e138:5242:e2e4`).
* Một Key Pair đã được tạo và lưu trữ để kết nối SSH an toàn.
* Security Group đã được cấu hình để cho phép truy cập HTTP (cổng 80) từ tất cả các địa chỉ IPv4 (`0.0.0.0/0`) và IPv6 (`::/0`).

#### 2.2. Cài đặt và cấu hình Web Server

* Kết nối SSH tới EC2 Instance bằng PuTTY.
* Chạy các lệnh sau để cài đặt và khởi động Apache Web Server:
    ```bash
    sudo yum update -y
    sudo yum install httpd -y
    sudo systemctl start httpd
    sudo systemctl enable httpd
    ```
* Một tệp `index.html` đã được tạo để kiểm tra hoạt động của Web Server.

### 3. Kiểm tra hiệu suất với Apache Benchmark (ab)

Sử dụng công cụ `ab` để kiểm tra khả năng xử lý của Web Server khi nhận 100 yêu cầu đồng thời (`-n 100`) với 10 yêu cầu cùng lúc (`-c 10`).

#### 3.1. Kiểm tra với IPv4

* **Lệnh:** `ab -n 100 -c 10 http://44.201.67.84/`
* **Kết quả:** (Bạn hãy điền kết quả của bạn vào đây)

#### 3.2. Kiểm tra với IPv6

* **Lệnh:** `ab -n 100 -c 10 http://[2600:1f10:4ff6:a8e0:38c9:e138:5242:e2e4]/`
* **Kết quả:** (Bạn hãy điền kết quả của bạn vào đây)

#### 3.3. Phân tích

(Bạn hãy so sánh các thông số như `Requests per second` và `Time per request` giữa hai kết quả để rút ra kết luận.)

### 4. Giám sát với Amazon CloudWatch

* Đã tạo một báo động trên CloudWatch để theo dõi mức sử dụng CPU (`CPUUtilization`) của EC2 Instance.
* Báo động sẽ được kích hoạt khi mức sử dụng CPU vượt quá một ngưỡng nhất định.
* Thông báo sẽ được gửi đến địa chỉ email đã đăng ký thông qua SNS topic.

(Bạn có thể thêm hình ảnh của báo động đã được tạo để minh họa.)

---
Đây là một bản nháp hoàn chỉnh, bạn chỉ cần điền kết quả kiểm tra hiệu suất và thêm hình ảnh CloudWatch để hoàn thành.
