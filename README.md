# spotify-end-to-end-Data-Engineering-Project
This project demonstrates an end-to-end data engineering pipeline built on AWS to extract, transform, and analyze Spotify data using Python and serverless architecture.

📌 Project Architecture

![image](https://github.com/user-attachments/assets/0f2afab5-7417-4fbe-9070-efb0d16627d1)


High-Level Flow:

1. Extract:

-- Spotify data is ingested using Python scripts deployed as AWS Lambda functions.

-- CloudWatch Events (EventBridge) triggers these Lambdas on a daily schedule.

-- Extracted data is stored in a raw zone within Amazon S3.

2. Transform:
-- Another Lambda function is triggered to perform transformations on the raw data.
   
-- The transformed data is saved in a curated zone in S3.

4. Load:
-- An AWS Glue Crawler scans the curated S3 bucket to create and update table schemas in the AWS Glue Data Catalog.
   
-- Data is made queryable using Amazon Athena for ad-hoc SQL-based analysis.




