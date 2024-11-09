# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting SSL/TLS Misconfigurations](#example-1) 
    - [Use Case 2 -- Improving Backend Target Security](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TargetTLSNegotiationErrorCount</b> metric for an AWS Application Load Balancer (ALB) tracks the number of TLS negotiation errors encountered between the ALB and the backend targets during secure HTTPS communications. These errors may occur when the ALB fails to establish a secure connection with the backend, often due to issues like mismatched SSL/TLS protocols, invalid certificates, or other configuration errors related to TLS handshakes.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TargetTLSNegotiationErrorCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Target TLS Negotiation Error Count


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Monitors the average number of TLS negotiation errors, which can indicate persistent issues with SSL/TLS communications.
  * <b>Sum</b>: Provides the total count of TLS negotiation errors, useful for understanding the scope of the issue.
  * <b>Minimum</b>: Identifies the lowest number of TLS negotiation errors observed in a given time period, helping you spot times when the negotiation error count was at its lowest, potentially indicating periods of stable secure connections.
  * <b>Maximum</b>: Highlights periods when the number of TLS negotiation errors was highest, pointing to potential issues with backend configurations or SSL/TLS protocols.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting SSL/TLS Misconfigurations <a name="example-1"></a>
Monitor Target TLS Negotiation Error Count to identify issues related to SSL/TLS handshake failures, which may be caused by certificate errors, unsupported protocols, or configuration mismatches between the ALB and backend.



## Use Case 2: Improving Backend Target Security <a name="example-2"></a>
Frequent TLS negotiation errors may highlight weak or insecure configurations on backend servers, prompting a review of security settings, SSL certificates, or supported TLS versions to ensure compliance with security standards.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html