# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure application gateway relies solely on the corresponding Azure API of the azure application gateway. The Azure API provides detailed information regarding the configuration of the application gateway, including its connectivity, configuration, etc.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Application Gateways - Get | self | 2021-08-01 | https://docs.microsoft.com/en-us/rest/api/application-gateway/application-gateways/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "appgw_aks_test_2(<ResourceGroup>)(<Subscription_ID_Prefix>)(ApplicationGateway)",
    "name": "appgw_aks_test_2",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/applicationGateways",
    "location": "westus2",
    "tags": {
        "managed-by-k8s-ingress": "1.5.3/94b2b229/2023-02-03-21:42T+0000"
    },
    "zones": [
        "1",
        "2",
        "3"
    ],
    "properties": {
        "provisioningState": "Succeeded",
        "resourceGuid": "00000000-0000-0000-0000-000000000000",
        "sku": {
            "name": "Standard_v2",
            "tier": "Standard_v2"
        },
        "operationalState": "Running",
        "gatewayIPConfigurations": [
            {
                "name": "appGatewayIpConfig",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/gatewayIPConfigurations/appGatewayIpConfig",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "subnet": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/virtualNetworks/aks-vnet-39472610/subnets/appgw-subnet"
                    }
                },
                "type": "Microsoft.Network/applicationGateways/gatewayIPConfigurations"
            }
        ],
        "sslCertificates": [],
        "trustedRootCertificates": [],
        "trustedClientCertificates": [],
        "sslProfiles": [],
        "frontendIPConfigurations": [
            {
                "name": "appGwPublicFrontendIp",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/frontendIPConfigurations/appGwPublicFrontendIp",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/applicationGateways/frontendIPConfigurations",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateIPAllocationMethod": "Dynamic",
                    "publicIPAddress": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/publicIPAddresses/public_IP_aks_test2_appgw"
                    },
                    "httpListeners": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/httpListeners/fl-e1903c8aa3446b7b3207aec6d6ecba8a"
                        }
                    ]
                }
            }
        ],
        "frontendPorts": [
            {
                "name": "port_80",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/frontendPorts/port_80",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "port": 80,
                    "httpListeners": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/httpListeners/fl-e1903c8aa3446b7b3207aec6d6ecba8a"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/frontendPorts"
            }
        ],
        "backendAddressPools": [
            {
                "name": "defaultaddresspool",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendAddressPools/defaultaddresspool",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "backendAddresses": []
                },
                "type": "Microsoft.Network/applicationGateways/backendAddressPools"
            },
            {
                "name": "pool-default-aspnetapp-80-bp-80",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendAddressPools/pool-default-aspnetapp-80-bp-80",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "backendAddresses": [
                        {
                            "ipAddress": "10.244.0.14"
                        }
                    ],
                    "requestRoutingRules": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/requestRoutingRules/rr-e1903c8aa3446b7b3207aec6d6ecba8a"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/backendAddressPools"
            }
        ],
        "loadDistributionPolicies": [],
        "backendHttpSettingsCollection": [
            {
                "name": "bp-default-aspnetapp-80-80-aspnetapp",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendHttpSettingsCollection/bp-default-aspnetapp-80-80-aspnetapp",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "port": 80,
                    "protocol": "Http",
                    "cookieBasedAffinity": "Disabled",
                    "pickHostNameFromBackendAddress": false,
                    "requestTimeout": 30,
                    "probe": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/probes/pb-default-aspnetapp-80-aspnetapp"
                    },
                    "requestRoutingRules": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/requestRoutingRules/rr-e1903c8aa3446b7b3207aec6d6ecba8a"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/backendHttpSettingsCollection"
            },
            {
                "name": "defaulthttpsetting",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendHttpSettingsCollection/defaulthttpsetting",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "port": 80,
                    "protocol": "Http",
                    "cookieBasedAffinity": "Disabled",
                    "pickHostNameFromBackendAddress": false,
                    "requestTimeout": 30,
                    "probe": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/probes/defaultprobe-Http"
                    }
                },
                "type": "Microsoft.Network/applicationGateways/backendHttpSettingsCollection"
            }
        ],
        "backendSettingsCollection": [],
        "httpListeners": [
            {
                "name": "fl-e1903c8aa3446b7b3207aec6d6ecba8a",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/httpListeners/fl-e1903c8aa3446b7b3207aec6d6ecba8a",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "frontendIPConfiguration": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/frontendIPConfigurations/appGwPublicFrontendIp"
                    },
                    "frontendPort": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/frontendPorts/port_80"
                    },
                    "protocol": "Http",
                    "hostNames": [],
                    "requireServerNameIndication": false,
                    "requestRoutingRules": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/requestRoutingRules/rr-e1903c8aa3446b7b3207aec6d6ecba8a"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/httpListeners"
            }
        ],
        "listeners": [],
        "urlPathMaps": [],
        "requestRoutingRules": [
            {
                "name": "rr-e1903c8aa3446b7b3207aec6d6ecba8a",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/requestRoutingRules/rr-e1903c8aa3446b7b3207aec6d6ecba8a",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "ruleType": "Basic",
                    "priority": 19500,
                    "httpListener": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/httpListeners/fl-e1903c8aa3446b7b3207aec6d6ecba8a"
                    },
                    "backendAddressPool": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendAddressPools/pool-default-aspnetapp-80-bp-80"
                    },
                    "backendHttpSettings": {
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendHttpSettingsCollection/bp-default-aspnetapp-80-80-aspnetapp"
                    }
                },
                "type": "Microsoft.Network/applicationGateways/requestRoutingRules"
            }
        ],
        "routingRules": [],
        "probes": [
            {
                "name": "defaultprobe-Http",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/probes/defaultprobe-Http",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "protocol": "Http",
                    "host": "localhost",
                    "path": "/",
                    "interval": 30,
                    "timeout": 30,
                    "unhealthyThreshold": 3,
                    "pickHostNameFromBackendHttpSettings": false,
                    "minServers": 0,
                    "match": {},
                    "backendHttpSettings": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendHttpSettingsCollection/defaulthttpsetting"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/probes"
            },
            {
                "name": "defaultprobe-Https",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/probes/defaultprobe-Https",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "protocol": "Https",
                    "host": "localhost",
                    "path": "/",
                    "interval": 30,
                    "timeout": 30,
                    "unhealthyThreshold": 3,
                    "pickHostNameFromBackendHttpSettings": false,
                    "minServers": 0,
                    "match": {}
                },
                "type": "Microsoft.Network/applicationGateways/probes"
            },
            {
                "name": "pb-default-aspnetapp-80-aspnetapp",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/probes/pb-default-aspnetapp-80-aspnetapp",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "properties": {
                    "provisioningState": "Succeeded",
                    "protocol": "Http",
                    "host": "localhost",
                    "path": "/",
                    "interval": 30,
                    "timeout": 30,
                    "unhealthyThreshold": 3,
                    "pickHostNameFromBackendHttpSettings": false,
                    "minServers": 0,
                    "match": {},
                    "backendHttpSettings": [
                        {
                            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/MC_aks_test_2_aks-test-2-public_westus2/providers/Microsoft.Network/applicationGateways/appgw_aks_test_2/backendHttpSettingsCollection/bp-default-aspnetapp-80-80-aspnetapp"
                        }
                    ]
                },
                "type": "Microsoft.Network/applicationGateways/probes"
            }
        ],
        "rewriteRuleSets": [],
        "redirectConfigurations": [],
        "privateLinkConfigurations": [],
        "privateEndpointConnections": [],
        "enableHttp2": false,
        "autoscaleConfiguration": {
            "minCapacity": 0,
            "maxCapacity": 3
        }
    }
}
```

</details>
<br />