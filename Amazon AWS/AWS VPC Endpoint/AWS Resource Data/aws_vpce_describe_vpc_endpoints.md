# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
A VPC (Virtual Private Cloud) endpoint in AWS is a network component that allows you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink, without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Traffic between your VPC and the AWS service does not leave the Amazon network.



The "Describe VPC Endpoints" API provides detailed information about specific VPC endpoints. The API response includes details of ENI attached to VPC endpoint, endpoint status, VPC endpoint service details and more.

This API is integrated into the AWS VPC Endpoint device in NetBrain and aligns with the describe_vpc_endpoints function of the AWS REST API, using the vpc-endpoint-id filter to retrieve specific endpoint information.



For more details about the AWS rest API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_vpc_endpoints.html

