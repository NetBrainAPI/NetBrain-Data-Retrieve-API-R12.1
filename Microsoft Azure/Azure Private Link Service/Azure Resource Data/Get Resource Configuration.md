# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>

The configuration of the Azure private link service relies solely on the corresponding Azure API of the private link service. The Azure API provides detailed information regarding the configuration of the azure private link service, including its connectivity, status, etc.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Private Link Services - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/private-link-services/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "public_service_test_privatelinkservice(<ResourceGroup>)(<Subscription_ID_Prefix>)(PrivateLinkService)",
    "name": "public_service_test_privatelinkservice",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateLinkServices/public_service_test_privatelinkservice",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/privateLinkServices",
    "location": "eastus",
    "tags": {
        "type": "dev"
    },
    "properties": {
        "provisioningState": "Succeeded",
        "resourceGuid": "00000000-0000-0000-0000-000000000000",
        "fqdns": [],
        "alias": "public_service_test_privatelinkservice.acb1b37c-fb58-47a8-bbbe-4137bd3064f2.eastus.azure.privatelinkservice",
        "visibility": {
            "subscriptions": []
        },
        "autoApproval": {
            "subscriptions": []
        },
        "enableProxyProtocol": false,
        "loadBalancerFrontendIpConfigurations": [
            {
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/loadBalancers/TestLBStandard/frontendIPConfigurations/LoadBalancerFrontEnd"
            }
        ],
        "ipConfigurations": [
            {
                "name": "Subnet1-1",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateLinkServices/public_service_test_privatelinkservice/ipConfigurations/Subnet1-1",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/privateLinkServices/ipConfigurations",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateIPAllocationMethod": "Dynamic",
                    "subnet": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualNetworks/East-VNET1/subnets/Subnet1"
                    },
                    "primary": false,
                    "privateIPAddressVersion": "IPv4"
                }
            },
            {
                "name": "Subnet1-2",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateLinkServices/public_service_test_privatelinkservice/ipConfigurations/Subnet1-2",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/privateLinkServices/ipConfigurations",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateIPAddress": "172.17.11.12",
                    "privateIPAllocationMethod": "Static",
                    "subnet": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/East-RG1/providers/Microsoft.Network/virtualNetworks/East-VNET1/subnets/Subnet1"
                    },
                    "primary": true,
                    "privateIPAddressVersion": "IPv4"
                }
            }
        ],
        "privateEndpointConnections": [
            {
                "name": "publicservicetest_privateendpoint_1.0e476d97-89ac-4dea-8771-23087d1294aa",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateLinkServices/public_service_test_privatelinkservice/privateEndpointConnections/publicservicetest_privateendpoint_1.0e476d97-89ac-4dea-8771-23087d1294aa",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateEndpoint": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateEndpoints/publicservicetest_privateendpoint_1"
                    },
                    "privateLinkServiceConnectionState": {
                        "status": "Approved",
                        "description": "Auto Approved",
                        "actionsRequired": "None"
                    },
                    "linkIdentifier": "184561670"
                },
                "type": "Microsoft.Network/privateLinkServices/privateEndpointConnections"
            },
            {
                "name": "2edSub-private-endpoint-pls.60e3456e-2c5c-4031-af30-08a12da52acc",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/privateLinkServices/public_service_test_privatelinkservice/privateEndpointConnections/2edSub-private-endpoint-pls.60e3456e-2c5c-4031-af30-08a12da52acc",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateEndpoint": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/paastestgroup/providers/Microsoft.Network/privateEndpoints/2edSub-private-endpoint-pls"
                    },
                    "privateLinkServiceConnectionState": {
                        "status": "Approved",
                        "description": "Auto Approved",
                        "actionsRequired": "None"
                    },
                    "linkIdentifier": "536904747"
                },
                "type": "Microsoft.Network/privateLinkServices/privateEndpointConnections"
            }
        ],
        "networkInterfaces": [
            {
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/public-service-test/providers/Microsoft.Network/networkInterfaces/public_service_test_privatelinkservice.nic.280a7b6f-4ef7-43ef-9a47-1b49c27127bf"
            }
        ]
    }
}
```

</details>
<br />