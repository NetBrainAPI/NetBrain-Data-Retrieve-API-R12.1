# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Routing Gaps in Network](#example-1) 
    - [Use Case 2 -- Troubleshooting Connectivity Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketDropCountBlackhole</b> metric for Transit Gateway Attachments tracks the number of packets dropped due to "blackhole" conditions, where packets are directed to an unreachable destination because of missing or invalid routes. Monitoring this metric helps in identifying and addressing routing configuration issues, as blackhole packet drops can disrupt connectivity and lead to data loss.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketDropCountBlackhole
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Per-Attachment Blackhole Packet Drop Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for identifying trends in blackholed packet drops over time.
  * <b>Sum</b>: Shows the total count of blackholed packets within the specified period.
  * <b>Minimum</b>: Indicates the lowest packet drop count, useful for identifying low-error periods.
  * <b>Maximum</b>: Highlights peak packet drop counts, helping detect periods with significant routing issues.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect blackhole conditions quickly.
    * <b>3600 seconds</b> for broader trend analysis over extended periods.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Routing Gaps in Network <a name="example-1"></a>
Monitor the PacketDropCountBlackhole metric to detect instances of blackholed packets due to routing configuration gaps, enabling timely corrections.

## Use Case 2: Troubleshooting Connectivity Issues <a name="example-2"></a>
Use this metric to diagnose connectivity problems caused by packets sent to unreachable destinations, allowing for quick resolution and improved data flow.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html