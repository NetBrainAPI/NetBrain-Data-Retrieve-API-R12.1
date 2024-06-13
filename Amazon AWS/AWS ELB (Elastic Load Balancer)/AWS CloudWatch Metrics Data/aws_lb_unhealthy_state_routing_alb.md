# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Unhealthy State Routing" metric in AWS typically relates to the health of targets associated with a routing policy, often seen in services like Amazon Route 53 or Network Load Balancers (NLB). It indicates the number of routing decisions that have been made based on health checks where the target is deemed unhealthy.

The API response contains the count of routing decisions made based on health checks where the target is considered unhealthy.

This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the UnhealthyStateRouting metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=UnhealthyStateRouting