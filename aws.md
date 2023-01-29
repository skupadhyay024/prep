How you can send request to S3 ?
IAM
What is AWS Lambda?
SNS and SQS 
``` Create an SNS topic first using SNS.Then create and subscribe multiple SQS standard queues to the SNS topic.Now whenever a message is sent to the SNS topic,the message will be fanned out to the SQS queues i.e. SNS will deliver the message to all the SQS queues that are subscribed to the topic. ```
DLQ


