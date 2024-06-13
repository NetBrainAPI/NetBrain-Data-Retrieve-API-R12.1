# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Client TLS Negotiation Error Count" metric in AWS provides insights into the number of TLS negotiation errors encountered by client applications accessing your AWS resources over TLS (Transport Layer Security). This metric is associated with AWS Application Load Balancers (ALB) when terminating TLS connections.

The API response contains the number of TLS connections initiated by the client that did not establish a session with the load balancer due to a TLS error. Possible causes include a mismatch of ciphers or protocols or the client failing to verify the server certificate and closing the connection.



This API is integrated into the AWS Application Loadbalancer in Netbrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.



We use the below parameter value to fetch the relevant metric data.


# Content <a name="content"></a>
|**Name**|**Value**|
|------|------|
| Metric Name | ClientTLSNegotiationErrorCount |
| Duration* | last 24 hours |
| Maximum Data Points* | 30 |
| Period* | 3600 |
| Stat* | Sum |

Duration: Refers to the period over which a particular metric is measured

Maximum Data Points: The maximum number of data points the request should return before paginating

Period: The granularity, in seconds, of the returned data points

Stat: The statistic to return. <b>Sum</b> is the sum of the values of the all data points collected during the period


For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the ClientTLSNegotiationErrorCount metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=ClientTLSNegotiationErrorCount