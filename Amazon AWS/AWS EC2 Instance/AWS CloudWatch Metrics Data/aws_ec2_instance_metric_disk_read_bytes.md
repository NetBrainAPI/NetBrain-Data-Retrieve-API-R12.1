# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
The "Disk Read Bytes" metric in AWS is a critical metric for monitoring the disk I/O performance of your EC2 instances. 
This metric provides insights into the amount of data read from the instance store volumes. The metric provides Bytes read from all instance store volumes available to the instance.

This API is integrated into the AWS Ec2 instance in NetBrain.It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the DiskReadBytes metric, please refer to the the following document: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics:~:text=Maximum-,DiskReadBytes,-Bytes%20read%20from