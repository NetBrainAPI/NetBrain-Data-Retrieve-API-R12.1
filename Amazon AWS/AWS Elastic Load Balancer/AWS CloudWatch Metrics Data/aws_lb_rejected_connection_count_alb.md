# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Rejected Connection Count" metric in AWS is essential for monitoring the performance and health of your Elastic Load Balancer (ELB). It tracks the number of connection requests that were rejected by the load balancer, which can indicate issues with capacity or configuration.

The API response contains the number of connection requests that the load balancer was unable to establish due to reaching the maximum number of allowed connections or other configuration issues.



This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the RejectedConnectionCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=RejectedConnectionCount