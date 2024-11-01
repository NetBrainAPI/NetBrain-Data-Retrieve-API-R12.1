# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Target TLS Negotiation Error Count" metric in AWS tracks the number of TLS (Transport Layer Security) negotiation errors that occur between the Elastic Load Balancer (ELB) and the targets (such as EC2 instances, containers, or Lambda functions). Monitoring this metric is crucial for ensuring secure and reliable connections between your load balancer and backend targets.

The API response contains the number of failed TLS negotiations between the load balancer and its registered targets.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TargetTLSNegotiationErrorCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=TargetTLSNegotiationErrorCount

