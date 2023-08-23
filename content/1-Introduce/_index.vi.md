---
title: "Giới thiệu"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

**Đường ống dữ liệu (pipeline data)** sử dụng **AWS Lambda, Amazon DynamoDB, Amazon S3 (Simple Storage Service), Amazon EventBridge, AWS Glue**. Trong đường ống này, AWS Lambda sẽ được sử dụng để gọi API và lưu trữ dữ liệu vào DynamoDB. Hàm Lambda này sẽ được kích hoạt tự động mỗi giờ thông qua Amazon EventBridge, được cấu hình để tạo lịch tự động. Sau đó, dữ liệu từ DynamoDB sẽ được xử lý ETL (Extract, Transform, Load) bởi AWS Glue và sau đó lưu trữ vào Amazon S3.

#### Sơ đồ dưới đây minh họa kiến trúc đường ống dữ liệu:

![0](/images/1.intro/0-image.png)
