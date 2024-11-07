# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Planning](#example-1) 
    - [Use Case 2 -- Analyzing Outbound Traffic Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesOutToSource</b> metric tracks the total number of bytes sent to the source through an AWS NAT Gateway. This metric is critical for monitoring outbound data traffic, helping to understand bandwidth utilization, identify performance issues, and optimize resource management.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesOutToSource
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Bytes Out To Source

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in outbound data traffic to sources over time.
  * <b>Sum</b>: Shows the total number of bytes sent to the source within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of bytes sent, helping to understand periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of bytes sent, which may suggest times of high outbound traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess outgoing traffic levels to sources.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Planning <a name="example-1"></a>
Analyze trends in outbound byte counts to inform capacity planning for the NAT Gateway. Consistently high outbound traffic may require scaling up resources to maintain performance and avoid potential bottlenecks.

## Use Case 2: Analyzing Outbound Traffic Patterns <a name="example-2"></a>
Track the outbound byte counts to identify patterns in data transfer over time, informing decisions about scaling resources and adjusting configurations to enhance data handling efficiency.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html