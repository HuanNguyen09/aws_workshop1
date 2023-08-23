---
title: "Tạo ETL job"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 6.2 </b> "
---

#### Khởi tạo job ETL


1. Vào trang **Glue**, ở tab bên trái chọn **ETL jobs**. Sau đó, chọn **Visual with a source taget**. **Source** chọn **AWS Glue Data Catalog**. Taget chọn **Amazon S3**. Chọn **Create**.

![0](/images/6-glue/6.2-jobs/im-19.png)
2. Chọn source **Data Catalog table**. Sau đó chọn các **database** và **Table** mà chúng ta đã tạo ở phần trước.

![0](/images/6-glue/6.2-jobs/im-18.png)

3. Chọn action transform. Tại đây chúng ta có thể đổi tên, đổi kiểu, xóa các trường dữ liệu.
![0](/images/6-glue/6.2-jobs/im-17.png)

4. Chọn taget **S3 bucket**. Tại đây ta chọn **Format: CSV**, **Type: None**, **S3 tagger: s3://weather-s3-db**.
![0](/images/6-glue/6.2-jobs/im-16.png)

5. Chọn tab **Job details**, đổi tên job: `DynamoDB-ETL-S3`. Chọn **IAM Role: Lab-role**.
![0](/images/6-glue/6.2-jobs/im-15.png)

6. Chọn tab **script**, tại đây chúng ta sửa đoạn code 
--- 
    frame=ApplyMapping-node2,

thành:

---     
    frame=ApplyMapping-node2.coalesce(1),

như hình. Sau đó chọn **Save** --> **Run**.
![0](/images/6-glue/6.2-jobs/im-14.png)

7. Chuyển qua tab **Runs**, sau khi ta thấy **Run status: Succeeded** thì job đã chạy thành công.
![0](/images/6-glue/6.2-jobs/im-13.png)

Kiểm tra kết quả bằng cách truy cập vào dịch vụ **S3**. Sau đó vào bảng **weather-s3-db**.

1. Ta thấy có 1 tệp vừa được khởi tạo, chúng ta dowload tệp về máy.
![0](/images/6-glue/6.2-jobs/im-12.png)

2. Mở tệp ta thấy dự liệu sau khi ETL thành công.
![0](/images/6-glue/6.2-jobs/im-11.png)



Tiếp theo, chúng ta sẽ thêm tính năng trigger.
