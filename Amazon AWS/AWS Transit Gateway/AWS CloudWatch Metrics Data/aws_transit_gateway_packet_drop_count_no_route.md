# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Missing Routes](#example-1) 
    - [Use Case 2 -- Ensuring Network Continuity](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketDropCountNoRoute</b> metric tracks the total number of packets dropped due to missing routes within an AWS Transit Gateway. These drops occur when packets are sent to the Transit Gateway without a defined route, leading to packet loss. Monitoring this metric helps identify routing gaps, allowing for proactive network management and reducing data loss due to incorrect configurations.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketDropCountNoRoute
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packet Drop Count No Route

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in dropped packets due to missing routes over time.
  * <b>Sum</b>: Shows the total number of packets dropped within the specified period due to routing issues.
  * <b>Minimum</b>: Indicates the lowest count of dropped packets, helpful for identifying low-drop periods.
  * <b>Maximum</b>: Highlights peak packet drops, potentially indicating significant routing issues or configuration errors.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect immediate routing issues.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Missing Routes <a name="example-1"></a>
Monitor the Packet Drop Count No Route metric to detect missing routes, ensuring proper routing configurations within the Transit Gateway to prevent data loss.

## Use Case 2: Ensuring Network Continuity <a name="example-2"></a>
Regularly observing this metric allows proactive identification of routing issues, minimizing packet drops and improving overall network resilience.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html