# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)
    - [Sample 1 -- Classic Firewall Rules](#sample-1) 
    - [Sample 2 -- Firewall Rules of Firewall Policies](#sample-2)


# Introduction <a name="introduction"></a>
Passing-in the keyword "firewall_rule" for the param `data_type`, the API returns the NAT rules, network rules, and applications rules of the Azure Firewall.
There are two types of firewall rules -- classic rules and firewall policy (ref: https://learn.microsoft.com/en-us/azure/firewall/rule-processing).
The classic firewall rules can be found directly in the firewall's Azure API data. The other type of firewall rule can be fetched via firewall policy and its base policy's Azure API data.


# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.

|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Azure Firewalls - Get | self | 2022-09-01 | https://learn.microsoft.com/en-us/rest/api/firewall/azure-firewalls/get | 
| Firewall Policies - Get | self | 2022-09-01 |   https://learn.microsoft.com/en-us/rest/api/virtualnetwork/firewall-policies/get | 

# Samples <a name="sample"></a>
## Sample 1 -- Classic Firewall Rules <a name="sample-1"></a>

<details>
<summary>API Response - Classic Firewall Rules</summary>
<p>

```json
[
  {
    "name": "networkRuleCollections",
    "properties": {
      "ruleCollections": [
        {
          "name": "netrulecoll",
          "priority": 112,
          "action": {
            "type": "Deny"
          },
          "rules": [
            {
              "name": "L4-traffic",
              "description": "Block traffic based on source IPs and ports",
              "sourceAddresses": [
                "192.168.1.1-192.168.1.12",
                "10.1.4.12-10.1.4.255"
              ],
              "destinationPorts": [
                "443-444",
                "8443"
              ],
              "destinationAddresses": [
                "*"
              ],
              "protocols": [
                "TCP"
              ]
            },
            {
              "name": "L4-traffic-with-FQDN",
              "description": "Block traffic based on source IPs and ports to amazon",
              "sourceAddresses": [
                "10.2.4.12-10.2.4.255"
              ],
              "destinationPorts": [
                "443-444",
                "8443"
              ],
              "destinationFqdns": [
                "www.amazon.com"
              ],
              "protocols": [
                "TCP"
              ]
            }
          ]
        }
      ]
    }
  },
  {
    "name": "natRuleCollections",
    "properties": {
      "ruleCollections": [
        {
          "name": "natrulecoll",
          "priority": 112,
          "action": {
            "type": "Dnat"
          },
          "rules": [
            {
              "name": "DNAT-HTTPS-traffic",
              "description": "D-NAT all outbound web traffic for inspection",
              "sourceAddresses": [
                "*"
              ],
              "destinationAddresses": [
                "1.2.3.4"
              ],
              "destinationPorts": [
                "443"
              ],
              "protocols": [
                "TCP"
              ],
              "translatedAddress": "1.2.3.5",
              "translatedPort": "8443"
            },
            {
              "name": "DNAT-HTTP-traffic-With-FQDN",
              "description": "D-NAT all inbound web traffic for inspection",
              "sourceAddresses": [
                "*"
              ],
              "destinationAddresses": [
                "1.2.3.4"
              ],
              "destinationPorts": [
                "80"
              ],
              "protocols": [
                "TCP"
              ],
              "translatedFqdn": "internalhttpserver",
              "translatedPort": "880"
            }
          ]
        }
      ]
    }
  },
  {
    "name": "applicationRuleCollections",
    "properties": {
      "ruleCollections": [
        {
          "name": "apprulecoll",
          "priority": 110,
          "action": {
            "type": "Deny"
          },
          "rules": [
            {
              "name": "rule1",
              "description": "Deny inbound rule",
              "protocols": [
                {
                  "protocolType": "Https",
                  "port": 443
                }
              ],
              "targetFqdns": [
                "www.test.com"
              ],
              "sourceAddresses": [
                "216.58.216.164",
                "10.0.0.0/24"
              ]
            }
          ]
        }
      ]
    }
  }
]

```
</p>
</details>


## Sample 2 -- Firewall Rules of Firewall Policies <a name="sample-2"></a>

<details>
<summary>API Response - Firewall Rules of Firewall Policies</summary>
<p>

```json
{
    "name": "firewallPolicy",
    "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/firewallPolicies/firewallPolicy",
    "type": "Microsoft.Network/firewallPolicies",
    "etag": "w/\\00000000-0000-0000-0000-000000000000\\",
    "location": "West US",
    "tags": {
        "key1": "value1"
    },
    "properties": {
        "size": "0.5MB",
        "provisioningState": "Succeeded",
        "threatIntelMode": "Alert",
        "threatIntelWhitelist": {
            "ipAddresses": [
                "20.3.4.5"
            ],
            "fqdns": [
                "*.microsoft.com"
            ]
        },
        "ruleCollectionGroups": [
            {
                "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/firewallPolicies/firewallPolicy/ruleCollectionGroups/ruleCollectionGroup1"
            }
        ],
        "insights": {
            "isEnabled": true,
            "retentionDays": 100,
            "logAnalyticsResources": {
                "workspaces": [
                    {
                        "region": "westus",
                        "workspaceId": {
                            "id": "/subscriptions/subid/resourcegroups/rg1/providers/microsoft.operationalinsights/workspaces/workspace1"
                        }
                    },
                    {
                        "region": "eastus",
                        "workspaceId": {
                            "id": "/subscriptions/subid/resourcegroups/rg1/providers/microsoft.operationalinsights/workspaces/workspace2"
                        }
                    }
                ],
                "defaultWorkspaceId": {
                    "id": "/subscriptions/subid/resourcegroups/rg1/providers/microsoft.operationalinsights/workspaces/defaultWorkspace"
                }
            }
        },
        "firewalls": [],
        "snat": {
            "privateRanges": [
                "IANAPrivateRanges"
            ]
        },
        "sql": {
            "allowSqlRedirect": true
        },
        "dnsSettings": {
            "servers": [
                "30.3.4.5"
            ],
            "enableProxy": true,
            "requireProxyForNetworkRules": false
        },
        "explicitProxy": {
            "enableExplicitProxy": true,
            "httpPort": 8087,
            "httpsPort": 8087,
            "enablePacFile": true,
            "pacFilePort": 8087,
            "pacFile": "https://tinawstorage.file.core.windows.net/?sv=2020-02-10&ss=bfqt&srt=sco&sp=rwdlacuptfx&se=2021-06-04T07:01:12Z&st=2021-06-03T23:01:12Z&sip=68.65.171.11&spr=https&sig=Plsa0RRVpGbY0IETZZOT6znOHcSro71LLTTbzquYPgs%3D"
        },
        "sku": {
            "tier": "Premium"
        },
        "intrusionDetection": {
            "mode": "Alert",
            "configuration": {
                "signatureOverrides": [
                    {
                        "id": "2525004",
                        "mode": "Deny"
                    }
                ],
                "bypassTrafficSettings": [
                    {
                        "name": "bypassRule1",
                        "description": "Rule 1",
                        "protocol": "TCP",
                        "sourceAddresses": [
                            "1.2.3.4"
                        ],
                        "destinationAddresses": [
                            "5.6.7.8"
                        ],
                        "destinationPorts": [
                            "*"
                        ]
                    }
                ]
            }
        },
        "transportSecurity": {
            "certificateAuthority": {
                "name": "clientcert",
                "keyVaultSecretId": "https://kv/secret"
            }
        }
    }
}

```
</p>
</details>
<br><br>
