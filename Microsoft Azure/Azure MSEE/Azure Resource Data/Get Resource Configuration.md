# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure MSEE relies solely on the corresponding Azure API response of the Azure express route circuit.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Express Route Circuits - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/expressroute/express-route-circuits/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "Bur-Netbond(Primary)(<ResourceGroup>)(<Subscription_ID_Prefix>)(MSEE)",
    "name": "Bur-Netbond",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/expressRouteCircuits",
    "location": "eastus",
    "properties": {
        "provisioningState": "Succeeded",
        "resourceGuid": "00000000-0000-0000-0000-000000000000",
        "peerings": [
            {
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
                    "primaryAzurePort": "",
                    "secondaryAzurePort": "",
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
            }
        ],
        "authorizations": [
            {
                "name": "MyAuthorization2",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/MyAuthorization2",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Available"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "MyAuthorization3",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/MyAuthorization3",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Used"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "MyAuthorization4",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/MyAuthorization4",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Used"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "2ed-AD-Auth",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/2ed-AD-Auth",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Available"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "publi",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/publi",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Available"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "2ed-AD-Auth-Canada-Central",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/2ed-AD-Auth-Canada-Central",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Available"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "2ed-AD-VWAN",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/2ed-AD-VWAN",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Used"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            },
            {
                "name": "to-West-VHUB",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/expressRouteCircuits/Bur-Netbond/authorizations/to-West-VHUB",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "authorizationKey": "00000000-0000-0000-0000-000000000000",
                    "authorizationUseStatus": "Available"
                },
                "type": "Microsoft.Network/expressRouteCircuits/authorizations"
            }
        ],
        "serviceProviderProperties": {
            "serviceProviderName": "AT&T Netbond",
            "peeringLocation": "Chicago",
            "bandwidthInMbps": 50
        },
        "circuitProvisioningState": "Enabled",
        "allowClassicOperations": false,
        "gatewayManagerEtag": "7",
        "serviceKey": "00000000-0000-0000-0000-000000000000",
        "serviceProviderProvisioningState": "Provisioned",
        "allowGlobalReach": false,
        "globalReachEnabled": false,
        "stag": 8
    },
    "sku": {
        "name": "Standard_MeteredData",
        "tier": "Premium",
        "family": "MeteredData"
    }
}
```

</details>
<br />