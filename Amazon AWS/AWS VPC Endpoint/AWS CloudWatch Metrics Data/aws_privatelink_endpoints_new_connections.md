# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Connection Surge During Peak Times](#example-1) 
    - [Use Case 2 -- Security and Anomaly Detection](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NewConnections</b> metric for VPC Endpoints tracks the number of new connections established through a PrivateLink endpoint within a specific period. This metric is essential for understanding connection patterns and helps identify surges in endpoint usage.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NewConnections
* <b>Namespace</b>: AWS/PrivateLinkEndpoints
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: New Connections

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Shows the average rate of new connections over the selected time period.
  * <b>Sum</b>: Displays the total number of new connections during the specified timeframe.
  * <b>Minimum</b>: Highlights the lowest rate of new connections.
  * <b>Maximum</b>: Identifies peak connection initiation moments.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Connection Surge During Peak Times <a name="example-1"></a>
Track New Connections  to observe connection surges during high-traffic periods, ensuring sufficient resources are available to handle increased demand.


## Use Case 2: Security and Anomaly Detection <a name="example-2"></a>
Analyze spikes in new connections, as unexpected surges may indicate potential unauthorized access attempts or other security concerns.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html