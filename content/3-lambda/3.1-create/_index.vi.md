---
title: "Khởi tạo lambda funtion"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1 </b> "
---

#### Khởi tạo lambda function
1. Nhập **Lambda** ở thanh tìm kiếm service trên AWS Console sau đó chọn **Lambda**.
![0](/images/3.lamda/im-35.png)

2. Chọn **Create function**
![1](/images/3.lamda/im-34.png)
3. Click **Author from scratch**.
4. Đặt tên cho function là `GetAPI-weather-function`.
5. Chọn **Runtime: Python 3.9**. **Architecture: x86_64**
![1](/images/3.lamda/im-33.png)
6. Click nút **Create function.**
![1](/images/3.lamda/im-32.png)

7. Đợi khoảng 3 phút để function được tạo. Khi Amazon DynamoDB được tạo xong, chúng ta sẽ thấy trạng thái như hình.
![1](/images/3.lamda/im-31.png)
8. Chúng ta copy đoạn mã sau và paste vào **Code source**.
---
    import boto3
    import requests
    import json

    def lambda_handler(event, context):
        #  Call API to get raw data
        api_url = "https://api.openweathermap.org/data/2.5/weather?lat=10.76&lon=106.66&appid=b0e2fd79db41681ab871e658860bc3e7"
        response = requests.get(api_url)

        if response.status_code == 200:
            # Get data from API responses
            raw_data = response.json()

            # Extract values from API responses
            temperature = str(raw_data["main"]["temp"])  # Temperature
            weather_description = raw_data["weather"][0]["description"]  # description
            wind_speed = str(raw_data["wind"]["speed"]) 
            pressure = str(raw_data["main"]["pressure"])  
            humidity = str(raw_data["main"]["humidity"])  
            visibility = str(raw_data["visibility"])  
            country = raw_data["sys"]["country"]  
            city_name = raw_data["name"]  
            
            # Store data in a DynamoDB table
            dynamodb = boto3.resource("dynamodb")
            table_name = "weather-Db"  # Replace with your actual DynamoDB table name
            table = dynamodb.Table(table_name)
            print(table)
            try:
                table.put_item(
                    Item={
                        "timestamp":  str(event["time"]), 
                        "temperature": temperature,  
                        "weather_description": weather_description, 
                        "wind_speed": wind_speed,  
                        "pressure": pressure,  
                        "humidity": humidity,  
                        "visibility": visibility,  
                        "country": country, 
                        "city_name": city_name  
                    }
                )
                return {
                    "statusCode": 200,
                    "body": json.dumps('Data has been stored in DynamoDB successfully.')
                }
            except Exception as e:
                return {
                    "statusCode": 500,
                    "body": f"Error storing data: {str(e)}"
                }
        else:
            return {
                "statusCode": response.status_code,
                "body": json.dumps('Failed to retrieve data from the API.')
            }

Sau đó click **Deploy**.

{{% notice note %}}
Source code trên sẽ giúp chúng ta thực hiện gọi API lấy dữ liệu và lưu về DynamoDB
{{% /notice %}}


![1](/images/3.lamda/im-29.png)

[Tiếp theo ta thêm layer cho funcion](/3.lamda/3.2-addLayers/)