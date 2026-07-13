---
title: "Worklog Tuần 2"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tìm hiểu các service AWS như EC2, RDS, Route 53, S3 để tìm ra service tối ưu cho dự án Backend Game API.
* Khảo sát và thiết kế giải pháp kiến trúc tổng thể cho dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu dịch vụ Amazon EC2: các loại instance, AMI, EBS, Elastic IP, Security Groups. <br> - Tìm hiểu dịch vụ Amazon RDS: các loại database engine (MySQL, PostgreSQL, Aurora), lớp instance. | 12/05/2026 | 12/05/2026 | |
| 3 | - Tìm hiểu Amazon Route 53: cách quản lý DNS, routing policies, hosted zones. <br> - Tìm hiểu Amazon S3: bucket, object storage, use cases cho game (asset storage, backup). | 13/05/2026 | 13/05/2026 | |
| 4 - 5 | - So sánh và đánh giá các service AWS phù hợp cho dự án Backend Game API. <br> - Xác định kiến trúc tối ưu: kết hợp EC2 cho compute, RDS cho database, S3 cho asset storage. | 14/05/2026 | 15/05/2026 | |
| 6 - CN | - Thiết kế giải pháp kiến trúc tổng thể cho dự án. <br> - Vẽ sơ đồ kiến trúc sơ bộ: <br> &emsp; + Client -> EC2 (Game Server) -> RDS (Database). <br> &emsp; + S3 cho lưu trữ asset tĩnh. <br> &emsp; + Route 53 cho quản lý tên miền. <br> - Trình bày và thảo luận giải pháp với nhóm. | 16/05/2026 | 17/05/2026 | |

### Kết quả đạt được tuần 2:

* Nắm rõ các service AWS cốt lõi: EC2, RDS, Route 53, S3 và cách chúng có thể ứng dụng vào dự án Backend Game API.
* Đánh giá và chọn được các service tối ưu cho dự án dựa trên yêu cầu kỹ thuật và chi phí.
* Hoàn thành khảo sát giải pháp và thiết kế sơ đồ kiến trúc sơ bộ cho hệ thống.
* Xác định được luồng dữ liệu chính: Client request qua EC2 -> xử lý logic game -> lưu trữ trên RDS, asset tĩnh phục vụ từ S3.
