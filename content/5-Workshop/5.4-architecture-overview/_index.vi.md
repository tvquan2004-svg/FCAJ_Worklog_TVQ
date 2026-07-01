---
title : "Kiến trúc và luồng xử lý"
date : 2026-06-18
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

#### Tổng quan kiến trúc hệ thống

Phần này tổng quan về kiến trúc toàn bộ hệ thống, bao gồm sự tương tác giữa các dịch vụ AWS và cách chúng phối hợp để tạo ra một giải pháp có khả năng mở rộng và bảo mật.

#### Các thành phần chính

+ **API Gateway** - Cửa ngõ tiếp nhận request từ Client, định tuyến đến các dịch vụ backend.
+ **Lambda Functions** - Xử lý logic nghiệp vụ không cần quản lý máy chủ.
+ **Aurora Database** - Lưu trữ dữ liệu chính với khả năng tự động mở rộng.
+ **CloudFront & WAF** - Bảo mật biên và phân phối nội dung.
+ **S3 Storage** - Lưu trữ backup và tài nguyên tĩnh.

#### Mô hình kiến trúc

Kiến trúc được phân tách thành các lớp:
1. **Edge Layer** (CloudFront + WAF) - Bảo vệ và tăng tốc
2. **API Layer** (API Gateway) - Định tuyến request
3. **Compute Layer** (Lambda) - Xử lý logic
4. **Database Layer** (Aurora + S3) - Lưu trữ và sao lưu

![overview](/images/diagram.png)
