# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
ELB (Elastic Load Balancer) attributes are settings that you can configure to control various aspects of your load balancer's behavior and performance. These attributes help you customize the load balancer to suit your specific needs. Some of ELB attributes are Idle Timeout, Deletion Protection, Access Logs, etc.

The "Describe ELB Attributes" API provides information about attributes of the specified ELB. The API response includes the configured value for attributes of the ELB.

This API is integrated into the AWS Application loadbalancer, Network loadbalancer and Gateway oadbalancer in NetBrain. It corresponds with the describe_load_balancer_attributes function of the AWS REST API, using the LoadBalancerArn filter to retrieve specific transit gateway route table information.



For more details about the AWS rest API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2/client/describe_load_balancer_attributes.html