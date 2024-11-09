# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
In AWS, an ELB (Elastic Load Balancer) listener is a component that checks for connection requests from clients using the specified protocol and port.



The <b>Describe ELB Listeners</b> API provides information about the Elastic Load balancer's listeners. The API response includes listener protocol, port, ARN, etc.

This API is integrated into the AWS Application loadbalancer, Network loadbalancer and Gateway oadbalancer in NetBrain. It corresponds with the `describe_listeners` function of the AWS REST API, using the `LoadBalancerArn filter` to retrieve specific transit gateway route table information.



For more details about the AWS rest API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2/client/describe_listeners.html