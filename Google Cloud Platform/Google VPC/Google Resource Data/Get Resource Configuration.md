# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google VPC Router relies solely on the corresponding Google API of the VPC Network. The Google API provides detailed information regarding the configuration of the virtual network, including its subnetworks, peerings, etc.

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| VPC Router - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/networks/get | 
| Subnetwork - Get | subnetworks | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/networks/get | 

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>
    
```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "central-vpc-hub-router(<vpc_id>-router)",
    "kind": "compute#network",
    "id": "xxxxxxxxxxxxxxxxxxx",
    "creationTimestamp": "2021-04-21T14:17:20.628-07:00",
    "name": "central-vpc-hub",
    "description": "Second Host Project",
    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
    "selfLinkWithId": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/xxxxxxxxxxxxxxxxxxx",
    "autoCreateSubnetworks": false,
    # Subnetworks: https://cloud.google.com/compute/docs/reference/rest/v1/networks/get
    "subnetworks": [
    {
            "kind": "compute#subnetwork",
            "id": "<subnetwork-id>",
            "creationTimestamp": "2021-11-29T07:11:15.160-08:00",
            "name": "australia-southeast-subnet1",
            "description": "australia-southeast-subnet1",
            "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/australia-vpc-spoke6",
            "ipCidrRange": "xx.xx.xx.xx/28",
            "gatewayAddress": "xx.xx.xx.xx",
            "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/australia-southeast1",
            "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/australia-southeast1/subnetworks/australia-southeast-subnet1",
            "privateIpGoogleAccess": true,
            "secondaryIpRanges": [
                {
                    "rangeName": "range-2",
                    "ipCidrRange": "xx.xx.xx.xx/28"
                }
            ],
            "fingerprint": "xxxxxxxxxx",
            "enableFlowLogs": false,
            "privateIpv6GoogleAccess": "DISABLE_GOOGLE_ACCESS",
            "purpose": "PRIVATE",
            "logConfig": {
                "enable": false,
                "aggregationInterval": "INTERVAL_5_SEC",
                "flowSampling": 0.5,
                "metadata": "INCLUDE_ALL_METADATA"
            },
            "stackType": "IPV4_ONLY"
        }
    ],
    "peerings": [
        {
            "name": "host-proj2-vpc-to-host-proj1-vpc",
            "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
            "state": "INACTIVE",
            "stateDetails": "[2022-04-22T17:42:28.882-07:00]: Peer network tried to connect and failed.",
            "autoCreateRoutes": true,
            "exportCustomRoutes": true,
            "importCustomRoutes": true,
            "exchangeSubnetRoutes": true,
            "exportSubnetRoutesWithPublicIp": true,
            "importSubnetRoutesWithPublicIp": true,
            "stackType": "IPV4_ONLY"
        }
    ],
    "routingConfig": {
        "routingMode": "GLOBAL"
    },
    "mtu": 1460,
    "networkFirewallPolicyEnforcementOrder": "AFTER_CLASSIC_FIREWALL"
}
```

</details>
<br />