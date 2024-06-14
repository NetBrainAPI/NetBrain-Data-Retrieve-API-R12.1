# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
In AWS, a Transit Gateway default route table is the primary routing table associated with a Transit Gateway.



The "Describe TGW Default Route Table" API retrieves information about the default route table of the transit gateway from which the API is called. The API response includes cidr prefix entry of the route table.

This API is integrated into the AWS Transit Gateway device in NetBrain. It corresponds with the describe_transit_gateway_route_tables function of the AWS REST API, using the transit-gateway-id filter to retrieve specific transit gateway route table information.



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_transit_gateway_route_tables.html