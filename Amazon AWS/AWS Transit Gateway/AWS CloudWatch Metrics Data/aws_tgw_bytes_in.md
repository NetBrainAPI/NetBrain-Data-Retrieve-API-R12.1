# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The <b>AWS TGW Bytes In</b> metric measures the total volume of inbound traffic (in bytes) passing through a Transit Gateway (TGW). This metric is essential for monitoring the amount of data entering your AWS network infrastructure through the Transit Gateway. This API provides the number of bytes received by the Transit Gateway from connected attachments, such as VPCs, VPN connections, or Direct Connect gateways.

This API is integrated into the AWS Transit Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the BytesIn metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html#:~:text=match%20a%20route.-,BytesIn,-The%20number%20of