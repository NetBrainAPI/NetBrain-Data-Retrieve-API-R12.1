# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Bottlenecks](#example-1) 
    - [Use Case 2 -- Identify Underutilized GWLBs](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ProcessedBytes</b> is a metric that tracks the total number of bytes processed by a Gateway Load Balancer (GWLB). By monitoring this metric, you can identify network performance issues, optimize GWLB configuration, and troubleshoot bandwidth-related problems.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ProcessedBytes
* <b>Namespace</b>: AWS/GatewayELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Processed Bytes

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of bytes processed by a Gateway Load Balancer.
  * <b>Sum</b>: The sum of the number of bytes processed by a Gateway Load Balancer.
  * <b>Minimum</b>: Minimum of the number of bytes processed by a Gateway Load Balancer.
  * <b>Maximum</b>: Maximum of the number of bytes processed by a Gateway Load Balancer.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Bottlenecks <a name="example-1"></a>
High values of ProcessedBytes can indicate network congestion or bandwidth limitations. By monitoring this metric, you can identify and troubleshoot performance bottlenecks.


## Use Case 2: Identify Underutilized GWLBs <a name="example-2"></a>
Low ProcessedBytes can indicate that an GWLB is underutilized. In such cases, you can consider consolidating GWLBs or downsizing them to reduce costs.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html