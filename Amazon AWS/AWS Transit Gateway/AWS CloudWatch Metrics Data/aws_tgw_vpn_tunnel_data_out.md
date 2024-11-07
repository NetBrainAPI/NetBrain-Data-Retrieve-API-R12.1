# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [Input Parameters](#input-parameters)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Outbound Bandwidth](#example-1) 
    - [Use Case 2 -- Identifying Outbound Traffic Anomalies](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TunnelDataOut</b> metric for Transit Gateway VPNs measures the amount of outbound data (in bytes) transmitted through a specific VPN tunnel, identified by <b>TUNNEL_IP_ADDRESS</b>. This metric is crucial for monitoring data flow from AWS to on-premises networks, ensuring optimal performance, and preventing congestion in outbound traffic.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TunnelDataOut
* <b>Namespace</b>: AWS/VPN
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: VPN Tunnel Data Out

# Input Parameters <a name="input-parameters"></a>
* <b>TUNNEL_IP_ADDRESS</b>: The public IP address of the VPN tunnel. This value is required to monitor the specific outbound data flow for the tunnel.


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for tracking the average data outflow over a period.
  * <b>Sum</b>: Shows the total amount of outbound data within the defined time range.
  * <b>Minimum</b>: Indicates the lowest outbound data volume during the period.
  * <b>Maximum</b>: Helps identify peak outbound data moments, which may indicate high traffic or congestion.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring of outbound data.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Outbound Bandwidth <a name="example-1"></a>
Track the <b>TunnelDataIn</b> metric using <b>TUNNEL_IP_ADDRESS</b> to monitor outbound bandwidth, ensuring there is no overuse or congestion in outbound traffic.


## Use Case 2: Identifying Outbound Traffic Anomalies <a name="example-2"></a>
Track this metric to detect sudden drops or spikes in outbound data, which could indicate issues with VPN tunnel stability or abnormal network traffic.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html