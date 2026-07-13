---
title: "Worklog Tuần 7"
date: 2026-06-15
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Phát triển các Dependent Services phục vụ logic game: Shop, Gift Code.
* Xây dựng cơ chế Cross-Service Communication qua API Gateway để các Lambda functions giao tiếp với nhau.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế kiến trúc cho lambda-transaction:<br>+ Xác định các API endpoints cần thiết.<br>+ Phân luồng dữ liệu giữa lambda-transaction và các core services (lambda-economy, lambda-inventory). | 16/06/2026 | 16/06/2026 | |
| 3 | - Phát triển chức năng Shop:<br>+ Xây dựng API mua vật phẩm bằng Coin/Gem.<br>+ Xử lý logic kiểm tra số dư và trừ tiền.<br>+ Cập nhật inventory cho người chơi sau giao dịch. | 17/06/2026 | 17/06/2026 | |
| 4 | - Phát triển chức năng Gift Code:<br>+ Xây dựng API tạo và nhận Gift Code.<br>+ Cơ chế xác thực mã, kiểm tra hạn sử dụng và số lần nhận.<br>+ Xử lý trao thưởng vật phẩm/tài nguyên. | 18/06/2026 | 18/06/2026 | |
| 5 - 6 | - Xây dựng Cross-Service Communication:<br>+ Thiết lập API Gateway làm trung gian giao tiếp giữa các Lambda.<br>+ Cấu hình IAM Role cho phép Lambda invoke lẫn nhau.<br>+ Xử lý lỗi và timeout khi giao tiếp giữa các services. | 19/06/2026 | 20/06/2026 | |
| CN | - Kiểm thử tích hợp toàn bộ luồng transaction:<br>+ Mua vật phẩm từ Shop -> trừ tiền -> nhận đồ.<br>+ Nhận Gift Code -> kiểm tra mã -> trao thưởng.<br>+ Kiểm tra tính nhất quán dữ liệu giữa các services. | 21/06/2026 | 21/06/2026 | |

### Kết quả đạt được tuần 7:

* Hoàn thành thiết kế và phát triển lambda-transaction với đầy đủ các API endpoints cho Shop và Gift Code.
* Hệ thống Shop hoạt động ổn định: người chơi có thể mua vật phẩm, hệ thống tự động kiểm tra số dư, trừ tiền và cập nhật inventory chính xác.
* Chức năng Gift Code được triển khai thành công với cơ chế xác thực mã, kiểm tra hạn sử dụng và giới hạn số lần nhận.
* Xây dựng thành công cơ chế Cross-Service Communication qua API Gateway, cho phép các Lambda functions giao tiếp an toàn và hiệu quả với nhau.
* Hoàn thành kiểm thử tích hợp, đảm bảo tính nhất quán dữ liệu xuyên suốt các luồng giao dịch.
