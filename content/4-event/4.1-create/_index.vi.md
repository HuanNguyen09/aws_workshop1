---
title: "Khởi tạo Schedules"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

#### Khởi tạo Schedules
1. Nhập **EventBridge** ở thanh tìm kiếm service trên AWS Console sau đó chọn **Amazon EventBridge**.
![0](/images/4-event/im-20.png)

2. Chọn tab **Schedules** phía bên trái. Sau đó chọn **Create schedules**
![0](/images/4-event/im-19.png)
3. Đặt tên cho schedules là `aotu-getAPI-weather-per-minute`.
![0](/images/4-event/im-18.png)
4. Ở phần **Schedule pattern**, chúng ta cấu hình như sau
![0](/images/4-event/im-17.png)

5. Kéo xuống cuối và chọn **Next**.
![0](/images/4-event/im-16.png)
6. Chọn **Templated targets** --> **AWS Lambda**
![0](/images/4-event/im-15.png)
7. Chọn **lambda function** ta đã tạo trước đó. 
![0](/images/4-event/im-14.png)
8. Kéo xuống cuối trang và chọn **Next**.
![0](/images/4-event/im-13.png)
9. Tắt **Retry Policy**.
![0](/images/4-event/im-12.png)
10. Kéo xuống cuối trang và chọn **Next**.
![0](/images/4-event/im-11.png)
11. Kiểm tra lại thông tin và chọn **Create schedules**.
![0](/images/4-event/im-10.png)
12. Đợi khoảng 3 phút để schedules được tạo. Khi tạo xong, chúng ta sẽ thấy trạng thái **Enabled** như hình.
![0](/images/4-event/im-09.png)
[Tiếp theo ta kiểm tra schedules có hoạt động không](./4.2-test/)