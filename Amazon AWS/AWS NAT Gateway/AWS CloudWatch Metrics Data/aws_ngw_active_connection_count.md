# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Planning](#example-1) 
    - [Use Case 2 -- Network Performance Optimization](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveConnectionCount</b> metric tracks the number of active connections through an AWS NAT Gateway. This metric is essential for monitoring the NAT Gateway's current usage and understanding the volume of active connections being handled, which can help optimize network performance and manage capacity requirements.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveConnectionCount
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Connection Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in active connections over time.
  * <b>Sum</b>: Shows the total number of active connections within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of active connections recorded, which can reveal low-traffic periods.
  * <b>Maximum</b>: Highlights peak counts of active connections, identifying times of highest network load.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to assess current connection counts.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Planning <a name="example-1"></a>
Monitor the ActiveConnectionCount to identify high-traffic periods, aiding in capacity planning to ensure the NAT Gateway can handle peak loads.


## Use Case 2: Network Performance Optimization <a name="example-2"></a>
Track active connection trends to detect potential bottlenecks and optimize NAT Gateway usage for improved network performance.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html