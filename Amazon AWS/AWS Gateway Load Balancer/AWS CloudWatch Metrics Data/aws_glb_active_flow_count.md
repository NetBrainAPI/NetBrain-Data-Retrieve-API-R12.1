# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify High-Traffic Periods](#example-1) 
    - [Use Case 2 -- Forecast Future Demand](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveFlowCount</b> is a metric that tracks the number of active connections handled by a Gateway Load Balancer (GWLB) at a given time. This metric helps you understand the load on your GWLB and identify potential performance bottlenecks.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveFlowCount
* <b>Namespace</b>: AWS/GatewayELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Flow Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of active connections handled by a Gateway Load Balancer (GWLB) at a given time.
  * <b>Sum</b>: The sum of the number of active connections handled by a Gateway Load Balancer (GWLB) at a given time.
  * <b>Minimum</b>: Minimum of the number of active connections handled by a Gateway Load Balancer (GWLB) at a given time.
  * <b>Maximum</b>: Maximum of the number of active connections handled by a Gateway Load Balancer (GWLB) at a given time.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify High-Traffic Periods <a name="example-1"></a>
By monitoring this metric, you can identify peak usage times and plan for additional capacity if needed.


## Use Case 2: Forecast Future Demand <a name="example-2"></a>
Analyzing historical ActiveFlowCount data can help predict future traffic patterns and plan for capacity scaling.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html