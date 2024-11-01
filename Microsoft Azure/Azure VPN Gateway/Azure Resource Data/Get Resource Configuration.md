# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure VPN gateway is dependent on the Azure API response of the Azure VPN gateway as the primary response. The full resource configuration consists of some associated resources' API data, including `remoteVpnSite`, `vpnSiteLink`.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Virtual Networks - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/virtual-networks/get | 
| Vpn Sites - Get | properties.connections.properties.remoteVpnSite | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-sites/get | 
| Vpn Site Links - Get | properties.connections.properties.vpnLinkConnections.properties.vpnSiteLink | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-site-links/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "e53bd582834840239c034dae44bfacc1-westus-gw(<ResourceGroup>)(<Subscription_ID_Prefix>)(VpnGateway)",
    "name": "e53bd582834840239c034dae44bfacc1-westus-gw",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnGateways/e53bd582834840239c034dae44bfacc1-westus-gw",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/vpnGateways",
    "location": "westus",
    "properties": {
        "provisioningState": "Succeeded",
        "connections": [
            {
                "name": "Connection-VPNSite-NoBGP-Test",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnGateways/e53bd582834840239c034dae44bfacc1-westus-gw/vpnConnections/Connection-VPNSite-NoBGP-Test",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/vpnGateways/vpnConnections",
                "properties": {
                    "provisioningState": "Succeeded",
                    "routingConfiguration": {
                        "associatedRouteTable": {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/West-VHUB/hubRouteTables/defaultRouteTable"
                        },
                        "propagatedRouteTables": {
                            "labels": [
                                "none"
                            ],
                            "ids": [
                                {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/West-VHUB/hubRouteTables/noneRouteTable"
                                }
                            ]
                        },
                        "vnetRoutes": {
                            "staticRoutes": []
                        }
                    },
                    "enableInternetSecurity": false,
                    # Vpn Sites: https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-sites/get
                    "remoteVpnSite": {
                        "name": "VPNSite-NoBGP-Test",
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/VPNSite-NoBGP-Test",
                        "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                        "type": "Microsoft.Network/vpnSites",
                        "location": "westus",
                        "properties": {
                            "provisioningState": "Succeeded",
                            "addressSpace": {
                                "addressPrefixes": [
                                    "172.17.37.0/24"
                                ]
                            },
                            "deviceProperties": {
                                "deviceVendor": "NetBrain",
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
                            # VPN Site Links: https://learn.microsoft.com/en-us/rest/api/virtualwan/vpn-site-links/get  
                            "vpnSiteLinks": [
                                {
                                    "name": "Burlington-Fortigate",
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/VPNSite-NoBGP-Test/vpnSiteLinks/Burlington-Fortigate",
                                    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                    "properties": {
                                        "provisioningState": "Succeeded",
                                        "ipAddress": "40.85.154.247",
                                        "linkProperties": {
                                            "linkProviderName": "NetBrain",
                                            "linkSpeedInMbps": 50
                                        }
                                    },
                                    "type": "Microsoft.Network/vpnSites/vpnSiteLinks"
                                },
                                {
                                    "name": "Burlington-ASA",
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/VPNSite-NoBGP-Test/vpnSiteLinks/Burlington-ASA",
                                    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                    "properties": {
                                        "provisioningState": "Succeeded",
                                        "ipAddress": "40.85.154.247",
                                        "linkProperties": {
                                            "linkProviderName": "NetBrain",
                                            "linkSpeedInMbps": 50
                                        }
                                    },
                                    "type": "Microsoft.Network/vpnSites/vpnSiteLinks"
                                }
                            ]
                        }
                    },
                    "vpnLinkConnections": [
                        {
                            "name": "Burlington-Fortigate",
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnGateways/e53bd582834840239c034dae44bfacc1-westus-gw/vpnConnections/Connection-VPNSite-NoBGP-Test/vpnLinkConnections/Burlington-Fortigate",
                            "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                            "properties": {
                                "provisioningState": "Succeeded",
                                "vpnSiteLink": {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/VPNSite-NoBGP-Test/vpnSiteLinks/Burlington-Fortigate"
                                },
                                "connectionBandwidth": 10,
                                "ipsecPolicies": [],
                                "vpnConnectionProtocolType": "IKEv2",
                                "sharedKey": "Netbrain123!",
                                "ingressBytesTransferred": 0,
                                "egressBytesTransferred": 0,
                                "packetCaptureDiagnosticState": "None",
                                "connectionStatusDetails": [],
                                "enableBgp": false,
                                "enableRateLimiting": false,
                                "useLocalAzureIpAddress": false,
                                "usePolicyBasedTrafficSelectors": false,
                                "routingWeight": 0,
                                "dpdTimeoutSeconds": 0,
                                "vpnLinkConnectionMode": "Default",
                                "vpnGatewayCustomBgpAddresses": []
                            },
                            "type": "Microsoft.Network/vpnGateways/vpnConnections/vpnLinkConnections"
                        },
                        {
                            "name": "Burlington-ASA",
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnGateways/e53bd582834840239c034dae44bfacc1-westus-gw/vpnConnections/Connection-VPNSite-NoBGP-Test/vpnLinkConnections/Burlington-ASA",
                            "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                            "properties": {
                                "provisioningState": "Succeeded",
                                "vpnSiteLink": {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/vpnSites/VPNSite-NoBGP-Test/vpnSiteLinks/Burlington-ASA"
                                },
                                "connectionBandwidth": 10,
                                "ipsecPolicies": [],
                                "vpnConnectionProtocolType": "IKEv2",
                                "sharedKey": "Netbrain123!",
                                "ingressBytesTransferred": 0,
                                "egressBytesTransferred": 0,
                                "packetCaptureDiagnosticState": "None",
                                "connectionStatusDetails": [],
                                "enableBgp": false,
                                "enableRateLimiting": false,
                                "useLocalAzureIpAddress": false,
                                "usePolicyBasedTrafficSelectors": false,
                                "routingWeight": 0,
                                "dpdTimeoutSeconds": 0,
                                "vpnLinkConnectionMode": "Default",
                                "vpnGatewayCustomBgpAddresses": []
                            },
                            "type": "Microsoft.Network/vpnGateways/vpnConnections/vpnLinkConnections"
                        }
                    ],
                    "ingressBytesTransferred": 0,
                    "egressBytesTransferred": 0
                }
            }
        ],
        "virtualHub": {
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/West-VHUB"
        },
        "bgpSettings": {
            "asn": 65515,
            "peerWeight": 0,
            "bgpPeeringAddresses": [
                {
                    "ipconfigurationId": "Instance0",
                    "defaultBgpIpAddresses": [
                        "172.17.25.14"
                    ],
                    "customBgpIpAddresses": [],
                    "tunnelIpAddresses": [
                        "20.157.87.52",
                        "172.17.25.6"
                    ]
                },
                {
                    "ipconfigurationId": "Instance1",
                    "defaultBgpIpAddresses": [
                        "172.17.25.15"
                    ],
                    "customBgpIpAddresses": [],
                    "tunnelIpAddresses": [
                        "20.157.87.54",
                        "172.17.25.7"
                    ]
                }
            ]
        },
        "vpnGatewayScaleUnit": 1,
        "packetCaptureDiagnosticState": "Failed",
        "ipConfigurations": [
            {
                "id": "Instance0",
                "publicIpAddress": "20.157.87.52",
                "privateIpAddress": "172.17.25.6"
            },
            {
                "id": "Instance1",
                "publicIpAddress": "20.157.87.54",
                "privateIpAddress": "172.17.25.7"
            }
        ],
        "natRules": [],
        "enableBgpRouteTranslationForNat": false,
        "isRoutingPreferenceInternet": true
    }
}
```

</details>
<br />
