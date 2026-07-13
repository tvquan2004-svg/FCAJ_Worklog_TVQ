---
title: "Worklog Tuần 10"
date: 2026-07-06
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Xây dựng hệ thống Dead Letter Queue (DLQ) để quản lý các message bị lỗi.
* Cấu hình RedrivePolicy với maxReceiveCount để tự động chuyển message lỗi sang DLQ.
* Thiết lập CloudWatch Metric và Alarm để giám sát DLQ.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu kiến trúc Dead Letter Queue:<br>+ Vai trò của DLQ trong hệ thống xử lý bất đồng bộ.<br>+ Cách SQS kết hợp với DLQ để quản lý message lỗi.<br>+ Các thông số cấu hình: maxReceiveCount, retention period. | 07/07/2026 | 07/07/2026 | |
| 3 | - Cấu hình RedrivePolicy:<br>+ Thiết lập maxReceiveCount = 3 (tự động chuyển sang DLQ sau 3 lần retry thất bại).<br>+ Tạo DLQ queue riêng cho từng loại message (game-economy-dlq.fifo, ...).<br>+ Cấu hình message retention 14 ngày trên DLQ. | 08/07/2026 | 08/07/2026 | |
| 4 | - Cấu hình functionResponseType: ReportBatchItemFailures:<br>+ Cho phép Lambda báo cáo message lỗi trong batch.<br>+ Xử lý partial failure: chỉ những message lỗi mới được retry.<br>+ Tích hợp với SQS event source mapping. | 09/07/2026 | 09/07/2026 | |
| 5 | - Kiểm thử retry và DLQ:<br>+ Gửi message lỗi cố ý để kiểm tra cơ chế retry.<br>+ Xác nhận message được retry đúng 3 lần.<br>+ Xác nhận message được chuyển sang DLQ sau khi retry thất bại. | 10/07/2026 | 10/07/2026 | |
| 6 - CN | - Thiết lập CloudWatch Metric và Alarm cho DLQ:<br>+ Tạo metric ApproximateNumberOfMessagesVisible cho DLQ.<br>+ Thiết lập CloudWatch Alarm khi DLQ có message (threshold > 0).<br>+ Cấu hình SNS notification gửi email/cảnh báo khi alarm kích hoạt. | 11/07/2026 | 12/07/2026 | |

### Kết quả đạt được tuần 10:

* Xây dựng thành công hệ thống Dead Letter Queue giúp quản lý các message bị lỗi trong xử lý bất đồng bộ.
* Cấu hình RedrivePolicy với maxReceiveCount = 3, message tự động chuyển sang DLQ sau 3 lần retry thất bại.
* Tạo DLQ queue riêng cho từng service (game-economy-dlq.fifo) với retention period 14 ngày.
* Cấu hình thành công ReportBatchItemFailures giúp xử lý partial failure trong batch processing.
* Kiểm thử retry thành công: message lỗi được retry đúng 3 lần trước khi chuyển sang DLQ.
* Thiết lập CloudWatch Metric và Alarm giám sát DLQ, gửi cảnh báo qua SNS khi có message lỗi phát sinh.
