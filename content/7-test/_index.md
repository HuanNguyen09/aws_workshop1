---
title : "Test"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

#### Automatic Execution Results of the Crawler and Trigger Job

##### Crawler
We can observe that the **Crawler** automatically executes at 30 minutes past every hour, as we have set up. The status is **Completed**.
![0](/images/7-test/im-03.png)

##### Trigger Job
We can see that the **ETL Job** automatically executes via the trigger at 40 minutes past every hour, as we have configured. The status is **Succeeded**.
![0](/images/7-test/im-04.png)
The data is successfully stored in the **S3 bucket** right after execution.
![0](/images/7-test/im-02.png)

