# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Missing Routes in Routing Table](#example-1) 
    - [Use Case 2 -- Diagnosing Packet Loss Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketDropCountNoRoute</b> metric for Transit Gateway Attachments measures the total number of packets dropped due to "no route" conditions, which occur when packets are directed to a destination without a defined route in the routing table. Monitoring this metric can help identify gaps in routing configurations that might lead to packet loss and potential connectivity issues.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketDropCountNoRoute
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Per-Attachment No Route Packet Drop Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for identifying trends in packets dropped due to no-route conditions.
  * <b>Sum</b>: Shows the total count of dropped packets due to missing routes within the specified period.
  * <b>Minimum</b>: Indicates the lowest packet drop count, useful for identifying minimal drop intervals.
  * <b>Maximum</b>: Highlights peak packet drop counts, helping identify times of significant routing issues.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect missing routes promptly.
    * <b>3600 seconds</b> for broader trend analysis over extended periods.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Missing Routes in Routing Table <a name="example-1"></a>
Track the PacketDropCountNoRoute metric to identify and address missing routes in the routing table, preventing potential connectivity disruptions.

## Use Case 2: Diagnosing Packet Loss Issues <a name="example-2"></a>
Use this metric to troubleshoot packet loss resulting from destinations with undefined routes, enhancing network performance and reducing data loss.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html