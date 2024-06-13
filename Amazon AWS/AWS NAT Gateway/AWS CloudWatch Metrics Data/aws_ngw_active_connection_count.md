# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
<b>Active Connection Count</b> metric refers to the number of active TCP connections through the NAT gateway at any given time. NAT Gateways are used to allow instances in private subnets to communicate with the internet or other AWS services, and they handle network address translation for outgoing traffic. This API provides the number of active TCP connections passing through the NAT gateway. Active connections are those where data is actively being transmitted or received.



This API is integrated into the AWS Nat Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ActiveConnectionCount metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway-cloudwatch.html#:~:text=ActiveConnectionCount

