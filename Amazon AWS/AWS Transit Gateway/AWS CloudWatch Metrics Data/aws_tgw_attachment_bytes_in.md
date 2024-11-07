# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Attachment-Specific Traffic Volume](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesIn</b> metric for Transit Gateway Attachments tracks the total volume of inbound data processed by each attachment to an AWS Transit Gateway. Monitoring this metric is essential for understanding the amount of data entering the network through specific attachments, which helps in traffic management and capacity planning.




# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesIn
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Per-Attachment Bytes In

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in inbound data over time.
  * <b>Sum</b>: Shows the total volume of data received through the attachment within the specified period.
  * <b>Minimum</b>: Indicates the lowest volume of inbound data, helpful for identifying low-traffic periods.
  * <b>Maximum</b>: Highlights peak inbound data volumes, which may signal high network usage.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to assess inbound traffic quickly.
    * <b>3600 seconds</b> for broader trend analysis over extended periods.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Attachment-Specific Traffic Volume <a name="example-1"></a>
Track the Bytes In metric for each Transit Gateway attachment to monitor the inbound traffic load, ensuring that each attachment operates within capacity limits.

## Use Case 2: Troubleshooting Network Performance <a name="example-2"></a>
Use this metric to identify periods of unusually high inbound traffic on specific attachments, which can help diagnose performance issues and optimize resource allocation.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html