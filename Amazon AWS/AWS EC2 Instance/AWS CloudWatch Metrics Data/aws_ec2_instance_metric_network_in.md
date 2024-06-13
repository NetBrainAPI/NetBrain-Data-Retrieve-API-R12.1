# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
    - [Cloud Watch API Parameters](#content-1) 


# Introduction <a name="introduction"></a>
The API is used to get the number of bytes received by the instance on all network interfaces. This AWS CloudWatch metricS identifies the volume of incoming network traffic to a single instance. 
The number reported is the number of bytes received during the last one hour.

The API is available for AWS EC2 device types in Netbrain and uses the AWS Cloudwatch metrics of AWS rest API.

# Content <a name="content"></a>
|**Name**|**Value**|
|------|------|
| AWS Device Type | EC2 Instance |
| AWS API Resource Type | Cloudwatch |
| AWS REST API Function | get_metric_data |
| AWS CloudWatch Metric Name | NetworkIn |

## AWS CloudWatch API Parameters <a name="content-1"></a>

|**Name**|**Value**|
|------|------|
| Duration | last 1 hour |
| Maximum Data Points* | 20 |
| Period* | 3600 sec |
| Stat* | Sum |

Maximum Data Points: The maximum number of data points the request should return before paginating

Period: The granularity, in seconds, of the returned data points

Stat: The statistic to return. <b>Sum</b> refers to the sum of the values of the all data points collected during the period




For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html
