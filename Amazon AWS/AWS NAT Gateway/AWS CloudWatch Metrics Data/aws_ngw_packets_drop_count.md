# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
<b>Packets Drop Count</b> metric tracks the number of packets that have been dropped by the NAT gateway due to various reasons, such as resource limitations or network conditions. When a NAT gateway drops packets, it means those packets were not forwarded to their intended destination or source due to constraints that prevented their proper handling.  This API provides the number of packets dropped by the NAT gateway

This API is integrated into the AWS Nat Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the PacketsDropCount metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway-cloudwatch.html#:~:text=is%20Sum.-,PacketsDropCount,-The%20number%20of