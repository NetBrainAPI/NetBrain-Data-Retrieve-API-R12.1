# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Target Response Time" metric in AWS is a critical measure for understanding the performance of your backend targets (such as EC2 instances, containers, or Lambda functions) behind an Elastic Load Balancer (ELB). This metric provides insights into how long it takes for a target to respond to a request after the load balancer has forwarded it.

The API response contains the time elapsed, in seconds, from when a request is sent from the load balancer to a target and when the target starts to send the response headers back to the load balancer.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TargetResponseTime metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=AvailabilityZone%2C%20LoadBalancer-,TargetResponseTime,-The%20time%20elapsed