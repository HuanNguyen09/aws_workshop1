---
title : "AWS Glue Service Configuration"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---

### Overview

**AWS Glue** is a powerful data integration and processing service on AWS. It offers several features to manage and process data in a cloud environment. Below is a brief introduction to three key features of AWS Glue:

**Crawler**: This feature automatically detects and analyzes the data structure from unstructured data sources such as Amazon S3, file systems, relational databases, and more. It scans the data sources and automatically creates table metadata in the AWS Glue Data Catalog. This makes it easy to process data without the need for manually specifying the data structure.

**ETL Jobs (Extract, Transform, Load)**: ETL Jobs enable building automated data processing workflows to extract data from sources, transform data according to specific rules and standards, and then load the processed data into a target destination. ETL Jobs can run automatically and are often used to normalize and optimize data before analysis.

**Trigger**: Triggers allow for the automatic activation of Glue jobs (ETL Jobs) or other data processing workflows when specific events occur. These events can be additions, modifications, or deletions of data in your data source. Triggers help create automated and flexible workflows, synchronizing data processing with changes in the data source.

### Contents

- [Create a Crawler](6.1-crawler/)
- [Create an ETL Job](6.2-jobs/)
- [Create a Trigger](6.3-trigger/)