# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Active Connection Count" metric in AWS typically refers to the number of active connections between clients and the Elastic Load Balancer (ELB). 
This metric is essential for understanding the current load on the load balancer and assessing its capacity to handle incoming traffic.

The API response contains the number of active connections between clients and the load balancer at any given time.

This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



We use the below parameter value to fetch the relevant metric data.


# Content <a name="content"></a>
|**Name**|**Value**|
|------|------|
| Metric Name | ActiveConnectionCount |
| Duration* | last 24 hours |
| Maximum Data Points* | 30 |
| Period* | 3600 |
| Stat* | Sum |


Duration: Refers to the period over which a particular metric is measured

Maximum Data Points: The maximum number of data points the request should return before paginating

Period: The granularity, in seconds, of the returned data points

Stat: The statistic to return. <b>Sum</b> is the sum of the values of the all data points collected during the period



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ActiveConnectionCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=ActiveConnectionCount