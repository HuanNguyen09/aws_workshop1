---
title : "Create Crawler"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 6.1. </b> "
---


#### Creating an IAM Role

To start, we need to create a role in **IAM**.

1. Enter "IAM" in the service search bar on the AWS Console, then select "IAM."

![VPC](/images/6-glue/6.1-crawler/im-41.png)

2. In the left navigation pane, select **Roles**. Then click **Create role**.

![VPC](/images/6-glue/6.1-crawler/im-40.png)

3. Choose **AWS service** and find AWS service **Glue**. Click *Next*.

![VPC](/images/6-glue/6.1-crawler/im-39.png)

4. Search for policies with the keyword `Power`. Select **PowerUserAccess** and click **Next**.

![VPC](/images/6-glue/6.1-crawler/im-38.png)

5. In the **Role name** field, enter: `Lab-role`.

![VPC](/images/6-glue/6.1-crawler/im-37.png)

6. Click **Create role**.

![VPC](/images/6-glue/6.1-crawler/im-36.png)

Next, we proceed to create the **crawler**.

1. Enter "Glue" in the service search bar on the AWS Console, then select "AWS Glue."

![VPC](/images/6-glue/6.1-crawler/im-35.png)

2. In the left navigation pane, select **Crawlers**. Click **Add database**.

![VPC](/images/6-glue/6.1-crawler/im-34.png)

3. Enter the database name as `datacatalog-dynamodb`. Click **Create database**.

![VPC](/images/6-glue/6.1-crawler/im-33.png)

4. Select the newly created database.

![VPC](/images/6-glue/6.1-crawler/im-32.png)

5. Click **Add tables using crawler**.

![VPC](/images/6-glue/6.1-crawler/im-31.png)

6. Enter the crawler name as `crawler-aotu-per-hour`. Click **Next**.

![VPC](/images/6-glue/6.1-crawler/im-30.png)

7. Click **Add a data source**.

![VPC](/images/6-glue/6.1-crawler/im-29.png)

8. Select **DynamoDB** and **weather-DB** (the name of the DynamoDB table created in part 2). Click **Add a DynamoDB data source**.

![VPC](/images/6-glue/6.1-crawler/im-28.png)

9. Choose the AIM role we created earlier: **Lab-role**. Click **Next**.

![VPC](/images/6-glue/6.1-crawler/im-27.png)

10. Enter the target database as `datacatalog-dynamodb`.

11. In the **Crawler schedule** section, select **Hourly** and **30** Minutes. Click **Next**.

![VPC](/images/6-glue/6.1-crawler/im-25.png)

12. Review the information and click **Create crawler**.

![VPC](/images/6-glue/6.1-crawler/im-24.png)

13. Click **Run crawler** and wait for about 2 minutes until the crawler completes its execution.

![VPC](/images/6-glue/6.1-crawler/im-23.png)

Check the result after the **crawler** execution.

1. Go to the database table we created in **datacatalog-dynamodb**.

![VPC](/images/6-glue/6.1-crawler/im-22.png)

2. We can see that the table **weather_db** has been successfully initialized.

![VPC](/images/6-glue/6.1-crawler/im-21.png)

3. Select the table **weather-db**, and we can see that the **crawler** has successfully extracted data from **DynamoDB** and built corresponding schemas.

![VPC](/images/6-glue/6.1-crawler/im-20.png)