# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Missing Routes in Routing Table](#example-1) 
    - [Use Case 2 -- Diagnosing Connectivity Problems](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesDroppedNoRoute</b> metric for Transit Gateway Attachments tracks the volume of data (in bytes) dropped due to no route, which occur when packets are sent to a destination for which no route exists in the routing table. Monitoring this metric helps identify routing gaps or configuration errors that could lead to connectivity issues and data loss.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesDroppedNoRoute
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Per-Attachment No Route Bytes Dropped

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in bytes dropped due to missing routes over time.
  * <b>Sum</b>: Shows the total volume of bytes dropped because of no-route conditions within the specified period.
  * <b>Minimum</b>: Indicates the lowest amount of dropped data, highlighting low-error periods.
  * <b>Maximum</b>: Highlights peak volumes of dropped data, helping identify significant routing issues.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring of no-route events.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Missing Routes in Routing Table <a name="example-1"></a>
Track the BytesDroppedNoRoute metric to detect instances where traffic is dropped due to missing routes, allowing for quick adjustments to the routing table to prevent data loss.

## Use Case 2: Diagnosing Connectivity Problems <a name="example-2"></a>
Use this metric to troubleshoot and resolve packet drops caused by destinations with no defined routes, improving the reliability of data transfers.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html