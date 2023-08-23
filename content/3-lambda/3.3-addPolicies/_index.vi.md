---
title: "Thêm Policies"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3.3 </b> "
---


#### Thêm policies cho function
Để **lambda** có thể lưu dữ liệu vào **DynamoDB**, ta cần thêm quyền cho nó.
1. Chọn tab **Configuration** --> **Permisstions**.
2. Click vào **Role name** để chuyển qua tab mới.
![1](/images/3.lamda/im-24.png)

3. Click **Add permisstions** --> **Add policies**.
![1](/images/3.lamda/im-22.png)

4. Tìm kiếm với từ khóa `DynamoDB`
5. Tích chọn **AmazonDynamoDBFullAccess**
6. Chọn **Add permisstions**.
![1](/images/3.lamda/im-21.png)

