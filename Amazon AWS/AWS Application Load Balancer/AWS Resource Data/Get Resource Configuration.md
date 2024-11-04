# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)


# Introduction <a name="introduction"></a>
AWS Load Balancer v2 includes **Network Load Balancer**, **Application Load Balancer**, and **Gateway Load Balancer**. The configuration of the AWS Load Balancer v2 is dependent on the AWS SDK response of the Load Balancer v2 as the primary response. The full resource configuration consists of some associated resources' data, including `load balancer policies`, `instance health`.

# Content <a name="content"></a>
Below are the AWS SDK used to generate this configuration.
|**Resource/Action**|**Relationship**|**AWS SDK document**|
|------|------|------|
| describe_load_balancers | self | https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/elbv2.html |


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "xxx(xxxxxxxxxxxxxxxxx)",
    "LoadBalancerArn": "xxx",
    "DNSName": "xxx",
    "CanonicalHostedZoneId": "12345",
    "CreatedTime": "2020-04-16 18:30:00.094000+00:00",
    "LoadBalancerName": "xxx",
    "Scheme": "internet-facing",
    "VpcId": "vpc-xxxxxxxxxxxxxxxxx",
    "State": {
        "Code": "active"
    },
    "Type": "network",
    "AvailabilityZones": [
        {
            "ZoneName": "us-east-1f",
            "SubnetId": "subnet-xxxxxxxxxxxxxxxxx",
            "LoadBalancerAddresses": []
        },
        {
            "ZoneName": "us-east-1b",
            "SubnetId": "subnet-xxxxxxxxxxxxxxxxx",
            "LoadBalancerAddresses": []
        },
        {
            "ZoneName": "us-east-1a",
            "SubnetId": "subnet-xxxxxxxxxxxxxxxxx",
            "LoadBalancerAddresses": []
        }
    ],
    "IpAddressType": "ipv4"
}
```
</details>
<br />
