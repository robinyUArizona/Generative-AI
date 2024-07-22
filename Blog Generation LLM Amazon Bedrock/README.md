

## Blog Content Generation steps:
- Created an API using Postman to accept user queries for generating blog content.
- Utilized Amazon API Gateway for deploying and managing the API.
- Upon triggering the API, it invokes an AWS Lambda function.
- The Lambda function interacts with Amazon Bedrock to generate the blog content.
- Once the blog content is created, it is saved to an Amazon S3 bucket.