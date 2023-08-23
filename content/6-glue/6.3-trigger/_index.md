---
title : "Create Trigger"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 6.3. </b> "
---

#### Logging

1. In the Glue service, in the left navigation pane, select **Triggers**, then click **Add trigger**.

![0](/images/6-glue/6.3-trigger/im-10.png)

2. Enter a name for the trigger: `trigger-job-per-hour`.

![0](/images/6-glue/6.3-trigger/im-09.png)

3. Select **Schedule** to create an automatic schedule. In the **Schedule** section, choose **Hourly**, **40 Minute**. Click **Next**. This setting will create an hourly schedule to run the trigger at minute 40.

![0](/images/6-glue/6.3-trigger/im-08.png)

4. Choose **Add a target resource**.

![0](/images/6-glue/6.3-trigger/im-07.png)

5. Select **Type: Job, Job name: DynamoDB-ETL-S3**. Click **Add**.

![0](/images/6-glue/6.3-trigger/im-06.png)

6. Check **Enable trigger on creation** to enable the trigger immediately after creation. Click **Create**.

![0](/images/6-glue/6.3-trigger/im-05.png)

Next, we will add new features to our web application with Amazon Rekognition.