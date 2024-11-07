# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring VPN Availability](#example-1) 
    - [Use Case 2 -- Troubleshooting Connectivity Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TunnelState</b> metric monitors the operational status of VPN tunnels associated with an AWS Virtual Private Gateway. This metric is essential for ensuring the availability and reliability of VPN connections, which are critical for secure communication between on-premises networks and AWS.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TunnelState
* <b>Namespace</b>: AWS/VPN
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: VPN Tunnel State

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: Useful for observing the general state of the VPN tunnels over time.
  * <b>Sum</b>: Shows the total number of tunnels in a specific state over the specified period.
  * <b>Minimum</b>: Indicates the lowest recorded state count, useful for understanding periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of active tunnels, which may suggest times of high usage.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess the operational status of VPN tunnels.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring VPN Availability <a name="example-1"></a>
Regularly check the VPN Tunnel State metric to ensure that all configured VPN tunnels are operational, allowing for continuous secure connections between networks.

## Use Case 2: Troubleshooting Connectivity Issues <a name="example-2"></a>
Utilize this metric to diagnose problems with VPN connections. A change in tunnel state may indicate issues that need immediate investigation, such as configuration errors or network disruptions.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html