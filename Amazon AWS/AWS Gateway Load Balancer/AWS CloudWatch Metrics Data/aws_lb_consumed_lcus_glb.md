# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
LCUs are a unit of measurement introduced by AWS to quantify the resources consumed by your load balancer to handle incoming requests and data processing. Consumed LCUs  measure the number of Load Balancer Capacity Units utilized by your load balancer.

The API response contains the number of load balancer capacity units (LCU) used by your load balancer.



This API is integrated into the AWS Gateway Loadbalancer in Netbrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ConsumedLCUs metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/cloudwatch-metrics.html#:~:text=AvailabilityZone%2C%20LoadBalancer-,ConsumedLCUs,-The%20number%20of

