---
title: "Tạo trigger"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 6.3 </b> "
---

#### **Logging**

1. Tại trang dịch vụ **Glue**, trên thanh điều hướng bên trái, ta chọn **Triggers**. Sau đó, click **Add trigger**
![0](/images/6-glue/6.3-trigger/im-10.png)

2. Điền tên cho trigger: `trigger-job-per-hour`
![0](/images/6-glue/6.3-trigger/im-09.png)

3. Chọn **Schedule** để tạo lịch tự động. Trong phần **Schudule** ta lân lượt chọn **Hourly**, **40 Minute**. Chọn **Next**. Thiết lập này sẽ tạo lịch chạy hằng giờ tại phút 40.
![0](/images/6-glue/6.3-trigger/im-08.png)

4. Chọn **Add a taget rtesource**.
![0](/images/6-glue/6.3-trigger/im-07.png)

5. Chúng ta chọn **Type: Job, Job name: DynamoDB-ETL-S3**. Click **Add**.
![0](/images/6-glue/6.3-trigger/im-06.png)

6. Tích chọn **Enable trigger on creation** để bật trigger ngay sau khi tạo thành công. Click **Create**.
![0](/images/6-glue/6.3-trigger/im-05.png)


Tiếp theo, chúng ta sẽ thêm tính năng mới vào ứng dụng web của chúng ta với Amazon Rekognition.
