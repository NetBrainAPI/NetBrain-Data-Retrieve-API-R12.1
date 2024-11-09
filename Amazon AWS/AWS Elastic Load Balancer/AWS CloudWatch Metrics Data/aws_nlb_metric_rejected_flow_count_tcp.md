# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Capacity Constraints](#example-1) 
    - [Use Case 2 -- Optimize Resource Allocation](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RejectedFlowCount_TCP</b> is a metric that tracks the number of TCP flow connections rejected by a Network Load Balancer (NLB) due to capacity limits or other reasons. By monitoring this metric, you can identify potential issues with NLB configuration, target group health, or network connectivity.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RejectedFlowCount_TCP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Rejected Flow Count TCP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of TCP flow connections rejected by a Network Load Balancer (NLB) due to capacity limits or other reasons.
  * <b>Sum</b>: The sum of the number of TCP flow connections rejected by a Network Load Balancer (NLB) due to capacity limits or other reasons.
  * <b>Minimum</b>: Minimum of the number of TCP flow connections rejected by a Network Load Balancer (NLB) due to capacity limits or other reasons.
  * <b>Maximum</b>: Maximum of the number of TCP flow connections rejected by a Network Load Balancer (NLB) due to capacity limits or other reasons.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Capacity Constraints <a name="example-1"></a>
High RejectedFlowCount values can indicate that the NLB is reaching its capacity limits and may require scaling or configuration adjustments.

## Use Case 2: Optimize Resource Allocation <a name="example-2"></a>
By analyzing the reasons for rejected TCP flows, you can optimize resource allocation to improve NLB performance.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html