---
title : "Create DynamoDB"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2. </b> "
---



#### Initializing Amazon DynamoDB
1. Enter "Amazon DynamoDB" in the service search bar on the AWS Console, then select "Amazon DynamoDB."
![0](/images/2.dynamodb/im-40.png)

2. Choose "Create table."
![1](/images/2.dynamodb/im-39.png)

3. Set the table name as `weather-Db`.

4. For the **Partition key**, enter the key to be used in the table. Enter `timestamp`.

5. In the **Table setting** section, choose **Default settings** to keep the default settings for other configurations.
![2](/images/2.dynamodb/im-38.png)

6. Click the **Create table** button.
![3](/images/2.dynamodb/im-37.png)

7. Wait for about 3 minutes for Amazon DynamoDB to be created. Once Amazon DynamoDB is successfully created, you will see the status as **Active** as shown in the image.
![4](/images/2.dynamodb/im-36.png)

