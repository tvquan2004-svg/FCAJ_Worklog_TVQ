---
title: "Worklog Tuần 8"
date: 2026-06-22
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Tạo HTTP API V2 tập trung để quản lý toàn bộ các endpoints của hệ thống.
* Cấu hình routing cho từng service và deploy lên AWS.
* Kiểm thử toàn bộ API hệ thống.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế cấu trúc HTTP API V2:<br>+ Xác định các routes cho từng service (auth, inventory, economy, transaction).<br>+ Lên kế hoạch mapping giữa API Gateway paths và Lambda functions. | 23/06/2026 | 23/06/2026 | |
| 3 | - Tạo HTTP API V2 trên API Gateway:<br>+ Cấu hình CORS cho phép client truy cập.<br>+ Thiết lập các stages (dev, staging, prod).<br>+ Tích hợp Lambda authorizer cho các endpoints yêu cầu xác thực. | 24/06/2026 | 24/06/2026 | |
| 4 | - Cấu hình routing chi tiết:<br>+ Định nghĩa routes và integrations cho từng Lambda.<br>+ Thiết lập request/response transformation nếu cần.<br>+ Cấu hình throttle và rate limiting. | 25/06/2026 | 25/06/2026 | |
| 5 | - Deploy toàn bộ Compute Services + API Gateway:<br>+ Deploy các Lambda functions lên AWS.<br>+ Cập nhật environment variables và permissions.<br>+ Deploy API Gateway lên stage production. | 26/06/2026 | 26/06/2026 | |
| 6 - CN | - Kiểm thử toàn diện hệ thống API:<br>+ Kiểm thử từng endpoint riêng lẻ.<br>+ Kiểm thử luồng xuyên suốt (end-to-end).<br>+ Kiểm tra error handling và response codes.<br>+ Tối ưu performance (cold start, latency). | 27/06/2026 | 28/06/2026 | |

### Kết quả đạt được tuần 8:

* Thiết kế và triển khai thành công HTTP API V2 tập trung, quản lý toàn bộ routes cho tất cả services.
* Hoàn thành cấu hình routing chi tiết với CORS, Lambda authorizer, và các stage environments.
* Deploy thành công toàn bộ Compute Services (lambda-auth, lambda-inventory, lambda-economy, lambda-transaction) lên AWS.
* API Gateway được deploy lên stage production sẵn sàng phục vụ.
* Hoàn thành kiểm thử toàn diện:
  * Tất cả endpoints hoạt động đúng chức năng.
  * Luồng end-to-end: authentication -> authorization -> business logic -> response hoạt động ổn định.
  * Error handling trả về mã lỗi phù hợp (400, 401, 403, 404, 500).
  * Đã tối ưu cold start bằng cách tăng allocated memory cho Lambda.
