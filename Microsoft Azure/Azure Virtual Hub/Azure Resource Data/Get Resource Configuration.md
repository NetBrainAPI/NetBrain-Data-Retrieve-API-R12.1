# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure virtual hub is dependent on the Azure API response of the Azure virtual hub as the primary response. The full resource configuration consists of some associated resources' API data, including `virtualWan`, `vpnSites`.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Virtual Hubs - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualwan/virtual-hubs/get | 
| Virtual Wans - Get | properties.virtualWan | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualwan/virtual-wans/get |
| Vpn Sites - Get | properties.virtualWan.properties.vpnSites | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-sites/get |


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "East-VHUB(<ResourceGroup>)(<Subscription_ID_Prefix>)(VirtualHub)",
    "name": "East-VHUB",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/virtualHubs",
    "location": "eastus",
    "properties": {
        "provisioningState": "Succeeded",
        "virtualHubRouteTableV2s": [],
        "addressPrefix": "172.17.253.0/24",
        "virtualRouterAsn": 65515,
        "virtualRouterIps": [
            "172.17.253.104",
            "172.17.253.105"
        ],
        "routeTable": {
            "routes": []
        },
        "virtualRouterAutoScaleConfiguration": {
            "minCapacity": 2
        },
        # Virtual Wans: https://learn.microsoft.com/en-us/rest/api/virtualwan/virtual-wans/get
        "virtualWan": {
            "name": "VWAN-TO-BUR",
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualWans/VWAN-TO-BUR",
            "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
            "type": "Microsoft.Network/virtualWans",
            "location": "eastus",
            "tags": {
                "DEMO-LAB": "NO CHANGE"
            },
            "properties": {
                "provisioningState": "Succeeded",
                "disableVpnEncryption": false,
                "allowBranchToBranchTraffic": true,
                "office365LocalBreakoutCategory": "None",
                "type": "Standard",
                "virtualHubs": [
                    {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB"
                    },
                    {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/West-VHUB"
                    }
                ],
                # Vpn Sites: https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-sites/get
                "vpnSites": [
                    {
                        "name": "Burlington",
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/Burlington",
                        "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                        "type": "Microsoft.Network/vpnSites",
                        "location": "eastus",
                        "properties": {
                            "provisioningState": "Succeeded",
                            "addressSpace": {
                                "addressPrefixes": [
                                    "172.17.251.0/30",
                                    "172.17.251.4/30"
                                ]
                            },
                            "deviceProperties": {
                                "deviceVendor": "Cisco",
                                "linkSpeedInMbps": 0
                            },
                            "virtualWan": {
                                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualWans/VWAN-TO-BUR"
                            },
                            "isSecuritySite": false,
                            "o365Policy": {
                                "breakOutCategories": {
                                    "optimize": false,
                                    "allow": false,
                                    "default": false
                                }
                            },
                            "vpnSiteLinks": [
                                {
                                    "name": "To-Lab-ASA",
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/Burlington/vpnSiteLinks/To-Lab-ASA",
                                    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                    "properties": {
                                        "provisioningState": "Succeeded",
                                        "ipAddress": "40.85.154.247",
                                        "bgpProperties": {
                                            "asn": 64666,
                                            "bgpPeeringAddress": "172.17.251.1"
                                        },
                                        "linkProperties": {
                                            "linkProviderName": "Crown Castle",
                                            "linkSpeedInMbps": 1
                                        }
                                    },
                                    "type": "Microsoft.Network/vpnSites/vpnSiteLinks"
                                },
                                {
                                    "name": "To-Bur-Fortigate",
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/Burlington/vpnSiteLinks/To-Bur-Fortigate",
                                    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                    "properties": {
                                        "provisioningState": "Succeeded",
                                        "ipAddress": "40.85.154.247",
                                        "bgpProperties": {
                                            "asn": 64665,
                                            "bgpPeeringAddress": "172.17.251.5"
                                        },
                                        "linkProperties": {
                                            "linkProviderName": "Crown Castle",
                                            "linkSpeedInMbps": 1
                                        }
                                    },
                                    "type": "Microsoft.Network/vpnSites/vpnSiteLinks"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "vpnGateway": {
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnGateways/a139004e542a42b9a685e94e4401e7ed-eastus-gw"
        },
        "expressRouteGateway": {
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteGateways/947de39baaf54512b65930c2300c7ded-eastus-er-gw"
        },
        "networkVirtualAppliances": [],
        "routingState": "Provisioned",
        "allowBranchToBranchTraffic": false,
        "preferredRoutingGateway": "ExpressRoute",
        "hubRoutingPreference": "ExpressRoute"
    }
}
```

</details>
<br />