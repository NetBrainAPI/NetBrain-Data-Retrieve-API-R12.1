# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Real-Time Monitoring of Connection Load](#example-1) 
    - [Use Case 2 -- Detecting Unusual Connection Activity](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveConnections</b> metric for VPC Endpoints tracks the number of active connections established through a PrivateLink endpoint. Monitoring this metric helps ensure stable endpoint performance and enables proactive management of connection loads.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveConnections
* <b>Namespace</b>: AWS/PrivateLinkEndpoints
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Connections

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Provides an overview of active connections over time.
  * <b>Sum</b>: Shows the cumulative number of connections in the specified period.
  * <b>Minimum</b>: Highlights the minimum number of connections, useful for identifying periods of low demand.
  * <b>Maximum</b>: Identifies peak connection counts.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Real-Time Monitoring of Connection Load <a name="example-1"></a>
Track <b>Active Connections</b> to maintain awareness of current connection loads, ensuring the endpoint remains within operational limits.



## Use Case 2: Detecting Unusual Connection Activity <a name="example-2"></a>
Use this metric to detect spikes in active connections that may indicate potential security events or configuration issues requiring investigation.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html