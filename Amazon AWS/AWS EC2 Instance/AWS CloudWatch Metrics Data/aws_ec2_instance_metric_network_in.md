# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
    - [Cloud Watch API Parameters](#content-1) 


# Introduction <a name="introduction"></a>
The API is used to get the number of bytes received by the instance on all network interfaces. This cloud watch metric identifies the volume of incoming network traffic to a single instance. 
The number reported is the number of bytes received during the last one hour.

The API is available for AWS EC2 device types in Netbrain and uses the cloud watch metric of AWS rest API.

# Content <a name="content"></a>
|**Highlight**|**Detail**|
|------|------|
| AWS Device Type | EC2 Instance |
| AWS API Resource Type | Cloudwatch |
| AWS REST API Function | get_metric_data |
| Cloud Watch Metric Name | NetworkIn |

## Cloud Watch API Parameters <a name="content-1"></a>

|**Highlight**|**Detail**|
|------|------|
| Duration | EC2 Instance |
| Maximum Data Points* | 20 |
| Period* | 3600 sec |
| Stat* | SUM |