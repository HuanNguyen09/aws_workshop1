---
title : "Create ETL job"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 6.2. </b> "
---

#### Creating an ETL Job

1. In the Glue service, in the left navigation pane, select **ETL jobs**, then choose **Visual with a source target**. Select **Source** as **AWS Glue Data Catalog** and **Target** as **Amazon S3**. Click **Create**.

![0](/images/6-glue/6.2-jobs/im-19.png)

2. Choose the source **Data Catalog table**. Then select the **database** and **Table** that we created in the previous part.

![0](/images/6-glue/6.2-jobs/im-18.png)

3. Choose the **action transform**. Here we can rename, change data types, and delete data fields.

![0](/images/6-glue/6.2-jobs/im-17.png)

4. Choose the **target S3 bucket**. Here we select **Format: CSV**, **Type: None**, and **S3 tagger: s3://weather-s3-db**.

![0](/images/6-glue/6.2-jobs/im-16.png)

5. Go to the **Job details** tab, change the job name to `DynamoDB-ETL-S3`. Choose **IAM Role: Lab-role**.

![0](/images/6-glue/6.2-jobs/im-15.png)

6. Go to the **script** tab, here we modify the code from:

--- 
    frame=ApplyMapping-node2,

to:

---     
    frame=ApplyMapping-node2.coalesce(1),

as shown in the image. Then click **Save** and **Run**.

![0](/images/6-glue/6.2-jobs/im-14.png)

7. Switch to the **Runs** tab, and after seeing the **Run status: Succeeded**, the job has run successfully.

![0](/images/6-glue/6.2-jobs/im-13.png)

Check the result by accessing the **S3** service. Then go to the **weather-s3-db** bucket.

1. We see that a file has just been created. Download the file to your machine.

![0](/images/6-glue/6.2-jobs/im-12.png)

2. Open the file, and we see the data after a successful ETL.

![0](/images/6-glue/6.2-jobs/im-11.png)

Next, we will add the trigger feature.