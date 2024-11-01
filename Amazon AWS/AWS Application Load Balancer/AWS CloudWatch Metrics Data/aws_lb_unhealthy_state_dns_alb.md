# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The "Unhealthy State DNS" metric in AWS typically pertains to health checks performed by Amazon Route 53, the DNS (Domain Name System) web service provided by Amazon Web Services. This metric monitors the number of DNS health checks that have entered an unhealthy state.

The API response contains the count of DNS health checks that have transitioned into an unhealthy state.

This API is integrated into the AWS Application Loadbalancer in NetBrain. It corresponds with the `get_metric_data` function of the CloudWatch resource in the AWS REST API.





For more details about the AWS CloudWatch API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html

For more details about the UnhealthyStateDNS metric, please refer to the following document: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metric-table:~:text=AvailabilityZone%2C%20LoadBalancer-,UnHealthyHostCount,-The%20number%20of