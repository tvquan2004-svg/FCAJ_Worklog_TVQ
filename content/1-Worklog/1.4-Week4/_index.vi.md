---
title: "Worklog Tuần 4"
date: 2026-05-25
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Tạo Amazon Aurora PostgreSQL cluster làm cơ sở dữ liệu chính cho hệ thống.
* Cấu hình RDS Proxy để gom kết nối, giảm tải database khi Lambda scale.
* Tạo CloudFormation Stack để tự động hóa triển khai hạ tầng.
* Cập nhật IAM Policy với cluster-id và database-user-name thực tế.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu Amazon Aurora PostgreSQL: <br> + Kiến trúc cluster, writer/reader instances. <br> + So sánh Aurora với RDS MySQL/PostgreSQL tiêu chuẩn. <br> + Các thông số cấu hình: instance class, storage, backup. | 26/05/2026 | 26/05/2026 | |
| 3 | - Tạo Amazon Aurora PostgreSQL cluster: <br> + Cấu hình VPC, subnet groups, security groups. <br> + Tạo writer instance cho read/write operations. <br> + Thiết lập automated backup và maintenance window. | 27/05/2026 | 27/05/2026 | |
| 4 | - Tìm hiểu và cấu hình RDS Proxy: <br> + Cách RDS Proxy gom kết nối từ Lambda để giảm tải database. <br> + Tạo RDS Proxy, kết nối với Aurora cluster. <br> + Cấu hình IAM Role cho phép Lambda sử dụng RDS Proxy. | 28/05/2026 | 28/05/2026 | |
| 5 | - Tạo CloudFormation Stack: <br> + Viết CloudFormation template cho toàn bộ hạ tầng. <br> + Tạo stack, triển khai các tài nguyên: Aurora, RDS Proxy, Security Groups. <br> - Cập nhật IAM Policy với cluster-id và database-user-name thực tế. | 29/05/2026 | 29/05/2026 | |
| 6 - CN | - Kiểm tra kết nối và hoàn thiện: <br> + Kiểm tra kết nối từ Lambda đến Aurora qua RDS Proxy. <br> + Xác nhận IAM Auth hoạt động. <br> + Tài liệu hóa cấu hình cho team. | 30/05/2026 | 31/05/2026 | |

### Kết quả đạt được tuần 4:

* Tạo thành công Amazon Aurora PostgreSQL cluster với writer instance, sẵn sàng cho production.
* Cấu hình RDS Proxy thành công, giúp gom kết nối từ Lambda, ngăn chặn tình trạng cạn kiệt kết nối database khi Lambda scale đột ngột.
* CloudFormation Stack được triển khai thành công, tự động hóa việc khởi tạo toàn bộ hạ tầng Aurora + RDS Proxy.
* IAM Policy được cập nhật với cluster-id và database-user-name thực tế, đảm bảo bảo mật và phân quyền chính xác.
* Kiểm tra kết nối Lambda -> RDS Proxy -> Aurora hoạt động ổn định.
