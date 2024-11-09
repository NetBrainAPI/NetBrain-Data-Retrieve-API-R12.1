# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Certificate Issues](#example-1) 
    - [Use Case 2 -- Check Target Group Health](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TargetTLSNegotiationErrorCount</b> is a metric that tracks the number of TLS negotiation errors encountered by a Network Load Balancer (NLB) when communicating with its target groups. This metric helps identify issues related to target group configuration, certificate misconfigurations, or network connectivity problems.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TargetTLSNegotiationErrorCount
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Target TLS Negotiation Error Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of TLS negotiation errors encountered by a Network Load Balancer (NLB) when communicating with its target groups.
  * <b>Sum</b>: The sum of the number of TLS negotiation errors encountered by a Network Load Balancer (NLB) when communicating with its target groups.
  * <b>Minimum</b>: Minimum of the number of TLS negotiation errors encountered by a Network Load Balancer (NLB) when communicating with its target groups.
  * <b>Maximum</b>: Maximum of the number of TLS negotiation errors encountered by a Network Load Balancer (NLB) when communicating with its target groups.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Certificate Issues <a name="example-1"></a>
Monitor this metric to identify target groups with invalid or expired SSL/TLS certificates.

## Use Case 2: Check Target Group Health <a name="example-2"></a>
High error counts can indicate health issues with the target group instances.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html