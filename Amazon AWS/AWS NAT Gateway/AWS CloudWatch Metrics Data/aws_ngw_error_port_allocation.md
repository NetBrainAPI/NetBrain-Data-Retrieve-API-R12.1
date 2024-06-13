# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
This API provides the number of times the NAT gateway could not allocate a source port.

This API is integrated into the AWS Nat Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ErrorPortAllocation metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway-cloudwatch.html#:~:text=is%20Sum.-,ErrorPortAllocation,-The%20number%20of