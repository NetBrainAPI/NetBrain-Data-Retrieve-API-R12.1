# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Security Monitoring](#example-1) 
    - [Use Case 2 -- Traffic Analysis](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>DesyncMitigationMode_NonCompliant_Request_Count</b> metric tracks the number of requests that do not comply with RFC 7230, which outlines HTTP/1.1. This mitigation mode helps protect against HTTP desynchronization attacks.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: DesyncMitigationMode_NonCompliant_Request_Count 
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Desync Mitigation Mode Non-Compliant Request Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of non-compliant requests, useful for trend analysis.
  * <b>Sum</b>: Total number of non-compliant requests in the specified time period.
  * <b>Minimum</b>: The period with the least number of non-compliant requests.
  * <b>Maximum</b>: The period with the highest number of non-compliant requests, useful for identifying peaks.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Security Monitoring <a name="example-1"></a>
Monitor Consumed LCUs to understand how much capacity your ALB is using, helping to identify cost-saving opportunities by scaling resources according to demand.


## Use Case 2: Traffic Analysis <a name="example-2"></a>
Analyze trends in rejected requests to identify if legitimate traffic is being mistakenly flagged as non-compliant, which may require adjustments to the desync mitigation settings.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html