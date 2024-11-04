# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
The number of connections that were not successfully established between the load balancer and the registered instances. Because the load balancer retries the connection when there are errors, this count can exceed the request rate. Note that this count also includes any connection errors related to health checks.



This API is integrated into the AWSClassic Loadbalancer in Netbrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the BackendConnectionErrors metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html#:~:text=Description-,BackendConnectionErrors,-The%20number%20of