# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
<b>Connection Established Count</b> metric refers to the number of TCP connections that have been successfully established through the NAT gateway over a specific period. This metric is essential for understanding the actual number of active connections that have been successfully set up through the NAT gateway. This API provides the number of TCP connections that have successfully been established through the NAT gateway.



This API is integrated into the AWS Nat Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ConnectionEstablishedCount metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway-cloudwatch.html#:~:text=is%20Sum.-,ConnectionEstablishedCount,-The%20number%20of

