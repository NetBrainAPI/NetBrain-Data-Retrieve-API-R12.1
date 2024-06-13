# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Unhealthy Host Count" metric in AWS refers to the number of unhealthy hosts, also known as targets, registered with your Elastic Load Balancer (ELB). This metric is essential for monitoring the health and availability of your backend resources and identifying potential issues that may affect the overall performance of your application.

The API response contains the number of targets that the load balancer has deemed unhealthy based on the health checks configured for your load balancer.



This API is integrated into the AWS Gateway Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the UnHealthyHostCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html#:~:text=AvailabilityZone%2C%20LoadBalancer-,UnHealthyHostCount,-The%20number%20of