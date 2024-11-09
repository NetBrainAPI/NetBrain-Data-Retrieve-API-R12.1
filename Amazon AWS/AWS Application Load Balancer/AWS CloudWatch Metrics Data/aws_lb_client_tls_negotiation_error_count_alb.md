# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Diagnosing Client Connection Issues](#example-1) 
    - [Use Case 2 -- Analyzing Impact of TLS Version Updates](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ClientTLSNegotiationErrorCount</b> metric for an AWS Application Load Balancer (ALB) monitors the number of TLS (Transport Layer Security) negotiation errors between clients and the ALB. This metric helps in identifying issues during the TLS handshake process, which can indicate potential misconfigurations, expired certificates, or incompatible TLS versions.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ClientTLSNegotiationErrorCount
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Client TLS Negotiation Error Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Provides the average rate of TLS negotiation errors over the selected period.
  * <b>Sum</b>: Shows the total number of TLS negotiation errors, useful for understanding the volume of failed handshakes.
  * <b>Minimum</b>: Highlights periods with no errors, which can help identify successful connection times.
  * <b>Maximum</b>: Captures peak error occurrences, which may indicate times of high failure rates.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Diagnosing Client Connection Issues <a name="example-1"></a>
Track ClientTLSNegotiationErrorCount to identify and troubleshoot connection problems due to TLS handshake failures, helping ensure clients can securely connect to your applications.



## Use Case 2: Analyzing Impact of TLS Version Updates <a name="example-2"></a>
After updating to a newer TLS version, monitor this metric to assess whether clients are compatible with the update, identifying if clients are experiencing increased handshake failures.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html