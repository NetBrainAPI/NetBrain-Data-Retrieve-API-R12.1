# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
In AWS Classic Load Balancer (CLB), "Spillover" refers to a mechanism where incoming requests that cannot be immediately processed due to backend server capacity limitations are queued up. When the queue reaches its maximum limit (configured as the spillover count), excess requests are then directed to additional backend instances or dropped, depending on the load balancer configuration. This API provides the number of requests that have been queued due to backend server capacity limitations exceeding a configured limit.

This API is integrated into the AWS Classic Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the SpilloverCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html#:~:text=of%20100%20requests.-,SpilloverCount,-The%20total%20number