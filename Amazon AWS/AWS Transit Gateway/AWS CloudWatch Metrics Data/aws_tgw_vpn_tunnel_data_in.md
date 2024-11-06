# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [Input Parameters](#input-parameters)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Bandwidth Utilization Tracking](#example-1) 
    - [Use Case 2 -- Identifying Data Ingress Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TunnelDataIn</b> metric for Transit Gateway VPNs measures the amount of inbound data (in bytes) received through a specific VPN tunnel, identified by <b>TUNNEL_IP_ADDRESS</b>. This metric helps track data inflows over the VPN connection, useful for monitoring bandwidth usage and managing data flow to prevent congestion.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TunnelDataIn
* <b>Namespace</b>: AWS/VPN
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: VPN Tunnel Data In

# Input Parameters <a name="input-parameters"></a>
* <b>TUNNEL_IP_ADDRESS</b>: The public IP address of the VPN tunnel. This value is required to specify and monitor the inbound data for the particular VPN tunnel.


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing the average data inflow over a specified period.
  * <b>Sum</b>: Shows the total inbound data within the defined time range.
  * <b>Minimum</b>: Indicates the lowest inbound data volume during the period.
  * <b>Maximum</b>: Useful for identifying peak inbound data moments, which may indicate high traffic loads.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring of inbound data.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Bandwidth Utilization Tracking <a name="example-1"></a>
Monitor the <b>TunnelDataIn</b> metric using <b>TUNNEL_IP_ADDRESS</b> to track bandwidth utilization, ensuring efficient VPN capacity management.


## Use Case 2: Identifying Data Ingress Patterns <a name="example-2"></a>
Analyze this metric over time to understand patterns of inbound data, which aids in forecasting and scaling VPN resources effectively.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html