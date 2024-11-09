# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Capacity Constraints](#example-1) 
    - [Use Case 2 -- Optimize NLB Configuration](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PortAllocationErrorCount</b> is a metric that tracks the number of times a Network Load Balancer (NLB) fails to allocate a port for a new target. This can occur when the NLB reaches its maximum number of targets or when there are insufficient available ports.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PortAllocationErrorCount
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Port Allocation Error Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of times a Network Load Balancer (NLB) fails to allocate a port for a new target.
  * <b>Sum</b>: The sum of the number of times a Network Load Balancer (NLB) fails to allocate a port for a new target.
  * <b>Minimum</b>: Minimum of the number of times a Network Load Balancer (NLB) fails to allocate a port for a new target.
  * <b>Maximum</b>: Maximum of the number of times a Network Load Balancer (NLB) fails to allocate a port for a new target.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Capacity Constraints <a name="example-1"></a>
By monitoring this metric, one can identify NLBs that are reaching their capacity limits.

## Use Case 2: Optimize NLB Configuration <a name="example-2"></a>
One can adjust the NLB's maximum number of targets or consider creating additional NLBs to distribute traffic more evenly.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html