# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- High NetworkPacketsOut](#example-1) 
    - [Use Case 2 -- Rightsizing Instances](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NetworkPacketsOut</b> is a metric that measures the number of network packets sent by an EC2 instance on all its network interfaces within a specified period. By monitoring this metric, you can identify network bottlenecks, troubleshoot performance issues, and optimize network configuration.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NetworkPacketsOut
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Network Packets Out

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of network packets sent by an EC2 instance on all its network interfaces within a specified period.
  * <b>Sum</b>: The sum of number of network packets sent by an EC2 instance on all its network interfaces within a specified period.
  * <b>Minimum</b>: The minimum number of network packets sent by an EC2 instance on all its network interfaces within a specified period.
  * <b>Maximum</b>: The maximum number of network packets sent by an EC2 instance on all its network interfaces within a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: High NetworkPacketsOut <a name="example-1"></a>
This can indicate that the instance is sending a large number of packets, potentially due to heavy traffic or inefficient network protocols. This can lead to network congestion and performance degradation.

## Use Case 2: Rightsizing Instances <a name="example-2"></a>
If an instance consistently has high NetworkPacketsOut, it may be underprovisioned in terms of network bandwidth. Upgrading to a larger instance type with higher network bandwidth can help improve performance and avoid bottlenecks.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html