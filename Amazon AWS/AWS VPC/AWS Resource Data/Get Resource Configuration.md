# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)


# Introduction <a name="introduction"></a>
The configuration of the AWS VPC Router is dependent on the AWS SDK response of the AWS virtual private cloud (VPC) as the primary response. The full resource configuration consists of some associated resources' data, including `vpc classic link`, `subnet`, and `vpc peering connections`.

# Content <a name="content"></a>
Below are the AWS SDK used to generate this configuration.
|**Resource/Action**|**Relationship**|**AWS SDK document**|
|------|------|------|
| describe_vpcs | self | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_vpcs.html|
| describe_vpc_classic_link | VpcClassicLinks | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_vpc_classic_link.html |
| describe_subnets | Subnets | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_subnets.html | 
| describe_vpc_peering_connections | VpcPeeringConnections | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_vpc_peering_connections.html |

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "xxx(vpc-xxxxxxxxxxxxxxxxx)",
    "CidrBlock": "192.168.0.0/24"
    "DhcpOptionsId": "xxxx-xxxxxxxxx",
    "State": "available",
    "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
    "OwnerId": "xxx",
    "InstanceTenancy": "default",
    "CidrBlockAssociationSet": [],
    "IsDefault": false,
    "Tags": [
        {
            "Key": "Name",
            "Value": "xxx"
        }
    ],
    # VPC Classic Links: https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_vpc_classic_link.html
    "VpcClassicLinks": [],
    # Subnets: https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_subnets.html
    "Subnets": [
        {
            "AvailabilityZone": "us-east-1a",
            "AvailabilityZoneId": "use1-az1",
            "AvailableIpAddressCount": 10,
            "CidrBlock": "192.168.0.0/24"
            "DefaultForAz": false,
            "MapPublicIpOnLaunch": false,
            "MapCustomerOwnedIpOnLaunch": false,
            "State": "available",
            "SubnetId": "subnet-xxxxxxxxxxxxxxxxx",
            "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
            "OwnerId": "xxx",
            "AssignIpv6AddressOnCreation": false,
            "Ipv6CidrBlockAssociationSet": [],
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "xxx"
                }
            ],
            "SubnetArn": "xxx",
            "EnableDns64": false,
            "Ipv6Native": false,
            "PrivateDnsNameOptionsOnLaunch": {
                "HostnameType": "ip-name",
                "EnableResourceNameDnsARecord": false,
                "EnableResourceNameDnsAAAARecord": false
            }
        }
    ],
    # VPC Peering Connections: https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_vpc_peering_connections.html
    "VpcPeeringConnections": [
        {
            "AccepterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    },
                    {
                        "CidrBlock": "192.168.0.0/24"
                    },
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "us-east-1"
            },
            "RequesterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "us-east-1"
            },
            "Status": {
                "Code": "active",
                "Message": "Active"
            },
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "xxx"
                }
            ],
            "VpcPeeringConnectionId": "pcx-xxxxxxxxxxxxxxxxx"
        },
        {
            "AccepterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    },
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "us-east-2"
            },
            "RequesterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "us-east-1"
            },
            "Status": {
                "Code": "active",
                "Message": "Active"
            },
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "xxx"
                }
            ],
            "VpcPeeringConnectionId": "pcx-xxxxxxxxxxxxxxxxx"
        },
        {
            "AccepterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "Ipv6CidrBlockSet": [
                    {
                        "Ipv6CidrBlock": "xxxx:xxxx:xxx:xxxx::/xx"
                    }
                ],
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    },
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "ca-central-1"
            },
            "RequesterVpcInfo": {
                "CidrBlock": "192.168.0.0/24"
                "CidrBlockSet": [
                    {
                        "CidrBlock": "192.168.0.0/24"
                    }
                ],
                "OwnerId": "xxx",
                "PeeringOptions": {
                    "AllowDnsResolutionFromRemoteVpc": false,
                    "AllowEgressFromLocalClassicLinkToRemoteVpc": false,
                    "AllowEgressFromLocalVpcToRemoteClassicLink": false
                },
                "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
                "Region": "us-east-1"
            },
            "Status": {
                "Code": "active",
                "Message": "Active"
            },
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "xxx"
                }
            ],
            "VpcPeeringConnectionId": "pcx-xxxxxxxxxxxxxxxxx"
        }
    ]
}
```

</details>
<br />

