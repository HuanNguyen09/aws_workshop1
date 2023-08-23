---
title : "Create Schedules"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1. </b> "
---
#### Initializing Schedules
1. Enter "EventBridge" in the service search bar on the AWS Console, then select "Amazon EventBridge."
![0](/images/4-event/im-20.png)

2. Choose the **Schedules** tab on the left side. Then select **Create schedule**.
![0](/images/4-event/im-19.png)

3. Set the schedule name as `auto-getAPI-weather-per-minute`.
![0](/images/4-event/im-18.png)

4. In the **Schedule pattern** section, configure it as follows:
![0](/images/4-event/im-17.png)

5. Scroll down to the bottom and click **Next**.
![0](/images/4-event/im-16.png)

6. Choose **Templated targets** --> **AWS Lambda**.
![0](/images/4-event/im-15.png)

7. Select the Lambda function that we created earlier.
![0](/images/4-event/im-14.png)

8. Scroll down to the bottom and click **Next**.
![0](/images/4-event/im-13.png)

9. Turn off **Retry Policy**.
![0](/images/4-event/im-12.png)

10. Scroll down to the bottom and click **Next**.
![0](/images/4-event/im-11.png)

11. Review the information and click **Create schedule**.
![0](/images/4-event/im-10.png)

12. Wait for about 3 minutes for the schedule to be created. Once it's done, you will see the status as **Enabled** as shown in the image.
![0](/images/4-event/im-09.png)

[Next, let's check if the schedules are working](./4.2-test/)