# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The metric in AWS VPN Gateway measures the total volume of data transmitted (outbound) through each VPN tunnel associated with your VPN Gateway. This metric is crucial for monitoring the amount of data flowing from your AWS environment to your on-premises network or other VPN-connected networks. This API provides the total amount of data (in bytes) transmitted through each VPN tunnel from your AWS Virtual Private Gateway (VGW) to the customer gateway (CGW) or other VPN endpoints.

This API is integrated into the AWS Virtual Private Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the TunnelDataOut metric, please refer to the following document: https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-cloudwatch-vpn.html#:~:text=Units%3A%20Bytes-,TunnelDataOut,-%E2%80%A0