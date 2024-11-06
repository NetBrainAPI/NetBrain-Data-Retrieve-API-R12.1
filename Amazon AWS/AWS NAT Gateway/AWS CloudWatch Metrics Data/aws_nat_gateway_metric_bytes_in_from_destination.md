# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Bandwidth Usage Monitoring](#example-1) 
    - [Use Case 2 -- Analyzing Data Transfer Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesInFromDestination</b> metric tracks the total number of bytes received from the destination through an AWS NAT Gateway. This metric is crucial for understanding the volume of inbound data traffic and helps in monitoring bandwidth usage, diagnosing performance issues, and optimizing resource allocation.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesInFromDestination
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Bytes In From Destination

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in inbound data traffic over time.
  * <b>Sum</b>: Shows the total number of active connections within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of bytes received, helpful for understanding periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of bytes received, which may suggest times of high traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess incoming traffic levels.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Bandwidth Usage Monitoring <a name="example-1"></a>
Monitor the BytesInFromDestination metric to assess inbound traffic levels and ensure that bandwidth allocation aligns with application needs, helping to manage costs and optimize performance.

## Use Case 2: Analyzing Data Transfer Patterns <a name="example-2"></a>
Track inbound byte counts to analyze data transfer patterns over time, which can inform decisions about resource scaling or changes to data processing strategies based on traffic trends.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html