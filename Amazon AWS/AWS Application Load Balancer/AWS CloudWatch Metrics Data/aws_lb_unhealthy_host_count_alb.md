# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Backend Issues](#example-1) 
    - [Use Case 2 -- Diagnosing Application Downtime](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>UnHealthyHostCount</b> metric for an AWS Application Load Balancer (ALB) shows the number of backend targets that have failed health checks and are therefore considered unhealthy. Monitoring this metric helps ensure that traffic is directed only to healthy targets, maintaining high availability and performance for applications.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: UnHealthyHostCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: UnHealthy Host Count


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: Shows the average number of unhealthy hosts, useful for identifying patterns over time.
  * <b>Sum</b>: Provides the total count of unhealthy hosts within the specified time, useful for analyzing the frequency of unavailability.
  * <b>Minimum</b>: Shows the minimum number of unhealthy hosts observed, indicating times when the backend was most stable.
  * <b>Maximum</b>: Indicates the peak number of unhealthy hosts, helpful for pinpointing times of significant backend health issues.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Backend Issues <a name="example-1"></a>
Monitor UnHealthy Host Count to detect potential backend issues. A high or increasing number of unhealthy hosts may indicate server performance issues or configuration errors requiring attention.



## Use Case 2: Diagnosing Application Downtime <a name="example-2"></a>
Track <b>UnHealthyHostCount</b> to quickly diagnose application downtime or degraded performance, allowing for faster response to backend issues.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html