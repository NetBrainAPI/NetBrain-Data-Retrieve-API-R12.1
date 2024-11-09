# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Resource Constraints](#example-1) 
    - [Use Case 2 -- Optimize NLB Configuration](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ConsumedLCUs_TCP</b> is a metric that tracks the number of Linux Container Units (LCUs) consumed by a Network Load Balancer (NLB) for processing TCP traffic. LCUs measure the relative CPU and memory capacity used by the NLB.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ConsumedLCUs_TCP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Consumed LCUs TCP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of Linux Container Units (LCUs) consumed by a Network Load Balancer (NLB) for processing TCP traffic.
  * <b>Sum</b>: The sum of the number of Linux Container Units (LCUs) consumed by a Network Load Balancer (NLB) for processing TCP traffic.
  * <b>Minimum</b>: Minimum of the number of Linux Container Units (LCUs) consumed by a Network Load Balancer (NLB) for processing TCP traffic.
  * <b>Maximum</b>: Maximum of the number of Linux Container Units (LCUs) consumed by a Network Load Balancer (NLB) for processing TCP traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Resource Constraints <a name="example-1"></a>
By monitoring ConsumedLCUs_TCP, you can identify NLBs that are approaching their capacity limits. This can help you proactively scale your NLBs to avoid performance degradation.

## Use Case 2: Optimize NLB Configuration <a name="example-2"></a>
By understanding the LCU consumption patterns, you can optimize the NLB's configuration, such as adjusting the number of listener rules or target groups.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html