# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Optimize NLB Configuration](#example-1) 
    - [Use Case 2 -- Rightsizing NLBs](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PeakPacketsPerSecond</b> is a metric that tracks the peak number of network packets processed by a Network Load Balancer (NLB) per second over a specified period. By monitoring this metric, you can identify performance bottlenecks, optimize NLB configuration, and plan for future capacity needs.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PeakPacketsPerSecond
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Peak Packets Per Second

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: The average number of network packets processed by a Network Load Balancer (NLB) per second over a specified period.
  * <b>Sum</b>: The sum of the number of network packets processed by a Network Load Balancer (NLB) per second over a specified period.
  * <b>Minimum</b>: Minimum of the number of network packets processed by a Network Load Balancer (NLB) per second over a specified period.
  * <b>Maximum</b>: Maximum of the number of network packets processed by a Network Load Balancer (NLB) per second over a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Optimize NLB Configuration <a name="example-1"></a>
By analyzing the peak traffic patterns, you can optimize the NLB configuration, such as increasing the number of target groups or adjusting the health check intervals.

## Use Case 2: Rightsizing NLBs <a name="example-2"></a>
By understanding the peak traffic load, you can choose the appropriate NLB instance type to ensure optimal performance and cost-effectiveness.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html