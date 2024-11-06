# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
In AWS, a subnet is a segmented portion of a Virtual Private Cloud (VPC) network where you can place resources such as EC2 instances, RDS databases, or Lambda functions.



The <b>Describe VPC Subnets</b> API offers detailed information all of the subntes in the VPC. The API response includes cidr block of subnet, subnet arn and more.

This API is integrated into the AWS VPC Router in NetBrain. It corresponds with the `describe_subnets` function of the AWS REST API, using the `vpc-id` filter to retrieve specific route table information.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_subnets.html