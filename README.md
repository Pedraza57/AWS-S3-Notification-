
# AWS S3 Notification ☁️
> [!IMPORTANT]
This script automates the setup of an AWS infrastructure for triggering a Lambda function in response to new objects being created in an S3 bucket. The Lambda function, in turn, publishes a notification to an SNS topic, and a subscription to this topic sends an email notification.

 ☣︎ This infrastructure is used by big comapnies such as Netflix to let their subscibers know a new show/movie is out. 

## 💻 What the Script Does 💻

1. Creates an IAM Role with the necessary permissions for Lambda function execution.
2. Attaches policies to the IAM Role for AWS Lambda and SNS access.
3. Creates an S3 bucket for storing objects.
4. Zips the Lambda function code for deployment.
5. Creates a Lambda function with the specified configuration.
6. Grants S3 permission to invoke the Lambda function.
7. Configures an S3 event trigger for the Lambda function.
8. Creates an SNS topic and subscribes the specified email address to it.
9. Publishes a test message to the SNS topic.


## Screenshots

![Screenshot 2023-04-14 at 7 06 46 PM](https://user-images.githubusercontent.com/43399466/232058778-a7299e9b-9892-471c-a05d-14d773b5b333.png)


## Documentation

º https://aws.amazon.com/cli/  
º https://docs.aws.amazon.com/lambda/  
º https://docs.aws.amazon.com/s3/  
º https://docs.aws.amazon.com/sns/

## Installation

Before running this script, make sure you have the AWS CLI installed and configured with the necessary credentials. Additionally, ensure that the jq tool is installed.

Edit the following variables in the script to match your project requirements:

- **"aws_region":** AWS region where the resources will be created.   
- **"bucket_name":** The name of the S3 bucket for which notifications will be configured.
- **"lambda_func_name":** The name of the Lambda function triggered by S3 events.   
- **"role_name":** The IAM role name associated with the Lambda function.   
- **"email_address":** The email address to receive SNS notifications.

```bash
  ./<name-of-your-script>
```
    
