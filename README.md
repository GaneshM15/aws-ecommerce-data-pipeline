\# AWS E-Commerce Data Pipeline



This project is a production-level automated data pipeline built using AWS services.



\## Architecture



S3 Raw Bucket → Lambda → Step Functions → AWS Glue PySpark Job 1 → S3 Processed Bucket → AWS Glue PySpark Job 2 → Amazon Redshift → SNS Notification



\## AWS Services Used



\- Amazon S3

\- AWS Lambda

\- AWS Step Functions

\- AWS Glue

\- Amazon Redshift

\- Amazon SNS

\- Amazon CloudWatch

\- IAM



\## Pipeline Flow



1\. CSV file is uploaded to S3 raw bucket.

2\. Lambda automatically triggers Step Function.

3\. Step Function starts Glue Job 1.

4\. Glue Job 1 cleans and transforms raw CSV data.

5\. Processed data is stored in S3 in Parquet format.

6\. Glue Job 2 loads processed data into Amazon Redshift.

7\. SNS sends success or failure notification.

8\. CloudWatch stores execution logs.



\## Key Features



\- Fully automated pipeline

\- Event-driven architecture

\- PySpark data transformation

\- PII masking

\- Data validation

\- Parquet output

\- Redshift data warehouse loading

\- Error handling and notifications

