---
title: "Xây dựng lambda function"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Trong phần này, chúng ta sẽ sử dụng lambda function để gọi API lấy dữu liệu thời tiết hiện tại ở thành phố Hồ Chí Minh từ web [**OpenWeatherMap**](https://openweathermap.org/api). Sau đó, lambda function sẽ lưu dữ liệu trong **DynamoDB**.

Một số khái niệm cần biết:
1. **Layer (lớp)** trong AWS Lambda là một cơ chế giúp bạn chia sẻ mã code và thư viện giữa nhiều hàm Lambda khác nhau một cách hiệu quả. Điều này giúp giảm dung lượng tệp của mỗi hàm, giảm thời gian xây dựng và cải thiện quản lý mã.

2. **Policies (chính sách)** là các tài liệu JSON định nghĩa quyền truy cập và hành động mà các đối tượng IAM (Identity and Access Management) có thể thực hiện trên các hàm Lambda và các tài nguyên liên quan khác. Policies giúp kiểm soát quyền truy cập và bảo mật cho các tài nguyên của Lambda, đảm bảo rằng chỉ những đối tượng được ủy quyền mới có thể thực hiện các hành động cần thiết.

### Nội dung

- [Khởi tạo](3.1-create/)
- [Thêm layers](3.2-addLayers/)
- [Thêm policies](3.3-addPolicies/)


