# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
Passing-in the keyword "configuration" for the param data_type, the API returns the Azure's original API response of Virtual Machine, with the details of some associated resources, including Network Interfaces, Network Security Groups.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.

|Resource/Action|Relationship|Azure API Version|Azure API document|
|------|------|------|------|
| Virtual Machines - Get | self | 2024-03-01 | https://learn.microsoft.com/en-us/rest/api/compute/virtual-machines/get
| Network Interfaces - Get | properties.networkProfile.networkInterfaces | 2023-09-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/network-interfaces/get
| Network Security Groups - Get | properties.networkProfile.networkInterfaces.properties.networkSecurityGroup | 2023-09-01 | https://learn.microsoft.com/en-us/rest/api/virtualnetwork/network-security-groups/get

# Samples <a name="sample"></a>

<details>
<summary>API Response</summary>
<p>

```json
{
    "name": "myVM",
    "id": "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/myVM",
    "type": "Microsoft.Compute/virtualMachines",
    "location": "West US",
    "tags": {
        "myTag1": "tagValue1"
    },
    "properties": {
        "vmId": "0f47b100-583c-48e3-a4c0-aefc2c9bbcc1",
        "hostGroup": {
            "id": "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/hostGroups/myHostGroup"
        },
        "hardwareProfile": {
            "vmSize": "Standard_D2s_v3"
        },
        "storageProfile": {
            "imageReference": {
                "publisher": "MicrosoftWindowsServer",
                "offer": "WindowsServer",
                "sku": "2016-Datacenter",
                "version": "latest"
            },
            "osDisk": {
                "osType": "Windows",
                "name": "myOsDisk",
                "createOption": "FromImage",
                "caching": "ReadWrite",
                "managedDisk": {
                    "storageAccountType": "Premium_LRS",
                    "id": "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/disks/myOsDisk"
                },
                "diskSizeGB": 30
            },
            "dataDisks": []
        },
        "osProfile": {
            "computerName": "myVM",
            "adminUsername": "admin",
            "windowsConfiguration": {
                "provisionVMAgent": true,
                "enableAutomaticUpdates": false
            },
            "secrets": []
        },
        "networkProfile": {      
            // Network Interface: https://learn.microsoft.com/en-us/rest/api/virtualnetwork/network-interfaces/get?tabs=HTTP    
            "networkInterfaces": [               
                {
                    "name": "test-nic",
                    "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkInterfaces/test-nic",
                    "location": "eastus",
                    "properties": {
                        "provisioningState": "Succeeded",
                        "ipConfigurations": [
                            {
                                "name": "ipconfig1",
                                "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkInterfaces/test-nic/ipConfigurations/ipconfig1",
                                "properties": {
                                    "provisioningState": "Succeeded",
                                    "privateIPAddress": "172.20.2.4",
                                    "privateIPAllocationMethod": "Dynamic",
                                    "publicIPAddress": {
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/publicIPAddresses/test-ip"
                                    },
                                    "subnet": {
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/rg1-vnet/subnets/default"
                                    },
                                    "primary": true,
                                    "privateIPAddressVersion": "IPv4"
                                }
                            }
                        ],
                        "dnsSettings": {
                            "dnsServers": [],
                            "appliedDnsServers": [],
                            "internalDomainNameSuffix": "test.bx.internal.cloudapp.net"
                        },
                        "macAddress": "00-0D-3A-1B-C7-21",
                        "enableAcceleratedNetworking": true,
                        "disableTcpStateTracking": true,
                        "enableIPForwarding": false,
                        // Network Security Groups: https://learn.microsoft.com/en-us/rest/api/virtualnetwork/network-security-groups/get?tabs=HTTP
                        "networkSecurityGroup": {
                            "name": "testnsg",
                            "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg",
                            "type": "Microsoft.Network/networkSecurityGroups",
                            "location": "westus",
                            "properties": {
                                "provisioningState": "Succeeded",
                                "securityRules": [
                                    {
                                        "name": "rule1",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/securityRules/rule1",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "80",
                                            "sourceAddressPrefix": "*",
                                            "destinationAddressPrefix": "*",
                                            "access": "Allow",
                                            "priority": 130,
                                            "direction": "Inbound"
                                        }
                                    }
                                ],
                                "defaultSecurityRules": [
                                    {
                                        "name": "AllowVnetInBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/AllowVnetInBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Allow inbound traffic from all VMs in VNET",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "VirtualNetwork",
                                            "destinationAddressPrefix": "VirtualNetwork",
                                            "access": "Allow",
                                            "priority": 65000,
                                            "direction": "Inbound"
                                        }
                                    },
                                    {
                                        "name": "AllowAzureLoadBalancerInBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/AllowAzureLoadBalancerInBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Allow inbound traffic from azure load balancer",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "AzureLoadBalancer",
                                            "destinationAddressPrefix": "*",
                                            "access": "Allow",
                                            "priority": 65001,
                                            "direction": "Inbound"
                                        }
                                    },
                                    {
                                        "name": "DenyAllInBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/DenyAllInBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Deny all inbound traffic",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "*",
                                            "destinationAddressPrefix": "*",
                                            "access": "Deny",
                                            "priority": 65500,
                                            "direction": "Inbound"
                                        }
                                    },
                                    {
                                        "name": "AllowVnetOutBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/AllowVnetOutBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "VirtualNetwork",
                                            "destinationAddressPrefix": "VirtualNetwork",
                                            "access": "Allow",
                                            "priority": 65000,
                                            "direction": "Outbound"
                                        }
                                    },
                                    {
                                        "name": "AllowInternetOutBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/AllowInternetOutBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Allow outbound traffic from all VMs to Internet",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "*",
                                            "destinationAddressPrefix": "Internet",
                                            "access": "Allow",
                                            "priority": 65001,
                                            "direction": "Outbound"
                                        }
                                    },
                                    {
                                        "name": "DenyAllOutBound",
                                        "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/networkSecurityGroups/testnsg/defaultSecurityRules/DenyAllOutBound",
                                        "properties": {
                                            "provisioningState": "Succeeded",
                                            "description": "Deny all outbound traffic",
                                            "protocol": "*",
                                            "sourcePortRange": "*",
                                            "destinationPortRange": "*",
                                            "sourceAddressPrefix": "*",
                                            "destinationAddressPrefix": "*",
                                            "access": "Deny",
                                            "priority": 65500,
                                            "direction": "Outbound"
                                        }
                                    }
                                ]
                            }
                        },
                        "primary": true,
                        "virtualMachine": {
                            "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Compute/virtualMachines/vm1"
                        },
                        "dscpConfiguration": {
                            "id": "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Compute/dscpConfiguration/mydscpconfiguration"
                        },
                        "vnetEncryptionSupported": false
                    },
                    "type": "Microsoft.Network/networkInterfaces"
                }
            ]
        },
        "provisioningState": "Succeeded"
    }
}

```
</p>
</details>