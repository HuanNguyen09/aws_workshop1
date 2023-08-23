---
title: "Dọn dẹp tài nguyên"
date: "`r Sys.Date()`"
weight: 8
chapter: false
pre: " <b> 8. </b> "
---

#### ETL jobs

1. Truy cập vào tab **ETL jobs** trong **AWS Glue** chọn các job đã khởi tạo trong bài lab. Sau đó chọn **Action** --> **Delete job(s)** 

![0](/images/8-terminate/im-01.png)
2. Điền `Delete`, chọn **Delete**
![0](/images/8-terminate/im-00.png)

### Thao tác tương tự với các tài nguyên đã khởi tạo trong bài lab theo thứ tự sau:

1. Trigger

2. Crawler

3. Data Catalog

4. S3 bucket
{{% notice warning %}}
Lưu ý: Khi xóa **S3 bucket**, ta cần xóa hết các file đã lưu trong bucket trước.
{{% /notice %}}
5. Lambda function

6. DynamoDB 

Vậy là chúng ta đã dọn dẹp tất cả tài nguyên trong workshop này.
