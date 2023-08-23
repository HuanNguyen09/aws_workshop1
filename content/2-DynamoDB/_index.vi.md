---
title: "Khởi tạo DynamoDB"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 2. </b> "
---



#### Khởi tạo Amazon DynamoDB
1. Nhập **Amazon DynamoDB** ở thanh tìm kiếm service trên AWS Console sau đó chọn **Amazon DynamoDB**.
![0](/images/2.dynamodb/im-40.png)

2. Chọn **Create table**
![1](/images/2.dynamodb/im-39.png)
3. Đặt tên cho table là `weather-Db`.

4. **Partition key**, hãy nhập khóa sử dụng trong bảng. Nhập `timestamp`

5. Sang phần **Table setting**, chọn **Default settings** giữ nguyên cài đặt mặc định cho các thiết lập khác.
![2](/images/2.dynamodb/im-38.png)
6. Click nút **Create table.**
![3](/images/2.dynamodb/im-37.png)

7. Đợi khoảng 3 phút để Amazon DynamoDB được tạo. Khi Amazon DynamoDB được tạo xong, chúng ta sẽ thấy trạng thái **Active** như hình.
![4](/images/2.dynamodb/im-36.png)