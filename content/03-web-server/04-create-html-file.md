---
title: "3.4 Tạo file HTML"
weight: 4
---

# 3.4 Tạo file HTML

Tạo một file HTML đơn giản để kiểm tra Web Server của bạn:

1.  Sử dụng lệnh sau để tạo file `index.html` trong thư mục `/var/www/html/`:
    `sudo echo "<h1>Hello IPv6 World!</h1>" | sudo tee /var/www/html/index.html`
2.  Kiểm tra trang web bằng cách truy cập địa chỉ IPv4 hoặc IPv6 của EC2 Instance trên trình duyệt.
