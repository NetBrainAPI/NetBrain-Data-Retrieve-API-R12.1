# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Target TLS Negotiation Error Count" metric for Network Load Balancers (NLB) in AWS measures the number of TLS (Transport Layer Security) negotiation errors encountered between the load balancer and the backend targets. This metric is crucial for identifying potential issues with TLS handshakes and ensuring secure communication between the NLB and its targets.



The API response contains the number of TLS negotiation errors that occur during the establishment of secure connections between the NLB and its backend targets.

This API is integrated into the AWS Network Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TargetTLSNegotiationErrorCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=TargetTLSNegotiationErrorCount