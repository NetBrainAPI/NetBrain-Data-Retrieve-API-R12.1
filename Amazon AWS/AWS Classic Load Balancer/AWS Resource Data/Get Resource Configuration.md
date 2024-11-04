# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the **AWS Classic Load Balancer** is dependent on the AWS SDK response of the Load Balancer as the primary response. The full resource configuration consists of some associated resources' data, including `load balancer policies`, `instance health`.

# Content <a name="content"></a>
Below are the AWS SDK used to generate this configuration.
|**Resource/Action**|**Relationship**|**AWS SDK document**|
|------|------|------|
| describe_load_balancers | self | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_load_balancers.html |
| describe_load_balancer_policies | PolicyDescriptions | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_load_balancer_policies.html |
| describe_instance_health | InstanceStates | https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_instance_health.html |

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "xxx(us-east-1-CLB-Test)",
    "LoadBalancerName": "xxx",
    "DNSName": "xxx",
    "CanonicalHostedZoneName": "xxx",
    "CanonicalHostedZoneNameID": "xxxxxxxxxxxxx",
    "ListenerDescriptions": [
        {
            "Listener": {
                "Protocol": "HTTP",
                "LoadBalancerPort": 80,
                "InstanceProtocol": "HTTP",
                "InstancePort": 80
            },
            "PolicyNames": []
        }
    ],
    "Policies": {
        "AppCookieStickinessPolicies": [],
        "LBCookieStickinessPolicies": [],
        "OtherPolicies": []
    },
    "BackendServerDescriptions": [],
    "AvailabilityZones": [
        "us-east-1a",
        "us-east-1f"
    ],
    "Subnets": [
        "subnet-xxxxxxxxxxxxxxxxx",
        "subnet-xxxxxxxxxxxxxxxxx"
    ],
    "VPCId": "vpc-xxxxxxxxxxxxxxxxx",
    "Instances": [
        {
            "InstanceId": "i-xxxxxxxxxxxxxxxxx"
        },
        {
            "InstanceId": "i-xxxxxxxxxxxxxxxxx"
        }
    ],
    "HealthCheck": {
        "Target": "HTTP:80/",
        "Interval": 30,
        "Timeout": 5,
        "UnhealthyThreshold": 2,
        "HealthyThreshold": 10
    },
    "SourceSecurityGroup": {
        "OwnerAlias": "xxxxxxxxxxxxxxxxx",
        "GroupName": "12345"
    },
    "SecurityGroups": [
        "sg-xxxxxxxxxxxxxxxxx",
        "sg-xxxxxxxxxxxxxxxxx"
    ],
    "CreatedTime": "2020-06-12 01:15:52.980000+00:00",
    "Scheme": "internet-facing",
    # Policy Descriptions: https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_load_balancer_policies.html
    "PolicyDescriptions": [],
    # Instance States: https://boto3.amazonaws.com/v1/documentation/api/1.26.86/reference/services/ec2/client/describe_instance_health.html
    "InstanceStates": [
        {
            "InstanceId": "i-xxxxxxxxxxxxxxxxx",
            "State": "InService",
            "ReasonCode": "N/A",
            "Description": "N/A"
        },
        {
            "InstanceId": "i-xxxxxxxxxxxxxxxxx",
            "State": "InService",
            "ReasonCode": "N/A",
            "Description": "N/A"
        }
    ]
}
```
</details>
<br />
  