---
title : " Resource cleanup"
date : "`r Sys.Date()`"
weight : 8
chapter : false
pre : " <b> 8. </b> "
---


#### ETL Jobs

1. Access the **ETL jobs** tab in **AWS Glue** and select the jobs that were created during the lab. Then choose **Action** --> **Delete job(s)**.

![0](/images/8-terminate/im-01.png)

2. Enter `Delete`, and then select **Delete**.

![0](/images/8-terminate/im-00.png)

### Perform similar actions with the resources created in the lab in the following order:

1. Trigger

2. Crawler

3. Data Catalog

4. S3 bucket

   **Note**: When deleting the **S3 bucket**, make sure to delete all files stored in the bucket first.

5. Lambda function

6. DynamoDB

With this, we have cleaned up all the resources used in this workshop.