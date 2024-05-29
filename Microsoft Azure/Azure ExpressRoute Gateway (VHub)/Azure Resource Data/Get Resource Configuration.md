# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure express route gateway is dependent on the Azure API response of the Azure express route gateway as the primary response. The full resource configuration consists of some associated resources' API data, including `expressRouteCircuitPeering`.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Express Route Gateways - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/expressroute/express-route-gateways/get | 
| Express Route Circuits - Get | properties.expressRouteConnections.properties.expressRouteCircuitPeering | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/expressroute/express-route-circuits/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "947de39baaf54512b65930c2300c7ded-eastus-er-gw(<ResourceGroup>)(<Subscription_ID_Prefix>)(ExpressRouteGateway)",
    "name": "947de39baaf54512b65930c2300c7ded-eastus-er-gw",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteGateways/947de39baaf54512b65930c2300c7ded-eastus-er-gw",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/expressRouteGateways",
    "location": "eastus",
    "properties": {
        "provisioningState": "Succeeded",
        "resourceGuid": "00000000-0000-0000-0000-000000000000",
        "virtualHub": {
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB"
        },
        "expressRouteConnections": [
            {
                "name": "ExRConnection-eastus-1596986809931",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteGateways/947de39baaf54512b65930c2300c7ded-eastus-er-gw/expressRouteConnections/ExRConnection-eastus-1596986809931",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/expressRouteGateways/expressRouteConnections",
                "properties": {
                    "provisioningState": "Succeeded",
                    "resourceGuid": "00000000-0000-0000-0000-000000000000",
                    "routingConfiguration": {
                        "associatedRouteTable": {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB/hubRouteTables/defaultRouteTable"
                        },
                        "propagatedRouteTables": {
                            "labels": [
                                "default"
                            ],
                            "ids": [
                                {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB/hubRouteTables/defaultRouteTable"
                                },
                                {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualHubs/East-VHUB/hubRouteTables/DefaultRouteTable"
                                }
                            ]
                        },
                        "vnetRoutes": {
                            "staticRoutes": []
                        }
                    },
                    # Express Route Circuits: https://learn.microsoft.com/en-us/rest/api/expressroute/express-route-circuits/get
                    "expressRouteCircuitPeering": {
                        "name": "AzurePrivatePeering",
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/peerings/AzurePrivatePeering",
                        "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                        "properties": {
                            "provisioningState": "Succeeded",
                            "peeringType": "AzurePrivatePeering",
                            "azureASN": 12076,
                            "peerASN": 8030,
                            "primaryPeerAddressPrefix": "172.17.254.8/30",
                            "secondaryPeerAddressPrefix": "172.17.254.12/30",
                            "primaryAzurePort": "<primaryAzurePort>",
                            "secondaryAzurePort": "<secondaryAzurePort>",
                            "state": "Enabled",
                            "vlanId": 1,
                            "gatewayManagerEtag": "7",
                            "lastModifiedBy": "Customer",
                            "microsoftPeeringConfig": {
                                "advertisedPublicPrefixes": [],
                                "advertisedCommunities": [],
                                "advertisedPublicPrefixesState": "NotConfigured",
                                "customerASN": 0,
                                "legacyMode": 0,
                                "routingRegistryName": "NONE"
                            },
                            "connections": [],
                            "peeredConnections": []
                        },
                        "type": "Microsoft.Network/expressRouteCircuits/peerings"
                    },
                    "routingWeight": 0,
                    "enableInternetSecurity": false
                }
            }
        ],
        "autoScaleConfiguration": {
            "bounds": {
                "min": 1
            }
        }
    }
}
```

</details>
<br />
