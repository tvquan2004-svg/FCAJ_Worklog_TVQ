---
title: "Worklog Tuần 3"
date: 2026-05-18
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Thiết lập IAM Policy và IAM Role để quản lý phân quyền truy cập tài nguyên AWS.
* Tính toán chi phí vận hành dự án với AWS Pricing Calculator.
* Thiết lập AWS Budgets: Cost Budget và Usage Budget để kiểm soát chi phí.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu / Ghi chú |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu về IAM (Identity and Access Management): <br> + Các thành phần: User, Group, Role, Policy. <br> + Phân biệt IAM User và IAM Role. <br> + Cấu trúc của một IAM Policy document (JSON). | 19/05/2026 | 19/05/2026 | |
| 3 | - Thiết lập IAM Policy: <br> + Viết policy cho phép Lambda truy cập RDS, SQS, S3. <br> + Áp dụng nguyên tắc least privilege. <br> - Thiết lập IAM Role: <br> + Tạo role cho Lambda với các policy đã viết. <br> + Gán role cho Lambda function. | 20/05/2026 | 20/05/2026 | |
| 4 | - Tính toán chi phí vận hành với AWS Pricing Calculator: <br> + Nhập thông số dự kiến: EC2, RDS, S3, Lambda, API Gateway. <br> + Ước tính chi phí hàng tháng. <br> + Lên kế hoạch tối ưu chi phí. | 21/05/2026 | 21/05/2026 | |
| 5 | - Thiết lập AWS Budgets: <br> + Cost Budget: ngân sách chi phí hàng tháng. <br> + Usage Budget: giới hạn sử dụng tài nguyên. <br> + Cấu hình cảnh báo qua email khi vượt ngưỡng. | 22/05/2026 | 22/05/2026 | |
| 6 - CN | - Kiểm tra và hoàn thiện: <br> + Review các IAM Policy đã tạo. <br> + Xác nhận budget hoạt động. <br> + Tài liệu hóa các policy và ngân sách cho nhóm. | 23/05/2026 | 24/05/2026 | |

### Kết quả đạt được tuần 3:

* Hiểu rõ cách hoạt động của IAM và cấu trúc IAM Policy document.
* Thiết lập thành công IAM Policy với nguyên tắc least privilege cho các service chính.
* Tạo IAM Role cho Lambda với quyền truy cập cần thiết đến RDS, SQS và S3.
* Hoàn thành tính toán chi phí vận hành dự án với AWS Pricing Calculator, giúp dự trù ngân sách chính xác.
* Thiết lập AWS Budgets gồm Cost Budget và Usage Budget với cảnh báo qua email, đảm bảo kiểm soát chi phí hiệu quả.
