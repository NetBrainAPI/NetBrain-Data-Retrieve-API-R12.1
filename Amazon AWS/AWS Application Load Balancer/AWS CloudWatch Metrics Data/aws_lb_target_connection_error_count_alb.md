# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Target Connection Error Count" metric in AWS is used to monitor the number of connection errors between your Elastic Load Balancer (ELB) and the registered targets (e.g., EC2 instances, containers, Lambda functions). This metric helps you identify and diagnose connectivity issues that may affect the performance and availability of your application.

The API response contains the number of connection errors that occurred when the load balancer attempted to establish a connection with the target.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following documenbt: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TargetConnectionErrorCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=TargetConnectionErrorCount