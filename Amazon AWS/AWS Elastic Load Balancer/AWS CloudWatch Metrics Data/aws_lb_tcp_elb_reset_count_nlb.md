# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detect Network Problems](#example-1) 
    - [Use Case 2 -- Identify Security Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TCP_ELB_Reset_Count</b> is a metric that tracks the number of TCP reset packets sent by a Network Load Balancer (NLB) to clients. This metric helps identify issues with the NLB itself, its target groups, or the underlying network infrastructure.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TCP_ELB_Reset_Count
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: TCP_ELB_Reset_Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of TCP reset packets sent by a Network Load Balancer (NLB) to clients.
  * <b>Sum</b>: The sum of the number of TCP reset packets sent by a Network Load Balancer (NLB) to clients.
  * <b>Minimum</b>: Minimum of the number of TCP reset packets sent by a Network Load Balancer (NLB) to clients.
  * <b>Maximum</b>: Maximum of the number of TCP reset packets sent by a Network Load Balancer (NLB) to clients.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detect Network Problems <a name="example-1"></a>
Increased TCP resets can be caused by network connectivity issues, such as packet loss or latency.

## Use Case 2: Identify Security Issues <a name="example-2"></a>
In some cases, high TCP reset counts can indicate security threats, such as DDoS attacks or port scanning.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html