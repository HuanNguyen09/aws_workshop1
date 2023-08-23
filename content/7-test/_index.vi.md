---
title: "Kiểm tra kết quả "
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

#### Kiểm tra kết quả thực thi tự động của trigger và crawler

##### Crawler
Chúng ta có thể thấy **Crawler** tự động thực thi vào phút thứ 30 mỗi giờ như ta đã thiết lập. Trạng thái **Completed**.
![0](/images/7-test/im-03.png)

##### Trigger job
Chúng ta có thể thấy **ETL Job** tự động thực thi thông qua trigger vào phút thứ 40 mỗi giờ như ta đã thiết lập. Trạng thái **Succeeded**.
![0](/images/7-test/im-04.png)
Dữ liệu được lưu thành công về **S3 bucket** ngay sau đó.
![0](/images/7-test/im-02.png)
