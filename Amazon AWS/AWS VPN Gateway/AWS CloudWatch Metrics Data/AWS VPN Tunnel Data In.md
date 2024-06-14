# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
<b>VPN Tunnel Data In</b> metric refers to the amount of incoming data (in bytes) that is received through each VPN tunnel associated with your VPN Gateway. This metric provides insights into the volume of traffic flowing into your AWS environment through the VPN connection. This API provides the amount of data (in bytes) received through each VPN tunnel associated with your AWS VPN Gateway.



This API is integrated into the AWS Virtual private Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TunnelDataIn metric, please refer to the following document: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html#:~:text=0%20and%201-,TunnelDataIn,-%E2%80%A0