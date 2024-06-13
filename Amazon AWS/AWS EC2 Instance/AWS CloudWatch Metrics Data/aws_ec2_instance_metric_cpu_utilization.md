# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
CPU utilization metrics in AWS are crucial for monitoring the performance and health of your EC2 instances. These metrics help you understand how much of the CPU's capacity is being used by your instances and can guide you in optimizing resource allocation, scaling, and cost management. This metrics provides the percentage of physical CPU time that Amazon EC2 uses to run the EC2 instance, which includes time spent to run both the user code and the Amazon EC2 code. 



This API is integrated into the AWS Ec2 instance in NetBrain.It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.




For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html