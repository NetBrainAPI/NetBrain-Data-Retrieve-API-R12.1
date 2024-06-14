# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
Security group acts as a virtual firewall for controlling inbound and outbound traffic for one or more instances.



The "Describe Security Groups" API offers a detailed information of all security groups within Virtual Private Cloud (VPC). The API response includes inbound and outbound rules of each security group

This API is integrated into the AWS VPC Router in NetBrain and aligns with the `describe_security_groups` function of the AWS REST API, utilizing the `vpc-id` filter for targeted retrieval of security groups.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_security_groups.html