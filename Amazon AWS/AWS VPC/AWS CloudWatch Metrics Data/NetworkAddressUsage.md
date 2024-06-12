# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
Network Address Usage metrics in AWS are used to monitor and track the usage of IP addresses within your Virtual Private Cloud (VPC). These metrics help you understand how many IP addresses are in use and can assist in managing IP address space efficiently.



This API is integrated into the AWS VPC Router in Netbrain.It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



We use the below parameter value to fetch the relevant metric data.

AWS CloudWatch API Parameters
|Name|Value|
|------|------|
| Metric name | NetworkAddressUsage |
| Duration* |  |
| Maximum Data Points* |  |
| Period* |  |
| Stat* |  |


Duration: Refers to the period over which a particular metric is measured

Maximum Data Points: The maximum number of data points the request should return before paginating

Period: The granularity, in seconds, of the returned data points

Stat: The statistic to return. Sum is the sum of the values of the all data points collected during the period



For more details about the AWS CloudWatch API, please refer to: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html