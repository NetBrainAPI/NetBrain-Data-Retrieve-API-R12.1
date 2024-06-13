# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
The "EBS Write Bytes" metric in AWS is a crucial indicator of the amount of data being written to Amazon Elastic Block Store (EBS) volumes attached to your EC2 instances. This metric measures the write throughput, showing how much data is being stored or modified on the EBS volumes over a specified time period.



The API response contains the Bytes written to all EBS volumes attached to the instance in a specified period of time.



This API is integrated into the AWS Ec2 instance in NetBrain.It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the EBSWriteBytes metric, please refer to the following document: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics:~:text=Maximum-,EBSWriteBytes,-Bytes%20written%20to

