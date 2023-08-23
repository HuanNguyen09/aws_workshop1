---
title : "Test"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2. </b> "
---

#### Checking Activity Status

Check through the **CloudWatch** service - where logs are stored.

1. Go back to the **Lambda** page. Access the **function** that we created earlier. Switch to the **Monitor** tab. Then select **View CloudWatch logs**.
![0](/images/4-event/im-08.png)

2. Click on the respective **logs stream**.
![0](/images/4-event/im-07.png)

3. The status data is stored here.
![0](/images/4-event/im-06.png)

Check the data stored in **DynamoDB** when the **Lambda function** executed successfully.

1. Go back to the **DynamoDB** page. Access the table that we created earlier. Choose **Explore table items**.
![0](/images/4-event/im-05.png)

2. Scroll down to the bottom of the page. Here, we can see the data fetched through the **Lambda function**.
![0](/images/4-event/im-04.png)

[Next, we will proceed to add policies to the function](3.3-addPolicies/)