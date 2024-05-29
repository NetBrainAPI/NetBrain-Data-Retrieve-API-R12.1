# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google Dedicated Interconnect is dependent on the Google API response of the interconnects as the primary response. The full resource configuration consists of some associated resources' Interconnect Attachments.

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| Dedicated Google Interconnect  - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/interconnects/get
| Interconnect Attachments - Get | interconnectAttachments | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/interconnectAttachments/get

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "chicago-zone2-cgcil02(<interconnect-id>-dedicateinterconnect)",
    "kind": "compute#interconnec",
    "description": "dedicated-interconnec",
    "selfLink": "https://compute.googleapis.com/compute/v1/projects/{project}/global/interconnects/{interconnect-name}",
    "id": "{interconnect-id}",
    "creationTimestamp": "2021-04-08T12:44:16.166-07:00",
    "name": "gcptonetbondb2",
    "location": "us-east4",
    "linkType": "LINK_TYPE_ETHERNET_10G_LR",
    "requestedLinkCount": 1,
    "interconnectType": "DEDICATED",
    "adminEnabled": false,
    "nocContactEmail": "example@ex.com",
    "customerName": "example-name",
    "operationalStatus": "OS_ACTIVE",
    "provisionedLinkCount": 1,
    # Interconnect Attachments: https://cloud.google.com/compute/docs/reference/rest/v1/interconnectAttachments/get
    "interconnectAttachments": [
        {

            "kind": "compute#interconnectAttachment",
            "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east4/interconnectAttachments/gcptonetbondb",
            "id": "<interconnect-id>",
            "creationTimestamp": "2021-04-08T12:44:16.166-07:00",
            "name": "gcptonetbondb",
            "router": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east4/routers/gcp-router-b",
            "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east4",
            "mtu": 1500,
            "cloudRouterIpAddress": "xx.xx.xx.xx/29",
            "customerRouterIpAddress": "xx.xx.xx.xx/29",
            "type": "PARTNER",
            "pairingKey": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/us-east4/2",
            "adminEnabled": true,
            "vlanTag8021q": 1141,
            "edgeAvailabilityDomain": "AVAILABILITY_DOMAIN_2",
            "bandwidth": "BPS_50M",
            "labelFingerprint": "xxxxxxxx",
            "state": "ACTIVE",
            "partnerAsn": "8030",
            "encryption": "NONE",
            "dataplaneVersion": 1,
            "stackType": "IPV4_ONLY"
            # ... with some additional params 
        }
    ],
    "peerIpAddress": "xx.xx.xx.xx",
    "googleIpAddress": "xx.xx.xx.xx",
    "googleReferenceId": "xxxxxxxxxx",
    "expectedOutages": [
        {
        "name": "outage-name",
        "description": "this is expected outage",
        "source": "GOOGLE",
        "state": "ACTIVE",
        "issueType": "OUTAGE",
        "affectedCircuits": [
            "IT_PARTIAL_OUTAGE"
        ],
        "startTime": "2021-04-08T12:44:16.166-07:00",
        "endTime": "2021-04-09T12:44:16.166-07:00"
        }
    ],
    "circuitInfos": [
        {
        "googleCircuitId": "xxxxxxxxxx",
        "googleDemarcId": "xxxxxxxxxx",
        "customerDemarcId": "xxxxxxxxxx"
        }
    ],
    "labels": {
        "label_key": "label_value"
    },
    "labelFingerprint": "xxxxxxxx",
    "state": "ACTIVE",
    "satisfiesPzs": true,
    "remoteLocation": "somewhere"
}
```

</details>
<br />