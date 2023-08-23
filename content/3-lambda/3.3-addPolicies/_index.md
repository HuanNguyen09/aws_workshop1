---
title : "Add policies"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---


#### Adding Policies to the Function
To allow the Lambda function to store data in DynamoDB, we need to add the necessary permissions.

1. Select the **Configuration** tab --> **Permissions**.

2. Click on the **Role name** to switch to a new tab.
![1](/images/3.lamda/im-24.png)

3. Click **Add permissions** --> **Add policies**.
![1](/images/3.lamda/im-22.png)

4. Search for the keyword `DynamoDB`.

5. Check the box for **AmazonDynamoDBFullAccess**.

6. Click **Add permissions**.
![1](/images/3.lamda/im-21.png)

By adding the `AmazonDynamoDBFullAccess` policy, the Lambda function will now have the necessary permissions to store data in DynamoDB successfully.