# Table of Contents
- [Introduction](#introduction)
- [Content](#content)

# Introduction <a name="introduction"></a>
The API is used to get the details of all the VPN connections on Transit Gateway. The response includes details of the customer gateway, VPN state, BGP state etc.

The API belongs to the device type AWS Transit gateway and uses the ec2 resource type of AWS rest API.

# Content <a name="content"></a>
|**Highlight**|**Detail**|
|------|------|
| AWS Device Type | AWS Transit Gateway |
| AWS API Resource Type | ec2 |
| AWS REST API Function | describe_vpn_connections |
| Filter key passed in API | transit-gateway-id |


For more details about the AWS REST API `describe_vpn_connections`, please refer to the following document:
https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_vpn_connections.html