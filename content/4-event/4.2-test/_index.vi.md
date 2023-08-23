---
title: "Kiểm tra "
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---



#### Kiểm tra tình trạng hoạt động
Kiểm tra qua dịch vụ **CloudWatch** - nơi lưu trữ file logs.
1. Về lại trang **Lambda**. Vào **function** mà chúng ta đã tạo trước đó. Chuyển qua tab **Monitor**. Và chọn **View CloudWatch logs**
![0](/images/4-event/im-08.png)

2. Click vào bản **logs stream**.
![0](/images/4-event/im-07.png)
3. Dữ liệu trạng thái được lưu trữ tại đây.
![0](/images/4-event/im-06.png)



Kiểm tra qua dữ liệu lưu về **DynamoDB** khi **lambda function** thực thi thành công.
1. Về lại trang **DynamoDB**. Vào table mà chúng ta đã tạo trước đó. Chọn **Explore table items**.

![0](/images/4-event/im-05.png)
2. Kéo xuống cuối trang. Chúng ta sẽ thấy dữ liệu được lấy về thông qua **Lambda function**. 
![0](/images/4-event/im-04.png)
[Tiếp theo, chúng ta sẽ đến phần thêm policies cho funcion](3.1-create/)