# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Security Group Blocked Flow Count Outbound TCP" metric for Network Load Balancers (NLB) in AWS measures the number of outbound TCP (Transmission Control Protocol) packets that are blocked by the associated security groups. This metric is essential for understanding potential connectivity issues or misconfigurations in the security groups that may affect outbound TCP traffic.

The API response contains the number of outbound TCP packets that are blocked by the security groups associated with the NLB.

This API is integrated into the AWS Network Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the SecurityGroupBlockedFlowCount_Outbound_TCP metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=SecurityGroupBlockedFlowCount_Outbound_TCP