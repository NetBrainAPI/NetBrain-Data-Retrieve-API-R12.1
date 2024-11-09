# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Session Affinity Problems](#example-1) 
    - [Use Case 2 -- Load Balancer Configuration Audits](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NonStickyRequestCount</b> metric tracks the number of requests where the load balancer chose a new target because it couldn't use an existing sticky session. This can happen when a request is made by a new client with no stickiness cookie, the stickiness cookie is invalid, or an error occurs while processing the cookie. Monitoring this metric helps ensure that the load balancer is correctly utilizing sticky sessions and that clients are consistently routed to the appropriate targets.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NonStickyRequestCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Non-Sticky Request Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of requests where no sticky session could be used, over the specified time period.
  * <b>Sum</b>: The total number of requests where a new target was chosen instead of using an existing sticky session.
  * <b>Minimum</b>: The least number of non-sticky requests during the selected period.
  * <b>Maximum</b>: The maximum number of non-sticky requests during the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Session Affinity Problems <a name="example-1"></a>
Use this metric to monitor situations where clients are not being consistently routed to the same target, which could impact the application’s performance or user experience, especially for stateful applications.


## Use Case 2: Load Balancer Configuration Audits <a name="example-2"></a>
Track non-sticky requests to verify that the load balancer’s session stickiness settings are configured correctly and to ensure that targets are being correctly chosen based on stickiness.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html