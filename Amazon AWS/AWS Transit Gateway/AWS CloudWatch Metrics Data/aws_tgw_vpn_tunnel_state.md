# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [Input Parameters](#input-parameters)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Ensuring VPN Redundancy](#example-1) 
    - [Use Case 2 -- Troubleshooting Connectivity Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TunnelState</b> metric for Transit Gateway VPNs tracks the current state of each VPN tunnel associated with a transit gateway. This metric provides real-time status (up or down) for monitoring and managing VPN connectivity, ensuring secure and reliable connections between on-premises networks and AWS.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TunnelState
* <b>Namespace</b>: AWS/VPN
* <b>Unit</b>: None
* <b>Display Name in NetBrain</b>: VPN Tunnel State

# Input Parameters <a name="input-parameters"></a>
* <b>TUNNEL_IP_ADDRESS</b>: The public IP address of the VPN tunnel. This value is required to identify and monitor the specific tunnel's state.


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Maximum
  * <b>Minimum</b>: Useful for checking the lowest state value within a period (e.g., 0 if the tunnel was down).
  * <b>Maximum</b>: Identifies if the tunnel remained up during the specified period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring of tunnel status.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Ensuring VPN Redundancy <a name="example-1"></a>
For VPNs with multiple tunnels, monitor this metric to confirm that at least one tunnel is up, providing redundancy and avoiding single points of failure.


## Use Case 2: Troubleshooting Connectivity Issues <a name="example-2"></a>
Use this metric with <b>TUNNEL_IP_ADDRESS</b> to diagnose intermittent VPN connectivity issues by observing the TunnelState, which indicates if a tunnel is fluctuating between up and down states.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html