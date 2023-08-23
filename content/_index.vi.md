---
title: "Serverless Application"
date: "`r Sys.Date()`"
weight: 1
chapter: false
---

# Triển khai đường ống dữ iệu sử dụng các dịch vụ của AWS

### Tổng quan

Trong bài workshop này, chúng ta sẽ tạo một **đường ống dữ liệu (pipeline data)** tự động lấy dữ liệu thông qua API, kết hợp với các dịch vụ của AWS như: **AWS Lambda, Amazon DynamoDB, Amazon S3 (Simple Storage Service), Amazon EventBridge, AWS Glue**
- **AWS Lambda**: là một dịch vụ tính toán đám mây dựa trên mô hình serverless của Amazon Web Services. Nó cho phép bạn chạy mã mà không cần quản lý các máy chủ phía sau, tự động mở rộng khi cần thiết, và tính giá theo thời gian thực thi. Lambda thường được kích hoạt bởi các sự kiện như yêu cầu HTTP hoặc sự kiện từ các dịch vụ AWS khác.
- **Amazon DynamoDB**: là một dịch vụ cơ sở dữ liệu NoSQL đám mây của AWS. Nó cung cấp khả năng lưu trữ và truy vấn dữ liệu linh hoạt và mở rộng được cho các ứng dụng web và di động. DynamoDB được thiết kế để cung cấp khả năng mở rộng tự động và đáng tin cậy, hỗ trợ các ứng dụng với lưu lượng truy vấn cao và yêu cầu thời gian thực.
- **Amazon S3 (Simple Storage Service)**: là một dịch vụ lưu trữ đám mây của AWS. Nó cung cấp khả năng lưu trữ không giới hạn cho các đối tượng dữ liệu như hình ảnh, video, tệp tin và dữ liệu lưu trữ. S3 được sử dụng rộng rãi như một giải pháp lưu trữ đáng tin cậy, dễ sử dụng và có khả năng mở rộng cho các ứng dụng web và di động.
- **Amazon EventBridge**: Amazon EventBridge là một dịch vụ trung gian sự kiện của AWS, cho phép các ứng dụng gửi và nhận các sự kiện từ các nguồn khác nhau trong hệ thống. Nó giúp bạn kết nối và tích hợp các ứng dụng và dịch vụ khác nhau, tự động kích hoạt hành động và xử lý dữ liệu theo các quy tắc được xác định trước.
- **AWS Glue**: là một dịch vụ ETL (Extract, Transform, Load) đám mây của AWS. Nó cho phép bạn trích xuất dữ liệu từ nhiều nguồn khác nhau, biến đổi dữ liệu theo các quy tắc xác định trước và tải dữ liệu vào các kho lưu trữ khác nhau. Glue tự động xác định cấu trúc dữ liệu, giúp giảm thiểu công việc và thời gian triển khai quy trình ETL.

![ConnectPrivate](/images/1.intro/0-image.png)


### Nội dung

1.  [Giới thiệu](1-introduce/)
2.  [Khởi tạo DynamoDB và cấu hình TTL ](2-DynamoDB/)
3.  [Xây dựng lambda function ](3-lambda/)
4.  [Sử dụng EventBridge tạo lịch tự động ](4-event/)
5.  [Khởi tạo S3](5-s3/)
6.  [Cấu hình AWS Glue](6-glue/)
7.  [Kiểm tra kết quả](7-test/)
8.  [Dọn dẹp tài nguyên](8-terminate/)


