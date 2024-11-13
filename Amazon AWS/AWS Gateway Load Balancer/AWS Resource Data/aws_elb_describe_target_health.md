# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
In AWS, ELB (Elastic Load Balancer) target health refers to the status of the targets (such as EC2 instances, IP addresses, or Lambda functions) registered with a load balancer. The health of these targets is determined by performing health checks based on the criteria you define.



The <b>Describe ELB Target Health</b> API offers insights into the health status of every target registered with the load balancer. This API retrieves the health status of targets registered under all target groups of the load balancer.

This API is integrated into the AWS Application loadbalancer, Network loadbalancer and Gateway loadbalancer in NetBrain. It corresponds with the `describe_target_health` function of the AWS REST API, using the `TargetGroupArn` filter to retrieve specific information.



For more details about the AWS rest API, Please check the AWS official document https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2/client/describe_target_health.html