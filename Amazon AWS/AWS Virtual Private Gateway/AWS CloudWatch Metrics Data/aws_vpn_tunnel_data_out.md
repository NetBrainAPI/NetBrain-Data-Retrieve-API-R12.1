# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Outbound Data Traffic](#example-1) 
    - [Use Case 2 -- Diagnosing Performance Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>VPN Tunnel Data Out</b> metric tracks the total amount of outbound data processed by VPN tunnels associated with an AWS Virtual Private Gateway. This metric is essential for monitoring data traffic over VPN connections, allowing for the assessment of performance and the identification of potential issues related to outbound data transfer.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TunnelDataOut
* <b>Namespace</b>: AWS/VPN
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: VPN Tunnel Data Out

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in outbound data traffic over time.
  * <b>Sum</b>: Shows the total amount of outbound data processed by the VPN tunnels within the specified period.
  * <b>Minimum</b>: Indicates the lowest data transfer volume, helping to identify periods of low activity.
  * <b>Maximum</b>: Highlights peak outbound data volumes, which may indicate times of high traffic or significant data transfers.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess outgoing data traffic.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Outbound Data Traffic <a name="example-1"></a>
Track the VPNTunnelDataOut metric to evaluate the volume of outbound data processed through VPN tunnels, ensuring optimal performance and resource allocation.

## Use Case 2: Diagnosing Performance Issues <a name="example-2"></a>
Use this metric to troubleshoot potential performance bottlenecks. A sudden decrease in outbound data may indicate connectivity issues or misconfigurations that need to be addressed.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html