# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detect Anomalous Traffic](#example-1) 
    - [Use Case 2 -- Investigate Unusual Behavior](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>SecurityGroupBlockedFlowCount_Outbound_ICMP</b> is a metric that tracks the number of ICMP packets blocked by security group rules associated with a Network Load Balancer (NLB). This metric helps identify potential security misconfigurations or intentional blocking rules that might be impacting network traffic.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: SecurityGroupBlockedFlowCount_Outbound_ICMP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Security Group Blocked Flow Count Outbound ICMP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of ICMP packets blocked by security group rules associated with a Network Load Balancer.
  * <b>Sum</b>: The sum of the number of ICMP packets blocked by security group rules associated with a Network Load Balancer.
  * <b>Minimum</b>: Minimum of the number of ICMP packets blocked by security group rules associated with a Network Load Balancer.
  * <b>Maximum</b>: Maximum of the number of ICMP packets blocked by security group rules associated with a Network Load Balancer.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detect Anomalous Traffic <a name="example-1"></a>
Sudden spikes in this metric might indicate a potential security incident, such as a DDoS attack targeting your NLB.

## Use Case 2: Investigate Unusual Behavior <a name="example-2"></a>
By analyzing the blocked ICMP traffic, you can identify and investigate any suspicious activity.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html