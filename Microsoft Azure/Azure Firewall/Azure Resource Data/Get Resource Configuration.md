# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Azure firewall is dependent on the Azure API response of the Azure firewall as the primary response. The full resource configuration consists of some associated resources' API data, including `publicIPAddress`, `subnet`.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Azure Firewalls - Get | self | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/firewall/azure-firewalls/get | 
| Public IP Addresses - Get | properties.ipConfigurations.properties.publicIPAddress | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/public-ip-addresses/get | 
| Subnets - Get | properties.ipConfigurations.properties.subnet | 2021-08-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/subnets/get | 


# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "Spoke-3-Firewall(<ResourceGroup>)(<Subscription_ID_Prefix>)(AzureFirewall)",
    "name": "Spoke-3-Firewall",
    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/azureFirewalls/Spoke-3-Firewall",
    "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
    "type": "Microsoft.Network/azureFirewalls",
    "location": "westus",
    "properties": {
        "provisioningState": "Succeeded",
        "sku": {
            "name": "AZFW_VNet",
            "tier": "Standard"
        },
        "threatIntelMode": "Alert",
        "additionalProperties": {},
        "ipConfigurations": [
            {
                "name": "Spoke-3-Firewall",
                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/azureFirewalls/Spoke-3-Firewall/azureFirewallIpConfigurations/Spoke-3-Firewall",
                "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                "type": "Microsoft.Network/azureFirewalls/azureFirewallIpConfigurations",
                "properties": {
                    "provisioningState": "Succeeded",
                    "privateIPAddress": "172.17.16.68",
                    "privateIPAllocationMethod": "Dynamic",
                    # Public IP Addresses: https://learn.microsoft.com/en-us/rest/api/virtualnetwork/public-ip-addresses/get
                    "publicIPAddress": {
                        "name": "Spoke-3-Firewall",
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/publicIPAddresses/Spoke-3-Firewall",
                        "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                        "location": "westus",
                        "tags": {},
                        "properties": {
                            "provisioningState": "Succeeded",
                            "resourceGuid": "00000000-0000-0000-0000-000000000000",
                            "ipAddress": "40.85.154.247",
                            "publicIPAddressVersion": "IPv4",
                            "publicIPAllocationMethod": "Static",
                            "idleTimeoutInMinutes": 4,
                            "ipTags": [],
                            "ipConfiguration": {
                                "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/azureFirewalls/Spoke-3-Firewall/azureFirewallIpConfigurations/Spoke-3-Firewall"
                            }
                        },
                        "type": "Microsoft.Network/publicIPAddresses",
                        "sku": {
                            "name": "Standard",
                            "tier": "Regional"
                        }
                    },
                    # Subnets: https://learn.microsoft.com/en-us/rest/api/virtualnetwork/subnets/get
                    "subnet": {
                        "name": "AzureFirewallSubnet",
                        "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/virtualNetworks/Spoke-VNET3/subnets/AzureFirewallSubnet",
                        "etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                        "properties": {
                            "provisioningState": "Succeeded",
                            "addressPrefix": "172.17.16.64/26",
                            "ipConfigurations": [
                                {
                                    "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/US-West-RG/providers/Microsoft.Network/azureFirewalls/Spoke-3-Firewall/azureFirewallIpConfigurations/Spoke-3-Firewall"
                                }
                            ],
                            "serviceEndpoints": [
                                {
                                    "provisioningState": "Succeeded",
                                    "service": "Microsoft.Storage",
                                    "locations": [
                                        "westus",
                                        "eastus"
                                    ]
                                }
                            ],
                            "delegations": [],
                            "privateEndpointNetworkPolicies": "Enabled",
                            "privateLinkServiceNetworkPolicies": "Enabled"
                        },
                        "type": "Microsoft.Network/virtualNetworks/subnets"
                    }
                }
            }
        ],
        "networkRuleCollections": [],
        "applicationRuleCollections": [],
        "natRuleCollections": [],
        "firewallPolicy": {
            "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/resourcegroups/US-West-RG/providers/Microsoft.Network/firewallPolicies/AzurePathTest-FW"
        }
    }
}
```

</details>
<br />