# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Network Bottlenecks](#example-1) 
    - [Use Case 2 -- Security Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NetworkPacketsIn</b> is a metric that measures the number of network packets received by an EC2 instance on all its network interfaces within a specified period. By monitoring this metric, you can identify network bottlenecks, troubleshoot performance issues, and optimize network configuration.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NetworkPacketsIn
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Network Packets In

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average of the number of network packets received by an EC2 instance on all its network interfaces within a specified period.
  * <b>Sum</b>: The sum of the number of network packets received by an EC2 instance on all its network interfaces within a specified period.
  * <b>Minimum</b>: The minimum of the number of network packets received by an EC2 instance on all its network interfaces within a specified period.
  * <b>Maximum</b>: The maximum of the number of network packets received by an EC2 instance on all its network interfaces within a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Network Bottlenecks <a name="example-1"></a>
High NetworkPacketsIn can indicate that the instance is experiencing network congestion or bandwidth limitations. This can impact the performance of applications that rely on network communication, such as web servers, databases, and streaming services.

## Use Case 2: Security Monitoring <a name="example-2"></a>
Abnormally high NetworkPacketsIn can sometimes indicate potential security threats, such as DDoS attacks or unauthorized access. By monitoring this metric, you can detect and respond to security incidents.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html