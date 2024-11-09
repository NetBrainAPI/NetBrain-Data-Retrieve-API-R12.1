# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Capacity Constraints](#example-1) 
    - [Use Case 2 -- Optimize Resource Allocation](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RejectedFlowCount</b> is a metric that tracks the number of flow connections rejected by a Gateway Load Balancer (GWLB) due to capacity limits or other reasons. By monitoring this metric, you can identify potential issues with GWLB configuration, target group health, or network connectivity.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RejectedFlowCount
* <b>Namespace</b>: AWS/GatewayELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Rejected Flow Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of flow connections rejected by a Gateway Load Balancer (GWLB) due to capacity limits or other reasons.
  * <b>Sum</b>: The sum of the number of flow connections rejected by a Gateway Load Balancer (GWLB) due to capacity limits or other reasons.
  * <b>Minimum</b>: Minimum of the number of flow connections rejected by a Gateway Load Balancer (GWLB) due to capacity limits or other reasons.
  * <b>Maximum</b>: Maximum of the number of flow connections rejected by a Gateway Load Balancer (GWLB) due to capacity limits or other reasons.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Capacity Constraints <a name="example-1"></a>
High RejectedFlowCount values can indicate that the GWLB is reaching its capacity limits and may require scaling or configuration adjustments.


## Use Case 2: Optimize Resource Allocation <a name="example-2"></a>
By analyzing the reasons for rejected flows, you can optimize resource allocation and scale your GWLB to handle increased traffic.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html