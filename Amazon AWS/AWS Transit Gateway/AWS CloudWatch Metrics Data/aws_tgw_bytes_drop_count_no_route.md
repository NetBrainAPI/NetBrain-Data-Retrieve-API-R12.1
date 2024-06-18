# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
<b>Bytes Drop Count No Route</b> metric measures the total number of bytes dropped by the Transit Gateway due to packets being sent to destinations for which no valid route exists.  This API provides the number of bytes dropped by the Transit Gateway because packets were sent to a destination without a valid route.



This API is integrated into the AWS Classic Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the BytesDropCountNoRoute metric, please refer to the following document: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html#:~:text=a%20blackhole%20route.-,BytesDropCountNoRoute,-The%20number%20of