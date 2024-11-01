# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Request Count" metric in AWS typically refers to the number of requests processed by a service, such as an Elastic Load Balancer (ELB), an API Gateway, or an Application Load Balancer (ALB). This metric is crucial for understanding the workload and traffic patterns of your application or service.

The API response contains the number of active connections between clients and the load balancer at any given time.

This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the RequestCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=AvailabilityZone%2C%20LoadBalancer-,RequestCount,-The%20number%20of