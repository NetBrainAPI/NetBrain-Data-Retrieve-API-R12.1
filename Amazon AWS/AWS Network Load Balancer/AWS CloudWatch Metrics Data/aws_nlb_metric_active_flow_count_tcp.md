# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Peak Traffic Analysis](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Latency](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveFlowCount_TCP</b> metric tracks the number of active TCP flows through an AWS Network Load Balancer (NLB). Monitoring this metric is crucial for identifying connection patterns and ensuring optimal load distribution across network resources, which can help in avoiding bottlenecks.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveFlowCount_TCP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Flow Count TCP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of active TCP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Sum</b>: The sum of the number of active TCP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Minimum</b>: The minimum number of active TCP connections handled by a Network Load Balancer (NLB) at a given time.
  * <b>Maximum</b>: The maximum number of active TCP connections handled by a Network Load Balancer (NLB) at a given time.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Peak Traffic Analysis <a name="example-1"></a>
During high-demand periods (e.g., product launches or sales), monitor this metric to ensure load balancers are handling traffic effectively.

## Use Case 2: Troubleshooting Network Latency <a name="example-2"></a>
Track active flow counts to diagnose network slowdowns by identifying unexpected spikes or drops in connections. 

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html