# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Unusual Traffic Patterns](#example-1) 
    - [Use Case 2 -- Tmonitor SSL/TLS Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveFlowCount_TLS</b> is a metric that tracks the number of active TLS connections handled by a Network Load Balancer (NLB) at a given time. This metric helps you understand the load on your NLB, especially for HTTPS traffic.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveFlowCount_TLS
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Flow Count TLS

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of active TLS connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Sum</b>: The sum of the number of active TLS connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Minimum</b>: The minimum number of active TLS connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Maximum</b>: The maximum number of active TLS connections handled by a Network Load Balancer (NLB) at a given time.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Unusual Traffic Patterns <a name="example-1"></a>
Analyzing the ActiveFlowCount_TLS metric can help you identify unusual traffic patterns that might indicate security threats, such as DDoS attacks.

## Use Case 2: Monitor SSL/TLS Performance <a name="example-2"></a>
By tracking the number of active TLS connections, you can assess the performance of your SSL/TLS termination and identify potential issues.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html