# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Analyzing Application Behavior](#example-1) 
    - [Use Case 2 -- Diagnosing Connectivity Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsOutToDestination</b> metric tracks the total number of packets sent to the destination through an AWS NAT Gateway. This metric is critical for monitoring outbound packet traffic, aiding in assessing network performance, diagnosing potential issues, and optimizing resource utilization.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsOutToDestination
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packets Out To Destination

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in outbound packet traffic over time.
  * <b>Sum</b>: Shows the total number of packets sent to the destination within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of packets sent, helping to understand periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of packets sent, which may suggest times of high outbound traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess outgoing packet levels.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Analyzing Application Behavior <a name="example-1"></a>
Track outgoing packet counts to correlate with application performance. Sudden increases in outbound packets may indicate higher application usage or data transfer requirements, prompting resource allocation adjustments.

## Use Case 2: Diagnosing Connectivity Issues <a name="example-2"></a>
Use this metric to troubleshoot potential connectivity issues. A significant drop in packets sent to the destination may suggest problems in the network path that require further investigation.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html