---
title: "Tạo Crawler"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 6.1 </b> "
---
#### Trước tiên, ta tạo role trong **AIM**
1. Nhập **AIM** ở thanh tìm kiếm service trên AWS Console sau đó chọn **AIM**.

![VPC](/images/6-glue/6.1-crawler/im-41.png)
2. Ở thanh điều hướng bên trái, chọn **Rules.**. Chọn **Create role**
![VPC](/images/6-glue/6.1-crawler/im-40.png)

3. Chọn **AWS service**. Tìm AWS service **Glue**. Chọn *Next**

![VPC](/images/6-glue/6.1-crawler/im-39.png)

4. Tìm **policies** với từ khóa `Power`. Tích vào **PowerUserAccess**. Chọn **Next**.

![VPC](/images/6-glue/6.1-crawler/im-38.png)
5. **Role name** điền: `Lab-role`.
![VPC](/images/6-glue/6.1-crawler/im-37.png)
6. Chọn **Create role**.
![VPC](/images/6-glue/6.1-crawler/im-36.png)
Tiếp theo, chúng ta tiến hành tạo **crawler**.
1. Nhập **Glue** ở thanh tìm kiếm service trên AWS Console sau đó chọn **AWS Glue**.
![VPC](/images/6-glue/6.1-crawler/im-35.png)
2. Ở thanh điều hướng bên trái, chọn **Rules.**. Chọn **Add database**
![VPC](/images/6-glue/6.1-crawler/im-34.png)
3. Điền tên database: `datacatalog-dynamodb`. Chọn **Create database**.

![VPC](/images/6-glue/6.1-crawler/im-33.png)
4. Chọn tên **databases** vừa khởi tạo.
![VPC](/images/6-glue/6.1-crawler/im-32.png)
5. Chọn **Add tables using crawler**. 
![VPC](/images/6-glue/6.1-crawler/im-31.png)
6. Điền tên **crawler**: `crawler-aotu-per-hour`. Chọn **Next**.
![VPC](/images/6-glue/6.1-crawler/im-30.png)
7. Chọn **Add a data source**.
![VPC](/images/6-glue/6.1-crawler/im-29.png)
8. Chọn **DynamoDB** và **weather-DB** (tên bảng DynamoDB đã khởi tạo ở phần 2). Chọn **Add a DynamoDB data source**.
![VPC](/images/6-glue/6.1-crawler/im-28.png)
9. Chọn **AIM role** ta khởi tạo ở trên: **Lab-role**. Chọn **Next**.
![VPC](/images/6-glue/6.1-crawler/im-27.png)
10. Điền taget database: `datacatalog-dynamodb`.

11. Phần **Crawler schedule**: ta lần lượt chọn **Hourly** và **30** Minute. Chọn **Next**.
![VPC](/images/6-glue/6.1-crawler/im-25.png)
12. Kiểm tra lại thông tin và chọn **create crawler**.
![VPC](/images/6-glue/6.1-crawler/im-24.png)

13. Chọn **Run crawler** và đợi khoảng 2 phút đến khi crawler thực hiện xong.
![VPC](/images/6-glue/6.1-crawler/im-23.png)

Kiểm tra kết quả sau khi **crawler** thực thi.
1. Vào bảng database mà ta đã tạo ở trên **datacatalog-dynamodb**.
![VPC](/images/6-glue/6.1-crawler/im-22.png)

2. Ta thấy bảng **weather_db** đã được khởi tạo.

![VPC](/images/6-glue/6.1-crawler/im-21.png)
3. Chọn vào bảng **weather-db**, chúng ta thấy **crawler** đã trích xuất dữ liệu thành công từ **DynamoDb** và xây dụng các schema tương ứng.
![VPC](/images/6-glue/6.1-crawler/im-20.png)

