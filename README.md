# api-gateway-tracking_info
fields @timestamp, @message, @logStream, @log
| sort @timestamp desc
| filter @message like 'ffnBzFZEoAMEDbw='
| limit 10000
 
https://repost.aws/knowledge-center/api-gateway-logs
 
Invoking a Lambda function using an Amazon API Gateway endpoint - AWS Lambda
docs.aws.amazon.com
https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html#apigateway-example-event
Troubleshoot API Gateway logs
I want to use Amazon API Gateway logs for troubleshooting API issues.
 
x-amz-apigw-id
 
is used in cloudwatch insight to track the client  request in request headers. 
 
(8670bd47-f948-4fe1-a849-455725e1ffdc) Received response. Status: 200, Integration latency: 356 ms
 
the format of a log line start with request id of the reqeust and other details. 
 
 
 
AWS Integration Endpoint RequestId : 4430a1ec-f7c4-4a01-93c0-8b5d12fa0901
 
this is used to track the endpoint, which in our case is lambda.
 
endpoint ID can be used to track bacl to lambda
 
trace ID is the best to use to find which stage is doing what. 
 
