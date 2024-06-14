# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
A VPC (Virtual Private Cloud) Endpoint Service Configuration in AWS enables you to privately expose services hosted in your own VPC to other VPCs or AWS services without requiring internet access.



The "Describe VPC Endpoint Service Configuration" API offers detailed information of VPC endpoint service configurations. The API response includes service status, load balancer arn etc.

This API is integrated into the AWS VPC Router in NetBrain and aligns with the `describe_vpc_endpoint_service_configurations` function of the AWS REST API.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_vpc_endpoint_service_configurations.html