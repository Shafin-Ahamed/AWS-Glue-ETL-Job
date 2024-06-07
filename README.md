# AWS-Glue-ETL-Job
This repository represents an ETL job that I put together in AWS Glue to convert CSV files to JSON files

1. Used S3 buckets for both an input (CSV files) and output (JSON files)
2. Set up an ETL job via AWS Glue to perform the conversion (Also assigned the appropriate IAM role + policies to the job so it has proper access to S3 and Lambda)
3. Setting up the ETL job also created a scripts bucket to house all of the job logs and information.
4. Created a Lambda function that has a trigger attached to the S3 input bucket. The python code is written so that it will trigger the AWS Glue job whenever any file is dropped into the input bucket.
   (Also assigned IAM role + policies)
5. Dropped a Game of Thrones CSV file into input bucket
6. Check CloudWatch Monitor logs to see if code ran successfully
7. Check ETL jobs in AWS Glue to see if job ran successfully
8. Check output bucket for output file. Take file and decompress it since it was compressed with gzip.
9. Success! JSON file is created!

In the jobs ran screenshot, I ran my job on other csv files to see if it worked properly, fyi.
I've also attached my original csv file, and the outputted JSON format of the file.
