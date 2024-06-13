# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "TCP Client Reset Count" metric for Network Load Balancers (NLB) in AWS tracks the number of times the TCP (Transmission Control Protocol) client resets occur. A TCP client reset typically happens when a client abruptly terminates a connection, and the NLB observes this action



The API response contains the total number of times the NLB observes TCP client resets.

This API is integrated into the AWS Network Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TCP_Client_Reset_Count metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=TargetTLSNegotiationErrorCount