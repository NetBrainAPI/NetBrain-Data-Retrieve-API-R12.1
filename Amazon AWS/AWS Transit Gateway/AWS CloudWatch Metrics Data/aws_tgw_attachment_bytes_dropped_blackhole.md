# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Routing Routes](#example-1) 
    - [Use Case 2 -- Analyzing Connectivity Problems](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesDroppedBlackhole</b> metric for Transit Gateway Attachments tracks the volume of data (in bytes) dropped due to "blackhole" conditions, where packets are sent to an unreachable destination due to missing or invalid routes. Monitoring this metric is crucial for identifying and addressing routing configuration issues, as blackhole traffic can lead to data loss and connectivity problems.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesDroppedBlackhole
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Per-Attachment Blackhole Bytes Dropped

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in blackholed traffic over time.
  * <b>Sum</b>: Shows the total volume of blackholed bytes within the specified period.
  * <b>Minimum</b>: Indicates the lowest volume of blackholed bytes, helping identify low-error periods.
  * <b>Maximum</b>: Highlights peak volumes of blackholed data, signaling potential routing issues.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly detect blackhole conditions.
    * <b>3600 seconds</b> for broader trend analysis over longer periods.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Routing Routes <a name="example-1"></a>
Monitor the Bytes Drop Count Blackhole metric to detect blackhole traffic due to misconfigured or missing routes, allowing for timely resolution to prevent data loss.

## Use Case 2: Analyzing Connectivity Problems <a name="example-2"></a>
Use this metric to troubleshoot instances of packet loss caused by unreachable destinations, enabling swift diagnosis and correction of routing errors.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html