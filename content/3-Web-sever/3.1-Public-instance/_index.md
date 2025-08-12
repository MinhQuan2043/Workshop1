---
title : "Kết nối tới Web Server công khai bằng IPv6"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---
![IPv6 Public Instance](/images/arc-02.png)

1. Cài đặt Web Server
    + Sử dụng SSH để kết nối tới instance của bạn.
    + Chạy các lệnh sau để cài đặt Apache Web Server:
    
    ```bash
    sudo apt update
    sudo apt install apache2 -y
    ```

2. Cấu hình Apache để hỗ trợ IPv6
    + Mở tệp cấu hình chính của Apache:
    
    ```bash
    sudo nano /etc/apache2/ports.conf
    ```
    
    + Đảm bảo rằng dòng sau tồn tại để Apache lắng nghe trên cổng 80 cho cả IPv4 và IPv6:
    
    ```
    Listen 80
    ```
    
    + Lưu và đóng tệp. Khởi động lại Apache để áp dụng các thay đổi:
    
    ```bash
    sudo systemctl restart apache2
    ```

3. Cấu hình tường lửa (Security Group) cho IPv6
    + Truy cập [AWS EC2 console](https://console.aws.amazon.com/ec2/v2/home).
    + Chọn **Security Groups** từ menu bên trái.
    + Chọn Security Group được gán cho instance của bạn.
    + Trong tab Inbound rules (Quy tắc vào), nhấp vào **Edit inbound rules**.
    + Thêm một quy tắc mới:
        + **Type**: HTTP
        + **Source**: Custom IPv6, nhập `::/0` (để cho phép mọi địa chỉ IPv6 truy cập).
    + Lưu lại các thay đổi.

{{% notice note %}}
Việc mở cổng HTTP với nguồn `::/0` cho phép mọi địa chỉ IPv6 trên internet truy cập vào web server của bạn. Đây là cấu hình cần thiết cho một máy chủ công khai.
{{% /notice %}}

4. Xác minh kết nối IPv6
    + Sao chép địa chỉ IPv6 công khai của instance từ trang EC2 console.
    + Từ máy tính của bạn, mở trình duyệt và truy cập địa chỉ IPv6 đó. Bạn cần đặt địa chỉ trong ngoặc vuông.
    
    ```
    http://[<Địa chỉ IPv6 của bạn>]
    ```
    
    + Bạn sẽ thấy trang chào mừng mặc định của Apache, điều này xác nhận rằng web server của bạn đã hoạt động thành công trên IPv6.
