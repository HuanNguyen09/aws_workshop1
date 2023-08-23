---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---


**The data pipeline** utilizes a combination of **AWS services, including AWS Lambda, Amazon DynamoDB, Amazon S3 (Simple Storage Service), Amazon EventBridge, and AWS Glue**. In this pipeline, AWS Lambda is used to invoke APIs and store data into DynamoDB. This Lambda function is triggered automatically every hour through Amazon EventBridge, which is configured to create a recurring schedule. Subsequently, data from DynamoDB undergoes ETL (Extract, Transform, Load) processing by AWS Glue and is then stored in Amazon S3.

#### The diagram below illustrates the data pipeline architecture:
![0](/images/1.intro/0-image.png)


### Content

1.  [Introduce](1-introduce/)
2.  [Create DynamoDB ](2-DynamoDB/)
3.  [Build lambda function](3-lambda/)
4.  [Use EventBridge to create automated calendars and audit](4-event/)
5.  [Create S3](5-s3/)
6.  [AWS Glue Service Configuration](6-glue/)
7.  [Test](7-test/)
8.  [Resource cleanup](8-terminate/)

