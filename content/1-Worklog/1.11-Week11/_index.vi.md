---
title: "Worklog Tuần 11"
date: 2026-07-13
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Xây dựng các hàm Lambda phục vụ chế độ bảo trì của hệ thống game.
* Tách biệt chức năng thành các Lambda độc lập: Start Maintenance, Stop Maintenance, Vacuum & Analyze, Reset Daily.
* Cấu hình EventBridge để tự động kích hoạt các Lambda theo lịch hoặc sự kiện.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế kiến trúc hệ thống bảo trì:<br>+ Xác định các chế độ bảo trì cần thiết.<br>+ Thiết kế luồng chuyển đổi trạng thái hệ thống (online -> maintenance -> online).<br>+ Xác định cơ chế khóa API khi bảo trì. | 14/07/2026 | 14/07/2026 | |
| 3 | - Xây dựng Lambda Start Maintenance & Stop Maintenance:<br>+ Lambda Start Maintenance: cập nhật stageVariables API Gateway, chặn request mới, thông báo bảo trì.<br>+ Lambda Stop Maintenance: khôi phục stageVariables, cho phép request trở lại.<br>+ Tích hợp với API Gateway SDK để thay đổi trạng thái. | 15/07/2026 | 15/07/2026 | |
| 4 | - Xây dựng Lambda Vacuum & Analyze:<br>+ Tự động chạy lệnh VACUUM để dọn dẹp dead tuples trong database.<br>+ Chạy ANALYZE để cập nhật statistics cho query planner.<br>+ Ghi log kết quả và thông báo hoàn thành. | 16/07/2026 | 16/07/2026 | |
| 5 | - Xây dựng Lambda Reset Daily:<br>+ Xử lý reset các dữ liệu hàng ngày (nhiệm vụ, quà tặng, lượt chơi miễn phí...).<br>+ Đảm bảo tính nhất quán dữ liệu khi reset.<br>+ Ghi log và thông báo kết quả reset. | 17/07/2026 | 17/07/2026 | |
| 6 - CN | - Cấu hình EventBridge và kiểm thử:<br>+ Tạo EventBridge rules cho từng Lambda với lịch schedule cụ thể.<br>+ Cấu hình CloudWatch Metric và log cho các maintenance tasks.<br>+ Kiểm thử toàn bộ luồng bảo trì tự động. | 18/07/2026 | 19/07/2026 | |

### Kết quả đạt được tuần 11:

* Hoàn thành thiết kế kiến trúc hệ thống bảo trì với các chế độ hoạt động rõ ràng.
* Xây dựng thành công Lambda Start Maintenance và Stop Maintenance, cho phép chuyển đổi trạng thái hệ thống linh hoạt thông qua API Gateway stageVariables.
* Lambda Vacuum & Analyze hoạt động hiệu quả, tự động dọn dẹp database và tối ưu query planner định kỳ.
* Lambda Reset Daily đảm bảo dữ liệu hàng ngày được reset đúng cách và nhất quán.
* Cấu hình EventBridge rules tự động kích hoạt các Lambda theo lịch trình:
  * Vacuum & Analyze: chạy hàng ngày lúc 2:00 AM.
  * Reset Daily: chạy hàng ngày lúc 0:00 AM.
  * Maintenance: kích hoạt theo sự kiện thủ công hoặc tự động khi cần.
* Hệ thống bảo trì tự động giúp giảm thiểu thời gian chết và tăng độ ổn định của hệ thống.
