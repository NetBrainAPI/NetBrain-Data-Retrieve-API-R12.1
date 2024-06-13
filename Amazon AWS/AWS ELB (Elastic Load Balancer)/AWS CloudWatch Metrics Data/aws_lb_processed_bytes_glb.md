# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Processed Bytes" metric for Network Load Balancers (NLB) in AWS tracks the total number of bytes processed by the load balancer. This metric provides insights into the amount of data flowing through the NLB, helping you understand its workload and capacity requirements.



The API response contains the total number of bytes processed by the NLB within a specific time frame.



This API is integrated into the AWS Gateway Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ProcessedBytes metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html#:~:text=AvailabilityZone%2C%20LoadBalancer-,ProcessedBytes,-The%20total%20number