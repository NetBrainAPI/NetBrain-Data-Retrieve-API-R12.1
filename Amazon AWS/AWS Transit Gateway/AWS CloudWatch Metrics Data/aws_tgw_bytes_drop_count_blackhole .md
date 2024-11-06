# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Troubleshooting Routing Issues](#example-1) 
    - [Use Case 2 -- Identifying Configuration Errors](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesDropCountBlackhole</b> metric tracks the total number of bytes dropped due to blackhole routing in an AWS Transit Gateway. Blackhole drops occur when packets are routed to an unavailable destination. Monitoring this metric helps identify and troubleshoot potential routing issues within the network, ensuring optimal traffic flow and connectivity.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesDropCountBlackhole
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Bytes Drop Count Blackhole

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in dropped bytes over time.
  * <b>Sum</b>: Shows the total bytes dropped within the specified period.
  * <b>Minimum</b>: Indicates the smallest volume of dropped data, helping to identify periods of lower activity.
  * <b>Maximum</b>: Highlights peak data drops, which may indicate times of routing instability or configuration errors.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect immediate issues.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Troubleshooting Routing Issues <a name="example-1"></a>
Monitor the Bytes Drop Count Blackhole metric to detect routing errors that result in packet drops, allowing for proactive troubleshooting and network optimization.

## Use Case 2: Identifying Configuration Errors <a name="example-2"></a>
Track this metric to identify blackhole routes caused by incorrect configurations, enabling timely corrections to prevent data loss.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html