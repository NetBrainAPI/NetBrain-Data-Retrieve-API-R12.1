# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Unusual Traffic Patterns](#example-1) 
    - [Use Case 2 -- Monitor UDP-Based Applications](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveFlowCount_UDP</b> is a CloudWatch metric that tracks the number of active UDP connections handled by a Network Load Balancer (NLB) at a given time. This metric helps you understand the load on your NLB, especially for UDP-based protocols like DNS or streaming.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveFlowCount_UDP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Flow Count UDP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of active UDP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Sum</b>: The sum of the number of active UDP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Minimum</b>: Minimum of the number of active UDP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Maximum</b>: Maximum of the number of active UDP connections handled by a Network Load Balancer (NLB) at a given time.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Unusual Traffic Patterns <a name="example-1"></a>
Analyzing the ActiveFlowCount_UDP metric can help you identify unusual traffic patterns that might indicate security threats, such as DDoS attacks targeting UDP ports.

## Use Case 2: Monitor UDP-Based Applications <a name="example-2"></a>
Track the performance of UDP-based applications, such as DNS servers or streaming services, by analyzing their ActiveFlowCount_UDP metrics.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html