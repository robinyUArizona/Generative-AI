

## Blog Content Generation steps:
- Created an API using Postman to accept user queries for generating blog content.
- Utilized Amazon API Gateway for deploying and managing the API.
- Upon triggering the API, it invokes an AWS Lambda function.
- The Lambda function interacts with Amazon Bedrock to generate the blog content.
- Once the blog content is created, it is saved to an Amazon S3 bucket.

  ![Alt text](https://github.com/robinyUArizona/Generative-AI/blob/main/Blog%20Generation%20LLM%20Amazon%20Bedrock/Blog%20Content%20Generation.png)

### Steps:
  1. Create a lambda function in AWS Lambda, use "Author from scratch" option
  2. Implement "app.py" in local vscode and later copy paste code in AWS Lambda
  3. 

#### API request
{
 "modelId": "meta.llama3-8b-instruct-v1:0",
 "contentType": "application/json",
 "accept": "application/json",
 "body": "{\"prompt\":\"this is where you place your input text\",\"max_gen_len\":512,\"temperature\":0.5,\"top_p\":0.9}"
}
#### Reference: 
  https://www.youtube.com/watch?v=3OP39y4dO_Y&list=PLZoTAELRMXVP5zpBfH7pab4aB1LbmCM1z&index=5
