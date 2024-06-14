# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
A VPC route table in AWS is like a map that tells network traffic where to go within a Virtual Private Cloud. It contains routes that determine how traffic should be directed to different destinations, such as other instances, the internet, or virtual private gateways.



The "Describe VPC Route Table" API offers detailed information all of the route table attached to the VPC. The API response includes attachment details, details of route propagation, list of routes and more.

This API is integrated into the AWS VPC Router in NetBrain. It corresponds with the describe_route_tables function of the AWS REST API, using the vpc-id filter to retrieve specific route table information.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_route_tables.html

