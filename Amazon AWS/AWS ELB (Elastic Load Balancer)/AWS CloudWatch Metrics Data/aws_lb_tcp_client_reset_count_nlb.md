# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "TCP_ELB_Reset_Count" metric for Network Load Balancers (NLB) in AWS measures the number of times the load balancer resets TCP connections. This metric is crucial for understanding the behavior of TCP connections handled by the NLB and diagnosing potential issues affecting network reliability and performance.



The API response contains the count of TCP connection resets performed by the NLB.

This API is integrated into the AWS Network Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TCP_ELB_Reset_Count metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=AvailabilityZone%2C%20LoadBalancer-,TCP_ELB_Reset_Count,-The%20total%20number