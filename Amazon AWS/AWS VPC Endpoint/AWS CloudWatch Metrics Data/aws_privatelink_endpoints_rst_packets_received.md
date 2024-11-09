# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Connection Issues](#example-1) 
    - [Use Case 2 -- Diagnosing Security Incidents](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RstPacketsReceived</b>metric for VPC Endpoints tracks the number of TCP reset (RST) packets received by the endpoint. RST packets are used to abruptly terminate TCP connections. Monitoring this metric is crucial for identifying connection issues, such as improper connection termination or security-related events.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RstPacketsReceived
* <b>Namespace</b>: AWS/PrivateLinkEndpoints
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: RST Packets Received

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Provides an overview of the average rate of RST packets received over time.
  * <b>Sum</b>: Shows the total number of RST packets received during the selected period.
  * <b>Minimum</b>: Highlights periods of minimal RST packet reception.
  * <b>Maximum</b>: Identifies peak occurrences of RST packet reception, potentially indicating issues with connection stability.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Connection Issues <a name="example-1"></a>
Track RstPacketsReceived to detect unusual connection terminations, helping identify issues with client or server-side connections.


## Use Case 2: Diagnosing Security Incidents <a name="example-2"></a>
Use this metric to detect potential malicious activity, such as denial-of-service attacks or unauthorized connection terminations, where RST packets may be used as part of an attack.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html