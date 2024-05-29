# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google Cloud NAT relies solely on the corresponding Google API of its cloud routers. The Google API provides detailed information regarding the configuration of the Google Cloud NAT, including its endpointTypes, natIps, etc.

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
    "netbrainHostName": "asia-vpc-spoke4(<vpc-id>-asia-vpc-spoke4)",
    "name": "asia-vpc-spoke4",
    "endpointTypes": [
        "ENDPOINT_TYPE_VM"
    ],
    "sourceSubnetworkIpRangesToNat": "ALL_SUBNETWORKS_ALL_IP_RANGES",
    "natIps": [
        "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west1/addresses/asia-vpc-spoke4-natip"
    ],
    "subnetworks": [
        {
            "name": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/subnetworks/subnet-2",
            "sourceIpRangesToNat": [
                "PRIMARY_IP_RANGE"
            ]
        }
    ],
    "natIpAllocateOption": "AUTO_ONLY",
    "minPortsPerVm": 64,
    "udpIdleTimeoutSec": 30,
    "icmpIdleTimeoutSec": 30,
    "tcpEstablishedIdleTimeoutSec": 1200,
    "tcpTransitoryIdleTimeoutSec": 30,
    "logConfig": {
        "enable": false,
        "filter": "ALL"
    },
    "enableEndpointIndependentMapping": false
}
```

</details>
<br />
