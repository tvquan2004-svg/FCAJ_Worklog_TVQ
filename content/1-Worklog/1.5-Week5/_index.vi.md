---
title: "Worklog Tuần 5"
date: 2026-06-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Thiết lập Monorepo với npm Workspaces để quản lý mã nguồn đa service.
* Xây dựng Lambda Handler Pattern chuẩn cho tất cả các service.
* Cấu hình Serverless Framework cho từng service để triển khai lên AWS.
* Kết nối database qua TypeORM kết hợp IAM Auth.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Thiết lập Monorepo với npm Workspaces: <br> + Cấu trúc thư mục: packages/shared, services/*. <br> + Khởi tạo root package.json với workspaces. <br> + Chia sẻ code chung (types, utils) qua shared package. | 02/06/2026 | 02/06/2026 | |
| 3 | - Xây dựng Lambda Handler Pattern: <br> + Thiết kế base handler class với error handling, logging, response format. <br> + Middleware pattern: authentication, validation, rate limiting. <br> + Standard response format cho tất cả API endpoints. | 03/06/2026 | 03/06/2026 | |
| 4 | - Cấu hình Serverless Framework: <br> + Tạo serverless.yml cho từng service. <br> + Cấu hình provider: runtime, region, stage, IAM Role. <br> + Cấu hình functions, events, environment variables. <br> + Plugin hỗ trợ: serverless-offline, serverless-dotenv. | 04/06/2026 | 04/06/2026 | |
| 5 | - Kết nối database qua TypeORM + IAM Auth: <br> + Cấu hình TypeORM DataSource với Aurora PostgreSQL. <br> + Tích hợp IAM Auth: dùng AWS SDK để lấy database auth token. <br> + Tạo entities và migrations cho các bảng dữ liệu. | 05/06/2026 | 05/06/2026 | |
| 6 - CN | - Kiểm tra tích hợp: <br> + Build monorepo, xác nhận dependency được resolve đúng. <br> + Chạy Lambda handler locally với serverless-offline. <br> + Kiểm tra kết nối database với IAM Auth. | 06/06/2026 | 07/06/2026 | |

### Kết quả đạt được tuần 5:

* Thiết lập thành công Monorepo với npm Workspaces, chia sẻ code chung qua shared package, giúp quản lý mã nguồn nhất quán giữa các service.
* Xây dựng Lambda Handler Pattern chuẩn với base handler, middleware support và response format thống nhất.
* Cấu hình Serverless Framework hoàn chỉnh cho từng service với đầy đủ functions, events và environment variables.
* Kết nối database thành công qua TypeORM + IAM Auth: sử dụng database auth token thay vì password truyền thống, tăng cường bảo mật.
* Tạo entities và migrations cho các bảng dữ liệu chính, sẵn sàng phát triển business logic.
