# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Outbound Traffic for Each Attachment](#example-1) 
    - [Use Case 2 -- Troubleshooting Traffic Congestion](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesOut</b> metric for Transit Gateway Attachments tracks the total volume of outbound data processed by each attachment to an AWS Transit Gateway. This metric is valuable for understanding the amount of data exiting the network through specific attachments, supporting effective traffic management and planning for network capacity.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesOut
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Per-Attachment Bytes Out

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in outbound data over time.
  * <b>Sum</b>: Shows the total volume of data sent through the attachment within the specified period.
  * <b>Minimum</b>: Indicates the lowest volume of outbound data, helpful for identifying low-traffic periods.
  * <b>Maximum</b>: Highlights peak outbound data volumes, which may indicate periods of high network activity.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to assess outbound traffic quickly.
    * <b>3600 seconds</b> for broader trend analysis over extended periods.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Outbound Traffic for Each Attachment <a name="example-1"></a>
Track the Bytes Out metric for individual Transit Gateway attachments to monitor outbound traffic loads, ensuring that each attachment operates within its expected capacity.

## Use Case 2: Troubleshooting Traffic Congestion <a name="example-2"></a>
Use this metric to detect periods of unusually high outbound traffic on attachments, which can aid in diagnosing network congestion and optimizing data flow.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html