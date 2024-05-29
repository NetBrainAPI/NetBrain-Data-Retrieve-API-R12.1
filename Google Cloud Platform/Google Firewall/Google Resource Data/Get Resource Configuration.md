# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the  Google Firewall relies solely on the corresponding Google API of its Networks. The Google API provides detailed information regarding the configuration of the Google Firewall, including its firewalls, firewallPolicys, etc.

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| Google Firewall - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/networks/getEffectiveFirewalls


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "<network-name>-firewall(<firewall-id>-firewall)",
    "id": "<firewall-id>-firewall",
    "name": "<network-name>-firewall(<firewall-id>-firewall)",
    "networkName": "<network-name>",
    "firewalls": [
        {
            "kind": "compute#firewall",
            "id": "<firewall-rule-id>",
            "creationTimestamp": "2021-08-18T16:38:53.844-07:00",
            "name": "allowalltraff",
            "description": "",
            "network": "https://www.googleapis.com/compute/v1/projects/<proj-id>/global/networks/<network-name>",
            "priority": 1000,
            "sourceRanges": [
                "0.0.0.0/0"
            ],
            "allowed": [
                {
                    "IPProtocol": "all"
                }
            ],
            "direction": "INGRESS",
            "logConfig": {
                "enable": false
            },
            "disabled": false,
            "selfLink": "https://www.googleapis.com/compute/v1/projects/<proj-id>/global/firewalls/allowalltraff"
        }
    ],
    "firewallPolicys": [
        {
            "name": "xxxxxxx",
            "type": "HIERARCHY",
            "shortName": "firewall-policy-org",
            "displayName": "firewall-policy-org",
            "rules": [
                {
                    "kind": "compute#firewallPolicyRule",
                    "description": "",
                    "priority": 500,
                    "match": {
                        "destIpRanges": [
                            "172.18.3.82"
                        ],
                        "layer4Configs": [
                            {
                                "ipProtocol": "tcp",
                                "ports": [
                                    "86"
                                ]
                            }
                        ]
                    },
                    "action": "allow",
                    "direction": "EGRESS",
                    "enableLogging": false
                }
            ]
        }
    ]
}
```

</details>
<br />
