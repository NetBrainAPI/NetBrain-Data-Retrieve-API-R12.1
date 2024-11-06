aws_vpc_describe_network_acls# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
In AWS, Network Access Control Lists (Network ACLs or NACLs) are a security layer that acts as a firewall for controlling traffic in and out of one or more subnets. Network ACLs allow you to set rules for both inbound and outbound traffic at the subnet level within a Virtual Private Cloud (VPC).



The <b>Describe Network ACLs</b> API provides a list of all Network ACLs within a VPC. The API response includes the inbound and outbound rules for each Network ACL in the VPC.



This API is part of the AWS VPC Router in NetBrain and utilizes the `describe_network_acls` function of the AWS REST API with the `vpc-id` filter to fetch information from AWS.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_network_acls.html