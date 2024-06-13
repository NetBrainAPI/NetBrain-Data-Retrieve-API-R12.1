# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
In AWS Classic Load Balancer (CLB), latency refers to the time taken by the load balancer to forward a request to the backend instance and receive the complete response. Monitoring latency is crucial as it directly impacts the responsiveness and performance of your application. The API provides the time taken by the load balancer to successfully respond to a request, measured in milliseconds (ms).

This API is integrated into the AWS Classic Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the Latency metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html#:~:text=us%2Dwest%2D2a.-,Latency,-%5BHTTP%20listener%5D%20The

