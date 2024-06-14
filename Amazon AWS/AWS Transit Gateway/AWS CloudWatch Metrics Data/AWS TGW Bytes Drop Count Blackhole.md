# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The AWS TGW (Transit Gateway) <b>Bytes Drop Count Blackhole</b> metric refers to the number of bytes dropped by a Transit Gateway due to the absence of a route or a routing blackhole. When a packet arrives at the Transit Gateway and there is no route that matches the destination, or if the route points to a blackhole (such as an invalid or inactive destination), the Transit Gateway drops the packet. This API provides the number of bytes dropped by the Transit Gateway because the packets were sent to a destination without a valid route or to a blackhole route.



This API is integrated into the AWS Classic Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the BytesDropCountBlackhole metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html