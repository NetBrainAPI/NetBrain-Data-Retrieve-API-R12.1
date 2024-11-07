# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Outbound Packet Volume per Attachment](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Congestion](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsOut</b> metric for Transit Gateway Attachments measures the total number of outbound packets sent from each attachment to an AWS Transit Gateway. This metric helps track outbound data flow at the packet level, assisting with traffic analysis, network optimization, and performance management.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsOut
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Per-Attachment Packets Out

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in outbound packet flow over time.
  * <b>Sum</b>: Shows the total count of outbound packets sent through the attachment within the specified period.
  * <b>Minimum</b>: Indicates the lowest packet count, useful for identifying low-traffic periods.
  * <b>Maximum</b>: Highlights peak packet counts, helping detect high-traffic intervals.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring of outbound packet rates.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Outbound Packet Volume per Attachment <a name="example-1"></a>
Track the Packets Out metric for each Transit Gateway attachment to observe outbound packet loads, ensuring each attachment functions within its capacity.

## Use Case 2: Troubleshooting Network Congestion <a name="example-2"></a>
Use this metric to detect spikes in outbound packet volume, assisting in diagnosing network congestion and optimizing performance.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html