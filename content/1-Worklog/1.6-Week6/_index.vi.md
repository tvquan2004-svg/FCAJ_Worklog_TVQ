---
title: "Worklog Tuần 6"
date: 2026-06-08
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Xây dựng Core Services cho hệ thống Backend Game API.
* Phát triển lambda-auth: xác thực và phân quyền người dùng.
* Phát triển lambda-inventory: quản lý kho đồ và trang bị.
* Phát triển lambda-economy: quản lý tiền tệ trong game (Coin, Gem).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế chi tiết Core Services: <br> + Xác định các API endpoints cho từng service. <br> + Thiết kế database schema: users, inventory_items, currencies. <br> + Xác định luồng dữ liệu giữa các services. | 09/06/2026 | 09/06/2026 | |
| 3 | - Phát triển lambda-auth: <br> + Xây dựng API đăng ký, đăng nhập, refresh token. <br> + Xác thực JWT token. <br> + Middleware xác thực cho các service khác. | 10/06/2026 | 10/06/2026 | |
| 4 | - Phát triển lambda-inventory: <br> + API thêm vật phẩm vào kho. <br> + API lấy danh sách vật phẩm, trang bị. <br> + API trang bị/tháo trang bị. <br> + Cập nhật số lượng vật phẩm khi sử dụng. | 11/06/2026 | 11/06/2026 | |
| 5 | - Phát triển lambda-economy: <br> + API thêm/trừ Coin, Gem. <br> + API kiểm tra số dư. <br> + API lịch sử giao dịch. <br> + Xử lý giao dịch đồng thời (concurrent transaction). | 12/06/2026 | 12/06/2026 | |
| 6 - CN | - Kiểm thử Core Services: <br> + Kiểm thử từng Lambda riêng lẻ. <br> + Kiểm thử luồng liên kết: auth -> inventory/economy. <br> + Kiểm tra error handling. <br> + Tối ưu performance Lambda. | 13/06/2026 | 14/06/2026 | |

### Kết quả đạt được tuần 6:

* Hoàn thành thiết kế chi tiết kiến trúc Core Services với đầy đủ API endpoints và database schema.
* lambda-auth phát triển hoàn chỉnh: đăng ký, đăng nhập, JWT authentication, refresh token, middleware xác thực.
* lambda-inventory hoạt động đầy đủ chức năng: quản lý kho đồ, thêm/xóa vật phẩm, trang bị/tháo trang bị.
* lambda-economy quản lý tiền tệ (Coin, Gem) với xử lý giao dịch đồng thời an toàn và lịch sử giao dịch chi tiết.
* Kiểm thử tích hợp thành công: luồng authentication -> authorization -> business logic hoạt động ổn định.
* Cả 3 Core Services sẵn sàng triển khai, làm nền tảng cho các Dependent Services ở các tuần tiếp theo.
