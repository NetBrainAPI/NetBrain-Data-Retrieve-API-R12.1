# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
The "Network Out" metric in AWS provides crucial insights into the outgoing network traffic from your EC2 instances. It measures the amount of data transferred out of your instance to the internet or other AWS services.

The metric provides The number of bytes sent out by the instance on all network interfaces. This metric identifies the volume of outgoing network traffic from a single instance.



This API is integrated into the AWS Ec2 instance in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the NetworkOut metric, please refer to the following document: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics:~:text=Maximum-,NetworkOut,-The%20number%20of