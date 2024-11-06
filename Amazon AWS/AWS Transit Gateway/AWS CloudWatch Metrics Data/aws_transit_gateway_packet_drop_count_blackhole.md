# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Diagnosing Routing Configuration Issues](#example-1) 
    - [Use Case 2 -- Improving Network Reliability](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketDropCountBlackhole</b> metric tracks the total number of packets dropped due to blackhole routing within an AWS Transit Gateway. Blackhole drops occur when packets are routed to an unavailable destination. Monitoring this metric helps identify potential routing issues and improve network traffic flow by resolving misconfigurations or connectivity problems.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketDropCountBlackhole
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packet Drop Count Blackhole

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in dropped packets over time.
  * <b>Sum</b>: Shows the total number of packets dropped within the specified period due to blackhole routing.
  * <b>Minimum</b>: Indicates the lowest count of dropped packets, helpful for identifying low-drop periods.
  * <b>Maximum</b>: Highlights peak packet drops, which may indicate significant routing issues or misconfigurations.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect immediate routing issues.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Diagnosing Routing Configuration Issues <a name="example-1"></a>
Monitor the Packet Drop Count Blackhole metric to detect misconfigured routes causing packets to be sent to non-existent destinations, ensuring network integrity.

## Use Case 2: Improving Network Reliability <a name="example-2"></a>
Regular observation of this metric helps ensure proper routing configurations, leading to improved network stability and reliability by preventing unnecessary packet drops.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html