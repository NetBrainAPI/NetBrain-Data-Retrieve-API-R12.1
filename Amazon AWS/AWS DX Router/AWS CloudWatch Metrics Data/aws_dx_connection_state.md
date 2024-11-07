# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Link Failures](#example-1) 
    - [Use Case 2 -- Post-incident Analysis](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ConnectionState</b> metric for AWS Direct Connect (DX) monitors the state of the connection between your on-premises network and AWS. It provides insight into the current operational state of the Direct Connect virtual interface, helping to identify if the link is operating normally, if there are any disruptions, or if the link is down.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ConnectionState
* <b>Namespace</b>: AWS/DX
* <b>Unit</b>: Boolean
* <b>Display Name in NetBrain</b>: Connection State

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average
  * <b>Average</b>: Returns the average connection state (active or inactive) for the selected period.
  * <b>Sum</b>: Provides the total count of connection state transitions during the selected period (active vs. inactive).
  * <b>Minimum</b>: Identifies periods of inactivity, providing insights into downtime or connection issues.
  * <b>Maximum</b>: Helps pinpoint times of active connections, which can be valuable for identifying the most reliable periods of connectivity.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Link Failures <a name="example-1"></a>
Use this metric to detect any disruptions in the connection. This can help in diagnosing and troubleshooting issues related to network failures, providing a clear signal for when intervention is required.


## Use Case 2: Post-incident Analysis <a name="example-2"></a>
After a network incident or outage, the <b>ConnectionState</b> metric provides historical insight into the status of the Direct Connect link. This can be used for post-mortem analysis to identify patterns, recurring issues, or sudden outages, enabling more effective planning for future network improvements.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/directconnect/latest/UserGuide/monitoring-cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html