# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
<b>VPN Tunnel State</b> metrics provide information about the operational status of individual VPN tunnels that are established between your AWS Virtual Private Gateway (VGW) and your customer gateway (CGW) or other VPN endpoints. These metrics are crucial for monitoring the connectivity and health of your VPN connections. This API provides the current operational state of each VPN tunnel associated with your AWS VPN Gateway.



This API is integrated into the AWS Virtual private Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TunnelState metric, please refer to the following document: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html#:~:text=Description-,TunnelState,-The%20state%20of