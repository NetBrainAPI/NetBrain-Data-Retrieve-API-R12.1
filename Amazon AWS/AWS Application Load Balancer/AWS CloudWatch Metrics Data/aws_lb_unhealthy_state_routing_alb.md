# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Zone-Level Routing Health](#example-1) 
    - [Use Case 2 -- Enhancing Zone Health Management](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>UnhealthyStateRouting</b> metric for an AWS Application Load Balancer (ALB) tracks the number of zones that do not meet the routing healthy state requirements, and therefore the load balancer distributes traffic to all targets in the zone, including the unhealthy targets.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: UnhealthyStateRouting   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Unhealthy State Routing


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Displays the average number of zones failing to meet routing health requirements, helpful for identifying trends in zone-level health stability.
  * <b>Sum</b>: Reflects the total count of zones with unmet health requirements within the specified period, useful for evaluating the overall impact on routing.
  * <b>Minimum</b>: Indicates periods with no zones failing routing health requirements, suggesting stable routing.
  * <b>Maximum</b>: Highlights peak numbers of affected zones, useful for identifying high-impact periods.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Zone-Level Routing Health <a name="example-1"></a>
Track Unhealthy State Routing to detect when specific zones fail to meet routing health requirements, ensuring you can address potential reliability risks as they arise.



## Use Case 2: Enhancing Zone Health Management <a name="example-2"></a>
Persistent routing issues in certain zones may indicate a need for adjusting health checks or scaling policies to maintain reliable routing within each zone.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html