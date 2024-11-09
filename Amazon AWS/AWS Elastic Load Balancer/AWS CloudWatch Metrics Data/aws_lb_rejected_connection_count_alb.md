# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Configuration Issues](#example-1) 
    - [Use Case 2 -- Improving User Experience](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RejectedConnectionCount</b> metric for an AWS Application Load Balancer (ALB) tracks the number of client connection requests that were rejected by the load balancer due to reaching connection limits or other restrictions. Monitoring this metric is essential for understanding capacity constraints and ensuring that the load balancer can handle incoming traffic without rejecting requests, especially during high-demand periods.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RejectedConnectionCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Rejected Connection Count


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Tracks the average rate of connection rejections, which can help in identifying patterns of resource limitations.
  * <b>Sum</b>: Shows the total number of rejected connections over the period, useful for understanding the frequency and scale of rejections.
  * <b>Minimum</b>: Highlights the lowest number of rejections within a specific period, useful for understanding baseline connectivity.
  * <b>Maximum</b>: Identifies peak rejection counts, which may signal times when additional load balancer resources are needed.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Configuration Issues <a name="example-1"></a>
Track this metric to identify rejections due to configuration issues, such as limits on maximum connections or security policies that may be inadvertently restricting traffic.

## Use Case 2: Improving User Experience <a name="example-2"></a>
By monitoring connection rejections, ensure that legitimate client requests are not denied due to resource limits, helping maintain a smooth user experience.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html