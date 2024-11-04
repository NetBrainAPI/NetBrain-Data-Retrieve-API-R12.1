# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
In AWS Classic Load Balancer (CLB), the metric for tracking the number of backend instances that are considered unhealthy is referred to as the "UnHealthy Host Count". This metric provides insights into the health status of the instances behind your load balancer, helping you to monitor and respond to instances that may be experiencing issues. This API provides the number of backend instances (hosts) that are currently considered unhealthy by the Classic Load Balancer



This API is integrated into the AWS Classic Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the UnHealthyHostCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html#:~:text=us%2Dwest%2D2a.-,UnHealthyHostCount,-The%20number%20of