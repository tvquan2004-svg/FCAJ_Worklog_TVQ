---
title: "Worklog Tuần 9"
date: 2026-06-29
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Xây dựng hệ thống xử lý bất đồng bộ với SQS FIFO để đảm bảo thứ tự giao dịch.
* Cấu hình Producer Lambda gửi message vào hàng đợi SQS.
* Xây dựng Consumer Lambda nhận và xử lý message từ SQS.
* Xử lý pessimistic lock trong transaction để tránh race condition.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu cơ chế SQS FIFO:<br>+ So sánh giữa Standard Queue và FIFO Queue.<br>+ Cách FIFO đảm bảo thứ tự message (First-In-First-Out).<br>+ Message Group ID và Deduplication ID. | 30/06/2026 | 30/06/2026 | |
| 3 | - Cấu hình Producer Lambda:<br>+ Tích hợp AWS SDK để gửi message vào SQS FIFO.<br>+ Thiết lập Message Group ID theo player ID để đảm bảo thứ tự giao dịch cho từng người chơi.<br>+ Xử lý lỗi gửi message và retry logic. | 01/07/2026 | 01/07/2026 | |
| 4 | - Xây dựng Consumer Lambda:<br>+ Cấu hình SQS trigger cho Lambda.<br>+ Xử lý message nhận được từ queue.<br>+ Implement pessimistic lock trong transaction để ngăn chặn xử lý trùng lặp. | 02/07/2026 | 02/07/2026 | |
| 5 | - Xử lý pessimistic locking:<br>+ Sử dụng database-level locking (SELECT FOR UPDATE).<br>+ Đảm bảo tính nhất quán khi nhiều message cùng xử lý một tài nguyên.<br>+ Xử lý timeout và rollback khi lock không thành công. | 03/07/2026 | 03/07/2026 | |
| 6 - CN | - Kiểm thử hệ thống bất đồng bộ:<br>+ Gửi nhiều message đồng thời, kiểm tra thứ tự xử lý.<br>+ Kiểm tra pessimistic lock hoạt động đúng.<br>+ Kiểm tra xử lý lỗi và retry. | 04/07/2026 | 05/07/2026 | |

### Kết quả đạt được tuần 9:

* Nắm vững kiến trúc SQS FIFO và cách áp dụng vào hệ thống giao dịch game để đảm bảo thứ tự xử lý.
* Xây dựng thành công Producer Lambda gửi message vào SQS FIFO với Message Group ID theo từng người chơi.
* Consumer Lambda được cấu hình với SQS trigger, tự động xử lý message khi có dữ liệu mới.
* Triển khai pessimistic lock (SELECT FOR UPDATE) trong transaction, đảm bảo không có race condition khi xử lý đồng thời nhiều giao dịch trên cùng một tài nguyên.
* Hệ thống xử lý bất đồng bộ hoạt động ổn định, đảm bảo thứ tự giao dịch và tính nhất quán dữ liệu.
