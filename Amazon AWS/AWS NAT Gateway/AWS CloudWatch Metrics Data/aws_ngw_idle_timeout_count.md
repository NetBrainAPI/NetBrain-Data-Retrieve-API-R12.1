# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Resource Optimization](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>IdleTimeoutCount</b> metric tracks the number of connections through an AWS NAT Gateway that were closed due to reaching the idle timeout limit. This metric is useful for understanding if connections are remaining open without activity for extended periods, which may lead to inefficient resource usage and unnecessary costs.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: IdleTimeoutCount
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Idle Timeout Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in idle timeouts over time.
  * <b>Sum</b>: Shows the total count of idle timeouts within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of idle timeouts recorded, helping to understand periods of optimal resource usage.
  * <b>Maximum</b>: Highlights peak counts of idle timeouts, which may suggest times of high inactivity.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly identify idle timeouts as they occur.
    * <b>3600 seconds</b> for analyzing overall trends and resource needs over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Resource Optimization <a name="example-1"></a>
Monitor the Idle Time out Count to identify periods of high idle timeouts, enabling adjustments to connection settings to optimize NAT Gateway resource usage.

## Use Case 2: Troubleshooting Network Issues <a name="example-2"></a>
Correlate high idle timeouts with application or network performance issues. If idle connections are being prematurely closed, this metric can help troubleshoot configuration issues that may be impacting expected connection behavior.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html