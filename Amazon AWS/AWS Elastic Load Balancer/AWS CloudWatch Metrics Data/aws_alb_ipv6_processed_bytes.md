# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Performance Analysis of IPv6 Traffic](#example-1) 
    - [Use Case 2 -- Capacity Planning for IPv6](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>IPv6ProcessedBytes</b> metric tracks the total number of bytes processed by the load balancer over IPv6. This includes the incoming and outgoing bytes for requests handled by the load balancer via IPv6. Monitoring this metric is useful for understanding the traffic volume handled over IPv6, helping in capacity planning and performance analysis.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: IPv6ProcessedBytes   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: IPv6 Processed Bytes

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of IPv6 bytes processed during the time period.
  * <b>Sum</b>: The total number of bytes processed over IPv6 in the selected period.
  * <b>Minimum</b>: The least number of IPv6 bytes processed in the selected period.
  * <b>Maximum</b>: The maximum number of IPv6 bytes processed in the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Performance Analysis of IPv6 Traffic <a name="example-1"></a>
Monitor changes in the amount of IPv6 traffic processed to assess load balancer performance and ensure that it can handle the volume efficiently.


## Use Case 2: Capacity Planning for IPv6 <a name="example-2"></a>
Use this metric to understand how much IPv6 traffic is being processed over time, assisting in future capacity planning for scaling the load balancer.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html