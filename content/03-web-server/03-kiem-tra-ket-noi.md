---
title: "3.3 Tạo file HTML và Kiểm tra Kết nối"
weight: 3
---

# 3.3 Tạo file HTML và Kiểm tra Kết nối

1.  **Tạo file HTML:**
    * Sử dụng lệnh sau để tạo file `index.html` trong thư mục `/var/www/html/`: `sudo echo "<h1>Hello IPv6 World!</h1>" | sudo tee /var/www/html/index.html`
    
2.  **Kiểm tra kết nối IPv6:**
    * Sao chép địa chỉ IPv6 công khai của instance từ trang EC2 console.
    * Mở trình duyệt và truy cập địa chỉ đó, bạn cần đặt địa chỉ trong ngoặc vuông: `http://[<Địa chỉ IPv6 của bạn>]`.
    * Bạn sẽ thấy nội dung `Hello IPv6 World!` hoặc trang chào mừng mặc định của Apache, điều này xác nhận rằng web server của bạn đã hoạt động trên IPv6.
