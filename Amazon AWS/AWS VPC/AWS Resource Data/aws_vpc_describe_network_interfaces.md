# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
Elastic Network Interface is virtual network interface that you can attach to an instance in your Virtual Private Cloud (VPC)



The "Describe Network Interfaces" API offers a comprehensive overview of all network interfaces associated with the designated Virtual Private Cloud (VPC). The API response includes IP address and MAC address of the interface, interface attachment details and more.

This API is integrated into the AWS VPC Router in NetBrain and aligns with the `describe_network_interfaces` function of the AWS REST API, utilizing the `vpc-id` filter for targeted retrieval of network interface information.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_network_interfaces.html