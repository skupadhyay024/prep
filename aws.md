### AWS
* How you can send request to S3 ?
**Amazon S3 is a REST service. You can send requests to Amazon S3 using the REST API or the AWS SDK**
* IAM
* What is AWS Lambda?
* SNS and SQS 
``` Create an SNS topic first using SNS.Then create and subscribe multiple SQS standard queues to the SNS topic.Now whenever a message is sent to the SNS topic,the message will be fanned out to the SQS queues i.e. SNS will deliver the message to all the SQS queues that are subscribed to the topic. ```
* DLQ
**Amazon SQS supports dead-letter queues (DLQ), which other queues (source queues) can target for messages 
that can't be processed (consumed) successfully. Dead-letter queues are useful for debugging your 
application or messaging system because they let you isolate unconsumed messages to determine why their processing doesn't succeed.**
* Lambda timeout
**Lambda runs your code for a set amount of time before timing out. Timeout is the maximum amount of time in seconds that a Lambda function can run. 
The default value for this setting is 3 seconds, but you can adjust this in increments of 1 second up to a maximum value of 15 minutes.**
* Lambda function failed how to check



