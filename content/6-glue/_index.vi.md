---
title: "Cấu hình dịch vụ AWS Glue"
date: "`r Sys.Date()`"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---
### Tổng quan

**AWS Glue** là một dịch vụ tích hợp và xử lý dữ liệu trên AWS. Nó cung cấp nhiều tính năng mạnh mẽ để quản lý và xử lý dữ liệu trong môi trường đám mây. Dưới đây là một giới thiệu ngắn về ba tính năng quan trọng của AWS Glue:

**Crawler (Điều hướng)**: là tính năng tự động phát hiện và phân tích cấu trúc dữ liệu từ các nguồn dữ liệu không cấu trúc như Amazon S3, hệ thống tệp, cơ sở dữ liệu quan hệ và nhiều nguồn khác. Nó quét các nguồn dữ liệu và tự động tạo các bản mô tả bảng (table metadata) trong AWS Glue Data Catalog. Điều này giúp dễ dàng xử lý dữ liệu mà không cần phải chỉ định cấu trúc dữ liệu thủ công.

**ETL Jobs (Xử lý dữ liệu Extract, Transform, Load)**: cho phép chúng taxây dựng các quy trình xử lý dữ liệu tự động để trích xuất dữ liệu từ nguồn, biến đổi (transform) dữ liệu theo các quy tắc và tiêu chuẩn cụ thể, sau đó tải dữ liệu đã xử lý vào nguồn đích. ETL Jobs có thể chạy tự động và thường được sử dụng để chuẩn hóa và tối ưu hóa dữ liệu trước khi phân tích.

**Trigger (Kích hoạt)**: cho phép chúng tatự động kích hoạt các công việc Glue (ETL Jobs) hoặc quy trình xử lý dữ liệu khác khi có sự kiện xảy ra. Sự kiện này có thể là việc thêm, sửa đổi hoặc xóa dữ liệu trong nguồn dữ liệu của bạn. Trigger giúp chúng tatạo các luồng công việc tự động và linh hoạt, đồng bộ hóa việc xử lý dữ liệu với sự thay đổi trong nguồn dữ liệu.

### Nội dung

- [Tạo Crawler](6.1-crawler/)
- [Tạo ETL job](6.2-jobs/)
- [Tạo trigger](6.3-trigger/)

