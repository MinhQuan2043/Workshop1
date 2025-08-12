---
title : "Kết nối tới Web Server riêng tư bằng IPv6"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---
![IPv6 Private Instance](/images/arc-02.png)

1. Cài đặt Web Server
    + Sử dụng SSH để kết nối tới instance của bạn.
    + Chạy các lệnh sau để cài đặt Apache Web Server (tương tự như Public Instance):
    
    ```bash
    sudo apt update
    sudo apt install apache2 -y
    ```

2. Cấu hình Apache để lắng nghe kết nối IPv6 cục bộ
    + Mở tệp cấu hình chính của Apache:
    
    ```bash
    sudo nano /etc/apache2/ports.conf
    ```
    
    + Đảm bảo rằng dòng `Listen 80` đã được thêm vào.
    + Lưu và đóng tệp. Khởi động lại Apache để áp dụng các thay đổi:
    
    ```bash
    sudo systemctl restart apache2
    ```

3. Cấu hình tường lửa (Security Group) cho IPv6 riêng tư
    + Truy cập [AWS EC2 console](https://console.aws.amazon.com/ec2/v2/home).
    + Chọn **Security Groups** từ menu bên trái.
    + Chọn Security Group được gán cho Private Instance của bạn.
    + Trong tab Inbound rules (Quy tắc vào), nhấp vào **Edit inbound rules**.
    + Thêm một quy tắc mới:
        + **Type**: HTTP
        + **Source**: Custom IPv6, và nhập địa chỉ IPv6 của mạng nội bộ của bạn (ví dụ: `2001:db8:1234:1::/64`). Điều này chỉ cho phép các máy trong mạng con này truy cập.
    + Lưu lại các thay đổi.

{{% notice note %}}
Khác với Public Instance, bạn không sử dụng `::/0` mà thay vào đó là địa chỉ mạng riêng của bạn. Điều này đảm bảo rằng web server chỉ có thể truy cập từ bên trong mạng nội bộ, tăng cường bảo mật.
{{% /notice %}}

4. Xác minh kết nối IPv6 nội bộ
    + Sao chép địa chỉ IPv6 riêng tư của instance từ trang EC2 console.
    + Từ một máy tính khác trong cùng mạng nội bộ, mở trình duyệt và truy cập địa chỉ IPv6 đó.
    
    ```
    http://[<Địa chỉ IPv6 riêng tư của bạn>]
    ```
    
    + Bạn sẽ thấy trang chào mừng mặc định của Apache, xác nhận rằng web server đã hoạt động.
