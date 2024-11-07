# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Management](#example-1) 
    - [Use Case 2 -- Diagnosing Infrastructure Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>UnHealthy Host Count</b> metric tracks the number of backend instances (hosts) registered with a Classic Load Balancer (CLB) that are considered unhealthy. A backend instance is marked as unhealthy if it fails health checks configured for the load balancer. Monitoring this metric is vital for ensuring that traffic is only routed to healthy instances, thereby maintaining application availability and reliability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: UnHealthyHostCount
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Unhealthy Host Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: Useful for observing trends in the number of unhealthy hosts over time.
  * <b>Sum</b>: Shows the total count of unhealthy hosts over the specified period, though this is less commonly used for this metric.
  * <b>Minimum</b>: Indicates the lowest number of unhealthy hosts recorded, revealing times with optimal health.
  * <b>Maximum</b>: Highlights peak counts of unhealthy hosts, which may indicate widespread issues affecting multiple instances.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly detect increases in unhealthy instances.
    * <b>3600 seconds</b> for broader analysis of health trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Management <a name="example-1"></a>
Track the UnHealthy Host Count to assess whether sufficient healthy instances are available to handle incoming traffic, aiding in scaling decisions.


## Use Case 2: Diagnosing Infrastructure Issues <a name="example-2"></a>
Monitor for spikes in unhealthy hosts to identify and troubleshoot potential issues with backend instances or health check configurations.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html