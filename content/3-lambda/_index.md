---
title : "Build lambda function"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

In this section, we will use a Lambda function to call an API and retrieve the current weather data for Ho Chi Minh City from the [OpenWeatherMap](https://openweathermap.org/api) website. Then, the Lambda function will store the data in **DynamoDB**.

Here are some key concepts to know:

1. **Layer**: In AWS Lambda, a "Layer" is a mechanism that allows you to share code and libraries among multiple Lambda functions efficiently. This helps reduce the file size of each function, reduces build time, and improves code management.

2. **Policies**: "Policies" are JSON documents that define the access and actions that IAM (Identity and Access Management) entities can perform on Lambda functions and other related resources. Policies help control access and security for Lambda resources, ensuring that only authorized entities can perform necessary actions.

### Contents

- [Initialization](3.1-create/)
- [Adding Layers](3.2-addLayers/)
- [Adding Policies](3.3-addPolicies/)