# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
LCUs are a unit of measurement introduced by AWS to quantify the resources consumed by your load balancer to handle incoming requests and data processing. Consumed LCUs  measure the number of Load Balancer Capacity Units utilized by your load balancer.

The API response contains the number of load balancer capacity units (LCU) used by your load balancer.



This API is integrated into the AWS Application Loadbalancer in Netbrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



We use the below parameter value to fetch the relevant metric data.


# Content <a name="content"></a>
|**Name**|**Value**|
|------|------|
| Metric Name | ConsumedLCUs |
| Duration* | last 24 hours |
| Maximum Data Points* | 30 |
| Period* | 3600 |
| Stat* | Average |

Duration: Refers to the period over which a particular metric is measured

Maximum Data Points: The maximum number of data points the request should return before paginating

Period: The granularity, in seconds, of the returned data points

Stat: The statistic to return

For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ConsumedLCUs metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=AvailabilityZone%2C%20LoadBalancer-,ConsumedLCUs,-The%20number%20of