# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "HTTPCode_Target_3XX_Count" metric in AWS tracks the number of HTTP 3xx redirection responses sent by the targets behind an Elastic Load Balancer (ELB). This metric helps you understand how often your backend targets (e.g., EC2 instances, containers, or Lambda functions) are issuing redirection responses.

The API response contains the number of HTTP 3xx status codes returned by the targets registered with your load balancer.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the HTTPCode_Target_3XX_Count metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=HTTPCode_Target_3XX_Count