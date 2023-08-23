---
title: "Thêm layers"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---



#### Thêm layers cho function
Trong đoạn mã có sử dụng 2 thư viện là **boto3 và requests**. Vì vậy, ta cần thêm 2 layers này vào để hàm lambda có thể thực thi được.
1. Click **Layers**.
![1](/images/3.lamda/im-28.png)

2. Click **Add Layers**.
![1](/images/3.lamda/im-27.png)

3. Chọn **Specify an ARN**.
4. Tại **Specify an ARN** chúng ta điền `arn:aws:lambda:ap-southeast-1:770693421928:layer:Klayers-p39-requests:15`
5. Chọn **Verify.** Sau có chọn **Add**
![1](/images/3.lamda/im-26.png)
6. Làm tương tự với layer **boto3** với ARN sau: `arn:aws:lambda:ap-southeast-1:770693421928:layer:Klayers-p39-boto3:17`
7. Kiểm tra thông tin layers được thêm.
![1](/images/3.lamda/im-25.png)

[Tiếp theo, chúng ta sẽ đến phần thêm policies cho funcion](3.1-create/)