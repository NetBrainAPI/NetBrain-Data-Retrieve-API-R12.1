# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Backend Performance Degradation](#example-1) 
    - [Use Case 2 -- Improving User Experience](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TargetConnectionErrorCount</b> metric for an AWS Application Load Balancer (ALB) measures the time taken by the backend target to respond to a request. Monitoring this metric is crucial for assessing the performance of the backend targets and ensuring they are providing responses within the expected time frame. High response times could indicate server performance issues, application bottlenecks, or resource constraints.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TargetResponseTime   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Seconds
* <b>Display Name in NetBrain</b>: Target Response Time


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Tracks the average response time of backend targets over a specified period, useful for identifying general performance trends.
  * <b>Sum</b>: Helps to understand the total response time, though less commonly used for time-based metrics like response time.
  * <b>Minimum</b>: Identifies the lowest response time, showing periods when the backend targets were performing optimally.
  * <b>Maximum</b>: Helps identify periods of degraded performance, highlighting when backend targets were responding slowly.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Backend Performance Degradation <a name="example-1"></a>
Monitor Target Response Time to identify when the backend target is experiencing high latency, which may indicate performance degradation, such as overloaded servers or application issues.



## Use Case 2: Improving User Experience <a name="example-2"></a>
Prolonged response times can negatively impact the user experience. Monitoring Target Response Time helps ensure that backend services are performing optimally, contributing to better application performance and user satisfaction.





# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html