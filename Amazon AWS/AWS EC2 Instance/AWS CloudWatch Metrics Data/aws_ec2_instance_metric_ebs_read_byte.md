# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
The "EBS Read Bytes" metric in AWS provides essential insights into the amount of data read from Amazon Elastic Block Store (EBS) volumes attached to your EC2 instances. It measures the read throughput, indicating how much data is being retrieved from the EBS volumes over a specified period.

The API response contains the Bytes read from all EBS volumes attached to the instance in a specified period of time.

This API is integrated into the AWS Ec2 instance in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the EBSReadBytes metric, please refer to the following document: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics:~:text=Maximum-,EBSReadBytes,-Bytes%20read%20from