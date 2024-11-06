# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Evaluating Application Load](#example-1) 
    - [Use Case 2 -- Identifying Traffic Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesInFromSource</b> metric tracks the total number of bytes received from the source through an AWS NAT Gateway. This metric is essential for monitoring the volume of incoming data traffic from the source, which can help in understanding bandwidth usage, identifying performance bottlenecks, and optimizing resource allocation.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesInFromSource
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Bytes In From Source

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in inbound data traffic from sources over time.
  * <b>Sum</b>: Shows the total number of bytes received from the source within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of bytes received, helpful for understanding periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of bytes received, which may suggest times of high traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess incoming traffic levels from sources.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Evaluating Application Load <a name="example-1"></a>
Use this metric to correlate incoming traffic with application performance. An increase in bytes from sources may indicate higher user activity or data retrieval, requiring adjustments to resource allocation to maintain application responsiveness.


## Use Case 2: Identifying Traffic Patterns <a name="example-2"></a>
Analyze inbound byte counts to identify traffic patterns over time, which can inform resource scaling decisions and help adjust configurations to improve data handling efficiency.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html