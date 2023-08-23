---
title: "Session Management"
date: "`r Sys.Date()`"
weight: 1
chapter: false
---

# Implementing Data Pipelines using AWS Services

### Overall

In this workshop, we will create an automated data pipeline that fetches data through an API, utilizing various AWS services such as AWS Lambda, Amazon DynamoDB, Amazon S3 (Simple Storage Service), Amazon EventBridge, and AWS Glue.

- **AWS Lambda**: It is a serverless cloud computing service by Amazon Web Services. Lambda allows you to run code without managing servers, automatically scales when needed, and charges based on real-time execution. Lambda is often triggered by events such as HTTP requests or events from other AWS services.

- **Amazon DynamoDB**: It is a NoSQL cloud database service by AWS. It provides flexible and scalable data storage and querying capabilities for web and mobile applications. DynamoDB is designed to offer automatic scaling and reliability, supporting applications with high query volume and real-time requirements.

- **Amazon S3 (Simple Storage Service)**: It is an AWS cloud storage service that offers unlimited storage for data objects like images, videos, files, and storage data. S3 is widely used as a reliable, easy-to-use, and scalable storage solution for web and mobile applications.

- **Amazon EventBridge**: Amazon EventBridge is an event bus service by AWS that allows applications to send and receive events from different sources in the system. It helps you connect and integrate various applications and services, automatically trigger actions, and process data based on predefined rules.

- **AWS Glue**: It is a cloud-based ETL (Extract, Transform, Load) service by AWS. It enables you to extract data from various sources, transform data based on predefined rules, and load data into different storage repositories. Glue automatically detects the data structure, minimizing the efforts and time required for ETL processes.

![ConnectPrivate](/images/1.intro/0-image.png)

### Content

1.  [Introduce](1-introduce/)
2.  [Create DynamoDB ](2-DynamoDB/)
3.  [Build lambda function](3-lambda/)
4.  [Use EventBridge to create automated calendars and audit](4-event/)
5.  [Create S3](5-s3/)
6.  [AWS Glue Service Configuration](6-glue/)
7.  [Test](7-test/)
8.  [Resource cleanup](8-terminate/)

