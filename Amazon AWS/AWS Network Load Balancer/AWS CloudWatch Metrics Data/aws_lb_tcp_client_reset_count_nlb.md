# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Application Errors](#example-1) 
    - [Use Case 2 -- Security Incident Detection](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TCP_Client_Reset_Count</b> is a metric that tracks the number of TCP reset packets received by a Network Load Balancer (NLB). This metric helps identify network connectivity issues, application errors, or security problems.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TCP_Client_Reset_Count
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: TCP Client Reset Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of TCP reset packets received by a Network Load Balancer.
  * <b>Sum</b>: The sum of the number of TCP reset packets received by a Network Load Balancer.
  * <b>Minimum</b>: Minimum of the number of TCP reset packets received by a Network Load Balancer.
  * <b>Maximum</b>: Maximum of the number of TCP reset packets received by a Network Load Balancer.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Application Errors <a name="example-1"></a>
TCP reset packets can be caused by application errors, such as unexpected exceptions or timeouts. By monitoring this metric, you can identify and address these issues.

## Use Case 2: Security Incident Detection <a name="example-2"></a>
In some cases, high TCP reset counts can indicate malicious activity, such as DDoS attacks or port scanning.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html