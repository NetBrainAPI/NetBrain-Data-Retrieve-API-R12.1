# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The <b>AWS TGW Bytes Out</b> metric measures the total volume of outbound traffic (in bytes) passing through a Transit Gateway (TGW). This metric provides insights into the amount of data leaving your AWS network infrastructure through the Transit Gateway. This API provides the number of bytes transmitted by the Transit Gateway to connected attachments, such as VPCs, VPN connections, or Direct Connect gateways.

This API is integrated into the AWS Transit Gateway in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the BytesOut metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html#:~:text=the%20transit%20gateway.-,BytesOut,-The%20number%20of

