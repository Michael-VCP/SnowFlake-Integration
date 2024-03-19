# SnowFlake-Integration

1. Create an S3 bucket
   -Bucket name
   -Default settings
2. Go inside bucket to upload file "Customer_info" and upload
3. Go inside data uploaded to copy "S3 URI"
4. Create IAM rule
   -Create policy for accessing object in the S3 bucket
   -Edit JSON file to define actions
   -Define policy name
5. Crate IAM Role
   -Select AWS account for trusted entity for outside accounts
   -Require external ID
   -Grant permission to the newly created permission
   -Define name to your role
   -Click role to copy role ARN number. Used for snowflake. 
6. Open Snowflake worksheet
   -"CREATE DATABASE DEMO;"
   -"CREATE SCHEMA DEMO_12032022;"
   -Create syntax - CREATE OR REPLACE STORAGE INTEGRATION aws_s3_integration
   -type = external_stage
   -Storage_provide = 'S3'
   -enabled=true
   -storage_aws_role_arn= (Copy/paste aws ARN)
   -storage_allowed_location= (Copy/paste aws scheme)
   
