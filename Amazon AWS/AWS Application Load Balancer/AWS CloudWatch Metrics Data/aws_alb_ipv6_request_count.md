# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Load Balancer Optimization](#example-1) 
    - [Use Case 2 -- IPv6 Traffic Analysis](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>IPv6RequestCount</b> metric measures the number of IPv6 requests received by the load balancer. This includes all incoming requests that are handled over IPv6. Tracking this metric helps in analyzing the amount of IPv6 traffic the load balancer is receiving and can assist in traffic distribution analysis and optimization.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: IPv6RequestCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: IPv6 Request Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of IPv6 requests received during the time period.
  * <b>Sum</b>: The total number of IPv6 requests received in the selected period.
  * <b>Minimum</b>: The least number of IPv6 requests received in the selected period.
  * <b>Maximum</b>: The maximum number of IPv6 requests received in the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Load Balancer Optimization <a name="example-1"></a>
Monitor the number of IPv6 requests to identify performance bottlenecks or any potential issues related to IPv6 traffic.


## Use Case 2: IPv6 Traffic Analysis <a name="example-2"></a>
Track the number of IPv6 requests to understand the volume of IPv6 traffic entering the system and help in planning the necessary resources for handling this traffic.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html