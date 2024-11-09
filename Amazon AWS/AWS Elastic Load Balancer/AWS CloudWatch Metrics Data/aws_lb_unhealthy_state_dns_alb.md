# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Improving DNS Reliability](#example-1) 
    - [Use Case 2 -- Diagnosing Service Outages](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>UnhealthyStateDNS</b> metric for an AWS Application Load Balancer (ALB) tracks instances where DNS resolution fails. Monitoring this metric helps identify DNS issues arising from backend health problems, which can impact application availability and user access.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: UnhealthyStateDNS   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Unhealthy State DNS


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Shows the average count of DNS failures due to unhealthy state, helpful for identifying patterns over time.
  * <b>Sum</b>: Total count of DNS failures within the specified time, useful for analyzing the frequency of availability issues.
  * <b>Minimum</b>: Identifies times when least DNS failures occurred.
  * <b>Maximum</b>: Indicates peak DNS failure counts, helpful for pinpointing periods of significant backend DNS issues.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Improving DNS Reliability <a name="example-1"></a>
Persistent DNS failures may indicate the need to adjust DNS configurations or backend health checks to improve reliability and access.




## Use Case 2: Diagnosing Service Outages <a name="example-2"></a>
Track <b>UnhealthyStateDNS</b> to diagnose potential service outages or degraded performance caused by backend failures affecting DNS resolution.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html