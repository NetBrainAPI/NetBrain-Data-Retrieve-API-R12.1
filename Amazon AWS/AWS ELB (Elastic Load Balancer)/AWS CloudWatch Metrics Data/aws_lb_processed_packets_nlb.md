# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Processed Packets" metric represents the number of packets handled by the load balancer. This metric provides insights into the network activity and workload that the NLB is managing.

The API response contains the total number of packets processed by the NLB within a specific time period.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ProcessedPackets  metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=AvailabilityZone%2C%20LoadBalancer-,ProcessedPackets,-The%20total%20number

