---
title : "Add layers"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---

#### Adding Layers to the Function
The provided code uses two libraries, **boto3** and **requests**. Therefore, we need to add these two layers to the Lambda function to make it executable.

1. Click **Layers**.
![1](/images/3.lamda/im-28.png)

2. Click **Add Layers**.
![1](/images/3.lamda/im-27.png)

3. Select **Specify an ARN**.

4. For **Specify an ARN**, enter `arn:aws:lambda:ap-southeast-1:770693421928:layer:Klayers-p39-requests:15`.

5. Click **Verify**, and then click **Add**.
![1](/images/3.lamda/im-26.png)

6. Repeat the process for the **boto3** layer with the following ARN: `arn:aws:lambda:ap-southeast-1:770693421928:layer:Klayers-p39-boto3:17`.

7. Verify the added layers' information.
![1](/images/3.lamda/im-25.png)

[Next, we will proceed to add policies to the function](3.3-addPolicies/)