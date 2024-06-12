# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google Cloud Router is dependent on the Google API response of the Google Cloud Router as the primary response. The Google API provides detailed information regarding the configuration of the routers, including its name, region, network, etc.

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| Cloud Routers - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/routers/get

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "central-cloud-router-2(<router_id>)",
    "kind": "compute#router",
    "id": "<router_id>",
    "creationTimestamp": "2021-02-09T09:02:01.340-08:00",
    "name": "central-cloud-router-2",
    "description": "",
    "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1",
    "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
    "interfaces": [
        {
            "name": "if-to-servproj3-bgpsession-1",
            "linkedVpnTunnel": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/vpnTunnels/to-servproj3-tunnel-1",
            "ipRange": "xx.xx.xx.xx/30"
        }
    ],
    "bgpPeers": [
        {
            "name": "to-servproj3-bgpsession-1",
            "interfaceName": "if-to-servproj3-bgpsession-1",
            "ipAddress": "xx.xx.xx.xx",
            "peerIpAddress": "xx.xx.xx.xx",
            "peerAsn": 65103,
            "advertiseMode": "CUSTOM",
            "advertisedGroups": [
                "ALL_SUBNETS"
            ],
            "advertisedIpRanges": [
                {
                    "range": "xx.xx.xx.xx/28",
                    "description": "custom route from host project 1 vpc spoke 3"
                },
                {
                    "range": "xx.xx.xx.xx/28",
                    "description": "from host project 1 central hub vpc"
                }
            ],
            "enable": "TRUE"
        }
    ],
    "bgp": {
        "asn": 65511,
        "advertiseMode": "DEFAULT"
    },
    "nats": [
        {
            "name": "asia-vpc-spoke4",
            "autoNetworkTier": "PREMIUM",
            "endpointTypes": [
                "ENDPOINT_TYPE_VM"
            ],
            "sourceSubnetworkIpRangesToNat": "ALL_SUBNETWORKS_ALL_IP_RANGES",
            "natIpAllocateOption": "AUTO_ONLY",
            "logConfig": {
                "enable": false,
                "filter": "ALL"
            },
            "enableEndpointIndependentMapping": false
        }
    ],
    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/routers/central-cloud-router-2",
    
    "encryptedInterconnectRouter": false
}
```

</details>
<br />