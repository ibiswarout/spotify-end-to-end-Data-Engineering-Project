# spotify-end-to-end-Data-Engineering-Project
This project demonstrates an end-to-end data engineering pipeline built on AWS to extract, transform, and analyze Spotify data using Python and serverless architecture.

📌 Project Architecture

![image](https://github.com/user-attachments/assets/0f2afab5-7417-4fbe-9070-efb0d16627d1)


**High-Level Flow:**

**1. Extract:**

- Spotify data is ingested using Python scripts deployed as AWS Lambda functions.

- CloudWatch Events (EventBridge) triggers these Lambdas on a daily schedule.

- Extracted data is stored in a raw zone within Amazon S3.

**2. Transform:**
   
- Another Lambda function is triggered to perform transformations on the raw data.
   
- The transformed data is saved in a curated zone in S3.

**3. Load:**
   
- An AWS Glue Crawler scans the curated S3 bucket to create and update table schemas in the AWS Glue Data Catalog.
   
- Data is made queryable using Amazon Athena for ad-hoc SQL-based analysis.

**🚀 Features**

✅ Serverless data extraction from the Spotify API

✅ Event-driven architecture using EventBridge for automation

✅ Secure data lake on Amazon S3 with raw and curated zones

✅ Scalable data cataloging and schema discovery with AWS Glue

✅ Fast analytics using Athena without needing to provision servers

✅ Modular and reusable Python code for Lambda functions


**🏗️ Tech Stack**

- Python (for Lambda ETL scripts)

- AWS Lambda

- Amazon S3

- Amazon EventBridge / CloudWatch Events

- AWS Glue (Crawler + Data Catalog)

- Amazon Athena (for analytics queries)


