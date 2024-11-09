# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Troubleshooting Authentication Delays](#example-1) 
    - [Use Case 2 -- Identifying Peak Load Impacts](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthLatency</b> metric measures the time taken, in milliseconds, for the load balancer to query the Identity Provider (IdP) for the ID token and user information. This metric reflects latency in the authentication flow, including cases where the query fails, measuring the time until failure.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthLatency   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Milliseconds
* <b>Display Name in NetBrain</b>: ELB Auth Latency

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Average latency in querying the IdP, useful for monitoring typical response times.
  * <b>Sum</b>: Total latency over the specified time period, indicating cumulative delay in the authentication process.
  * <b>Minimum</b>: Lowest observed latency, indicating optimal query performance during the period.
  * <b>Maximum</b>: Highest observed latency, useful for identifying spikes or delays.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for tracking near real-time latency changes.
    * <b>3600 seconds</b> for a broader view of latency trends over time.

# Use Cases Example <a name="example"></a>
## Use Case 1: Troubleshooting Authentication Delays <a name="example-1"></a>
Investigate spikes in ELB Auth Latency to identify and resolve sources of latency, whether network-related or due to IdP processing times.





## Use Case 2: Identifying Peak Load Impacts <a name="example-2"></a>
Monitor latency trends during high traffic to see how peak load impacts IdP response times, helping optimize authentication for high-demand periods.







# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html