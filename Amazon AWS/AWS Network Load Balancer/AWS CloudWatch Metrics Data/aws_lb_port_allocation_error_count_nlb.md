# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Port Allocation Error Count" metric for Network Load Balancers (NLB) in AWS measures the number of times port allocation errors occur. These errors typically happen when there is a failure in allocating a port for a connection due to resource constraints or configuration issues.



The API response contains the number of times the NLB encounters errors while attempting to allocate ports for incoming connections.



This API is integrated into the AWS Network Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the PortAllocationErrorCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html#:~:text=PortAllocationErrorCount