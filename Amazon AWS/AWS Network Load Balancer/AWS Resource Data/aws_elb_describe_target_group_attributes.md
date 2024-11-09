# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
ELB (Elastic Load Balancer) target group attributes are configurable settings that allow you to customize the behavior and characteristics of target groups associated with your load balancer. Some of the target attributes are Stickiness, Slow Start etc.



The <b>Describe ELB Target Group Attributes</b> API provides details of the target group attributes of ELB. The API response includes the configured value for attributes of target groups.

This API is integrated into the AWS Application loadbalancer, Network loadbalancer and Gateway oadbalancer in NetBrain. This API corresponds with the `describe_target_group_attributes` function of the AWS REST API. It utilizes the `TargetGroupArn` filter to retrieve attributes of target groups associated with a specified ELB.

For more details about the AWS RESTful API, please check the AWS official document https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2/client/describe_target_group_attributes.html