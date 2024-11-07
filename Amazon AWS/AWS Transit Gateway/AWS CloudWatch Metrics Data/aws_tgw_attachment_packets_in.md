# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Inbound Packet Volume per Attachment](#example-1) 
    - [Use Case 2 -- Troubleshooting High Traffic Events](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsIn</b> metric for Transit Gateway Attachments measures the total number of inbound packets received by each attachment to an AWS Transit Gateway. This metric is important for tracking data flow at the packet level, aiding in traffic analysis, network health monitoring, and performance optimization.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsIn
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Per-Attachment Packets In

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing general trends in packet reception over time.
  * <b>Sum</b>: Shows the total count of inbound packets received through the attachment within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of packets, which can help identify low-traffic periods.
  * <b>Maximum</b>: Highlights peak packet counts, useful for detecting high-traffic intervals.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring of inbound packet rates.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Inbound Packet Volume per Attachment <a name="example-1"></a>
Track the Packets In metric for each Transit Gateway attachment to observe inbound packet loads, ensuring each attachment operates effectively and within its capacity.

## Use Case 2: Troubleshooting High Traffic Events <a name="example-2"></a>
Use this metric to identify spikes in inbound packet volume, which can help diagnose network congestion and optimize data flow.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html