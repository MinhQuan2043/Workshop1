---
title: "3.3 Tạo file HTML và Kiểm tra Kết nối"
weight: 3
---

# 3.3 Tạo file HTML và Kiểm tra Kết nối

1.  **Tạo file HTML:**
    * Sử dụng lệnh sau để tạo một file `index.html` đơn giản trong thư mục gốc của web server:
        ```bash
        sudo sh -c 'echo "<h1>Hello IPv6 World!</h1>" > /var/www/html/index.html'
        ```

2.  **Kiểm tra kết nối IPv4 và IPv6:**
    * **Kiểm tra bằng trình duyệt:**
        * **IPv4:** Truy cập `http://<Địa chỉ IPv4 công cộng của instance>`
        * **IPv6:** Truy cập `http://[<Địa chỉ IPv6 công cộng của instance>]`
    * **Kiểm tra bằng terminal:**
        * Sử dụng lệnh `curl` để kiểm tra kết nối với cả hai giao thức.
        * Kiểm tra IPv4:
            ```bash
            curl -4 http://<Địa chỉ IPv4 công cộng>
            ```
        * Kiểm tra IPv6:
            ```bash
            curl -6 http://[<Địa chỉ IPv6 công cộng>]
            ```
    * Kết quả mong đợi từ cả hai cách kiểm tra là trang web sẽ hiển thị nội dung `Hello IPv6 World!`, xác nhận web server đã hoạt động thành công trên cả hai giao thức.
