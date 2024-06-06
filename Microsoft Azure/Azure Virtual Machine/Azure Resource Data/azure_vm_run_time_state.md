# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
Passing-in the keyword "run_time_state" for the param data_type, the API returns the Azure's API response of "Virtual Machine - Instance View", which describes the run-time state of a virtual machine. The data structure of "statuses" field is modified from original response for easier usage.

# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.
We also added some basic properties from NetBrain data model, including "name", "id", "vmId", "type", "location", and "hardwareProfile".

|Resource/Action|Relationship|Azure API Version|Azure API document|
|------|------|------|------|
| Virtual Machines - Instance View | self | 2024-03-01 | https://learn.microsoft.com/en-us/rest/api/compute/virtual-machines/instance-view?tabs=HTTP

# Samples <a name="sample"></a>

<details>
<summary>API Response</summary>
<p>

```json
{
    "name": "myVM",
    "id": "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/myVM",
    "vmId": "d8d7134c-3b51-4abc-8d19-dc46d8653fc3",
    "type": "Microsoft.Compute/virtualMachines",
    "location": "eastus",
    "hardwareProfile": {
        "vmSize": "Standard_B1ls"
    },
    "computerName": "myVM",
    "osName": "Windows Server 2016 Datacenter",
    "osVersion": "Microsoft Windows NT 10.0.14393.0",
    "vmAgent": {
        "vmAgentVersion": "2.7.41491.949",
        "statuses": {
            "ProvisioningState": {
                "code": "ProvisioningState/succeeded",
                "level": "Info",
                "displayStatus": "Ready",
                "message": "GuestAgent is running and accepting new configurations.",
                "time": "2023-07-01T23:11:22+00:00"
            }
        }
    },
    "disks": [
        {
            "name": "myOsDisk",
            "statuses": {
                "ProvisioningState": {
                    "code": "ProvisioningState/succeeded",
                    "level": "Info",
                    "displayStatus": "Provisioning succeeded",
                    "time": "2023-07-01T21:29:47.477089+00:00"
                }
            }
        }
    ],
    "hyperVGeneration": "V1",
    "assignedHost": "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/hostGroups/myHostGroup/hosts/myHost",
    "statuses": {
        "ProvisioningState": {
            "code": "ProvisioningState/succeeded",
            "level": "Info",
            "displayStatus": "Provisioning succeeded",
            "time": "2023-07-01T21:30:12.8051917+00:00"
        },
        "PowerState": {
            "code": "PowerState/running",
            "level": "Info",
            "displayStatus": "VM running"
        }
    }
}

```
</p>
</details>